# Use Case Specification: รายละเอียดกรณีเคลียร์ User ออกจากระบบ

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 16 |
| **2. Use Case Name** | เคลียร์ user ออกจากระบบ |
| **3. Primary Actor** | System admin |
| **4. Description** | System admin สามารถเคลียร์ User ที่จบการศึกษาไปแล้วออกจากระบบได้ |
| **5. Trigger** | System admin ต้องการเคลียร์ User ที่จบการศึกษาแล้วออกจากระบบ |
| **6. Preconditions** | PRE-1 System admin รู้ข้อมูลว่า User คนไหนได้จบการศึกษาไปแล้ว <br> PRE-2 System admin ยืนยันตัวตนสำเร็จ |
| **7. Postconditions** | POST-1 User นั้น ๆ ไม่สามารถเข้าสู่ระบบได้อีก <br>POST-2 บัญชีของUser นั้น ๆ ถูกตั้งสถานะเป็น isActive เป็น false ในฐานข้อมูล  |
| **11. Priority** | Low |
| **12. Frequency of Use** | 0 – 10 ครั้งต่อปี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. System admin เลือก "Account Config" จากหน้า Main Menu 
    - ระบบแสดงชื่อผู้ใช้ที่ยังใช้งานในระบบได้อยู่ 
2. System admin เลือกผู้ใช้จากรายการชื่อทั้งหมดที่มี 
    - System admin ทำการกด checkbox ตามบัญชีที่ต้องการทำการปิดบัญชี 
3. System admin กดปุ่ม "ปิดบัญชี" 
    - ระบบแสดงข้อความแจ้งเตือน: "ยืนยันการปิดบัญชีหรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. System admin กดยืนยัน 
    - ระบบตั้งสถานะบัญชีนั้น ๆ เป็นปิดการใช้งาน 
    - ระบบแสดงข้อความแจ้งเตือน "ปิดบัญชีสำเร็จ" 
5. หากต้องการปิดบัญชีอื่น ๆ เพิ่มเติม: 
    - ระบบนำ System admin กลับไปที่หน้ารายชื่อผู้ใช้ 
6. System admin ทำซ้ำขั้นตอน 2 - 4 
7. Use Case สิ้นสุดเมื่อ System admin ไม่ต้องปิดบัญชีแล้ว 

#### 9. Alternative Flow
**System admin ยกเลิกการปิดบัญชี**
1. System admin เลือก "Account Config" จากหน้า Main Menu 
    - ระบบแสดงชื่อผู้ใช้ที่ยังใช้งานในระบบได้อยู่ 
2. System admin เลือกผู้ใช้จากรายการชื่อทั้งหมดที่มี 
    - System admin ทำการกด checkbox ตามบัญชีที่ต้องการทำการปิดบัญชี 
3. System admin กดปุ่ม "ปิดบัญชี" 
    - ระบบแสดงข้อความแจ้งเตือน: "ยืนยันการปิดบัญชีหรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. System admin กดปุ่มยกเลิก 
5. บัญชีจะยังสามารถใช้งานได้ปกติ 
6. Alternative Flow สิ้นสุด 

#### 10. Exceptions
- None

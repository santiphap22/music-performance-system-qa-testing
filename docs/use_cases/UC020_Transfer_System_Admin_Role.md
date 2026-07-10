# Use Case Specification: รายละเอียดกรณีโอนย้ายสิทธิ์ system admin

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 20 |
| **2. Use Case Name** | โอนย้ายสิทธิ์ system admin |
| **3. Primary Actor** | System admin |
| **4. Description** | System admin ต้องการโอนย้ายสิทธิ์ผู้ดูแลให้คนในชุมนุมในกรณีที่หมดวาระหรือออกจากชุมนุม |
| **5. Trigger** | System admin ต้องการโอนย้ายสิทธิ์ System admin ให้สมาชิกคนอื่น  |
| **6. Preconditions** | PRE-1 ชุมนุม Sci Band ได้มีการพูดคุยตกลงกันแล้วว่าจะมอบสิทธิ์ System admin ให้สมาชิกคนใด |
| **7. Postconditions** | POST-1 สิทธิ์ System admin ถูกโอนย้ายไปยังบัญชีใหม <br>POST-2 Systemadmin คนเก่าไม่มีสิทธิ์ System admin อีกต่อไป  |
| **11. Priority** | High |
| **12. Frequency of Use** | 1 ครั้งต่อปี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. System admin เลือก "Transfer System Admin" จากหน้า Main Menu 
    - ระบบแสดงหน้า Transfer System Admin ซึ่งมีรายชื่อบัญชีผู้ใช้ทั้งหมดที่ยังสามารถใช้งานในระบบได้อยู่ 
2. System admin เลือกชื่อสมาชิกจากรายการชื่อทั้งหมดที่มี 
    - System admin ทำเลือกผู้ใช้ที่ต้องการให้สิทธิ์โดยสามารถโอนย้ายให้ได้เพียงคนเดียวเท่านั้น 
3. System admin กดปุ่ม "โอนย้ายสิทธิ์" 
    - ระบบแสดงข้อความแจ้งเตือน: "โปรดยืนยันการโอนสิทธิ ์ System admin การดำเนินการนี้จะไม่สามารถย้อนกลับได้" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. System admin กดยืนยัน
    - ระบบตั้งสถานะบัญชีนั้น ๆ เป็น System admin ในฐานข้อมูล 
    - ระบบจะทำการลบสิทธิ์ System admin คนเก่าออกจากระบบ 
    - ระบบแสดงข้อความแจ้งเตือน "โอนย้ายสิทธิ์สำเร็จ"    

#### 9. Alternative Flow
**System admin ยกเลิกการโอนย้ายสิทธิ์** 
1. System admin เลือก "Transfer System Admin " จากหน้า Main Menu 
    - ระบบแสดงหน้า Transfer System Admin ซึ่งมีรายชื่อบัญชีผู้ใช้ทั้งหมดที่ยังสามารถใช้งานในระบบได้อย 
2. System admin เลือกชื่อสมาชิกจากรายการชื่อทั้งหมดที่มี 
    - System admin ทำเลือกผู้ใช้ที่ต้องการให้สิทธิ์โดยสามารถโอนย้ายให้ได้เพียงคนเดียวเท่านั้น 
3. System admin กดปุ่ม "โอนย้ายสิทธิ์" 
    - ระบบแสดงข้อความแจ้งเตือน: "โปรดยืนยันการโอนสิทธิ ์ System admin การดำเนินการนี้จะไม่สามารถย้อนกลับได้" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. System admin กดยกเลิก 
5. Alternative Flow สิ้นสุด

#### 10. Exceptions
- None

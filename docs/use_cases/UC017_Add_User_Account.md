# Use Case Specification: รายละเอียดกรณีเพิ่มบัญชีผู้ใช้เข้าสู่ระบบ

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 17 |
| **2. Use Case Name** | เพิ่มบัญชีผู้ใช้เข้าสู่ระบบ |
| **3. Primary Actor** | System admin |
| **4. Description** | System admin สามารถเพิ่ม User ใหม่ให้สามารถเข้าใช้งานระบบได้ |
| **5. Trigger** | System admin ต้องการเพิ่ม User เพื่อใช้งานในระบบ |
| **6. Preconditions** | PRE-1 System admin มีข้อมูล Google form ที่สมาชิกได้ทำ<br>การกรอกตอนสมัครเข้า Sci Band <br> PRE-2 System admin ยืนยันตัวตนสำเร็จ <br> PRE-3 System admin และสมาชิกต้องทำการตรวจสอบความถูกต้องของข้อมูล<br>ใน Google form ก่อน |
| **7. Postconditions** | POST-1 ข้อมูลบัญชีผู้ใช้ถูกเพิ่มลงในฐานข้อมูล <br>POST-2 User นั ้น ๆ สามารถเข้าสู่ระบบได้  |
| **11. Priority** | High |
| **12. Frequency of Use** | 1 - 5 ครั้งต่อปี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. System admin เลือก "Account Config" จากหน้า Main Menu 
    - ระบบแสดงหน้าเพิ่มบัญชีผู้ใช้ใหม่ ซึ่งมีปุ่ม เพิ่มบัญชี 
2. System admin กดปุ่มเพิ่มบัญชี 
3. ระบบแสดงข้อความ “เพิ่มบัญชีสำเร็จ” 
4. Use Case สิ้นสุด 

#### 9. Alternative Flow
- None

#### 10. Exceptions
- None

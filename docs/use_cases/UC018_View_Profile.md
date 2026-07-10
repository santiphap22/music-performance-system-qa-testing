# Use Case Specification: รายละเอียดกรณีดู Profile

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 18 |
| **2. Use Case Name** | ดู Profile |
| **3. Primary Actor** | User ทุกประเภท |
| **4. Description** | User ทุกประเภทสามารถดู Profile ของตัวเองได้ว่าข้อมูลถูกต้องหรือไม่ |
| **5. Trigger** | User ต้องการดู Profile ของตัวเอง |
| **6. Preconditions** | PRE-1 System admin มีการเพิ่มบัญชีผู้ใช้ลงไปในระบบแล้ว <br> PRE-2 User ยืนยันตัวตนสำเร็จ |
| **7. Postconditions** | POST-1 User ตรวจสอบดู Profile สำเร็จ  |
| **11. Priority** | Medium |
| **12. Frequency of Use** | 0 - 5 ครั้งต่อปี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. User เลือก "Profile" จากหน้า Main Menu 
    - ระบบแสดงหน้า Profile ของผู้ใช้ 
2. User ทำการดูรายละเอียด Profile ของตัวเองโดยประกอบไปด้วยข้อมูล ชื่อ-นามสกุล, ชื่อเล่น, ตำแหน่งในระบบ, discord Id, discord username  

#### 9. Alternative Flow
- None

#### 10. Exceptions
- None

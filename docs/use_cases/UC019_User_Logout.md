# Use Case Specification: รายละเอียดกรณี Logout

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 19 |
| **2. Use Case Name** | Logout |
| **3. Primary Actor** | User ทุกประเภท |
| **4. Description** | User สามารถ logout ออกจากระบบเมื่อไม่ใช้งาน |
| **5. Trigger** | User ต้องการ logout ออกจากระบบ |
| **6. Preconditions** | PRE-1 User ได้ Login ค้างไว้ในแอปพลิเคชัน |
| **7. Postconditions** | POST-1 User ออกจากระบบสำเร็จ  |
| **11. Priority** | Medium |
| **12. Frequency of Use** | 0 - 3 ครั้งต่อปี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. User เลือก "Profile" จากหน้า Main Menu
    - ระบบแสดงหน้า Profile ของผู้ใช้ 
2. User ทำการกดปุ่ม "logout" 
    - ระบบแสดงข้อความแจ้งเตือน: "คุณต้องการออกจากระบบหรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
3. User กดยืนยัน 
    - ระบบแสดงข้อความแจ้งเตือน: "ออกจากระบบสำเร็จ" 
o ระบบนำผู้ใช้ไปสู่หน้าเข้าสู่ระบบ   

#### 9. Alternative Flow
**User ยกเลิกการออกจากระบบ** 
1. User เลือก "Profile" จากหน้า Main Menu 
    - ระบบแสดงหน้า Profile ของผู้ใช้ 
2. User ทำการกดปุ่ม "logout" 
    - ระบบแสดงข้อความแจ้งเตือน: "คุณต้องการออกจากระบบหรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
3. User กดยกเลิก 
4. Alternative Flow สิ้นสุด

#### 10. Exceptions
- None

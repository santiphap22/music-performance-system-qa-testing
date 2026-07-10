# Use Case Specification: รายละเอียดกรณีลบงานแสดงดนตรี

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 5 |
| **2. Use Case Name** | ลบงานแสดงดนตรี |
| **3. Primary Actor** | Backstage |
| **4. Description** | Backstage สามารถลบงานแสดงดนตรีที่ถูกยกเลิกไปแล้วหรือเสร็จสิ้นแล้วได้ |
| **5. Trigger** | งานแสดงดนตรีถูกยกเลิก Backstage จึงต้องการลบงานแสดงดนตรี |
| **6. Preconditions** | PRE-1 Backstage ทำการยืนยันตัวตนสำเร็จ<br> PRE-2 มีการยืนยันแล้วว่างานแสดงดนตรีนั้น ๆ ถูกยกเลิก |
| **7. Postconditions** | POST-1 งานแสดงดนตรีถูกลบออกจากระบบ |
| **11. Priority** | medium |
| **12. Frequency of Use** | 0 - 1 ครั้งต่อหนึ่งงานแสดงดนตรี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมด 
2. Backstage เลือกงานแสดงดนตรีที่ต้องการ 
3. Backstage กดปุ่ม “ลบ Event” 
    - ระบบแสดงข้อความแจ้งเตือน: "ต้องการลบ Event หรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. Backstage กดยืนยัน 
    - ระบบลบงานแสดงดนตรีออกจากรายการEvent ทั้งหมด 
    - ระบบแสดงข้อความแจ้งเตือน: "ลบ Eventสำเร็จ" 
5. หากต้องการลบงานแสดงดนตรีอื่น ๆ เพิ่มเติม: 
    - ระบบนำ Backstage กลับไปที่หน้ารวมงานแสดงดนตรีทั้งหมด 
    - Backstage เลือกงานแสดงดนตรีอื่น ๆ และทำซ้ำขั้นตอน 2 - 4 
6. Use Case สิ้นสุดเมื่อ Backstage ไม่ต้องการลบEventเพิ่มเติม 

#### 9. Alternative Flow
**Backstage ต้องการยกเลิกการลบงานแสดงดนตรี**
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมด 
2. Backstage เลือกงานแสดงดนตรีที่ต้องการ 
3. Backstage กดปุ่ม “ลบ Event” 
    - ระบบแสดงข้อความแจ้งเตือน: "ต้องการลบ Event หรือไม่" พร้อมปุ่ม "ยืนยัน" และ "ยกเลิก" 
4. Backstage กดปุ่มยกเลิก 
5. สิ้นสุด Alternative flow 

#### 10. Exceptions
- None

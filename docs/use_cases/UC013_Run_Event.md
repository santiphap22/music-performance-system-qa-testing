# Use Case Specification: รายละเอียดกรณี Run event

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 13 |
| **2. Use Case Name** | Run event |
| **3. Primary Actor** | Backstage |
| **4. Description** | Backstage สามารถเริ่มงานแสดงดนตรีที่เลือกได้เมื่อถึงวันแสดงจริงตามที่ได้กรอกไว้ภายในระบบ เพื่อทำการรันคิวเพลงและเปิดระบบการแจ้งเตือนให้กับ performer |
| **5. Trigger** | Backstage ต้องการเริ่มงานแสดงดนตรี ในเวลานั้น |
| **6. Preconditions** | PRE-1 Backstage ยืนยันตัวตนสำเร็จ <br> PRE-2 Backstage มีการเพิ่มงานแสดงดนตรีลงไปในระบบแล้ว <br> PRE-3 Backstage ได้เพิ่มเพลงลงไปในงานแสดงดนตรีนั้น ๆแล้ว<br> PRE-4 วันที่ต้องการ run event ตรงกับวันจัด event ที่ได้กรอกไว้ภายในระบบ |
| **7. Postconditions** | POST-1 Backstage ทำการเริ่มงานแสดงดนตรีสำเร็จ |
| **11. Priority** | High |
| **12. Frequency of Use** | 1 ครั้งต่อ 1 งานดนตรี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมดที่เกี่ยวข้อง 
2. Backstage เลือกงานงานแสดงดนตรีจากรายการงานแสดงดนตรีที่มี 
    - ระบบทำการแสดงหน้ารายละเอียดของงานแสดงดนตรีที่เลือก 
3. Backstage กดปุ่ม "เริ่ม Event"

#### 9. Alternative Flow
- None

#### 10. Exceptions
**Backstage เลือก Event ไม่ตรงกับวันจริง** 
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมดที่เกี่ยวข้อง 
2. Backstage เลือกงานงานแสดงดนตรีจากรายการที่มี 
    - ระบบทำการแสดงหน้ารายละเอียดของงานแสดงดนตรีที่เลือก 
3. Backstage กดปุ่ม "เริ่ม Event" 
    - ระบบแสดงข้อความการแจ้งเตือน "ไม่สามารถเริ่ม Event ได้เนื่องจากยังไม่ถึงวันกำหนดการ" 
4. Backstage ตรวจสอบและเลือกงานแสดงดนตรีให้ถูกต้องอีกครั้ง 
5. Use case ดำเนินตามปกติ

# Use Case Specification: รายละเอียดกรณี Assign เพลงให้ Performer

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 12 |
| **2. Use Case Name** | assign เพลงให้ Performer |
| **3. Primary Actor** | Backstage |
| **4. Description** | Backstage สามารถ Assign เพลงให้ Performer เพื่อใช้ในการจัด Queue และแจ้งเตือน Queue ในขณะที่ขึ้นแสดง |
| **5. Trigger** | Backstage ต้องการ Assign เพลงให้ performer |
| **6. Preconditions** | PRE-1 Backstage มีการเพิ่ม Event ลงไปในระบบแล้ว <br> PRE-2 Backstage ได้เพิ่มเพลงลงไปใน Event นั้นๆแล้ว <br> PRE-3 Backstage ยืนยันตัวตนสำเร็จ |
| **7. Postconditions** | POST-1 Performer ถูก Assign ไปยังเพลงที่เกี่ยวข้องอย่างถูกต้อง |
| **11. Priority** | High |
| **12. Frequency of Use** | 4-12 ครั้งต่อเพลง |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมด 
2. Backstage เลือกงานงานแสดงดนตรีจากรายการที่มี 
3. Backstage กดปุ่ม "ดูรายชื่อเพลง" 
4. ระบบแสดงรายชื่อเพลงที่ใช้ในการแสดงของงานแสดงดนตรีนั้น  
5. Backstage เลือกเพลงที่ต้องการจะ assign
    - ระบบทำการแสดงหน้ารายละเอียดของเพลงโดยจะมี ชื่อเพลง จำนวน performer ในแต่ละตำแหน่ง , คีย์เพลง (Song Key) ,อ้างอิงเพลง (reference) 
6. Backstage เลือกตำแหน่ง ของ performer ที่ต้องการจะ assign 
7. Backstage เลือกชื่อ Performer ทั้งหมดที่ต้องการและกดยืนยัน 
    - ระบบบันทึกข้อมูลการ Assign 
8. หากต้องการ Assign เพลงเพิ่มเติมในตำแหน่งอื่น ๆ 
9. Backstage กดย้อนกลับไปยังหน้ารายชื่อเพลงที่ต้องการ Assign 
10. Backstage ทำซ้ำขั้นตอน 5 - 9 
11. Use Case สิ้นสุดเมื่อ Backstage ไม่ต้องการ Assign เพลงเพิ่มเติม

#### 9. Alternative Flow
**Backstage ต้องการยกเลิกการ assign** 
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมด 
2. Backstage เลือกงานงานแสดงดนตรีจากรายการที่มี 
    - ระบบทำการแสดงหน้ารายละเอียดของงานแสดงดนตรีที่เลือก 
3. Backstage กดปุ่ม "ดูรายชื่อเพลง" 
    - ระบบแสดงรายชื่อเพลงที่ใช้ในการแสดงของงานแสดงดนตรีนั้น
4. Backstage เลือกเพลงที่ต้องการจะ assign 
    - ระบบทำการแสดงหน้ารายละเอียดของเพลงโดยจะมี ชื่อเพลง จำนวน performer ในแต่ละตำแหน่ง , คีย์เพลง (Song Key) ,อ้างอิงเพลง (reference) 
5. Backstage เลือกตำแหน่ง ของ performer ที่ต้องการจะ assign 
6. Backstage เลือกชื่อ Performer ทั้งหมดที่ต้องการและกดยืนยัน 
7. Backstage ตัดสินใจยกเลิกการ assign โดยกดย้อนกลับ 
8. สิ้นสุด alternative flow 

#### 10. Exceptions
**เพลงยังไม่ได้ถูกเพิ่มลงไปในระบบ**
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมด 
2. Backstage เลือกงานงานแสดงดนตรีที่เกี่ยวข้อง 
    - ระบบทำการแสดงหน้ารายละเอียดของ งานแสดงดนตรีที่เลือก 
3. Backstage กดปุ่ม "ดูรายชื่อเพลง" 
4. ระบบแสดงรายการเพลง 
5. Backstage ไม่พบเพลงที่ต้องการ 
    - Backstage ดำเนินการตาม Use Case: เพิ่มเพลงใน Queue เพื่อเพิ่มเพลงที่ต้องการ 
6. ระบบกลับไปที่หน้ารายการเพลง
    - Backstage เลือกเพลงที่เพิ่งเพิ่มและดำเนินการ Assign เพลงต่อไป 
7. Use Case ดำเนินการตามปกติ 

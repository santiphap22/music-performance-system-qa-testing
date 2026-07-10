# Use Case Specification: รายละเอียดกรณีแจ้งเตือน Queue ให้ Performer

| Use Case Attribute | Specification Details |
| :--- | :--- |
| **1. Use Case ID** | 15 |
| **2. Use Case Name** | แจ้งเตือน queue ให้ Performer |
| **3. Primary Actor** | Backstage |
| **4. Description** | Backstage สามารถกดแจ้งเตือนให้นักดนตรีในเพลงถัดไปโดยแจ้งเตือนผ่าน Discord direct message ด้วย Discord bot |
| **5. Trigger** | ฺBackstage ต้องการแจ้งเตือนเพลงให้นักดนตรีระหว่างการจัดแสดงดนตรีในเวลานั้นๆ |
| **6. Preconditions** | PRE-1 Backstage ทำการยืนยันตัวตนสำเร็จ <br> PRE-2 Backstage ได้ทำการเพิ่ม event ลงในระบบแล้ว <br> PRE-3 Backstage ทำการสร้างคิวเพลงและ assign performer ครบเรียบร้อยแล้ว <br> PRE-4 Backstage ทำการกด run event แล้ว |
| **7. Postconditions** | POST-1 performer ที่เกี่ยวข้องได้รับแจ้งเตือนผ่าน discord direct message |
| **11. Priority** | High |
| **12. Frequency of Use** | 5 – 30 ครั้งต่อหนึ่งงานดนตรี |

---

### Workflows & Flow of Events

#### 8. Normal Flow
1. Backstage เลือก "Event" จากหน้า Main Menu 
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมดที่เกี่ยวข้อง 
2. Backstage เลือกงานงานแสดงดนตรีที่ได้กด run 
ไปแล้ว 
    - ระบบจะแสดงว่ากำลังเล่นเพลงอะไรอยู่ ณ ตอนนี้ ด้วยการไฮไลท์สี พร้อมปุ่มแจ้งเตือนและปุ่มสำหรับเลือกเพลงถัดไป 
3. Backstage กดปุ่มแจ้งเตือน 
    - ระบบแสดงหน้าฟอร์มโดยสามารถเลือกกรอกข้อความเพิ่มเติมถึง performer ได้ 
4. Backstage ทำการกดปุ่ม "แจ้งเตือน Performer" 
    - ระบบจะทำการส่งข้อมูลติดต่อไปที่ discord bot 
    - discord bot จะส่ง direct message ไปให้ performer ที่เกี่ยวข้องของเพลงนั้นๆ 
    - performer ได้รับการแจ้งเตือนเป็นข้อความว่า "เพลงต่อไปเป็นเพลงของคุณแล้วกรุณามาเตรียมตัว" 
    - ระบบจะแสดงข้อความ "แจ้งเตือนสำเร็จ" 
5. หากต้องการส่งแจ้งเตือนเพลงอื่น ๆ 
    - ระบบจะพาไปที่หน้า queue เพลง 
6. Backstage ทำ use case เลือกเพลงถัดไป 
7. Backstage ทำซ้ำขั้นตอน 2 - 4 
8. Use case จะสิ้นสุดเมื่อ Event นั้นจบลงแล้ว 

#### 9. Alternative Flow
**Backstage ต้องการเขียน notification message ด้วยตนเอง**
1. Backstage เลือก "Event" จากหน้า Main Menu
    - ระบบแสดงรายการงานแสดงดนตรีทั้งหมดที่เกี่ยวข้อง 
2. Backstage เลือกงานงานแสดงดนตรีที่ได้กด run ไปแล้ว 
    - ระบบจะแสดงว่ากำลังเล่นเพลงอะไรอยู่ ณ ตอนนี้ ด้วยการไฮไลท์สี พร้อมปุ่มแจ้งเตือนและปุ่มสำหรับเลือกเพลงถัดไป 
3. Backstage กดปุ่มแจ้งเตือน 
    - ระบบแสดงหน้าฟอร์มโดยสามารถเลือกกรอกข้อความเพิ่มเติมถึง performer ได้ 
4. Backstage ทำการกรอกข้อความส่งไปที่ performer 
    - Backstage ทำการกดปุ่ม "แจ้งเตือน Performer" 
    - ระบบทำการติดต่อส่งข้อมูลไปที่ discord bot 
    - Discord bot ส่งข้อความไปให้ Performer ที่เกี่ยวข้องในเพลงนั้น ๆ 
    - performer ได้รับการแจ้งเตือนเป็นข้อความว่า "เพลงต่อไปเป็นเพลงของคุณแล้วกรุณามาเตรียมตัว"และต่อด้วยข้อความเพิ่มเติมที่ Backstage ได้กรอกมา 
    - ระบบแสดงข้อความ “แจ้งเตือนสำเร็จ” 
5. หากต้องการส่งแจ้งเตือนเพลงอื่นๆ 
    - ระบบจะพาไปที่หน้า queue เพลง 
6. Backstage ทำ use case เลือกเพลงถัดไป

#### 10. Exceptions
- None

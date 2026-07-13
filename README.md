# music-performance-system-qa-testing
This repository contains the comprehensive Software Quality Assurance (QA) documentation and test artifacts for the SCI BAND MUSIC PERFORMANCE MANAGEMENT SYSTEM. The project focuses on rigorous Manual Testing based on business workflows, requirement analysis, and backend API validation to ensure system stability and an optimal user experience before deployment.

---

## Project Overview & Scope
The SCI Band Management System is designed to streamline live music coordination, band performance schedules, and live event queue management. 

As a Quality Gatekeeper, my responsibility was to analyze the system requirements, map them into comprehensive test documentation, and validate both the frontend application workflows and backend API behaviors against the specifications.

### Tech Stack & Tools Used
* Documentation & Mapping: Dillinger.io (Markdown)
* API Specification & Discovery: Swagger / OpenAPI UI
* API Testing: Postman
* Defect Tracking: GitHub Issues / Markdown Documentation
* Testing Types Covered: Functional Testing, Integration Testing, End-to-End (E2E) Workflow Testing, API Validation, Negative/Exception Testing.

---

## Use Case & Test Coverage Matrix

The system features 20 core Use Cases. The table below maps these requirements into their respective detailed specifications and test coverage. 

Note: Click on the links below to view the full specification for each Use Case.

| Use Case ID | Requirement / Use Case Name | Primary Actor | Description | Documentation Link |
| :---: | :---: | :---: | :---: | :---: |
| 1. | login | User ทุกประเภท| User สามารถเข้าสู่ระบบเพื่อใช้งานแอปพลิเคชันตามสิทธิ์ของตนเองได้ | [View Full Spec](./docs/use_cases/UC001_User_Registration.md) |
| 2. | ดูรายละเอียดงานแสดงดนตรี | User ทุกประเภท | User ทุกคนสามารถดูรายละเอียดงานแสดงดนตรีแต่ละงาน เพื่อทราบถึงข้อมูลงานแสดงนั้นๆได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 3. | สร้างงานแสดงดนตรี | Backstage | Backstage สามารถสร้างงานแสดงดนตรีขึ้นมาเพื่อนำข้อมูลเข้าสู่ระบบและเพื่อให้ผู้ใช้ทุกคนสามารถเข้ามาดูรายละเอียดได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 4. | แก้ไขรายละเอียดงานแสดงดนตรี | Backstage | Backstage สามารถการแก้ไขรายละเอียดงานแสดงดนตรีที่สร้างเอาไว้ เช่น ชื่อ วันเวลา | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 5. | ลบงานแสดงดนตรี | Backstage | Backstage สามารถลบงานแสดงดนตรีที่ถูกยกเลิกไปแล้วหรือเสร็จสิ้นแล้วได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 6. | ดู queue เพลง | User ทุกประเภท | User สามารถดูคิวเพลงในแต่ละงานแสดงดนตรีได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 7. | เพิ่มเพลงลงใน queue | Backstage | Backstage สามารถเพิ่มเพลงลงใน queue ของงานแสดงดนตรีนั้น ๆ ได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 8. | แก้ไขเพลงใน Queue | Backstage | Backstage สามารถแก้ไขชื่อเพลง รายละเอียด และ Performer ที่เล่นในเพลงนั้น ๆ ได้  | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 9. | ย้าย Queue เพลง | Backstage | Backstage สามารถย้าย queue เพลงได้กรณีที่มีการเปลี่ยนแปลงของ queue เพลงก่อนจะเริ่มงานแสดงดนตรี | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 10. | ลบเพลงใน Queue | Backstage | Backstage สามารถลบเพลงออกจาก Queue ของงานแสดงดนตรีนั้นๆได้ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 11. | ดูรายละเอียดเพลง | User ทุกประเภท | User ทุกคนสามารถดูรายละเอียดในแต่ละเพลงได้ว่าเพลงนั้นมี Performer คนไหนเล่นบ้าง รวมถึง ชื่อเพลง, คีย์เพลง และอ้างอิงเพลง (reference) | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 12. | assign เพลงให้ Performer | Backstage | Backstage สามารถ Assign เพลงให้ Performer เพื่อใช้ในการจัด Queue และแจ้งเตือน Queue ในขณะที่ขึ้นแสดง | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 13. | Run event | Backstage | Backstage สามารถเริ่มงานแสดงดนตรีที่เลือกได้เมื่อถึงวันแสดงจริงตามที่ได้กรอกไว้ภายในระบบ เพื่อทำการรันคิวเพลงและเปิดระบบการแจ้งเตือนให้กับ Performer | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 14. | เลือกเพลงถัดไป | Backstage | Backstage สามารถเลือกเพลงถัดไปในการแสดงสดเพื่อเป็นการรันคิวเพลง | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 15. | แจ้งเตือน queue ให้ Performer | Backstage | Backstage สามารถกดแจ้งเตือนให้นักดนตรีในเพลงถัดไปโดยแจ้งเตือนผ่าน Discord direct message ด้วย Discord bot | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 16. | เคลียร์ user ออกจากระบบ | System admin | System admin สามารถเคลียร์ User ที่จบการศึกษาไปแล้วออกจากระบบได้และระบบจะทำการลบผู้ใช้ออกจาก discord channels โดยอัตโนมัต | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 17. | เพิ่มบัญชีผู้ใช้เข้าสู่ระบบ | System admin | System adminสามารถเพิ่ม User ใหม่ให้สามารถเข้าใช้งานระบบได้และระบบจะทำการเพิ่มผู้ใช้เข้าสู่ discord channels ที่เกี่ยวข้องโดยอัตโนมัติ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 18. | ดู Profile | User ทุกประเภท | User ทุกคนสามารถดู Profile ของตัวเองได้ว่าข้อมูลถูกต้องหรือไม่ | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 19. | Logout | User ทุกประเภท | User สามารถ logout ออกจากระบบเมื่อไม่ใช้งาน | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |
| 20. | โอนย้ายสิทธิ์ system admin | System admin | System adminต้องการโอนย้ายสิทธิ์ผู้ดูแลให้คนในชุมนุมในกรณีที่หมดวาระหรือออกจากชุมนุม | [View Full Spec](./docs/use_cases/UC002_User_Login.md) |


---

## Core Test Deliverables

To meet professional QA standards, the project deliverables are structured as follows:

### 1. Requirements & Workflow Analysis (Manual Testing)
* Test Scenarios & Test Cases: Developed detailed test steps based on Normal Flows, Alternative Flows, and Exceptions defined in the Use Case Specifications.
* End-to-End Workflows: Verified critical business flows, such as a full cycle of creating a performance event (UC003), managing the song queue (UC006-UC010), and running live events (UC013-UC014).

### 2. Integration & API Testing
* API Specification Review: Utilized Swagger UI to analyze API endpoints, required request parameters, header requirements, and schema definitions.
* Behavior Validation: Validated HTTP response codes (e.g., 200 OK, 201 Created, 400 Bad Request, 404 Not Found) via Postman based on the Swagger specifications.
* Data Integration: Verified backend payload responses to ensure JSON structures contain correct data types and mandatory fields.

### 3. Defect Management & Reporting
* Sample Bug Reports: Structured clear, actionable Defect Reports containing Steps to Reproduce, Expected vs. Actual Results, Severity/Priority levels, and environment details to ensure seamless collaboration with developers.

---

## Repository Structure

```text
├── README.md                      # Main portfolio landing page (This file)
├── docs/
│   ├── use_cases/                 # Detailed Use Case Specifications (UC001 - UC020)
│   │   ├── UC001_User_Login.md
│   │   └── UC002_View_Performance_Details.md
│   │   └── UC003_Create_Performance.md
│   │   └── UC004_Update_Performance_Details.md
│   │   └── UC005_Delete_Performance.md
│   │   └── UC006_View_Song_Queue.md
│   │   └── UC007_Add_Song_To_Queue.md
│   │   └── UC008_Update_Song_In_Queue.md
│   │   └── UC009_Move_Song_Queue.md
│   │   └── UC010_Delete_Song_From_Queue.md
│   │   └── UC011_View_Song_Details.md
│   │   └── UC012_Assign_Song_To_Performer.md
│   │   └── UC013_Run_Event.md
│   │   └── UC014_Select_Next_Song.md
│   │   └── UC015_Notify_Queue_To_Performer.md
│   │   └── UC016_Remove_User_From_System.md
│   │   └── UC017_Add_User_Account.md
│   │   └── UC018_View_Profile.md
│   │   └── UC019_User_Logout.md
│   │   └── UC020_Transfer_System_Admin_Role.md
│   ├── test_cases/                # Manual Test Case sheets (Happy Path / Negative Cases)
│   └── api_testing/               # API Spec mappings and Postman collections
└── defects/                       # Documented Defect/Bug Reports

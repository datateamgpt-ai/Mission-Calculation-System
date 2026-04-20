# Todo: ระบบล็อกอิน + จัดการผู้ใช้ + เชิญเข้าใช้งาน

## Phase 1: อัพเกรด full-stack
- [x] เรียก webdev_add_feature เพื่อเพิ่ม web-db-user
- [x] ศึกษา README ที่ได้หลังอัพเกรด

## Phase 1.5: Branding
- [x] เพิ่มชื่อ "สำนักงานวิชาการ" ใน Navbar, Home, Footer และทุกหน้าที่เกี่ยวข้อง

## Phase 2: พัฒนาระบบ
- [x] เพิ่มระบบล็อกอิน (Manus OAuth)
- [x] สร้างหน้าจัดการผู้ใช้งานสำหรับแอดมิน
- [x] เพิ่มระบบเชิญคนเข้าใช้งาน พร้อมลิงก์รับ 500 เครดิตฟรี (https://manus.im/invitation/W8WBBIUOKL15SO)
- [x] ป้องกันหน้าที่ต้องล็อกอินก่อนเข้าใช้งาน
- [x] แอดมินจัดการ role ผู้ใช้ได้ (admin/user)

## Phase 3: ทดสอบ
- [x] ทดสอบระบบล็อกอิน
- [x] ทดสอบหน้าจัดการผู้ใช้
- [x] ทดสอบลิงก์เชิญ
- [x] vitest tests ผ่านทั้งหมด (10/10)

## Phase 4: ระบบแจ้งเตือนผู้ดูแลระบบ
- [x] เพิ่มระบบแจ้งเตือน admin เมื่อมีผู้ใช้ใหม่ลงทะเบียน (notifyOwner ใน OAuth callback)
- [ ] เพิ่มหน้าแสดงประวัติการแจ้งเตือน (notification log) ใน admin panel
- [x] เขียน vitest tests สำหรับระบบแจ้งเตือน

## Phase 5: ปรับปรุงคำเตือนหน้าตรวจสอบพันธกิจ
- [x] ปรับคำเตือนให้แสดงสาเหตุที่ชัดเจน (StructuredWarning type)
- [x] เพิ่มแนวทางแก้ไขเบื้องต้นที่ผู้อัพโหลดทำได้เอง (cause + resolution fields)
- [x] ปรับ UI ให้อ่านง่ายและเข้าใจได้ทันที (accordion expand/collapse + color-coded levels)
- [x] vitest tests สำหรับ calculator structured warnings (13 tests)

## Phase 6: ระบบกำหนดสิทธิ์การมองเห็น + จำกัดล็อกอิน @spu.ac.th
- [x] จำกัดล็อกอินเฉพาะอีเมล @spu.ac.th เท่านั้น (ปฏิเสธ gmail.com และอื่นๆ เด็ดขาด)
- [x] สร้าง database schema สำหรับ user_permissions (กำหนดคณะที่เห็นได้)
- [x] สร้าง database schema สำหรับ user_teacher_permissions (กำหนดอาจารย์ที่เห็นผลคำนวณได้)
- [x] สร้าง tRPC API สำหรับจัดการสิทธิ์ (CRUD permissions)
- [x] ปรับหน้า Admin จัดการผู้ใช้ให้กำหนดสิทธิ์คณะ/อาจารย์ได้
- [x] กรองข้อมูลหน้าตรวจสอบพันธกิจตามสิทธิ์ผู้ใช้
- [x] กรองข้อมูลหน้าข้อมูลพันธกิจ/รายวิชาตามสิทธิ์ผู้ใช้
- [x] เขียน vitest tests สำหรับระบบสิทธิ์

## Phase 7: ดูผลคำนวณรายบุคคล + ระบบขอแก้ไข + Admin กำหนด Admin
- [x] สร้างหน้าดูผลคำนวณพันธกิจรายบุคคล (เลือกอาจารย์ → ดูรายละเอียดเฉพาะท่า- [x] สร้าง database schema สำหรับ edit_requestsำขอแก้ไข + สาเหตุ + เอกสารแนบ + สถานะอนุมัติ)
- [x] สร้าง API สำหรับ submit/list/approve/reject edit requests
- [x] สร้าง UI สำหรับผู้ใช้ส่งคำขอแก้ไข (ฟอร์ม + แนบไฟล์ + ระบุสาเหตุ)
- [x] สร้างหน้า Admin อนุมัติ/ปฏิเสธคำขอแก้ไข
- [x] Admin สามารถกำหนด role admin ให้ผู้ใช้คนอื่นได้
- [x] เพิ่มการกรองข้อมูลตามสิทธิ์ในหน้า MissionData, CourseData, CheckMission
- [x] เขียน vitest tests สำหรับ edit request flow

## Phase 8: ลิงก์คำเชิญหน้าล็อกอิน
- [x] เพิ่มลิงก์คำเชิญ https://manus.im/invitation/W8WBBIUOKL15SO ในหน้า Home/Login
- [x] แจ้งว่าใช้ได้เฉพาะอีเมล @spu.ac.th เท่านั้น
- [x] ปรับ LoginErrorPage ให้แสดงลิงก์คำเชิญด้วย

## Phase 8.5: แดชบอร์ดเลือก "ทั้งหมด" + สิทธิ์ตามการอัพโหลด
- [x] แดชบอร์ดเพิ่มตัวเลือก "ทั้งหมด" ดูข้อมูลรวมทุกคณะ
- [x] เจ้าหน้าที่เห็นเฉพาะคณะที่ตัวเองอัพโหลด + คณะที่ Admin กำหนด
- [x] Admin กำหนดผู้ดูข้อมูลคณะได้ในหน้าจัดการทีม

## Phase 9: ประวัติการคำนวณย้อนหลังรายเดือน + เปรียบเทียบ
- [x] สร้าง DB schema สำหรับ calculation_snapshots (บันทึกผลคำนวณแต่ละรอบ)
- [x] สร้าง DB schema สำหรับ calculation_snapshot_details (รายละเอียดแต่ละอาจารย์)
- [x] สร้าง tRPC API สำหรับบันทึกผลคำนวณ (save snapshot)
- [x] สร้าง tRPC API สำหรับดึงรายการ snapshots + รายละเอียด
- [x] สร้าง tRPC API สำหรับเปรียบเทียบ 2 snapshots
- [x] เพิ่มปุ่ม "บันทึกผลคำนวณ" ในหน้า CheckMission
- [x] สร้างหน้า CalculationHistoryPage ดูรายการประวัติคำนวณ
- [x] สร้างหน้า CompareSnapshotsPage เปรียบเทียบ 2 เดือน
- [x] เพิ่ม route + navigation ใน App.tsx และ Navbar
- [x] เขียน vitest tests สำหรับ calculation history (14 tests, 55 total passed)

## Phase 10: กราฟเส้นแนวโน้มค่าสอนรวมรายเดือน
- [x] สร้าง tRPC API สำหรับดึงข้อมูลแนวโน้ม (snapshots.trend)
- [x] สร้าง TrendChartPage หรือเพิ่มกราฟในหน้า CalculationHistoryPage
- [x] ใช้ Recharts สร้างกราฟเส้นแสดงค่าสอนรวม/เบิกได้/จำนวนอาจารย์ตามเวลา
- [x] เพิ่มตัวกรองคณะในกราฟ
- [x] เพิ่ม route + navigation ใน App.tsx และ Navbar
- [x] เขียน vitest tests สำหรับ trend API (5 tests, 60 total passed)

## Phase 11: ปรับปรุง Tooltip กราฟแท่งจำนวนอาจารย์
- [x] ปรับ snapshots.trend API ให้ส่งข้อมูลรายละเอียดอาจารย์ top 5 ในแต่ละ snapshot
- [x] สร้าง Custom Tooltip component แสดงรายชื่ออาจารย์ ค่าสอน หน่วยกิตเบิกได้
- [x] ทดสอบ UI hover บนกราฟแท่ง

## Phase 12: ระบบอนุมัติผลคำนวณ (Approval System)

### DB Schema
- [x] เพิ่ม role 'approver' ใน user schema
- [x] สร้างตาราง approval_requests (id, snapshot_id, submitted_by, status, note, locked_data_hash, created_at, updated_at)
- [x] สร้างตาราง approval_decisions (id, request_id, decided_by, decision, comment, decided_at)
- [x] สร้างตาราง approval_audit_logs แทน approval_revisions (audit trail ครบถ้วนกว่า)
- [x] Run pnpm db:push

### Backend API
- [x] สร้าง approval.submit — ส่งขออนุมัติพร้อม hash ข้อมูล
- [x] สร้าง approval.myRequests — ดูรายการที่ส่งไป
- [x] สร้าง approval.pending — ดูรายการรออนุมัติ (approver only, กรองตามสิทธิ์คณะ)
- [x] สร้าง approval.detail — ดูรายละเอียดรายการ + hash verification
- [x] สร้าง approval.decide — อนุมัติ/ปฏิเสธ/ขอแก้ไข พร้อม hash verification + audit trail
- [x] สร้าง approval.resubmit — รวมใน submit (revision chain auto-detect)
- [x] สร้าง approval.history — ประวัติทั้งหมดพร้อม audit trail + กรองคณะ
- [x] สร้าง approval.pendingCount — นับจำนวนรออนุมัติสำหรับ badge + กรองคณะ

### UI ฝั่งเจ้าหน้าที่
- [x] สร้าง SubmitApprovalDialog ใน CalculationHistoryPage (ส่งขออนุมัติจากหน้าประวัติคำนวณ)
- [x] สร้าง MyApprovalsPage — ดูสถานะรายการ + คอมเมนต์ผู้บริหาร

### UI ฝั่งผู้บริหาร
- [x] สร้าง ApprovalDashboardPage — รายการรออนุมัติ + สรุปยอด
- [x] สร้าง ApprovalDetailPage — ดูรายละเอียด + ปุ่มตัดสินใจ (อนุมัติ/ปฏิเสธ/ขอแก้ไข)

### UI ส่วนกลาง
- [x] สร้าง ApprovalHistoryPage — ประวัติการอนุมัติ (audit trail) (รวมใน ApprovalDetailPage)
- [x] เพิ่ม routes ใน App.tsx
- [x] เพิ่มเมนูใน Navbar (แยกตาม role)
- [x] เพิ่ม notification badge สำหรับรายการรออนุมัติ (Navbar + Dashboard)

### ความรัดกุม (Security & Audit)
- [x] Hash ข้อมูลผลคำนวณตอนส่งอนุมัติ เพื่อตรวจสอบว่าไม่ถูกแก้ไข (SHA-256)
- [x] ล็อคข้อมูล snapshot หลังส่งอนุมัติ ห้ามลบ/แก้ไข
- [x] บันทึก audit trail ทุก action (ใคร ทำอะไร เมื่อไหร่)
- [x] ป้องกันการอนุมัติซ้ำ / ส่งซ้ำ
- [x] Vitest tests สำหรับ approval flow ทั้งหมด (27 tests ผ่าน)

### พิมพ์รายงานรายบุคคล (Printable Report)
- [x] สร้างหน้า PrintableTeacherReport — รายงานสรุปพันธกิจรายบุคคลสำหรับพิมพ์
- [x] แสดงข้อมูล: ชื่อ-สกุล, คณะ, อัตรา, จำนวนพันธกิจ, จำนวนวิชา, เงินที่คำนวณได้
- [x] ปุ่มพิมพ์ (window.print) + CSS @media print สำหรับ layout A4 landscape
- [x] เข้าถึงได้จากหน้า ApprovalDetailPage (ปุ่มพิมพ์รายงาน)

### กรองสิทธิ์คณะในระบบอนุมัติ
- [x] ผู้บริหาร/approver เห็นเฉพาะคณะที่ตัวเองมีสิทธิ์ดูแล
- [x] Admin เห็นทุกคณะ

## Phase 13: แก้ไขระบบ Data Sharing (User เห็นข้อมูลที่ Admin อัพโหลด)

- [x] เพิ่มตาราง shared_faculty_data ใน DB schema (เก็บ JSON ข้อมูลอาจารย์+วิชา)
- [x] เพิ่ม sharedData router ใน routers.ts (listFaculties, getFacultyData, upsertFacultyData, deleteFacultyData)
- [x] แก้ไข UploadPage ให้บันทึกข้อมูลลง DB หลังอัพโหลด Excel (admin)
- [x] แก้ไข DataContext + SharedDataContext ให้ sync กับ DB
- [x] แก้ไข PermissionDialog ใน AdminUsersPage ให้ดึงรายชื่อคณะจาก DB
- [x] เพิ่มหน้า AdminFacultyDataPage สำหรับ Admin ดูและลบข้อมูลที่อัพโหลดไว้ใน DB
- [x] ทดสอบ flow: Admin อัพโหลด → User ที่มีสิทธิ์เห็นข้อมูล

## Phase 14: Admin Faculty Data Management + Notifications + Auto-Sync

### Feature 1: หน้า Admin จัดการข้อมูลคณะ
- [x] สร้าง API endpoint ลบข้อมูลคณะ (sharedData.deleteFaculty)
- [x] สร้าง API endpoint อัพเดตข้อมูลคณะ (re-upload/replace)
- [x] สร้าง API endpoint ดูรายละเอียดคณะ (จำนวนอาจารย์, วิชา, วันที่อัพโหลด)
- [x] สร้างหน้า AdminFacultyDataPage — ตารางแสดงคณะทั้งหมดใน DB + กรองตามภาคเรียน
- [x] ปุ่มลบ + ยืนยันก่อนลบ
- [x] ปุ่มอัพเดต (re-upload Excel ทับข้อมูลเดิม)
- [x] เพิ่ม route + Navbar menu

### Feature 2: ระบบแจ้งเตือน User
- [x] สร้างตาราง userNotifications ใน DB schema
- [x] สร้าง API endpoint สร้าง notification เมื่อ Admin อัพโหลดข้อมูล
- [x] สร้าง API endpoint ดึง notifications ของ user
- [x] สร้าง API endpoint mark as read
- [x] สร้าง Bell icon (NotificationBell) + notification dropdown ใน Navbar
- [x] แจ้งเตือนอัตโนมัติเมื่อ Admin อัพโหลด/อัพเดต/ลบข้อมูลคณะ

### Feature 3: ระบบ Sync อัตโนมัติ
- [x] สร้าง data version tracking (dataVersions table ใน DB)
- [x] สร้าง API endpoint ตรวจสอบ data version (dataVersion.get)
- [x] สร้าง auto-sync polling ใน SharedDataContext (30s interval)
- [x] เมื่อ version เปลี่ยน → auto-refresh SharedDataContext
- [x] แสดง toast แจ้ง user ว่ามีข้อมูลใหม่

### Testing & Delivery
- [x] Vitest tests ผ่านทั้งหมด (87 tests)
- [ ] Checkpoint + ส่งมอบ

## Phase 15: แยกข้อมูลอาจารย์/รายวิชาตามภาคเรียน
- [x] ปรับ schema sharedFacultyData เพิ่ม semester field + unique constraint (facultyName + semester)
- [x] อัพเดต API endpoints (upsert/list/get/delete) ให้รองรับ semester
- [x] อัพเดต UploadPage ให้เลือกภาคเรียนก่อนอัพโหลด
- [x] อัพเดต AdminFacultyDataPage ให้แสดง/กรอง/ลบตามภาคเรียน
- [x] อัพเดต SharedDataContext ให้ดึงข้อมูลตาม semester + auto-sync polling
- [x] อัพเดต usePermissions ให้รองรับ semester
- [x] อัพเดต MissionDataPage, CourseDataPage, CheckMissionPage ให้เลือกภาคเรียน
- [x] เพิ่ม routes + Navbar menu สำหรับ AdminFacultyDataPage
- [x] เขียน vitest tests (87 tests ผ่าน)
- [ ] Checkpoint + ส่งมอบ

## Phase 16: หลักการคำนวณพันธกิจรายวิชากลุ่ม 500 (Self-Paced Learning)
- [x] ตรวจสอบโครงสร้าง calculator.ts, excelParser.ts, DataContext
- [x] แก้ไข calculator.ts เพิ่ม logic คำนวณกลุ่ม 500 (Class Size 160, 50%, 2 กรณี)
- [x] แก้ไข excelParser.ts ตรวจจับรายวิชากลุ่ม 500 + ดึงคอลัมน์ "ลง" (จำนวน นศ.)
- [x] อัพเดต DataContext/interfaces เพิ่ม field isGroup500, enrolledStudents
- [x] อัพเดต CheckMissionPage แสดงผลกลุ่ม 500 (badge, tooltip, คำนวณแยก)
- [x] อัพเดต MissionDataPage, CourseDataPage แสดง badge กลุ่ม 500
- [x] อัพเดต PrintableTeacherReport รองรับกลุ่ม 500
- [x] อัพเดต snapshot storage รองรับกลุ่ม 500
- [x] เขียน vitest tests สำหรับ logic กลุ่ม 500 (21 tests ผ่าน, 108 total)
- [x] Checkpoint + ส่งมอบ

## Phase 17: กราฟแท่งเปรียบเทียบภาระงานวิชาปกติ vs กลุ่ม 500 ในหน้า TrendChart
- [x] ศึกษาโครงสร้าง TrendChartPage และ trend API ปัจจุบัน
- [x] เพิ่ม Group 500 data ใน trend API (normalMissionCredits, group500MissionCredits)
- [x] สร้างกราฟแท่ง Stacked Bar เปรียบเทียบปกติ vs กลุ่ม 500 ใน TrendChartPage
- [x] เขียน vitest tests สำหรับ trend API ที่อัพเดต (111 tests ผ่าน)
- [x] Checkpoint + ส่งมอบ

## Phase 18: เพิ่มโลโก้ OAA และข้อมูลติดต่อสำนักงานวิชาการ
- [x] อัพโหลดโลโก้ OAA ไปยัง S3 และเตรียมข้อมูล
- [x] เพิ่มโลโก้ OAA ที่มุมซ้ายบนของ Header (ขนาดใหญ่ชัดเจน)
- [x] เพิ่มส่วน Contact Information ที่ส่วนท้ายของหน้า Home
- [x] ทดสอบ, save checkpoint, ส่งมอบ

## Phase 19: ระบบข่าวสารและอัปเดต
- [x] ออกแบบ DB schema (news table) + อัพโหลด PDF ตัวอย่างไป S3
- [x] สร้าง API procedures (CRUD news + file upload) + push migration
- [x] สร้างหน้า Admin จัดการข่าว (สร้าง/แก้ไข/ลบ/แนบไฟล์)
- [x] เพิ่มส่วนข่าวสารในหน้า Home + หน้าอ่านข่าวเต็ม (NewsDetailPage)
- [x] เขียน vitest tests สำหรับ news API (18 tests ผ่าน, 129 total)
- [x] ทดสอบ, save checkpoint, ส่งมอบ

## Phase 20: เพิ่ม role 'executive' สำหรับผู้บริหารคณะ/หน่วยงาน
- [x] ศึกษาโครงสร้าง role ปัจจุบัน (admin, user, approver)
- [x] อัพเดต DB schema — เพิ่ม executive ใน role enum + สร้าง comments table
- [x] อัพเดต backend API — เพิ่ม comment procedures, ปรับ permission guards ให้ executive ดูได้แต่แก้ไม่ได้
- [x] อัพเดต frontend — UI สำหรับ executive (view-only + comment), หน้าจัดการผู้ใช้เพิ่ม role executive
- [x] เขียน vitest tests สำหรับ executive role และ comment API (19 tests ผ่าน, 148 total)
- [x] ทดสอบ, save checkpoint, ส่งมอบ

## Phase 21: เพิ่มระบบคอมเมนต์ในหน้าอนุมัติ
- [x] ศึกษา ApprovalDetailPage และ comments API ปัจจุบัน
- [x] อัพเดต backend API — เพิ่ม approval comment procedures (list/add by approvalRequestId)
- [x] อัพเดต ApprovalDetailPage — เพิ่ม CommentsSection สำหรับคำขออนุมัติ
- [ ] เขียน vitest tests สำหรับ approval comments
- [ ] ทดสอบ, save checkpoint, ส่งมอบ
- [x] แก้ไขข่าวสารในหน้า Home ให้แสดงข่าวล่าสุดอยู่ทางซ้าย
- [x] แก้ไข dropdown menu ให้มี scrollbar เลื่อนได้เมื่อรายการเยอะ
- [x] จัดกลุ่มเมนู Navbar เป็น dropdown ย่อย (ข้อมูล / คำนวณ / จัดการ)
- [x] แก้ไขเบอร์ติดต่อในหน้า Home เป็น "0 2558 6888 ต่อ 1127, 1128"
- [x] สร้าง FAQ Component พร้อม 5 ข้อคำถามที่สำคัญ
- [x] เพิ่ม FAQ Section ลงในหน้า Home
- [x] สร้าง FAQ database schema + migrations
- [x] สร้าง tRPC procedures สำหรับ FAQ CRUD (create, read, update, delete)
- [x] สร้าง Admin FAQ Management page
- [x] เพิ่ม Like/Highlight feature สำหรับ FAQ
- [x] อัปเดต FAQSection component ให้แสดง like count และ featured items
- [x] เพิ่มเมนู "จัดการ FAQ" ในเมนู "จัดการ" (Navbar)
- [x] เพิ่ม Search/Filter ใน FAQ Section สำหรับผู้ใช้ค้นหาคำถาม
- [x] เพิ่ม Excel Import FAQ สำหรับ Admin นำเข้าคำถามจำนวนมาก
- [x] เพิ่ม FAQ Analytics สำหรับ Admin ดูสถิติ Like และ View count
- [x] ตรวจสอบและแก้ไขสูตรการคำนวณกลุ่ม 500 ให้มาจาก Column "Lec" หรือ "Lab" ในข้อมูลรายวิชา
- [x] แก้ไขเมนู "จัดการ FAQ" ให้ปรากฏใน Navbar อย่างถูกต้อง
- [x] ตรวจสอบ Excel Import FAQ ทำงานถูกต้อง
- [x] ตรวจสอบ FAQ Analytics ทำงานถูกต้อง
- [x] แก้ไขข้อผิดพลาด "Maximum update depth exceeded" ใน FAQSection.tsx บรรทัดที่ 23
- [x] แก้ไขข้อความภาษาไทยที่แสดงเป็น Unicode escape sequences ในหน้าประวัติการคำนวณ (รายละเอียด)

## Phase 27: แก้ไข 4 รายการ (Bug fixes + New features)
- [x] แก้ไข dropdown เลือกคณะในหน้ารายบุคคล — เลือกแล้วล็อคทุกคณะ ไม่สามารถเปลี่ยนได้
- [x] เพิ่ม Export CSV สำหรับผลตรวจพันธกิจที่บันทึกแล้ว
- [x] แก้ไขหน้า Home — ส่วนข่าวสารหายไป- [x] เพิ่มเมนู ตารางสอนของอาจารย์รายบุคคล

## Phase 28: แจ้งเตือนเมื่อผลคำนวณพร้อมดาวน์โหลด CSV
- [x] เพิ่ม notification เมื่อบันทึกผลคำนวณพันธกิจสำเร็จ — แจ้งเตือนผู้ใช้ที่เกี่ยวข้อง
- [x] แสดง notification ในระบบ bell icon พร้อม link ไปหน้า CalculationHistory เพื่อดาวน์โหลด CSV
- [x] แจ้งเตือน owner ผ่าน notifyOwner เมื่อมีการบันทึกผลคำนวณใหม่


## Phase 29: ปรับปรุงระบบตามความต้องการ (ลำดับความสำคัญ)

### Priority 1: กรองข้อมูลตามสาขาวิชา
- [x] เพิ่มระดับ "สาขาวิชา" ใน Database schema (sharedFacultyData)
- [x] อัพเดต Excel template เพิ่มคอลัมน์ "สาขาวิชา"
- [x] เพิ่ม filter สาขาวิชาในหน้า MissionDataPage
- [x] เพิ่ม filter สาขาวิชาในหน้า CourseDataPage
- [x] เพิ่ม filter สาขาวิชาในหน้า CheckMissionPage
- [x] เพิ่ม filter สาขาวิชาในหน้า TeacherDetailPage
- [x] เพิ่ม filter สาขาวิชาในหน้า TeacherSchedulePage
- [x] แก้ Excel parser อ่านคอลัมน์ "สาขา" จากทั้ง 2 ไฟล์ Excel
- [ ] เขียน vitest tests สำหรับ branch filtering

### Priority 2: แสดงเวลาสอน + Same As status
- [ ] เพิ่มคอลัมน์ "เวลาสอน" ในหน้า CourseDataPage (display only)
- [ ] เพิ่ม logic ตรวจจับ "Same As" (วิชาที่มีกลุ่ม A นำหน้า เช่น A100, A500)
- [ ] เพิ่ม badge/status แสดง "Same As" ในหน้า CourseDataPage
- [ ] เพิ่ม badge/status แสดง "Same As" ในหน้า CheckMissionPage
- [ ] ปรับ calculator logic ให้ skip "Same As" courses ในการคำนวณ
- [ ] เขียน vitest tests สำหรับ Same As detection

### Priority 3: ล็อคอัตราค่าตอบแทน
- [ ] สร้าง master data table สำหรับอัตราค่าสอน (compensation_rates)
- [ ] ปรับ Excel upload ให้อ้างอิง compensation rates จาก master data
- [ ] ล็อคอัตราค่าสอนในระบบ ไม่ให้แก้ไขจาก Excel
- [ ] สร้าง Admin page จัดการอัตราค่าสอน (CRUD)
- [ ] เขียน vitest tests สำหรับ compensation rates

### Priority 4: Export Excel + PDF
- [ ] เพิ่ม Excel export สำหรับผลตรวจพันธกิจ (ใช้ openpyxl)
- [ ] เพิ่ม PDF export สำหรับผลตรวจพันธกิจ (ใช้ reportlab)
- [ ] เพิ่มปุ่ม Export Excel/PDF ในหน้า CalculationHistoryPage
- [ ] เขียน vitest tests สำหรับ export functionality

### Priority 5: AI วิเคราะห์แนวโน้ม
- [ ] สร้าง tRPC procedure สำหรับ AI analysis (เปรียบเทียบภาระงาน/งบประมาณระหว่างภาค)
- [ ] เพิ่ม AI analysis section ในหน้า TrendChartPage
- [ ] แสดงผลวิเคราะห์ (ความแตกต่าง, สาเหตุที่เป็นไปได้, ข้อเสนอแนะ)
- [ ] เขียน vitest tests สำหรับ AI analysis

### Priority 6: ยึดสังกัดรายวิชาเป็นหลัก
- [ ] ศึกษา logic การคำนวณปัจจุบัน
- [ ] ปรับ calculator ให้ยึดสังกัดรายวิชา แม้อาจารย์จากคณะอื่นมาสอน
- [ ] อัพเดต CheckMissionPage แสดง "สังกัดรายวิชา" ชัดเจน
- [ ] เขียน vitest tests สำหรับ course affiliation logic

### Priority 7: ตรวจสอบความครบถ้วนกับฐานข้อมูลทะเบียน
- [ ] ออกแบบ validation logic (เทียบข้อมูลรายวิชาที่อัพโหลด vs ข้อมูลจากทะเบียน)
- [ ] สร้าง import template สำหรับข้อมูลจากทะเบียน (Excel/CSV)
- [ ] เพิ่ม validation report ในหน้า Admin
- [ ] แสดง warning/error เมื่อข้อมูลไม่ตรงกับทะเบียน
- [ ] เขียน vitest tests สำหรับ validation logic


## Phase 30: เพิ่มแสดงข้อมูลงบประมาณแยกตามหมวด
- [x] ศึกษา CheckMissionPage และ calculation result structure
- [x] เพิ่ม budget breakdown calculation (regular vs special mission)
- [x] เพิ่ม Budget Summary Card ในหน้า CheckMissionPage
- [x] แสดงข้อมูล: งบประมาณอาจารย์ประจำ, อาจารย์พิเศษ, รวมทั้งสิ้น
- [ ] เขียน vitest tests สำหรับ budget calculation

## Phase 31: ปรับปรุงระบบตามเอกสาร PDF (11 รายการ)

### A. MissionDataPage (หน้าข้อมูลพันธกิจ)
- [x] A1: แยก Summary Card แสดงจำนวนอาจารย์ประจำ vs อาจารย์พิเศษ
- [x] A2: แสดงรายชื่ออาจารย์ที่ไม่ได้จัดการสอน (missing teachers) พร้อมให้ติดตามสถานะได้

### B. CourseDataPage (หน้ารายวิชา)
- [x] B1: เพิ่ม Summary Card จำแนก ทฤษฎี/ปฏิบัติ
- [x] B2: เพิ่มจำนวนกลุ่ม (sections) ใน Self-Paced card

### C. TeacherDetailPage (หน้ารายละเอียดอาจารย์)
- [x] C1: เพิ่มสถานะ On/Off toggle สำหรับแต่ละวิชา (Off = ไม่นำไปคำนวณ)

### D. CheckMissionPage (หน้าตรวจสอบพันธกิจ)
- [x] D1: ปรับปรุง name matching ให้ยืดหยุ่นมากขึ้น (fuzzy matching)
- [x] D2: เพิ่ม label "เพดานงบประมาณ" ที่ชัดเจน (ห้ามเบิกเกินอัตรานี้)

### E. TeacherSchedulePage (หน้าตารางสอน)
- [x] E1: ปรับเป็น Weekly Schedule Grid (ตารางรายสัปดาห์ เห็นความหนาแน่น)
- [x] E2: แสดงความหนาแน่นของตารางสอน (สีเข้มเมื่ออัดแน่น)
- [x] E3: แสดง On/Off status ในตาราง

### F. Testing
- [x] F1: เขียน vitest tests สำหรับการปรับปรุงทั้งหมด
- [x] E4: ใช้ตัวอย่างรูปตารางสอนจากผู้ใช้ — Weekly Grid แกน Y=วัน(M,T,W,H,F,S,U), แกน X=เวลา 08-21, สีแยกทฤษฎี(เหลือง)/ปฏิบัติ(ชมพู/ม่วง)

### F. Master Faculty List (Dropdown ชื่อคณะ/วิทยาลัย)
- [x] F1: สร้าง Master Faculty List constant (12 คณะ/วิทยาลัย)
- [x] F2: เปลี่ยน UploadPage — ชื่อคณะเป็น Dropdown แทนการกรอก
- [x] F3: เปลี่ยน MissionDataPage — เลือกคณะเป็น Dropdown จาก Master List
- [x] F4: เปลี่ยน CourseDataPage — เลือกคณะเป็น Dropdown จาก Master List
- [x] F5: เปลี่ยน TeacherDetailPage — เลือกคณะเป็น Dropdown จาก Master List
- [x] F6: เปลี่ยน CheckMissionPage — เลือกคณะเป็น Dropdown จาก Master List
- [x] F7: เปลี่ยน TeacherSchedulePage — เลือกคณะเป็น Dropdown จาก Master List
- [x] F8: เปลี่ยน DashboardPage + EditRequestsPage + AdminUsersPage — เพิ่ม MASTER_FACULTIES
- [x] F9: ตรวจสอบทุกจุดอื่นที่ใช้ชื่อคณะ — ครบทุกหน้า

## Phase 32: แก้ไขการจับชื่อคณะจากข้อมูลในไฟล์ Excel
- [ ] G1: ตรวจสอบ Excel parser ว่าอ่านคอลัมน์ "คณะ" อย่างไร
- [ ] G2: แก้ไข parser ให้ดึงชื่อคณะจากคอลัมน์ "คณะ" ในแถวข้อมูล (ไม่ใช่ชื่อไฟล์)
- [ ] G3: แก้ไข UploadPage ให้ auto-detect ชื่อคณะจากข้อมูลในไฟล์ (แสดงใน dropdown เป็น readonly)
- [ ] G4: แสดงผลข้อมูลพันธกิจตามชื่อคณะที่ถูกต้องในทุกหน้า
- [ ] G5: เขียน vitest tests และ save checkpoint

## Phase 32: Dual Upload Mode (อัพโหลดทั้งหมด vs รายคณะ)
- [x] G1: เพิ่ม parseMissionTeacherByFaculty() — แยกข้อมูลอาจารย์ตามคอลัมน์ คณะ คืน Map<facultyName, teachers[]>
- [x] G2: เพิ่ม parseCourseByFaculty() — แยกข้อมูลรายวิชาตามคอลัมน์ คณะ คืน Map<facultyName, courses[]>
- [x] G3: ปรับ UploadPage เพิ่ม mode toggle: อัพโหลดทั้งหมด vs อัพโหลดรายคณะ
- [x] G4: โหมด อัพโหลดทั้งหมด — auto-split ตามคณะ, แสดงสรุปรายคณะที่พบ
- [x] G5: โหมด อัพโหลดรายคณะ — เลือกคณะ Dropdown แล้วอัพโหลด (เหมือนเดิม)
- [x] G6: เขียน vitest tests สำหรับ parseMissionTeacherByFaculty และ parseCourseByFaculty (15 tests ผ่าน, 214 total)

# Workshop Files — Claude Cowork for Business (Siam Food Services)

ไฟล์ประกอบการอบรม 1 วัน สำหรับบริษัทจัดจำหน่ายอาหาร (Frozen / Chilled / Dry / Beverage / Packaging) ขายให้ร้านอาหาร โรงแรม และเคเทอริ่งในประเทศไทย

> **ข้อมูลทั้งหมดเป็นข้อมูลจำลอง (mock)** ชื่อบริษัท ลูกค้า พนักงาน สินค้า และตัวเลข ถูกสร้างขึ้นเพื่อการอบรมเท่านั้น ไม่เกี่ยวข้องกับบุคคลหรือบริษัทจริง

## วิธีดาวน์โหลด

**แบบ ZIP (แนะนำสำหรับผู้เรียน)**
1. เปิดหน้า repo นี้บน GitHub
2. คลิกปุ่มสีเขียว **Code** → **Download ZIP**
3. แตกไฟล์ไว้ในโฟลเดอร์ เช่น `Documents/claude-workshop/`

หรือดาวน์โหลดตรง: `https://github.com/batprem/siam-food-service-claude-workshop/archive/refs/heads/main.zip`

**แบบ git**
```
git clone https://github.com/batprem/siam-food-service-claude-workshop.git
```

## โครงสร้างไฟล์และการใช้งาน

| ไฟล์ / โฟลเดอร์ | ใช้ใน | ใช้ทำอะไร |
|---|---|---|
| `cheat_sheet.md` | ทุก Module | สูตร prompt และตัวอย่างตามแผนก |
| **module-2-play-with-claude/** | Module 2: ลองเล่น Claude | |
| `sales_q3.xlsx` | Workshop 2.1 | ยอดขาย ก.ค.–ก.ย. 2569 ~300 รายการ ให้ Claude สรุป/หา insight |
| `expense_report_jul/aug/sep.xlsx` | Workshop 2.2 | รายงานค่าใช้จ่ายรายเดือน แต่ละไฟล์มี ~5 รายการที่ผิดนโยบาย |
| `expense_policy.md` | Workshop 2.2 | นโยบายเบิกค่าใช้จ่ายฉบับย่อ ใช้คู่กับไฟล์ expense |
| `messy_folder/` | Workshop 2.3 "จัดไฟล์" | ไฟล์ตั้งชื่อมั่ว 16 ไฟล์ ให้ Claude เสนอโครงสร้างและเปลี่ยนชื่อ |
| **module-3-prompt-and-skill/** | Module 3: Prompt และ Skill | |
| `sales_daily.xlsx` | Workshop 3.1 | ยอดขายรายวัน ก.ค.–ก.ย. 2569 (ส.ค. ≈ 11.4 ล้าน ต่ำกว่าเป้า 12 ล้าน) |
| `complaints.txt` | Workshop 3.2 | ข้อร้องเรียน 12 รายการจาก LINE OA มี lot ซ้ำ 3 ครั้ง และ 2 รายการไม่ระบุสินค้า |
| `qa_severity_criteria.md` | Workshop 3.2 | เกณฑ์ สูง/กลาง/ต่ำ สำหรับคัดกรองข้อร้องเรียน |
| `sales_mock.csv` | Workshop 3.3 HTML dashboard | ยอดขาย 12 เดือน × หมวด × ภูมิภาค × SKU (720 แถว) |
| `inventory_mock.xlsx` | Workshop 3.3 / Capstone | สต็อก 200 รายการ 3 คลัง ~15% หมดอายุภายใน 30 วันจาก 25 ก.ย. 2569 |
| `SKILL_TEMPLATE.md` | Workshop 3.4 | แม่แบบเขียน SKILL.md |
| `example-skills/` | Workshop 3.4 | ตัวอย่าง skill 3 ตัว: sales-visit-report, expense-policy-check, complaint-triage |
| `company_template.pptx` | Workshop 3.5 | เทมเพลตสไลด์ 3 แบบ (ปก / คั่นส่วน / เนื้อหา) |
| **module-4-fabric-mcp/** | Module 4: ต่อข้อมูลผ่าน MCP | |
| `mcp_setup_guide.md` | Workshop 4.1 | ขั้นตอนเพิ่ม connector ใน Claude Desktop และการแก้ปัญหา |
| `sample_questions.md` | Workshop 4.2 | คำถามภาษาธรรมชาติแยกตามแผนก |
| **module-5-capstone/** | Module 5: Capstone | |
| `capstone_brief.md` | Capstone | โจทย์ pipeline Marketing → Buyer → Production → Sales, timebox, เกณฑ์ตัดสิน |
| `handoff_templates/` | Capstone | แม่แบบไฟล์ส่งต่อ 4 ไฟล์ |

## ข้อมูลอ้างอิงในไฟล์

- วันที่อ้างอิง "วันนี้" ของข้อมูล: **25 กันยายน 2569 (2026-09-25)**
- หมวดสินค้า: Frozen, Chilled, Dry, Beverage, Packaging
- ภูมิภาค: กรุงเทพ, ภาคกลาง, ภาคตะวันออก, ภาคเหนือ, ภาคอีสาน, ภาคใต้
- คลังสินค้า: บางนา, วังน้อย, ขอนแก่น
- รหัส SKU: FZ- (Frozen), CH- (Chilled), DR- (Dry), BV- (Beverage), PK- (Packaging)
- lot ที่มีปัญหาในแบบฝึกหัด: **FZ-1042 lot L2609A**

## หมายเหตุ

- ไฟล์ .pdf / .docx ใน `messy_folder/` เป็น placeholder มีข้อความสั้น ๆ เท่านั้น
- URL ของ MCP connector ไม่อยู่ใน repo นี้ ผู้สอนจะแจกในห้องอบรม

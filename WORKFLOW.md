# GitHub × ChatGPT × Obsidian Workflow

ระบบนี้แบ่งหน้าที่ให้แต่ละเครื่องมือชัดเจน เพื่อให้เขียนนิยายระยะยาวร่วมกันได้โดยไม่ทำ canon สูญหายหรือขัดแย้ง

## หน้าที่ของแต่ละส่วน

### GitHub — แหล่งความจริงและประวัติ
- เก็บไฟล์ Markdown, YAML Properties, Wikilinks และประวัติทุก commit
- `main` คือสถานะที่ยอมรับแล้วของ Story Bible
- ทุกการเปลี่ยน canon ต้องมี commit ที่อธิบายว่าเพิ่ม เปลี่ยน หรือยกเลิกอะไร
- ใช้ diff ตรวจว่า ChatGPT หรือผู้เขียนแก้เกินขอบเขตหรือไม่

### Obsidian — โต๊ะทำงานของผู้เขียน
- เปิด repository ทั้งโฟลเดอร์เป็น vault
- ใช้ Graph, Backlinks, Properties และ Search สำรวจความเชื่อมโยง
- เพิ่มหรือแก้ Event, Character และ Ledger ผ่านโฟลเดอร์ `templates/`
- เขียนร่างและข้อเสนอได้ แต่ต้องกำหนด `canon_status` ให้ถูกต้องก่อน commit

### ChatGPT — ผู้ช่วยเขียนและตรวจ continuity
- อ่าน canon และ ledger ก่อนเสนอหรือเขียนฉาก
- แยกข้อเท็จจริงที่ยืนยันแล้วออกจากการเสนอใหม่
- ช่วยแตกฉาก ตรวจว่าใครรู้อะไร ตรวจ timeline และผลต่อความสัมพันธ์
- เมื่อได้รับอนุญาตจึงแก้ repository และ commit พร้อมรายงานไฟล์ที่เปลี่ยน
- ห้ามยกระดับ PROPOSED/TBD เป็น CANON เอง

## วงจรการทำงานแนะนำ

1. **Pull** — ดึง `main` ล่าสุดจาก GitHub ก่อนเริ่ม
2. **Inspect** — เปิด [[indexes/home|Vault Home]], Event ที่เกี่ยวข้อง และ Ledgers ใน Obsidian
3. **Brief** — สร้างงานจาก [[templates/chatgpt-task-template]] ระบุขอบเขตและสิ่งที่ห้ามเปลี่ยน
4. **Draft** — ให้ ChatGPT เสนอฉาก/โครง/การแก้ พร้อมระบุ CANON กับ PROPOSED
5. **Review** — ตรวจข้อเสนอใน Obsidian และตัดสินใจสิ่งที่จะยืนยัน
6. **Update** — แก้ Event, Character, Timeline, Relationship, Knowledge และ Dialogue เท่าที่ได้รับผล
7. **Audit** — ใช้ [[templates/continuity-audit-template]] ตรวจความต่อเนื่อง
8. **Commit & Push** — commit หนึ่งหัวข้อที่ชัดเจน แล้วส่งขึ้น GitHub
9. **Sync** — เครื่องอื่น pull ก่อนทำงานต่อ

## กฎเปลี่ยน Canon
1. ผู้สร้างระบุชัดว่า “เป็น canon”, “ยืนยัน”, “เปลี่ยน canon” หรือความหมายเทียบเท่า
2. เพิ่ม/แก้ไฟล์ใน `canon/`
3. ปรับ Character/Event Notes และ Ledgers ที่ได้รับผล
4. บันทึกใน [[workflow/decision-log|Decision Log]]
5. Commit ด้วยข้อความขึ้นต้น `canon:`

## สถานะงาน
- `CANON` — ยืนยันแล้ว
- `CANON_WITH_TBD_DETAILS` — ตัวตนหรือแกนยืนยัน รายละเอียดยังเปิด
- `CANON_ARC_DIRECTION` — ยืนยันทิศทาง ไม่ได้ล็อกทุกฉาก
- `CANON_ENDPOINT` — ยืนยันผลลัพธ์ปลายช่วง
- `PROPOSED` — ข้อเสนอที่รอผู้สร้างเลือก
- `UNDECIDED` / `TBD` — ยังไม่มีคำตัดสิน

## เมื่อเกิดความขัดแย้ง
- ใช้คำตัดสินล่าสุดของผู้สร้างเป็นหลัก
- อย่าลบข้อมูลเก่าโดยไม่ดูผลกระทบ; ใช้ Git history และ diff
- ตรวจ Event ถัดไป, backlinks, Knowledge Ledger และ Dialogue Ledger
- หากข้อมูลไม่พอ ให้คง TBD แทนการเดา

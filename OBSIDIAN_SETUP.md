# เปิด Hero เป็น Obsidian Vault

Repository นี้มีโฟลเดอร์ `.obsidian/` แล้ว จึงถือเป็น Obsidian vault ที่ตั้งค่าพื้นฐานพร้อมใช้งาน

## วิธีเปิดครั้งแรก
1. Clone หรือดาวน์โหลด repository `sakon9654/Hero` ลงเครื่อง
2. เปิด Obsidian
3. เลือก **Manage vaults → Open folder as vault**
4. เลือกโฟลเดอร์ราก `Hero`
5. เปิด [[indexes/home|Vault Home]] เป็นหน้าเริ่มต้น

## สิ่งที่ตั้งค่าไว้
- อัปเดต Wikilinks อัตโนมัติเมื่อย้ายหรือเปลี่ยนชื่อโน้ต
- สร้างลิงก์แบบ relative เพื่อให้ repository ย้ายเครื่องได้
- เก็บไฟล์แนบใน `attachments/`
- เปิด core plugins ที่ใช้กับ vault นี้ เช่น Graph, Backlinks, Outgoing Links, Properties และ Templates
- Templates core plugin ใช้โฟลเดอร์ `templates/`
- ไม่ติดตั้ง community plugin ใดโดยอัตโนมัติ เพื่อความปลอดภัยและลดปัญหาข้ามเครื่อง
- ไฟล์สถานะหน้าต่าง `workspace.json` ถูกละเว้นจาก Git เพราะเป็นการจัดหน้าจอเฉพาะเครื่อง

## วิธีเพิ่มข้อมูล
- เหตุการณ์ใหม่: [[templates/event-template]]
- ตัวละครใหม่: [[templates/character-template]]
- ความสัมพันธ์: [[templates/relationship-update-template]]
- ความรู้ของตัวละคร: [[templates/knowledge-update-template]]
- บทสนทนาสำคัญ: [[templates/dialogue-entry-template]]

หลังเพิ่มเหตุการณ์ ให้ปรับ [[continuity/timeline]], [[continuity/relationship-ledger]], [[continuity/knowledge-ledger]] และ [[continuity/dialogue-ledger]] เท่าที่เหตุการณ์นั้นเปลี่ยนสถานะจริง

## Canon safety
ตรวจ `canon_status` ทุกครั้ง:
- `CANON` — ยืนยันแล้ว
- `CANON_WITH_TBD_DETAILS`, `CANON_ARC_DIRECTION`, `CANON_ENDPOINT` — ยืนยันเฉพาะแกน
- `PROPOSED`, `UNDECIDED`, `TBD` — ยังไม่ใช่ canon

รายละเอียดการสร้าง vault จากโฟลเดอร์เดิมและการใช้ Templates อ้างอิงจากเอกสารทางการของ Obsidian

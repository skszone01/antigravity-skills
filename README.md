# 🚀 Antigravity Skills Collection

คลังรวมทักษะขั้นสูง (Custom Skills & Agentic Protocols) สำหรับใช้งานบน **Google Antigravity (AGY)**

---

## 🏛️ สกิลเด่นในคลัง (Featured Skills)

### 1. 🤖 [subagent](./subagent/SKILL.md) — 3-Tier Enterprise Multi-SubAgent Hierarchy Protocol
ระบบควบคุมและกระจายงานขั้นสูงแบบพีระมิด 3 ชั้น **(หัวหน้าใหญ่ ➔ รองหัวหน้า ➔ ลูกน้องช่างเฉพาะทาง 1:N)** ออกแบบมาเพื่อแก้ปัญหาโปรเจกต์ขนาดใหญ่ที่ซับซ้อน ป้องกันโค้ดชนกัน 100% และจัดการวงจรชีวิตกระบวนการอย่างสมบูรณ์

#### จุดเด่นสำคัญ:
- **Autonomous Auto-Assessment (โหมดประเมินงานอัตโนมัติ):** สั่งพิมพ์แค่ `/subagent` ลอยๆ ระบบจะสแกน Git Status, Uncommitted Diff, และ Build Logs เพื่อระบุปัญหาและจัดช่างเข้าประจำจุดเองทันที
- **Two-Tier File Whitelist (ระบบคุมไฟล์ 2 ชั้น):**
  - *ระดับหัวหน้าใหญ่ (Macro):* ล็อกแดนข้ามฝ่าย (เช่น UI ห้ามแตะ DB)
  - *ระดับรองหัวหน้า (Micro):* คุมลูกน้องในสังกัดตนเอง (1:N) ไม่ให้ลูกน้องแย่งกันแก้ไฟล์เดียวกัน
- **Zero-Bias Independent Audit:** เมื่อรวมงานเสร็จ หัวหน้าใหญ่จะ Spawn ทีมตรวจรับงานชุดใหม่เอี่ยม (Fresh Context) ปราศจากความทรงจำเดิม เพื่อตรวจ Review Diff รวมแบบ 100% ไร้อคติ
- **Empirical Build Gate:** บังคับรันคำสั่งคอมไพล์จริงให้ผ่านก่อนส่งตรวจรับงานเสมอ
- **Zero-Hanging Cleanup:** บังคับเรียก `manage_subagents: kill_all` เคลียร์ทรัพยากรทุกตัวทันทีเมื่องานจบ ป้องกัน Spinner หมุนค้างใน UI

---

## 📦 วิธีติดตั้งและนำไปใช้งาน (Installation & Usage)

### 1. ติดตั้งลงในเครื่องของคุณ:
โคลน Repository นี้ไปไว้ที่โฟลเดอร์ Skills ของ Antigravity:
```bash
# Windows PowerShell
git clone https://github.com/skszone01/antigravity-skills.git "$env:USERPROFILE\.gemini\config\skills"
```
หรือหากมีโฟลเดอร์อยู่แล้ว สามารถคัดลอกเฉพาะโฟลเดอร์สกิลที่ต้องการ (เช่น โฟลเดอร์ `subagent/`) ไปวางไว้ที่:
`~/.gemini/config/skills/`

### 2. เรียกใช้งานในแชท Antigravity:
พิมพ์คำสั่ง Slash Command:
```text
/subagent
```
(หรือ `/subagent [รายละเอียดงานที่ต้องการให้ช่วย]`)

# Claude Website Workshop

Workshop ลงมือสร้างเว็บไซต์จริงด้วย Claude Code — ตั้งแต่ติดตั้งจนถึงสร้างเว็บด้วย AI

---

## ก่อนเริ่ม (Prerequisites)

- [Node.js](https://nodejs.org/) v18+
- npm (ติดมากับ Node.js)
- [Anthropic API Key](https://console.anthropic.com/)

---

## เริ่มต้นใช้งาน

### 1. ติดตั้ง Claude Code

```bash
# ติดตั้งแบบ global
npm install -g @anthropic-ai/claude-code

# หรือรันโดยไม่ต้องติดตั้ง
npx @anthropic-ai/claude-code
```

### 2. Clone project นี้

```bash
git clone https://github.com/hspotlight/claude-website-workshop.git
cd claude-website-workshop
```

### 3. เริ่ม Claude Code

```bash
# เปิด interactive mode
claude

# เริ่มพร้อม prompt ทันที
claude "explain this project"

# ต่อจาก session ที่แล้ว
claude --continue

# รันแบบ headless (ไม่มี UI)
claude -p "what does this project do?"
```

---

## หน้าเว็บในโปรเจกต์นี้

| ไฟล์ | สไตล์ | คำอธิบาย |
|------|-------|----------|
| `index.html` | Terminal / dev-lab | หน้าหลัก รวม link ไปทุกหน้า |
| `bakery.html` | Dark luxury / French | ร้านเบเกอรี่ มี cart และ filter สินค้า |
| `reading-fast.html` | Editorial brutalist | Landing page ขาย e-book วิธีอ่านหนังสือเร็ว |

---

## Deploy ขึ้น GitHub Pages

1. Push code ขึ้น GitHub
2. ไปที่ repo → **Settings → Pages**
3. เลือก source: **Deploy from a branch → `main` → `/ (root)`**
4. เว็บจะขึ้นที่ `https://<username>.github.io/<repo-name>/`

---

## AI Skills จาก Matt Pocock

**Matt Pocock** เป็น TypeScript educator ชื่อดัง (เจ้าของ [Total TypeScript](https://www.totaltypescript.com/)) ที่ได้สร้างระบบ **Skills** สำหรับ Claude Code ขึ้นมา

### Skills คืออะไร?

Skills คือ slash command พิเศษที่ติดตั้งเพิ่มใน Claude Code เพื่อขยายความสามารถให้ทำงานเฉพาะทางได้ดีขึ้น เช่น เขียน test, วิจารณ์แผน, สร้าง PRD ฯลฯ

แทนที่จะพิมพ์ prompt ยาวๆ ซ้ำๆ — พิมพ์แค่ `/skill-name` แล้ว Claude จะรู้ว่าต้องทำอะไร

### Skills ที่ติดตั้งใน Project นี้ (`.claude/skills/`)

#### 🔨 วางแผน & ออกแบบ

| Skill | Command | ทำอะไร |
|-------|---------|--------|
| **grill-me** | `/grill-me` | สัมภาษณ์แผนอย่างโหด เพื่อหาจุดอ่อนก่อนลงมือสร้าง |
| **grill-with-docs** | `/grill-with-docs` | เหมือน grill-me แต่สร้าง ADR และ glossary ระหว่าง interview ด้วย |
| **grilling** | `/grilling` | Stress-test ความคิด plan หรือ decision ก่อน commit |
| **codebase-design** | `/codebase-design` | ออกแบบ module interface แบบ deep module — ลด complexity, เพิ่ม clarity |
| **domain-modeling** | `/domain-modeling` | สร้าง domain model และ ubiquitous language ของ project |
| **wayfinder** | `/wayfinder` | วางแผนงานใหญ่เกินกว่า 1 session เป็น decision tickets บน issue tracker |

#### 💻 Development

| Skill | Command | ทำอะไร |
|-------|---------|--------|
| **tdd** | `/tdd` | Test-Driven Development — เขียน test ก่อน แล้วค่อย implement (red→green→refactor) |
| **code-review** | `/code-review` | รีวิว code ตั้งแต่ commit/branch ที่กำหนด ตาม Standards และ Spec คู่กัน |
| **implement** | `/implement` | Implement งานจาก spec หรือ tickets ที่เตรียมไว้ |

#### 📋 Spec & Tickets

| Skill | Command | ทำอะไร |
|-------|---------|--------|
| **to-spec** | `/to-spec` | แปลงบทสนทนาเป็น spec แล้ว publish ไปที่ issue tracker ทันที |
| **to-tickets** | `/to-tickets` | แตกงานเป็น tracer-bullet tickets พร้อม blocking edges ส่งไป tracker |

#### 🔁 Workflow & Agent

| Skill | Command | ทำอะไร |
|-------|---------|--------|
| **handoff** | `/handoff` | Compact บทสนทนาปัจจุบันเป็น handoff doc ให้ agent อื่นทำงานต่อ |
| **teach** | `/teach` | สอน skill หรือ concept ใหม่ภายใน workspace นี้ |
| **writing-great-skills** | `/writing-great-skills` | Reference สำหรับเขียน skill ที่ดี — vocabulary และ principles |

### ค้นหา Skills เพิ่มเติม

พิมพ์ `/find-skills` ใน Claude Code เพื่อดู skills ที่มีให้ติดตั้งทั้งหมด

---

## โครงสร้างโปรเจกต์

```
.
├── CLAUDE.md            # คำสั่งและ context สำหรับ Claude Code
├── README.md            # ไฟล์นี้
├── index.html           # หน้า index (สไตล์ terminal)
├── bakery.html          # หน้าร้านเบเกอรี่
├── reading-fast.html    # หน้า landing page ขาย e-book
├── .claude/             # Settings และ skills ของ Claude Code
└── .agents/             # Agent skills (grill-me, qa, tdd, to-prd)
```

---

## License

Workshop material — สำหรับการเรียนรู้

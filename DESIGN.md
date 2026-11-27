# DESIGN.md — Mini Cafe Full-Stack Slidev Design System

เอกสารนี้กำหนดมาตรฐานการออกแบบ **Apple Keynote / Linear Editorial** สำหรับชุดสไลด์หลักสูตร **Fundamentals of Web Development (0% → 100% ใน 10 วัน)** เพื่อให้สไลด์ทุกบท (`00-overview` ถึง `10-day10`) มีภาพลักษณ์สวยงาม มินิมอล อ่านง่าย และคุมคุณภาพได้เหมือนกัน 100% ทั้งสำหรับคนทำสไลด์และ AI Agent

---

## 1. Art Direction & Core Principles

- **สไตล์หลัก:** Apple Keynote / Linear Editorial — พื้นหลัง Gradient เต็มจอ + ตัวอักษรสีขาวบริสุทธิ์ (`#ffffff`) + เส้นแบ่ง Hairline บางเฉียบ (`1px`) + กระจกฝ้าโปร่งบาง (`Ultra-Thin Glass`) เฉพาะจุดเน้น
- **No Boxes Inside Boxes:** ห้ามหุ้มทุกหัวข้อด้วยกล่องการ์ดขาวทึบ ให้ปล่อยพื้นที่ว่างหายใจอย่างน้อย **40–50%** ของหน้าสไลด์
- **No Emoji (กฎเหล็ก):** ห้ามใช้ Emoji ในสไลด์, Footer, SVG หรือหัวข้อใดๆ ให้ใช้ **Carbon Vector Icons** ที่มากับ Slidev (เช่น `<carbon:rocket />`, `<carbon:cafe />`, `<carbon:code />`) และโลโก้ SVG ใน `public/logos/` เท่านั้น
- **Vary the Rhythm:** ห้ามวางเลย์เอาต์แบบเดียวกันติดกัน 2 หน้า สลับจังหวะระหว่าง Cover, Asymmetric Split, Hairline Spec Sheet, 4-Column Chapters, Interactive Visual, และ Dark Code Window
- **Punchy Copy + Rich Notes:** ข้อความบนสไลด์ต้องสั้นคม (1 บรรทัด/ประเด็น) เพื่อให้คนฟังโฟกัสที่ผู้สอน แล้วย้ายคำอธิบายละเอียดโทน *"รุ่นพี่มานั่งเล่าให้ฟังข้างๆ"* ไปไว้ใน **Presenter Notes** (`<!-- ... -->`) ทุกหน้า

---

## 2. Visual Tokens & Surfaces

อ้างอิงจาก [style.css](./style.css), [slides.md](./slides.md), และ [setup/shiki.ts](./setup/shiki.ts):

### 2.1 Background & Contrast Veil
- **Wallpaper:** `/images/bg-gradient.png` (`Pastel Peach to Blue Gradient Wallpaper.png`)
- **Contrast Scrim (`.slidev-layout::before`):** ฉากกั้นโปร่งแสงบางๆ `linear-gradient(135deg, rgba(15,23,42,0.30) 0%, rgba(30,27,75,0.16) 52%, rgba(15,23,42,0.28) 100%)` เพื่อรักษาสีพาสเทลเดิมไว้ 100% แต่ทำให้ตัวอักษรสีขาวอ่านคมชัดทุกมุม (รวมถึงมุมพีชสว่างด้านซ้ายล่าง)

### 2.2 Color & Opacity Scale
| Token / Utility | Value | การใช้งาน |
| :--- | :--- | :--- |
| `--ink-white` | `#ffffff` | หัวข้อ (H1–H3), คำเน้น `<strong>`, ตัวเลขหลัก |
| `--ink-soft` | `rgba(255, 255, 255, 0.84)` | เนื้อหาหลัก (Body text) |
| `--ink-muted` | `rgba(255, 255, 255, 0.62)` | Metadata, ป้ายวัน (`DAY 1–5`), เลขหน้า Footer |
| `--hairline` | `rgba(255, 255, 255, 0.24)` | เส้นแบ่งแถวและคอลัมน์ (`1px`) |
| `text-emerald-200` / `bg-emerald-300` | Emerald Accent | จุดหมายปลายทาง / Milestone สำคัญ (เช่น Day 10 Launch) |

### 2.3 Surfaces & Utility Classes (`style.css`)
- **`.thin-glass`** — กระจกฝ้าโปร่งบางสไตล์ visionOS (`rgba(255,255,255,0.12)` + `backdrop-filter: blur(22px)` + `border: 1px solid rgba(255,255,255,0.25)`) ใช้สำหรับแผงสรุป, แผนภาพ Interactive, หรือ Tip Banner เท่านั้น
- **`.hairline-row`** — แถวรายการคั่นด้วยเส้นล่าง `1px solid rgba(255,255,255,0.24)` (แถวสุดท้ายไม่มีเส้น)
- **`.eyebrow-mono`** — ป้ายหมวดหมู่บนหัวข้อ ใช้ `JetBrains Mono` ตัวพิมพ์ใหญ่ `0.78rem` `tracking: 0.1em` คู่กับ `<carbon:... class="w-4 h-4" />`
- **`.logo-chip`** (`41.6px`) / **`.logo-chip-sm`** (`33.6px`) — แผ่นรองโลโก้สีขาว `rgba(255,255,255,0.92)` มุมโค้ง เพื่อให้โลโก้เทคโนโลยีสีเข้ม (เช่น PHP, MariaDB, Apache) คมชัดไม่จมไปกับพื้นหลัง
- **`.code-window`** + **`.code-window-bar`** — หน้าต่างโค้ดสีเข้มสไตล์ macOS (`rgba(15,23,42,0.88)` + `blur(24px)`) จับคู่กับธีม Shiki `vitesse-dark` ใน `setup/shiki.ts`

---

## 3. Typography & Canvas Budget

- **ฟอนต์หลัก (Thai + Sans):** `IBM Plex Sans Thai`
- **ฟอนต์โค้ด & Metadata:** `JetBrains Mono`
- **ขนาดมาตรฐาน:**
  - Cover H1: `3.35rem` (`leading-[1.08]`, `font-extrabold`)
  - Section H1: `2.15rem – 2.65rem` (`font-extrabold`)
  - Item Title: `17px – 20px` (`font-bold`)
  - Body Copy: `13.5px – 16px` (`text-white/80`)
  - Code Window: `0.92rem` (`line-height: 1.52`)
- **Canvas Safe Height Budget (สำคัญมาก):**
  - กรอบ Slidev มาตรฐานคือ `980px × 552px`
  - Padding ของ `.slidev-layout` คือบน `2.25rem` (36px), ข้าง `3.5rem` (56px), ล่าง `3.25rem` (52px สำหรับ Footer ใน `global-bottom.vue`)
  - **ความสูงปลอดภัยของเนื้อหาไม่ควรเกิน `460px`** (ถ้ามีกล่อง Interactive ให้คุม `max-h-[365px]`, ถ้ามี Code Block ไม่ควรเกิน **14–15 บรรทัด**)

---

## 4. Layout Blueprints (7 รูปแบบหลักสำหรับ Day 1–10)

### Pattern A — Dramatic Keynote Cover
หัวข้อ Display ขนาดใหญ่ชิดซ้าย + Eyebrow ด้านบน + แถบโลโก้ลอยใต้เส้น `border-t border-white/25` ด้านล่าง

### Pattern B — Asymmetric Split (40 / 60)
ฝั่งซ้าย (`col-span-5 pr-6 border-r border-white/25`) เป็น Statement / Quote ขนาดใหญ่ ฝั่งขวา (`col-span-7`) เป็นรายการ `.hairline-row` พร้อมตัวเลข `01`–`04` (`font-mono text-2xl text-white/45`)

### Pattern C — Editorial Spec Sheet (สลับซ้าย–ขวา)
ฝั่งหนึ่ง (`col-span-4`) เป็นหัวข้อใหญ่ + ช่วงวันขนาดใหญ่ (`DAY 01—07` สี `text-white/35`) อีกฝั่ง (`col-span-8`) เป็นลิสต์ `.hairline-row` 5 แถว (`.logo-chip-sm` + ชื่อ + คำอธิบาย 1 บรรทัด + แท็กวันฝั่งขวา)

### Pattern D — Giant-Number Horizontal Chapters
4 คอลัมน์ (`grid-cols-4 border-t border-white/25 pt-6`) คั่นด้วยเส้นแนวตั้ง `border-r border-white/20` (ไร้กรอบการ์ด) หัวคอลัมน์เป็นตัวเลข `01`–`04` ขนาด `text-4xl`

### Pattern E — Interactive Split (Visual + Hairline List)
`grid-cols-12 gap-7 max-h-[365px]` — ซ้ายเป็น Vue Component ใน `.thin-glass` (เช่น `<HouseAnalogy :step="$clicks" />`), ขวาเป็น `.hairline-row` ที่เปิดทีละขั้นด้วย `v-click="1"` ถึง `v-click="4"`

### Pattern F — Code Animation (Shiki Magic Move)
ใช้แสดงวิวัฒนาการโค้ดที่ค่อยๆ แปลงร่างอย่างสมูท:
````markdown
<div class="code-window">
<div class="code-window-bar">
  <div class="code-dots">
    <span class="bg-rose-400" />
    <span class="bg-amber-400" />
    <span class="bg-emerald-400" />
  </div>
  <span class="text-xs font-mono text-white/60">filename.ext</span>
</div>

````md magic-move {lines: true}
```html
<!-- Step 1 -->
```

```html
<!-- Step 2 -->
```
````

</div>
````

### Pattern G — Code Line Highlight
ใช้โฟกัสโค้ดทีละส่วนพร้อมดิมบรรทัดอื่น (`has-highlighted` ใน `style.css`):
````markdown
<div class="code-window">
<div class="code-window-bar">...</div>

```yaml {all|2-5|6-10|11-14|all}{lines:true}
# ไม่ควรเกิน 14 บรรทัดเพื่อไม่ให้ชน Footer
```

</div>
````

---

## 5. Animation & Motion Guidelines

- **Slide Transition:** ใช้ `transition: slide-left` สำหรับสไลด์เนื้อหาทั่วไป และ `transition: fade-out` สำหรับหน้าปกและหน้าปิดท้าย
- **Entrance Motion:** ใช้ `v-motion` กับหัวข้อหรือบล็อกหลักด้วยระยะขยับเล็กๆ (`10px – 20px`) และเวลา `400ms – 560ms`
- **Step-by-Step Reveal:** ใช้ `v-click` กับรายการย่อย/แถว/คอลัมน์ เพื่อให้ผู้สอนค่อยๆ เปิดทีละประเด็น
- **Floating Logos:** ใช้ `.animate-float` คู่กับ `style="animation-delay: 0.2s"` แบบสลับจังหวะเฉพาะแถบโลโก้หน้าปก
- **SVG Data Flow:** ใช้ `.animate-dash` สำหรับเส้นประแสดงการไหลของข้อมูลในแผนภาพ SVG

---

## 6. Project Structure & Assets

```text
slide_full-stack/
├── DESIGN.md                 # เอกสาร Design System ฉบับนี้
├── slides.md                 # ไฟล์หลัก (Headmatter + src: imports สำหรับทุกวัน)
├── style.css                 # Global Keynote styles, glass, hairlines, code-window
├── global-bottom.vue         # Minimal footer + progress bar (ซ่อนในหน้า 1 อัตโนมัติ)
├── setup/
│   └── shiki.ts              # บังคับธีม Shiki เป็น vitesse-dark สำหรับหน้าต่างโค้ด
├── components/
│   └── HouseAnalogy.vue      # Interactive SVG Blueprint (sync กับ :step="$clicks")
├── pages/
│   └── 00-overview.md        # บท 00 (เพิ่ม 01-day1.md .. 10-day10.md ในโฟลเดอร์นี้)
└── public/
    ├── images/
    │   └── bg-gradient.png   # พื้นหลัง Pastel Peach to Blue Gradient
    └── logos/                # โลโก้ SVG ทั้ง 10 ตัว (Offline-ready 100%)
        ├── apache.svg
        ├── chrome.svg
        ├── css3.svg
        ├── docker.svg
        ├── html5.svg
        ├── javascript.svg
        ├── mariadb.svg
        ├── php.svg
        ├── phpmyadmin.svg
        └── vscode.svg
```

### การเพิ่มบทเรียนใหม่ (Day 1–10)
สร้างไฟล์ใน `pages/01-day1.md` แล้วนำเข้าต่อท้ายใน `slides.md`:
```yaml
---
src: ./pages/01-day1.md
---
```

---

## 7. Slidev Technical Guardrails (ข้อควรระวังกันบั๊ก)

1. **ห้ามเว้นบรรทัดว่างภายใน HTML Block:** ใน Markdown ของ Slidev ถ้ามีบรรทัดว่างคั่นกลาง `<div>...</div>` แล้วบรรทัดถัดไปย่อหน้า 4 ช่องขึ้นไป Markdown จะตีความเป็น **Code Block** ทันที ให้เขียน HTML ต่อเนื่องไม่มีบรรทัดว่างภายใน
2. **เว้นบรรทัดว่างรอบ Fenced Code Block เสมอ:** ในหน้าที่มี `magic-move` หรือ ` ```lang ` ภายใน `<div class="code-window">` ต้องเว้น 1 บรรทัดว่างก่อนและหลัง Code Block และห้ามย่อหน้าแท็กปิด `</div>` เกิน 2 ช่อง
3. **กำหนด `style="font-size: ...px"` ใน SVG `<text>` เสมอ:** ห้ามใช้แค่แอตทริบิวต์ `font-size="10"` เพราะ CSS ของ Slidev จะ Override ให้ตัวอักษรใน SVG ขยายล้นกรอบ
4. **ตรวจ Build ทุกครั้งหลังแก้ไข:** รัน `npm run build` เพื่อยืนยันว่า Vue template, Carbon icons, Shiki Magic Move และ Line Highlight คอมไพล์ผ่าน 100%

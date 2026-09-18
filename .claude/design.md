# PLearn DE — Design System (design.md)

คู่มืออ้างอิงสำหรับสร้าง Landing Page ของ **PLearn DE (เพลินดี)** — Learning & Workshop Design Team
เอกสารนี้สรุปจาก handoff bundle `plearn-de-branding-design` (Brand Deck, Brand Board, Landing Page prototype)

> **กฎเหล็ก:** ขาวคือพื้นผิวหลักของแบรนด์ ไม่ใช่แค่พื้นหลัง · เขียวหนึ่งบล็อกต่อหนึ่งหน้าจอ · ไม่มีเงา ไม่มีเกรเดียนต์ ไม่มีสีเน้นตัวที่สอง

---

## 1. Brand foundation

| | |
|---|---|
| **Name** | PLearn DE (เพลินดี) |
| **Descriptor** | Learning & Workshop Design Team |
| **Essence** | เราเชื่อว่าคนทำงานไม่ใช่แค่ฟันเฟืองขององค์กร แต่เป็นมนุษย์ที่มีทั้งศักยภาพที่รอการปลดล็อกและพร้อมเติบโตอย่างไม่หยุดยั้ง |
| **Promise** | เราออกแบบประสบการณ์การเรียนรู้จากหัวใจ เพื่อให้ผู้คนได้เชื่อมโยงกับตัวเอง ผู้อื่น และงานที่ทำ จนเกิดพลังในการเปลี่ยนแปลงจริง |
| **Vision** | สร้างระบบนิเวศการเรียนรู้ที่ทุกคนเป็นเจ้าของ ปลดล็อกศักยภาพและคืนความเป็นมนุษย์ให้กับทุกการเติบโตอย่างยั่งยืน |
| **Mission** | PLearn DE คือ Learning & Workshop Design Team ที่เชื่อในศักยภาพของมนุษย์ เราออกแบบประสบการณ์การเรียนรู้ที่ตอบโจทย์ทั้งคนทำงานและองค์กรที่ต้องการปลดล็อกศักยภาพของมนุษย์ และสร้างวัฒนธรรมการทำงานที่เติบโตไปพร้อม ๆ กัน |
| **Contact** | Facebook — https://www.facebook.com/profile.php?id=61557383098262 |

**Style keywords:** Quiet · Airy · Systematic · Unhurried · Human-scale · Warm minimal · Rounded, not cute

---

## 2. Color tokens

พาเลตต์เดียวของแบรนด์ — ห้ามเพิ่มสีนอกชุดนี้

```css
:root {
  /* Brand */
  --forest-ink:  #1F4D35; /* ตัวอักษรเข้ม / พื้นเข้ม / โลโก้หลัก */
  --green:       #2E7A52; /* สีหลักของแบรนด์ — accent, links, dots */
  --soft-green:  #8FBFA4; /* ไดอะแกรม เส้นกราฟิก จุดโปร่ง */
  --mist:        #EFF5F1; /* พื้นรอง (section สลับ) */
  --white:       #FFFFFF; /* พื้นหลัก */

  /* Text */
  --text:        #1F2A23; /* body / headline บนพื้นสว่าง */
  --text-muted:  #3E4B43; /* paragraph รอง */
  --text-subtle: #5A6A5E; /* eyebrow / caption / meta */
  --on-dark:     #FFFFFF;
  --on-dark-dim: #C6DCCF; /* ข้อความรองบนพื้น forest ink */

  /* Lines & surfaces */
  --border:      #DCE5DF; /* เส้นขอบ card / divider */
  --border-soft: #E5EBE7; /* เส้นใต้ header / card outline */
  --board-bg:    #E8EDE9; /* พื้นหลัง board / mockup tray */
}
```

### กติกาการใช้สี
- **60/30/10 แบบกลับด้าน:** ขาว (+Mist) เป็นพื้นส่วนใหญ่ → Forest Ink/Green เป็นหมึกและบล็อก → Soft Green เป็นรายละเอียด
- **เขียวหนึ่งบล็อกต่อหนึ่ง viewport** ให้สีเขียวเป็นจุดเดียวที่สายตาไปหยุด
- ห้าม gradient, ห้าม drop shadow บนองค์ประกอบแบรนด์, ห้ามสีเน้นตัวที่สอง
- บนพื้น `--forest-ink` ใช้ `--white` เป็นหัวข้อ และ `--on-dark-dim` / `--soft-green` เป็นข้อความรอง

---

## 3. Typography

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anuphan:wght@300..700&family=IBM+Plex+Sans+Thai:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

```css
@font-face {
  font-family: 'Bauhaus 93';
  src: url('/fonts/BAUHS93.ttf') format('truetype');
  font-weight: 400; font-style: normal; font-display: swap;
}
```

| Role | Family | Weight | ใช้กับ |
|---|---|---|---|
| **Logotype** | Bauhaus 93 | 400 | โลโก้ไทป์ และ **ตัวเลขลำดับ** (01 02 03) **เท่านั้น** |
| **Headings** | Anuphan | 500–600 | พาดหัวไทย/อังกฤษทุกระดับ |
| **Body** | IBM Plex Sans Thai | 300–500 | เนื้อหา คำอธิบาย eyebrow ปุ่ม เมนู |

> **ห้าม** ใช้ Bauhaus 93 เป็นพาดหัวหรือเนื้อหาเด็ดขาด
> Anuphan และ IBM Plex Sans Thai รองรับไทย+ละตินในครอบครัวเดียว → สองภาษานั่งบนเส้นฐานเดียวกัน ทั้งคู่เป็นฟอนต์ไม่มีหัว

### Type scale (web)

```css
--fs-h1:     clamp(38px, 5.6vw, 72px);  /* Anuphan 600, lh 1.22, ls -0.01em */
--fs-h2:     clamp(30px, 3.8vw, 48px);  /* Anuphan 600, lh 1.25 */
--fs-h2-alt: clamp(26px, 3.2vw, 42px);  /* H2 บนพื้นเข้ม */
--fs-h3:     27px;                      /* Anuphan 600, lh 1.3 */
--fs-h3-sm:  26px;                      /* การ์ดบริการ */
--fs-h4:     26px;                      /* ชื่อขั้นใน roadmap 5D */
--fs-lead:   clamp(17px, 2vw, 22px);    /* Plex, lh 1.7 */
--fs-body:   17px;                      /* Plex, lh 1.7 */
--fs-body-sm:16px;                      /* lh 1.6 */
--fs-meta:   15px;                      /* Plex, color --text-subtle */
--fs-eyebrow:14px;                      /* uppercase, ls 0.2em, --text-subtle */
--fs-nav:    15px;
```

- พาดหัวยาวใส่ `text-wrap: pretty`
- **ห้ามย่อตัวอักษรให้เล็กลงเพื่อยัดเนื้อหา** — ตัดเนื้อหาแทน
- ลำดับชัดสามชั้นเท่านั้น: พาดหัว → เนื้อหา → หมายเหตุ (ไม่มีชั้นที่สี่ในชิ้นงานเดียว)

---

## 4. Logo

โลโก้คือ **เส้นเดียวไม่ยกปากกา** = ตัว P ของ PLearn + วงจรการเรียนรู้ของ Kolb, และ **จุดสีเขียวที่แยกออกมา** = "connect the dot" ที่ผู้เรียนต้องเชื่อมเอง

### SVG (สำหรับฝังในเว็บ)

```html
<!-- On light -->
<svg width="48" height="48" viewBox="0 0 120 120" fill="none" role="img" aria-label="PLearn DE">
  <path d="M26 88c0-30 14-52 34-52s26 14 26 26-10 22-22 22-20-10-20-22 10-26 30-26h13"
        stroke="#1F4D35" stroke-width="11" stroke-linecap="round"/>
  <circle cx="94" cy="88" r="7" fill="#2E7A52"/>
</svg>

<!-- Reversed (on forest ink) — stroke #FFFFFF, dot #8FBFA4 -->
```

Lockup: mark + `<span style="font-family:'Bauhaus 93'">PLearn DE</span>` โดย wordmark ชิดเข้าหา mark (`margin-left:-4px` ที่ขนาด 48px; ในแบบ stacked wordmark ซ้อนขึ้น `margin-top:-52px` ที่ mark 300px)

### Lockups
1. **Stacked** — mark ด้านบน wordmark ด้านล่าง → ใช้เป็นหลัก
2. **Horizontal** — mark ซ้าย wordmark ขวา → header / footer
3. **Reversed** — บนพื้น `--forest-ink`
4. **Mark เดี่ยว** — favicon, avatar, จุดเล็ก

### กฎการใช้โลโก้
- **Clear space** = ความสูงของจุด × 4 รอบด้าน
- **ขนาดต่ำสุด** 24px (จอ) / 8 มม. (พิมพ์)
- **ห้าม:** ยืด-บีบสัดส่วน · เปลี่ยนสีนอกชุดแบรนด์ · ใส่เงา/เส้นขอบ/ไล่เฉด · วางบนภาพถ่ายลายตา · เปลี่ยนฟอนต์โลโก้ไทป์

### ไฟล์ที่ export ไว้แล้ว
`logo-stacked-forest` · `logo-stacked-white` · `logo-horizontal-forest` · `logo-horizontal-white` · `logo-mark-forest` · `logo-mark-white` · `logo-mark-mono-dark` · `logo-mark-mono-white` (PNG)

---

## 5. Graphic elements

### 5.1 Unrolled cycle (เส้นวงจรที่คลี่ออก)
เส้นคลื่นจากโลโก้ที่คลี่ออกเป็นเส้นตรง — ใช้เป็นเส้นคั่นและ **ขอบล่างของหน้า**

```html
<svg width="100%" height="200" viewBox="0 0 400 64" fill="none" preserveAspectRatio="none">
  <path d="M0 48c60 0 60-32 120-32s60 32 120 32 60-32 120-32"
        stroke="#8FBFA4" stroke-width="7" stroke-linecap="round"/>
</svg>
```
ใช้ที่ opacity 0.45–0.55, `pointer-events:none`, วางชิดขอบล่างของ section

### 5.2 Connect the dot (stepper)
จุดทึบ `--green` = ผ่านแล้ว, จุดโปร่ง (`border:4px solid var(--soft-green)`) = ยังไม่ถึง, คั่นด้วยเส้น `--border` สูง 5–6px radius 99px
ใช้บอกลำดับขั้นของเวิร์กชอป / progress

### 5.3 Patterns
6 ตัวเลือก มาจากคำศัพท์เดียวกันของโลโก้ — **เลือกหนึ่งเป็นตัวหลัก** ใช้เป็นพื้นหลังเบา ๆ เท่านั้น

| Pattern | ที่มา |
|---|---|
| **Wave** | เส้นวงจรคลี่ — สงบที่สุด (แนะนำสำหรับเว็บ) |
| **Spiral** | ตัว P ซ้ำเป็นตาราง |
| **Dot Grid** | จุดทึบสลับจุดโปร่ง |
| **Connect** | จุดกับเส้นเชื่อม |
| **Arc** | ส่วนโค้งเดียวซ้ำทแยง |
| **Open End** | ปลายเปิดกับจุดถัดไป |

ไฟล์: `pattern-{wave,spiral,dot,connect,arc,openend}-{tile,sheet}.png`

### 5.4 Shape language
Radius 14–20px · round caps ทุกเส้น · outline 2px · **no shadows · no gradients · one accent only**

---

## 6. Layout & spacing

```css
--container: 1200px;
--gutter:    32px;
--section-y: 96px;       /* padding บน-ล่างของ section */
--hero-y:    110px 120px;
--radius-lg: 20px;       /* card ใหญ่ */
--radius-md: 18px;
--radius-sm: 16px;
--radius-pill: 999px;    /* ปุ่ม / tag / stepper */
```

- Container: `max-width:1200px; margin:0 auto; padding:96px 32px;`
- Grid การ์ด: `grid-template-columns: repeat(auto-fit, minmax(min(100%, 280px), 1fr)); gap:24px;`
- **ที่ว่างคือองค์ประกอบ** — อย่างน้อย 1/3 ของทุกชิ้นงานต้องเป็นที่ว่าง ไม่เติมให้เต็ม
- จังหวะพื้นหลัง: สลับ `--white` / `--mist` / `--forest-ink` เพื่อสร้างจังหวะการอ่าน

---

## 7. Components

### Eyebrow
```css
font-size:14px; letter-spacing:0.2em; text-transform:uppercase; color:var(--text-subtle);
```
บางจุดนำด้วย dot 12px `--green`

### Button — primary
```css
font-size:17px; font-weight:600; color:#FFF; background:var(--forest-ink);
border-radius:999px; padding:16px 32px;
/* hover: background: var(--green) */
```

### Button — secondary
```css
font-size:17px; font-weight:600; color:var(--forest-ink);
background:var(--white); border:2px solid var(--soft-green);
border-radius:999px; padding:14px 30px;
/* hover: background: var(--mist); border-color: var(--forest-ink) */
```
พื้นขาวทึบเสมอ — ปุ่มมักวางทับเส้นคลื่น ถ้าปล่อยโปร่งจะกลืนกับพื้นหลัง

### Card — outline (บริการ)
```css
border:2px solid var(--border-soft); border-radius:20px; padding:34px 32px;
/* hover: border-color: var(--soft-green) */
```
นำด้วย dot 14px: ทึบ `--green` = บริการหลัก, โปร่ง `border:4px solid var(--soft-green)` = บริการเสริม

### Card — filled (บนพื้น Mist)
```css
background:#FFF; border-radius:20px; padding:36px 34px;
```
นำด้วยเลขลำดับ Bauhaus 93 22px สี `--green`

### Card — inverted (เน้นหนึ่งใบต่อ grid)
```css
background:var(--forest-ink); border-radius:20px; padding:34px 32px;
```
dot `--soft-green`, หัวข้อ `#FFF`, meta `--on-dark-dim`

### Header (sticky)
```css
position:sticky; top:0; z-index:20;
background:rgba(255,255,255,0.94); backdrop-filter:blur(10px);
border-bottom:1px solid var(--border-soft);
padding:16px 32px; /* ภายใน container 1200px */
```
ซ้าย = logo lockup แนวนอน (mark 48px + wordmark 19px), ขวา = nav gap 28px + ปุ่ม pill

---

## 8. Landing page — โครงหน้า

ลำดับ section ตาม prototype `PLearn DE Landing Page.dc.html`

| # | Section | id | พื้นหลัง | เนื้อหา |
|---|---|---|---|---|
| 0 | Header sticky | — | white 94% + blur | logo · ปัญหาที่เจอ / บริการ / 5D Framework / ผลงาน · ปุ่ม "ทักเราทาง Facebook" |
| 1 | Hero | `#top` | `--white` + wave ขอบล่าง | eyebrow "Learning & Workshop Design Team" · H1 "ออกแบบการเรียนรู้ที่คนกล้าพูด และทีมเห็นการเติบโตของตัวเอง" · lead = Brand Essence · ปุ่มคู่ |
| 2 | Problem | `#problem` | `--mist` | eyebrow "The problem" · H2 "ปัญหาที่องค์กรมักเจอ" · 3 filled cards (01 อบรมแล้วไม่ได้ใช้ต่อ / 02 ประชุมแล้วไม่มีข้อสรุป / 03 ทีมโตแต่ไม่รู้ว่าโตตรงไหน) |
| 3 | Services | `#services` | `--white` | eyebrow "Core Service" · H2 "บริการหลัก" · 5 cards (ดูตาราง §8.1) |
| 3b | Shapes | — | `--mist` | eyebrow "How we think" · H2 "ชิ้นส่วนที่ต่างกัน ประกอบกันได้หลายแบบ" · เรขาคณิต 6 ชิ้นวน 6 ฟอร์ม 30s (กระจาย → ม้ากระดก → จรวด → บ้าน → พานรัฐธรรมนูญ → วงจร) |
| 4 | 5D Framework | `#framework` | `--forest-ink` | ซ้าย: "5D" Bauhaus `clamp(88px, 9vw, 128px)` `--soft-green` (ตัวเด่นของ section) · eyebrow "How we work" · H2 "Design Framework" · ย่อหน้าอธิบาย · ขวา: **roadmap ริบบิ้นคดเคี้ยว** (ดู §8.2) |
| 5 | Our work | `#work` | `--white` | eyebrow "Our work" · H2 "ผลงานที่ผ่านมา" · grid ภาพ 4:3 × 3 · แถบโลโก้ลูกค้า 5 ช่อง สูง 84px |
| 6 | CTA | — | `--mist` + wave ขอบล่าง | H2 "อยากคุยเรื่องทีมของคุณ ทักเรามาได้เลย" · "เริ่มจากการคุยกันสั้น ๆ เพื่อเข้าใจสถานการณ์ แล้วเราจะเสนอโครงกระบวนการให้" · ปุ่ม primary กึ่งกลาง |
| 7 | Footer | — | `--forest-ink` | logo reversed 52px · "Learning & Workshop Design Team" · ลิงก์ Facebook |

### 8.1 บริการหลัก

| การ์ด | สไตล์ | คำอธิบาย | Tag |
|---|---|---|---|
| **Facilitation Workshop** | outline · dot ทึบ | ออกแบบและนำกระบวนการประชุมให้ถึงเป้าหมาย โดยทุกคนในห้องมีส่วนร่วมจริง | Foresight · Strategy · Participatory · AAR |
| **Learning Design** | outline · dot ทึบ | ออกแบบหลักสูตรและสื่อการเรียนรู้เฉพาะองค์กร เริ่มจากบริบทของคุณ ไม่ใช่ของสำเร็จรูป | Bespoke |
| **In House Training** | outline · dot ทึบ | จัดอบรมในองค์กรของคุณ ปรับเนื้อหาและกรณีศึกษาให้ตรงกับงานที่ทีมทำอยู่ | Foresight for Facilitators · Facilitator for Manager · Learning Design · Workshop Design · Leadership Development |
| **Public Course** | outline · dot โปร่ง | หลักสูตรเปิดสำหรับบุคคลทั่วไป ได้เรียนและแลกเปลี่ยนกับคนต่างองค์กร | Foresight for Facilitators · Facilitator for Manager · Learning Design · Workshop Design |
| **Team Building** | **inverted** · dot soft green | กิจกรรมที่ทำให้ทีมมองเห็นการเติบโตของตัวเอง และกลับไปทำงานด้วยกันได้ดีขึ้น | Empowerment |

### 8.2 5D Framework — roadmap ถนนโค้งกลับตัว + ลูกกลมไหลตามสกรอลล์

Grid 3 คอลัมน์ `1fr 260px 1fr` แถวคงที่ `150 150 150 150 175px` · ถนนเป็น SVG เดียว (viewBox 260×775, `preserveAspectRatio="none"`) อยู่คอลัมน์กลางพาดทั้ง 5 แถว · เส้น `--green` หนา 30 หน่วย ปลาย/ข้อต่อมน

```
M130 138  C130 150 145 150 160 150    → หยดลงจากจุดเริ่มแล้วเลี้ยวขวา
          A75 75 0 0 1 160 300        → U-turn ขวา ยอดโค้ง (235,225) = กลางแถว 2
          L100 300                    → วิ่งซ้าย
          A75 75 0 0 0 100 450        → U-turn ซ้าย ยอดโค้ง (25,375) = กลางแถว 3
          L160 450                    → วิ่งขวา
          A75 75 0 0 1 160 600        → U-turn ขวา ยอดโค้ง (235,525) = กลางแถว 4
          C140 600 130 606 130 620    → จบกลางล่าง
```

**ลูกกลม** `.roadmap__ball` (`--soft-green` r 10) เริ่มที่ (130,138) แล้ว JS ย้ายไปตาม `getPointAtLength(t × ความยาวเส้น)` โดย `t` = ระยะที่ roadmap เลื่อนผ่านจอ (0 เมื่อขอบบนถึง 80% ของจอ → 1 เมื่อขอบล่างถึง 25%) อัปเดตผ่าน rAF บน scroll/resize · reduce-motion หรือไม่มี JS → ลูกกลมอยู่จุดเริ่ม

| Step | ตำแหน่ง | ไทย | Output |
|---|---|---|---|
| **Discover** | แถว 1 คอลัมน์กลาง เหนือจุดเริ่ม (กึ่งกลาง) | วิเคราะห์ความต้องการ | Needs Analysis · Persona / Context |
| **Define** | แถว 2 คอลัมน์ขวา | กำหนดวัตถุประสงค์ | Learning Objectives · Success Criteria |
| **Design** | แถว 3 คอลัมน์ซ้าย (ชิดขวา) | ออกแบบประสบการณ์ | Learning Journey · Activity Design |
| **Deliver** | แถว 4 คอลัมน์ขวา | จัดกระบวนการ | Facilitation Plan · Materials & Tools |
| **Debrief** | แถว 5 คอลัมน์กลาง ใต้ปลายเส้น (กึ่งกลาง) | สะท้อนผล & วัดผล | Evaluation Report · Next Steps |

ป้าย: eyebrow "Step one…" 12px ls 0.2em `--soft-green` → ชื่อ Anuphan 600 26px ขาว → ไทย 16px → Output 14px `--on-dark-dim`

**มือถือ (≤1000px)** เส้นเกลียวซ่อน เปลี่ยนเป็นรายการแนวตั้งบนราง 4px `--green` มีจุด `--soft-green` 18px คั่นแต่ละขั้น

---

### 7.1 Hover บนจอสัมผัส
เอฟเฟกต์ที่ผูกกับ `:hover` แล้ว**เปลี่ยนสถานะค้าง** (หยุด marquee, ซูมรูป) ต้องอยู่ใน `@media (hover: hover)` เสมอ — บนมือถือการแตะจะทำให้ `:hover` ติดค้างที่ element นั้นจนกว่าจะแตะที่อื่น เคยทำให้แถบภาพหยุดถาวรหลังแตะดูรูป · เอฟเฟกต์เล็ก ๆ อย่างสีปุ่ม/เส้นขอบเปลี่ยนไม่เป็นไร

---

## 9. Photography & imagery

**เอา:** ห้องจริง · คนจริง · แสงธรรมชาติ · สีหน้าตามธรรมชาติ · ระยะกลางถึงใกล้ · ปรับแค่แสงกับคอนทราสต์
**ไม่เอา:** สต็อกโฟโต้ยิ้มเข้ากล้อง · ฟิลเตอร์สีจัด · ภาพซ้อนสีเขียว · ภาพที่จัดท่ามากเกินไป
**ห้าม** วางข้อความทับภาพถ่ายโดยไม่มีพื้นรอง

ช่องภาพในเว็บ: radius 18px (งาน) / 10px (โลโก้ลูกค้า) · aspect 4:3 · object-fit cover

---

## 10. Voice & content

- ภาษาไทยเป็นหลัก ประโยคสั้น ไม่ใช้ศัพท์ที่ต้องแปลอีกที
- เขียนจากอาการที่ลูกค้าเจอจริง ไม่ขายศัพท์เทคนิค
- CTA เดียวทั้งหน้า: **"ทักเราทาง Facebook"**
- หัวข้อ = topic noun-phrase สั้น ๆ ไทยคู่อังกฤษเมื่อจำเป็น

---

## 11. Do / Don't — checklist ก่อน ship

**Do**
- [ ] พื้นขาวเป็นหลัก สลับ Mist เพื่อสร้างจังหวะ
- [ ] เขียวหนึ่งบล็อกใหญ่ต่อหนึ่งช่วงหน้าจอ
- [ ] เส้นวงจรคลี่เป็นขอบล่างของ hero และ CTA
- [ ] stepper "connect the dot" บอกลำดับเมื่อมีขั้นตอน
- [ ] ที่ว่างอย่างน้อย 1/3 ของทุก section
- [ ] ลำดับชัดสามชั้น: พาดหัว → เนื้อหา → หมายเหตุ

**Don't**
- [ ] ~~ย่อตัวอักษรต่ำกว่าสเกลเพื่อยัดเนื้อหา~~
- [ ] ~~เงา เกรเดียนต์ หรือสีเน้นตัวที่สอง~~
- [ ] ~~Bauhaus 93 เป็นพาดหัวหรือเนื้อหา~~
- [ ] ~~ข้อความทับภาพถ่ายโดยไม่มีพื้นรอง~~
- [ ] ~~โลโก้เล็กกว่า 24px หรือแก้สี/สัดส่วน~~

---

## 12. Source files

Handoff bundle: `plearn-de-branding-design/`

| ไฟล์ | เนื้อหา |
|---|---|
| `project/PLearn DE Landing Page.dc.html` | prototype หน้า landing (อ้างอิงหลักของ §8) |
| `project/PLearn DE Brand Deck.dc.html` | brand guideline 12 หน้า + layout template 4 แบบ |
| `project/PLearn DE Brand Board.dc.html` | brand board สรุปหนึ่งหน้า |
| `project/PLearn DE Service Deck.dc.html` | เด็คนำเสนอบริการ |
| `project/PLearn De Brand Identity.dc.html` | **exploration ยุคก่อน** (พาเลตต์ #2E5B40/ครีม) — ไม่ใช่ระบบปัจจุบัน |
| `project/PLearn De Logo Directions.dc.html`, `Logo Explorations.dc.html` | ทางเลือกโลโก้ |
| `project/exports/` | PNG โลโก้ + แพทเทิร์น, `fonts/BAUHS93.ttf` |

> หมายเหตุ: ไฟล์ `.dc.html` เป็น prototype ไม่ใช่ production code — ให้ recreate ให้ตรงผลลัพธ์ทางสายตา ไม่ต้องลอกโครงสร้างภายใน

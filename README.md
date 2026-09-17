# PLearn DE — Landing Page

หน้าเว็บของ **PLearn DE (เพลินดี)** — Learning & Workshop Design Team
Static HTML/CSS ไม่มี build step · deploy บน Netlify

- Design system: [`.claude/design.md`](.claude/design.md)
- Live: https://plearnde.netlify.app

## โครงสร้าง

```
index.html      หน้าเดียว 7 sections (hero → problem → services → 5D → work → CTA → footer)
styles.css      tokens + components ตาม design.md
fonts/          BAUHS93.ttf (Bauhaus 93 — โลโก้ไทป์เท่านั้น)
assets/         favicon.svg, logo PNG
netlify.toml    publish = "."
```

ฟอนต์ Anuphan และ IBM Plex Sans Thai โหลดจาก Google Fonts

## รันในเครื่อง

```bash
python3 -m http.server 8765
```

แล้วเปิด http://localhost:8765

## ใส่รูปผลงานและโลโก้ลูกค้า

ใน `index.html` section `#work` มีช่องว่าง 3 + 5 ช่อง แทนที่ `<span>` ด้วย `<img>`:

```html
<!-- ก่อน -->
<figure class="slot slot--work" style="margin:0"><span>ภาพงานที่ 1</span></figure>

<!-- หลัง -->
<figure class="slot slot--work" style="margin:0">
  <img src="assets/work/workshop-01.jpg" alt="เวิร์กชอป Foresight ให้ทีมกลยุทธ์">
</figure>
```

- ภาพผลงาน: สัดส่วน 4:3, ห้องจริง แสงธรรมชาติ ไม่ใส่ฟิลเตอร์ (ดู design.md §9)
- โลโก้ลูกค้า: PNG/SVG พื้นโปร่ง, จะถูก `object-fit: contain` ให้พอดีช่องสูง 84px

## Deploy

Netlify deploy อัตโนมัติจาก branch `main` เมื่อเชื่อม repo นี้กับ site `plearnde` แล้ว
หรือ deploy ด้วยมือ:

```bash
npx netlify-cli deploy --prod --dir=.
```

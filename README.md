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

## รูปภาพ

**ผลงาน** (`assets/work/`) — แถบภาพเลื่อนต่อเนื่อง (marquee) กลไกเดียวกับโลโก้ลูกค้า: ภาพชุดเดียวกันเขียน **สองชุด** แล้วเลื่อนแทร็ก `-50%` ทำให้วนไม่มีรอยต่อ **เพิ่มภาพต้องเติมทั้งสองชุด** (ชุดที่สอง `aria-hidden` และ `alt=""`)

ปรับความเร็ว/ขนาดที่ตัวแปรใน `.marquee.marquee--photos` — `--marquee-duration` (90s เดสก์ท็อป, 70s มือถือ), `--photo-width`, `--marquee-gap`

> ชื่อคลาสต้องเขียน `.marquee.marquee--photos` (ซ้ำสองคลาส) เพราะ `.marquee` ฐานประกาศทีหลังในไฟล์ ถ้าเขียนคลาสเดียวจะโดน override

ย่อภาพก่อนใส่เสมอ — ภาพจากกล้องมักใหญ่ 3MB+:

```bash
sips -Z 1400 -s format jpeg -s formatOptions 68 ต้นฉบับ.JPG --out assets/work/ชื่อใหม่.jpg
```

แนวทางภาพ: ห้องจริง แสงธรรมชาติ ไม่ใส่ฟิลเตอร์ (ดู `design.md` §9) · ใส่ `alt` ภาษาไทยทุกภาพ
ไฟล์ต้นฉบับความละเอียดเต็มเก็บไว้นอก repo ที่ `../workshop-photos-original/`

**โลโก้ลูกค้า** (`assets/clients/`) — วิ่งเป็น marquee ต่อเนื่อง โลโก้แต่ละตัวเขียนไว้ **สองชุด** ใน `index.html` (ชุดที่สองเป็น `aria-hidden` ทำให้ loop ไร้รอยต่อ) เพิ่มโลโก้ต้องเติมทั้งสองชุด · ไฟล์ PNG/SVG พื้นโปร่งจะสวยที่สุด

## วิดีโอ

ไฟล์วิดีโอ **ห้ามวางในโฟลเดอร์นี้** — `netlify deploy --dir=.` อัปโหลดทุกอย่างในโฟลเดอร์ ไม่สนใจ `.gitignore`
ต้นฉบับเก็บไว้ที่ `../workshop-videos-original/` ถ้าจะขึ้นเว็บ แนะนำอัปโหลด YouTube/Vimeo แล้ว embed

## Deploy

Netlify deploy อัตโนมัติจาก branch `main` เมื่อเชื่อม repo นี้กับ site `plearnde` แล้ว
หรือ deploy ด้วยมือ:

```bash
npx netlify-cli deploy --prod --dir=.
```

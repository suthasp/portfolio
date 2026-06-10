# OnePort-style Link-in-Bio (Static)

เว็บ portfolio แบบ bento grid ไฟล์เดียว (`index.html`) ไม่ต้องใช้ build tool

## ฟีเจอร์
- Dark + Light theme สลับได้ (จำค่าไว้ใน localStorage)
- Bento grid responsive (desktop / tablet / mobile)
- Social cards: Instagram, GitHub, Spotify, YouTube, Dribbble
- Project cards, Hire-me, Newsletter form

## Deploy ขึ้น GitHub Pages

1. สร้าง repo ใหม่บน GitHub เช่น `my-portfolio` (หรือ `<username>.github.io` ถ้าอยากได้ URL หลัก)
2. อัปโหลด `index.html` ไปที่ root ของ repo:
   ```bash
   git init
   git add index.html
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<username>/my-portfolio.git
   git push -u origin main
   ```
3. ไปที่ repo → **Settings → Pages**
4. Source: **Deploy from a branch** → Branch: `main` / folder: `/ (root)` → Save
5. รอ 1-2 นาที เว็บจะขึ้นที่ `https://<username>.github.io/my-portfolio/`

## แก้เนื้อหา
- ชื่อ/intro: แก้ใน `<section class="card c-intro">`
- ลิงก์ social: แก้ `href` ของแต่ละ card (ตอนนี้เป็น `username` placeholder)
- อีเมล: แก้ `mailto:hello@example.com`
- รูปโปรเจกต์: แทน gradient ด้วยรูปจริง — เพิ่ม `background-image:url(...)` ใน class `.p1`–`.p5`
- Newsletter form ตอนนี้เป็น demo — ต่อ service จริงได้ เช่น Formspree หรือ Buttondown

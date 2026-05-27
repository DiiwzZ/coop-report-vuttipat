# รายงานผลการปฏิบัติงานสหกิจศึกษา
### วุฒิภัทร ประไพ · 1650702333
**บริษัท อัพบีน จำกัด (Admission Premium)** · มกราคม – พฤษภาคม 2569  
คณะเทคโนโลยีสารสนเทศและนวัตกรรม · มหาวิทยาลัยกรุงเทพ

---

## เปิดดูได้ทันที

เปิด `index.html` ใน browser โดยตรง หรือ serve ด้วย:

```bash
npx serve .
# หรือ
python -m http.server 8080
```

ใช้ Arrow keys / Space / คลิก dot ด้านขวาเพื่อเปลี่ยน slide

---

## Deploy

### GitHub Pages
1. Push repo ขึ้น GitHub
2. Settings → Pages → Source: `main` branch, root `/`
3. เข้าถึงได้ที่ `https://<username>.github.io/<repo>/`

### Netlify
ลาก root folder ไปวางที่ [app.netlify.com/drop](https://app.netlify.com/drop) — ได้ลิงก์ทันที

### Vercel
```bash
npx vercel --prod
```

---

## โครงไฟล์

```
index.html          ← presentation (deploy target)
assets/
  logos/            ← UpBean, Admission Premium, Bangkok University
  articles/         ← screenshots บทความ
  facebook-posts/   ← infographic posts
  graphics/         ← งานกราฟิก
  portfolio-wall/   ← ภาพรวมผลงาน (gallery tiles)
  videos/           ← TikTok / Reel thumbnails
scripts/
  export-pdf.sh     ← export PDF จาก presentation
README.md
```

---

## Export PDF

ต้องการ Node.js

```bash
bash scripts/export-pdf.sh ./index.html ./presentation.pdf
```

PDF แสดงทุก slide แบบ static ชัดเจน (animation ถูกปิดอัตโนมัติผ่าน `?export=1`)

---

## URL Parameters

| Parameter | ผล |
|---|---|
| `?export=1` | ปิด animation ทั้งหมด สำหรับ export PDF |

---

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `→` / `Space` | Slide ถัดไป |
| `←` | Slide ก่อนหน้า |
| `Home` | Slide แรก |
| `End` | Slide สุดท้าย |
| Swipe | Mobile navigation |

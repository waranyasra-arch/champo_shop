# Shampoo House — โปรเจกต์ร้านยาสระผม

## ไฟล์
- `shampoo_shop_google_sheets_template.xlsx` — เทมเพลตข้อมูลสินค้า/ออเดอร์/แพ็กสินค้า เปิดด้วย Google Sheets ได้
- `index.html` — เว็บไซต์ร้านค้าแบบ static พร้อมตะกร้าและฟอร์มข้อมูลจัดส่ง

## ตั้งค่า Google Sheets
1. อัปโหลดไฟล์ XLSX ไป Google Drive แล้วเลือกเปิดด้วย Google Sheets
2. ในแท็บ `Products` ให้แก้ชื่อ/ราคา/จำนวนสต็อกได้ตามต้องการ
3. ไปที่ File > Share > Publish to web
4. เลือกชีต `Products` และรูปแบบ `Comma-separated values (.csv)` แล้วกด Publish
5. คัดลอก URL CSV ที่ได้ แล้วเปิด `index.html` แก้ `const SHEET_CSV_URL = "";` โดยวาง URL ไว้ในเครื่องหมายคำพูด

## Deploy ผ่าน Vercel
1. สร้าง repository ใหม่บน GitHub แล้วอัปโหลด `index.html` (และไฟล์อื่นที่ต้องการ)
2. เข้า Vercel แล้วเลือก Add New > Project
3. Import repository จาก GitHub แล้วกด Deploy
4. Vercel จะแสดง URL เว็บไซต์ เช่น `https://ชื่อโปรเจกต์.vercel.app`

## ข้อจำกัดของเวอร์ชันตัวอย่าง
- ฟอร์มสั่งซื้อยังไม่บันทึกข้อมูลลง Google Sheets อัตโนมัติ และไม่มีระบบชำระเงิน
- ต้องตั้งค่า Publish to web และ Deploy ด้วยบัญชี Google/GitHub/Vercel ของเจ้าของงาน จึงจะได้ URL จริง

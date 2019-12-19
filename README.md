UI มีองค์ประกอบดังนี้
- Web application ใช้ Template ของ Creative Tim ซึ่ง license เป็นแบบ MIT
- RECENT GARBAGE : บอกปริมาณขยะล่าสุด
- STATUS : บอกสถานะของขยะ
  - Full เมื่อ RECENT GARBAGE >= 0.8
  - Not full เมื่อ RECENT GARBAGE < 0.8
- RECENT OPEN : บอกเวลาที่ถังขยะเปิดล่าสุด
- TODAY OPEN : บอกจำนวนครั้งที่ถังขยะเปิดในวันนี้
- Garbage 12 hours history : แสดงปริมาณขยะใน 12 ชั่วโมง ที่ผ่านมา
  - โดยหากภายในชั่วโมงเดียวกันเก็บปริมาณขยะหลายค่า ระบบจะนำค่าสุดท้ายของชั่วโมงนั้นมา plot graph
- Open time : แสดงเวลาที่ถังเปิด 7 อันล่าสุด
- Close time : แสดงเวลาที่ถังปิด 50 อันล่าสุด
- Garbage stats : แสดงข้อมูลปริมาณขยะ ณ เวลาต่างๆ 50 อันล่าสุด

Development
- ใช้ github page ในการ production
- ใช้ realtime database ของ firebase ในการเก็บข้อมูล ทำให้ web application ไม่จำเป็นต้องรีเฟรชเมื่อข้อมูลมีการอัพเดต
- ใช้ Chart.js ในการ plot graph
- ใช้ Moment.js ในการเปรียบเทียบเวลา และการแสดงผล
- ใช้ jQuery ในการอัพเดตส่วนต่างๆของ web application เมื่อ realtime database ถูก create / update / delete

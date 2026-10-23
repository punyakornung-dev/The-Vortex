# 🎯 AI Mock Interview Analyzer (Ultra Edition 3.0)

ระบบจำลองการสัมภาษณ์งานและการสอบคัดเลือกอัจฉริยะ (Single Page Web Application) แบบ Client-side 100% สไตล์ Cyber-Modern SaaS Dark Mode ด้วยเทคโนโลยี MediaPipe Face Mesh, Web Speech API และ Google Gemini AI

---

## ✨ ลูกเล่นใหม่ & การเปลี่ยนโทนสี (New Features & Gimmicks in v3.0)

### 1. 🎨 Dynamic Theme Switcher (เปลี่ยนโทนสีได้ 5 ธีมทันทีแบบเรียลไทม์)
กดปุ่มเลือกธีมที่มุมบนขวาใน Header เพื่อสลับโทนสี Cyber ทั้งระบบ:
- 🔮 **Cyber Neon (ค่าเริ่มต้น)**: โทนม่วง-คราม (Indigo & Violet) พร้อมนีออนเขียวมรกต
- ⚡ **Emerald Matrix**: โทนแฮกเกอร์ไซไฟ เขียวมรกต & ไซแอนนีออน (Emerald & Cyan)
- 🌅 **Solar Cyber**: โทนดวงอาทิตย์ระเบิด ชมพู-ส้ม-เหลืองอำพัน (Rose & Orange)
- 🌌 **Deep Ocean**: โทนใต้ทะเลลึก ฟ้าสว่าง-น้ำเงินนีออน (Sky & Electric Blue)
- 👑 **Executive Gold**: โทนทองคำหรูหราของผู้บริหาร (Champagne Gold & Bronze)
*(ธีมสีที่เลือกจะถูกบันทึกลง `localStorage` ให้อัตโนมัติ)*

### 2. 🔊 AI Voice Question Synthesizer (Text-to-Speech)
- มีปุ่มลำโพงข้างคำถาม หรือเปิดสวิตช์ **"🔊 AI อ่านคำถามด้วยเสียง"** ในหน้าตั้งค่า
- เมื่อคำถามใหม่ปรากฏขึ้น ระบบจะจำลองเสียงกรรมการพูดอ่านคำถามภาษาไทย/อังกฤษออกมาเป็นเสียงจริง พร้อมแอนิเมชันคลื่นเสียงปากพูด

### 3. ⏱️ Stress Interview Mode (โหมดกดดันเวลา 60 วินาที)
- สามารถเปิดสวิตช์ **"โหมดกดดันเวลา"** ก่อนเริ่มสัมภาษณ์
- มีแถบเวลานับถอยหลัง 60 วินาทีต่อคำถาม เมื่อเหลือ 15 วินาทีสุดท้าย แถบจะกะพริบเป็นสีแดงสดและมีเสียงบี๊บเตือนความเร็ว

### 4. ⚡ Sci-Fi Synthesizer Sound Effects (Web Audio API)
- เสียงเอฟเฟกต์ Sci-Fi สังเคราะห์ 100% โดยไม่ต้องโหลดไฟล์เสียงภายนอก:
  - เสียงคลิกปุ่ม UI Futuristic Click
  - เสียงแจ้งเตือนเตือนหลบสายตา (Warning Chime)
  - เสียงแฟนฟาร์เฉลิมฉลองเมื่อจบการสัมภาษณ์ (Victory Fanfare)
  - ปุ่มเปิด/ปิดเสียง SFX ที่มุมขวาบน

### 5. 🔦 Interactive Mouse Spotlight Glow
- ลำแสงสปอตไลต์นีออนลอยตามเคอร์เซอร์เมาส์ สร้างมิติสะท้อนแสงบนกระจก Glassmorphism แบบ 3D

### 6. 📜 Official Evaluation Certificate & Print to PDF
- ในหน้าสรุปผลการสัมภาษณ์ สามารถกดปุ่ม **"ดูใบรับรองผล / สั่งพิมพ์ PDF"** เพื่อเปิดหน้าต่าง Certificate มีตราประทับ Holographic Seal, ลายเซ็นดิจิทัล และกดสั่งพิมพ์บันทึกเป็น PDF (`window.print()`) ได้ทันที

---

## 🚀 วิธีการเปิดใช้งาน
เปิดไฟล์ [index.html](file:///C:/Users/Punyakorn/.gemini/antigravity/scratch/ai-mock-interview/index.html) ผ่านเบราว์เซอร์ **Google Chrome** หรือ **Microsoft Edge** หรือนำขึ้น **GitHub Pages** ได้ทันที

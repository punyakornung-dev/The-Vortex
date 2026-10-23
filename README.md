# 🎯 AI Mock Interview Analyzer

ระบบจำลองการสัมภาษณ์งานและการสอบคัดเลือกอัจฉริยะ (Single Page Web Application) แบบ Client-side 100% สไตล์ Cyber-Modern SaaS Dark Mode ด้วยเทคโนโลยี MediaPipe Face Mesh, Web Speech API และ Google Gemini AI

---

## ✨ ไฮไลต์ฟีเจอร์เด่น (Key Features)

1. **🎨 Cyber-Modern Glassmorphism UI/UX**:
   - ออกแบบด้วยโทนสี Dark Mode (Slate-950) ตัดกับแสงนีออนเรืองแสง (Indigo, Violet, Emerald, Crimson)
   - แอนิเมชัน Floating Button, Pulse Glow, Real-time Soundwave Bars และ Canvas Confetti พลุกระดาษเมื่อสัมภาษณ์เสร็จ
   - โมเดล Monetization ตาราง Pricing 3 ระดับ (Free, Pro 199.-, VIP 499.-) พร้อมการ์ด Pro เรืองแสงโดดเด่น

2. **🎯 Dynamic 2-Level Goal Selection**:
   - เมนูเลือกเป้าหมาย 2 ชั้น (สอบเข้ามหาลัย, สมัครงาน Tech & Corporate, สอบทุนต่างประเทศ, สตาร์ทอัพและการระดมทุน) พร้อมคลังคำถามสัมภาษณ์เฉพาะทางกว่า 50 คำถาม

3. **👁️ Real-time Eye Contact Tracking (MediaPipe Face Mesh)**:
   - ตรวจจับตำแหน่งดวงตา รูม่านตา (Iris) และทิศทางใบหน้าผ่านกล้องเว็บแคม
   - หากผู้ใช้หลบสายตาหรือไม่มองกล้องเกิน **3 วินาที** จะมีหน้าต่างแจ้งเตือนสีแดงกะพริบกลางจอทันที (*Eye Contact Warning Glow*)

4. **🎙️ Real-time Thai Speech-to-Text (Web Speech API)**:
   - แปลงเสียงพูดภาษาไทยเป็นข้อความ Subtitle ลอยอยู่ด้านล่างหน้าจอแบบเรียลไทม์ พร้อมนับจำนวนคำ

5. **📊 Interactive Report Dashboard**:
   - **Eye Contact Score**: กราฟวงกลม SVG Circle Progress แสดงเปอร์เซ็นต์เวลามองกล้องแบบแอนิเมชัน
   - **AI Evaluation**: ส่งบทถอดเสียงผ่าน `fetch()` ไปยัง **Google Gemini API** (`gemini-1.5-flash`) เพื่อสวมบทบาทเป็นกรรมการ ให้คะแนนรวม X/10, จุดเด่น, จุดที่ควรปรับปรุง และคำแนะนำเชิงกลยุทธ์
   - **Offline AI Fallback Engine**: หากไม่ได้ใส่ API Key ระบบจะไม่พัง แต่จะคำนวณและประเมินผลผ่านอัลกอริทึมออฟไลน์จำลองโดยอัตโนมัติ
   - ปุ่มดาวน์โหลดรายงาน PDF (จำลองระบบ Pro Plan) และปุ่มเริ่มฝึกซ้อมใหม่

---

## 🚀 วิธีการเปิดใช้งาน (How to Run)

### 1. เปิดผ่านเบราว์เซอร์โดยตรง (Local File)
ดับเบิลคลิกเปิดไฟล์ `index.html` หรือคลิกลิงก์:
```
file:///C:/Users/Punyakorn/.gemini/antigravity/scratch/ai-mock-interview/index.html
```
*(แนะนำให้ใช้งานบน Google Chrome หรือ Microsoft Edge เพื่อรองรับ Web Speech API และกล้องเว็บแคมอย่างสมบูรณ์แบบ)*

### 2. นำไป Deploy บน GitHub Pages
1. สร้าง GitHub Repository ใหม่ (เช่น `ai-mock-interview`)
2. อัปโหลดไฟล์ `index.html` ขึ้นที่ Root directory หรือสาขา `main`
3. ไปที่แท็บ **Settings** > **Pages**
4. เลือก Source เป็น `Deploy from a branch` (Branch: `main` / `root`) แล้วกด **Save**
5. รอ 1-2 นาที คุณจะได้ URL สำหรับใช้งานออนไลน์ได้ทันที 100% ฟรี!

---

## 🔑 การตั้งค่า Gemini API Key (ทางเลือก)
1. กดที่ปุ่ม **"ตั้งค่า API Key"** บริเวณมุมขวาบนของแถบนำทาง (Header)
2. นำ API Key ที่ได้จาก [Google AI Studio](https://aistudio.google.com/app/apikey) มากรอก แล้วกดบันทึก
3. คีย์จะถูกจัดเก็บไว้ใน `localStorage` ของเบราว์เซอร์ผู้ใช้เท่านั้น ปลอดภัย 100% ไม่มีเซิร์ฟเวอร์คั่นกลาง

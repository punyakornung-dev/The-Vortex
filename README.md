# 🎙️ AI Mock Interview - ระบบจำลองการสัมภาษณ์เสมือนจริงด้วย AI

เว็บแอปพลิเคชันจำลองการสัมภาษณ์เสมือนจริง (AI Mock Interview) ทำงานแบบ **Client-side 100% (ไม่มี Backend)** พัฒนาด้วย **HTML, Tailwind CSS (ผ่าน CDN), Vanilla JavaScript**, และ **MediaPipe Face Mesh** พร้อมส่งขึ้น GitHub Pages ได้ทันที

---

## 🌟 ฟังก์ชันหลักตามข้อกำหนด

### 1. โครงสร้าง UI และกล้องเว็บแคม
- พื้นที่แสดงผลวิดีโอจากกล้อง Webcam (`<video>`) ปรับขนาด Responsive เต็มกรอบ
- สคริปต์ขอสิทธิ์เปิดกล้องอัตโนมัติทันทีที่เข้าเว็บ (`navigator.mediaDevices.getUserMedia`)
- ปุ่มควบคุมการสัมภาษณ์: **"เริ่มสัมภาษณ์"** และ **"จบการสัมภาษณ์"**
- กล่องแสดงคำถามจำลอง เช่น *"ทำไมถึงอยากเข้าเรียนคณะวิศวกรรมศาสตร์?"* พร้อมปุ่มสลับคำถามตัวอย่าง

### 2. ระบบประมวลผลภาษากาย (MediaPipe Face Mesh)
- โหลดไลบรารี `@mediapipe/face_mesh` และ `@mediapipe/camera_utils` ผ่าน CDN
- ตรวจจับใบหน้าและคำนวณการมองกล้อง (Eye Contact / Head Pose Estimation) แบบ Real-time
- **ระบบแจ้งเตือนสีแดง:** หากผู้ใช้ละสายตาหรือไม่มองกล้องติดต่อกันเกิน **3 วินาที** จะมีแบนเนอร์แจ้งเตือนสีแดงกระพริบกลางจอว่า **"กรุณามองกล้อง"** ทันที
- บันทึกเปอร์เซ็นต์เวลาที่มองกล้องตลอดระยะเวลาสัมภาษณ์ เพื่อนำไปรายงานผล

### 3. ระบบประมวลผลเสียงและตรวจคำตอบ (Speech-to-Text & LLM)
- ใช้ **Web Speech API** แปลงเสียงพูดภาษาไทย (`th-TH`) เป็นข้อความแบบ Real-time
- เชื่อมต่อ LLM API ด้วย `fetch()` พร้อมประกาศตัวแปร `const API_KEY = "YOUR_API_KEY"` ไว้อย่างชัดเจน (และมี UI ให้กรอก/บันทึกลง LocalStorage ได้อย่างสะดวก)
- กำหนด System Prompt:
  > `"คุณคืออาจารย์สอบสัมภาษณ์ ให้คะแนนคำตอบนี้ 1-10 พร้อมคำแนะนำสั้นๆ"`
- มีระบบ **Intelligent Heuristic Evaluation Fallback** สำรอง เพื่อให้ทดสอบได้ทันทีแม้ยังไม่ได้ใส่ API Key

### 4. หน้าแดชบอร์ดสรุปผลและ Business Model
- เมื่อกด **"จบการสัมภาษณ์"** ระบบจะปิดกล้องและเปลี่ยนหน้าไปยัง **Report Dashboard**
- แสดงผลสรุป:
  - **เปอร์เซ็นต์การมองกล้อง** พร้อมกราฟวงกลมและคำแนะนำด้านภาษากาย
  - **คะแนนจากอาจารย์สัมภาษณ์ (1-10)** พร้อมข้อเสนอแนะและข้อความที่ถอดเสียงได้
- ส่วน **"Upgrade to Premium"** แสดงโมเดลการสร้างรายได้ (Monetization):
  - แผนทดลองฟรี (Free Tier)
  - แผนยอดนิยม Pro Student (199 บาท/เดือน) - ซ้อมไม่จำกัด + คลังข้อสอบ 500+ ข้อ
  - แผน VIP ตลอดชีพ (499 บาท)

---

## 🚀 วิธีการทดสอบบนเครื่อง Local

เนื่องจากเบราว์เซอร์ (Chrome, Edge, Safari) กำหนดความปลอดภัยให้การขอสิทธิ์เข้าถึงกล้องและไมโครโฟนทำงานได้เฉพาะบน **HTTPS** หรือ **localhost**:

### วิธีที่ 1: ใช้ Python Local Server (ง่ายที่สุด)
เปิด Terminal หรือ PowerShell ที่โฟลเดอร์โปรเจกต์ แล้วรัน:
```bash
python -m http.server 8000
```
จากนั้นเปิดเบราว์เซอร์ไปที่: `http://localhost:8000`

### วิธีที่ 2: ใช้ส่วนขยาย Live Server ใน VS Code
คลิกขวาที่ไฟล์ `index.html` แล้วเลือก **"Open with Live Server"**

---

## 🌐 วิธีนำขึ้น GitHub และเปิดใช้งาน GitHub Pages

1. **สร้าง Repository บน GitHub:**
   - เข้าไปที่ [GitHub](https://github.com) แล้วสร้าง Repository ใหม่ (เช่น `ai-mock-interview`)
   - ตั้งค่าเป็น **Public**

2. **Push โค้ดขึ้น GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: AI Mock Interview Client-side App"
   git branch -M main
   git remote add origin https://github.com/<YOUR_USERNAME>/ai-mock-interview.git
   git push -u origin main
   ```

3. **เปิดใช้งาน GitHub Pages:**
   - ไปที่หน้า Repository บน GitHub -> แท็บ **Settings**
   - ในเมนูด้านซ้าย เลือกหัวข้อ **Pages**
   - ใต้หัวข้อ **Build and deployment**:
     - **Source**: เลือก `Deploy from a branch`
     - **Branch**: เลือก `main` และโฟลเดอร์ `/ (root)`
     - กดปุ่ม **Save**
   - รอประมาณ 1-2 นาที คุณจะได้ URL เว็บไซต์ เช่น:
     `https://<YOUR_USERNAME>.github.io/ai-mock-interview/` (ซึ่งเป็น HTTPS รองรับกล้องและไมโครโฟนได้ 100%)

---

## 📁 โครงสร้างไฟล์

```
ai-mock-interview/
├── index.html       # ไฟล์หลักบรรจุโครงสร้าง HTML, Tailwind CDN, และสคริปต์ JavaScript ทั้งหมด
└── README.md        # เอกสารแนะนำการติดตั้งและขั้นตอน Deploy ขึ้น GitHub Pages
```

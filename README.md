# Bot-Topup-Wallet-
# 🎉 TrueMoney Topup Discord Bot (by XZNP)

🧧 ระบบเติมเงินผ่าน **ซองอั่งเปา TrueMoney** บน Discord ด้วย `Modal UI` ที่ใช้งานง่ายและปลอดภัย พร้อมตัดค่าธรรมเนียมอัตโนมัติ และส่ง Embed สรุปผลอย่างมืออาชีพ

---

## 📦 โครงสร้างระบบ
\`\`\`bash
truemoney-topup-bot/
├── bot.py                    # ไฟล์หลักสำหรับรันบอท
├── config.py                 # ตั้งค่าต่างๆ (API, เบอร์, Token ฯลฯ)
├── requirements.txt          # ไลบรารีที่ต้องติดตั้ง
│
├── data/
│   └── users.json            # ฐานข้อมูลผู้ใช้ (เครดิต & เงิน)
│
├── utils/
│   └── user_db.py            # ฟังก์ชันโหลด/บันทึก users.json
│
└── modals/
    └── topup_modal.py        # Modal UI ฟอร์มกรอกลิงก์ซอง
\`\`\`

---

## 🚀 วิธีติดตั้ง & ใช้งาน

1. **ติดตั้งไลบรารี**
   \`\`\`bash
   pip install -r requirements.txt
   \`\`\`

2. **ตั้งค่าใน \`config.py\`**
   \`\`\`python
   BOT_TOKEN = "ใส่ Token ของบอท"
   API_KEY = "API Key จากระบบ Truemoney Wallet"
   phone = "เบอร์ที่ผูกซองอั่งเปา"
   ChannelLOGMoney = 123456789012345678  # ช่องสำหรับส่ง Log
   footer = "© XZNP System"
   \`\`\`

3. **สร้างไฟล์ฐานข้อมูล**
   \`\`\`bash
   mkdir data
   echo "{}" > data/users.json
   \`\`\`

4. **รันบอท**
   \`\`\`bash
   python bot.py
   \`\`\`

5. **ใช้คำสั่ง \`/topup\` ใน Discord**
   - ระบบจะเปิดฟอร์มให้กรอกลิงก์ซอง
   - ตรวจสอบลิงก์อัตโนมัติผ่าน API
   - ส่ง Embed แจ้งผลการเติมพร้อมค่าธรรมเนียม & เครดิตที่ได้รับ

---

## 🧾 ค่าธรรมเนียม

| รายการ | อัตรา |
|--------|--------|
| ค่าธรรมเนียมซอง | \`1.1%\` หักจากยอดก่อนเติมเข้าเครดิต |

---

## 🛡️ ความปลอดภัย

- ใช้ \`ephemeral\` message ป้องกันการมองเห็นจากบุคคลอื่น
- ใช้ \`Modal UI\` ใน Discord ซึ่งเป็นฟีเจอร์อย่างเป็นทางการ
- ไม่เก็บรหัสผ่านหรือข้อมูลส่วนตัวใดๆ

---

## 💬 UI ตัวอย่าง (Embed สรุปผล)

\`\`\`
🎉 เติมเงินสำเร็จ!
💵 จำนวนเงิน: 100.00 บาท
📉 ค่าธรรมเนียม: 1.10 บาท
🟢 เครดิตที่ได้รับ: 98.90 บาท
\`\`\`

---

## 👨‍💻 เครดิต / Credit

- 🛠 พัฒนาโดย: **XZNP Development**
- 🌐 เว็บไซต์: [https://xznp.store](https://xznp.store)
- 💡 ระบบ API โดย: [XZNP TrueMoney Wallet API](https://api.xznp.store)
- ✨ Discord UI โดย: [nextcord Modal UI](https://docs.nextcord.dev/en/latest/)

---

## 🧧 ปล. สำหรับแจกจ่าย

> สามารถนำไปแจกต่อ แก้ไข หรือนำไปพัฒนาต่อได้ **แต่กรุณาให้เครดิตผู้พัฒนา**

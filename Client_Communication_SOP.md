# AUMATIQ — Client Communication SOP
### Doctor/Clinic Automation ক্লায়েন্টদের জন্য সম্পূর্ণ কমিউনিকেশন প্রসেস
*কোথায়, কখন, কী পাঠাবে — Interest তৈরি থেকে Satisfaction পর্যন্ত*

---

## ধাপ ০ — টেমপ্লেট ফাইলগুলো কোথায় রাখবে

`aumatiq-sops` GitHub repo-তে একটা ফোল্ডার বানাও:

```
aumatiq-sops/
└── client-communication/
    ├── Email_Template_Doctor_Automation.html
    ├── WhatsApp_Templates_Doctor_Automation.txt
    ├── Client_Welcome_Packet.html          ← blank টেমপ্লেট (future client)
    └── Client_Welcome_Packet_DrAsma_DEMO.pdf ← ভরা উদাহরণ (reference)
```

এটাই তোমার **একবার বানানো, বারবার ব্যবহার করা** central library। নতুন
client এলে এখান থেকে কপি করে placeholder বদলাবে — নতুন করে কিছু লিখতে
হবে না।

---

## ধাপ ১ — পুরো Client Journey: কোন ধাপে কোন চ্যানেল

| # | পর্যায় | চ্যানেল | কেন এই চ্যানেল |
|---|---|---|---|
| 1 | প্রথম যোগাযোগ / inquiry reply | **WhatsApp** | দ্রুত, personal, বাংলাদেশে সবাই WhatsApp checks করে |
| 2 | Proposal / pricing শেয়ার | **Email** | Formal, save করে রাখা যায়, PDF attach করা যায় |
| 3 | System ডেলিভারি (launch day) | **দুটোই** (Email প্রথমে, তারপর WhatsApp) | Email = official record + attachment, WhatsApp = তাৎক্ষণিক নজরে আনা |
| 4 | Install না করলে reminder | **WhatsApp** | Email অনেকেই miss করে, WhatsApp সাথে সাথে দেখে |
| 5 | মাসিক check-in | **WhatsApp** (হালকা), **Email** (মাস শেষে report) | দুই জায়গাতেই presence বজায় রাখা |
| 6 | সমস্যা/support request | **WhatsApp** (acknowledge সাথে সাথে) | Response speed = trust |
| 7 | Review/Testimonial চাওয়া | **WhatsApp** | সবচেয়ে বেশি reply আসে এখানে |
| 8 | Upsell/নতুন feature অফার | **WhatsApp** প্রথমে, ইন্টারেস্টেড হলে **Email**-এ ডিটেইল | নরম approach আগে, formal পরে |

---

## ধাপ ২ — EMAIL: কী কোথায় লিখবে (Step by Step)

### কোন email client দিয়ে পাঠাবে
`contact@aumatiq.com` থেকে পাঠাও (Gmail/Google Workspace ইনবক্স থেকে) —
কখনো personal জিমেইল থেকে না, এতে ব্র্যান্ড অপেশাদার লাগে।

### Subject Line (কপি করে বসাও)
```
🎉 {{CLINIC_NAME}} — আপনার AUMATIQ সিস্টেম এখন লাইভ
```

### Body — কী করবে
1. Gmail-এ নতুন মেইল লিখো
2. `Email_Template_Doctor_Automation.html` ফাইলটা যেকোনো ব্রাউজারে খোলো
   (Chrome/Edge)
3. পুরো পেজ **সিলেক্ট করে (Ctrl+A) কপি করো (Ctrl+C)**
4. Gmail-এর body-তে **paste করো (Ctrl+V)** — Gmail নিজে থেকেই formatting,
   রং, বাটন সব ঠিক রেখে বসাবে (এটা একটা "rendered HTML" email, raw কোড
   না)
5. সব `{{PLACEHOLDER}}` ম্যানুয়ালি বদলে দাও (CLINIC_NAME, CONTACT_NAME,
   PUBLIC_URL, DASHBOARD_URL, DASHBOARD_USERNAME)

### Attachment — কী জুড়বে
`Client_Welcome_Packet_DrAsma_DEMO.pdf`-এর মতো একটা **ভরা PDF** attach
করো (আমি প্রতিটা client-এর জন্য এই PDF বানিয়ে দেব — শুধু আমাকে
CLINIC_NAME, contact name, links আর retainer amount বললেই একটা রেডি
PDF পেয়ে যাবে)। এই PDF-টাই ক্লায়েন্ট রেখে দেবে, print করতে পারবে, পরে
ফিরে দেখতে পারবে — email body শুধু quick overview-এর জন্য।

### কখন পাঠাবে
সিস্টেম টেস্ট করে ১০০% রেডি হওয়ার পরই — কখনো "প্রায় শেষ" অবস্থায় না,
কারণ প্রথম ইমপ্রেশনটাই সবচেয়ে গুরুত্বপূর্ণ।

---

## ধাপ ৩ — WHATSAPP: কী কোথায় লিখবে (Step by Step)

### কোন নাম্বার থেকে
AUMATIQ-এর অফিসিয়াল WhatsApp Business নাম্বার থেকে (personal নাম্বার না) —
Business profile-এ AUMATIQ লোগো + bio সেট করা থাকতে হবে।

### প্রতিটা টেমপ্লেট কখন পাঠাবে

| টেমপ্লেট | কখন পাঠাবে |
|---|---|
| Template 1 — Launch Delivery | Email পাঠানোর ঠিক ১৫-৩০ মিনিট পর (যাতে ক্লায়েন্ট আগে email-এ পুরো ডিটেইল দেখে নেয়, WhatsApp শুধু নজরে আনার জন্য) |
| Template 2 — Install Reminder | ডেলিভারির ৩ দিন পরও যদি install না করে |
| Template 3 — Monthly Check-in | প্রতি মাসের ১-২ তারিখে |
| Template 4 — Support Acknowledgment | ক্লায়েন্ট মেসেজ দেওয়ার সাথে সাথে (৫ মিনিটের মধ্যে — এটাই সবচেয়ে জরুরি নিয়ম) |
| Template 5 — Upsell Offer | ডেলিভারির অন্তত ৪৫-৬০ দিন পর, ক্লায়েন্ট সিস্টেমে comfortable হওয়ার পর |

### কীভাবে পাঠাবে
1. `WhatsApp_Templates_Doctor_Automation.txt` ফাইল থেকে দরকারি টেমপ্লেট কপি করো
2. `{{PLACEHOLDER}}` গুলো বদলে দাও
3. WhatsApp-এ paste করো — emoji, bold (`*text*`) সব ঠিকভাবে দেখাবে
4. পাঠানোর আগে একবার পুরো মেসেজ নিজে পড়ে দেখো — কোনো `{{}}` ভুলে থেকে
   গেলে সেটা খুবই অপেশাদার দেখাবে

---

## ধাপ ৪ — Client-কে "Interested & Satisfied" রাখার সম্পূর্ণ Timeline

```
Day 0   → Email (Welcome Packet PDF) + WhatsApp (Launch template)
Day 1   → নিজে থেকেই একবার call/WhatsApp করে জিজ্ঞেস করো: "সব ঠিকমতো
           খুলছে তো?" (এই ছোট গেস্চারটাই সবচেয়ে বেশি বিশ্বাস তৈরি করে)
Day 3   → Install না করলে Template 2 পাঠাও
Day 7   → এক সপ্তাহ চেক-ইন: "প্রথম সপ্তাহ কেমন গেল?" (ছোট WhatsApp মেসেজ)
Day 30  → Template 3 (Monthly Check-in) + email-এ ছোট performance report
Day 45+ → সন্তুষ্ট থাকলে Google Review-এর অনুরোধ করো (নতুন WhatsApp
           টেমপ্লেট লাগবে — চাইলে বানিয়ে দিতে পারি)
Day 60+ → Template 5 (Upsell) — যদি মানানসই নতুন ফিচার থাকে
```

### দ্রুত response = বিশ্বাস
যেকোনো WhatsApp মেসেজের উত্তর **২ ঘণ্টার মধ্যে** দেওয়ার commitment
রাখো (Email template-এও এটাই লেখা আছে) — এই promise ভাঙলে ক্লায়েন্ট
সবচেয়ে বেশি হতাশ হয়।

### Personal touch যোগ করার সহজ উপায়
- ক্লায়েন্টের নাম দিয়েই সম্বোধন করো, "Dear Sir/Madam" না
- প্রতিটা মেসেজে অন্তত একটা নির্দিষ্ট সংখ্যা/তথ্য দাও (কতগুলো booking
  হয়েছে, কতগুলো reminder গেছে) — এতে মনে হয় সিস্টেমটা সত্যিই কাজ করছে,
  শুধু কথার কথা না

---

## Quick Reference — এক নজরে

| প্রশ্ন | উত্তর |
|---|---|
| কোথা থেকে Email পাঠাব? | `contact@aumatiq.com` (Gmail/Workspace) |
| কোথা থেকে WhatsApp পাঠাব? | AUMATIQ Business নাম্বার |
| Attachment কী দেব? | ভরা Welcome Packet PDF |
| কতক্ষণে reply দিতে হবে? | ২ ঘণ্টার মধ্যে (WhatsApp সাপোর্টে ৫ মিনিট) |
| নতুন client এলে কী করব? | এই SOP-র টেমপ্লেট ফাইল কপি করে placeholder বদলাও |

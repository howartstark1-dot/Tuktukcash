# 🛺 TukTukCash - Cash on Go (Telegram Mini App)

**TukTukCash** হলো একটি আধুনিক ও লাইটওয়েট টেলিগ্রাম মিনি অ্যাপ (Telegram Mini App)। এই অ্যাপটির মাধ্যমে ব্যবহারকারীরা বিজ্ঞাপন দেখে এবং বন্ধুদের রেফার করে সরাসরি টাকা আয় করতে পারেন। সম্পূর্ণ অ্যাপ্লিকেশনটি ফ্রন্টএন্ড-ভিত্তিক সিঙ্গেল ফাইল আর্কিটেকচারে তৈরি, যেখানে **Firebase Realtime Database** এর মাধ্যমে লাইভ ডাটা সিঙ্ক এবং **Monetag** এর বিজ্ঞাপনের ব্যবস্থা রয়েছে।

---

## 🌟 বৈশিষ্ট্যসমূহ (Features)

- **📱 টেলিগ্রাম ইন্টিগ্রেশন:** Telegram WebApp SDK ব্যবহার করে ব্যবহারকারীর নাম ও ইউজার আইডি ডাইনামিকভাবে লোড হয়।
- **📺 অ্যাড দেখে আয় (Watch & Earn):** Monetag Ad Network ব্যবহার করে অ্যাড সম্পন্ন করলে সরাসরি ৳৫.০০ ব্যালেন্সে যুক্ত হয়।
- **👥 রেফারেল সিস্টেম:** ডাইনামিক রেফারেল লিংক জেনারেটর। প্রতিটি সফল রেফারে ৳২০.০০ বোনাস পাওয়া যায়।
- **🔥 ফায়ারবেজ লাইভ সিঙ্ক:** Firebase Realtime Database এর মাধ্যমে ব্যালেন্স, কমপ্লিট করা টাস্ক, দেখা বিজ্ঞাপনের সংখ্যা লাইভ সেভ এবং সিঙ্ক হয়।
- **💳 ওয়ালেট ও উত্তোলন:** বিকাশ (bKash) এবং নগদ (Nagad) এর মাধ্যমে মিনিমাম ৳২০০ টাকা হলে উত্তোলনের (Withdrawal) আবেদন করা যায়।
- **🎨 আধুনিক রেসপন্সিভ ডিজাইন:** Tailwind CSS এবং Phosphor Icons ব্যবহার করে সম্পূর্ণ মোবাইল-বান্ধব UI তৈরি করা হয়েছে।

---

## 🛠️ ব্যবহৃত টেকনোলজি (Tech Stack)

- **Frontend:** HTML5, Tailwind CSS, JavaScript (ES6+)
- **Icons:** Phosphor Icons
- **Database:** Firebase Realtime Database
- **Ad Network:** Monetag SDK (Zone ID: 12012404)
- **Platform Integration:** Telegram WebApp SDK

---

## 📁 প্রজেক্ট স্ট্রাকচার (Project Structure)

এটি একটি সিঙ্গেল ফাইল ওয়েব অ্যাপ্লিকেশন (`index.html`)। ফাইলের ভেতরেই প্রয়োজনীয় কোডগুলো সাজানো রয়েছে:

```text
.
├── index.html          # মূল কোড ফাইল (HTML, CSS, JS, Firebase & SDKs)
└── README.md           # প্রজেক্ট ডকুমেন্টেশন
```

---

## 🚀 গিটহাব পেজেস বা সার্ভারে সেটআপ পদ্ধতি (Setup Instructions)

### ১. রিপোজিটরি ক্লোন করুন (Clone Repository):
```bash
git clone https://github.com/your-username/tuktukcash.git
cd tuktukcash
```

### ২. টেলিগ্রাম বটের সাথে কানেক্ট করুন:
আপনার টেলিগ্রাম বট ইউজারনেম পরিবর্তন করতে চাইলে `index.html` ফাইলের এই অংশটি এডিট করুন:
```javascript
const botUsername = "Tuktukcashbot"; // এখানে আপনার বটের ইউজারনেম দিন
```

### ৩. ফায়ারবেজ সেটআপ (Firebase Setup):
প্রজেক্টটি আপনার নিজস্ব ফায়ারবেজ অ্যাকাউন্টের সাথে যুক্ত করতে `index.html` ফাইলের `firebaseConfig` পরিবর্তন করুন:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  databaseURL: "YOUR_DATABASE_URL",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

---

## 🤖 টেলিগ্রাম বটের সাথে মিনি অ্যাপ যুক্ত করার নিয়ম

১. টেলিগ্রামে `@BotFather` এ যান।
২. আপনার বটের জন্য `/newapp` অথবা `/setmenubutton` কমান্ড সিলেক্ট করুন।
৩. মিনি অ্যাপের URL হিসেবে আপনার **GitHub Pages** বা **Vercel/Netlify** এ হোস্ট করা লিঙ্কটি দিন (যেমন: `https://your-username.github.io/tuktukcash/`)।

---

## 📄 লাইসেন্স (License)

এই প্রজেক্টটি [MIT License](LICENSE) এর অধীনে ওপেন সোর্স করা হয়েছে।

---

> **নোট:** এই অ্যাপটি কেবল ডেমো ও শিক্ষার উদ্দেশ্যে তৈরি করা হয়েছে। আসল পেমেন্ট প্রসেসিংয়ের জন্য ব্যাকএন্ড এডমিন প্যানেল ব্যবহার করা বাঞ্ছনীয়।
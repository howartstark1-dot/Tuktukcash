# 🚖 Tuktukcash - Production Ready Telegram Mini App (TMA)

সম্পূর্ণ রিয়েল লজিক ও খাঁটি ইউজার সিস্টেম সম্বলিত **Telegram Mini App**। এতে কোনো ডামি বা ফেক হিস্ট্রি রাখা হয়নি। সমস্ত ইউজার ডেটা, পয়েন্ট ও রেফারেল সরাসরি টেলিগ্রাম ইউজার আইডি দিয়ে **Firebase Realtime Database**-এ সংরক্ষিত ও সিঙ্ক হয়।

---

## 📁 GitHub রিপোজিটরির ৪টি মূল ফাইল

আপনার GitHub রিপোজিটরিতে (`tuktukcash`) নিচের ৪টি ফাইল আপলোড করলেই অ্যাপটি শতভাগ স্বয়ংক্রিয়ভাবে কাজ করবে:

```text
tuktukcash/
├── index.html        # মূল আর্নিং ড্যাশবোর্ড, পয়েন্ট কার্ডে টেলিগ্রাম গ্রুপ বাটন, রিয়েল রেফারেল সিস্টেম ও Monetag Ads
├── withdraw.html     # বিকাশ ও নগদ উইথড্র পোর্টাল (১০টি রিয়েল রেফারেল আনলক শর্ত সহ)
├── history.html      # রিয়েলটাইম আরটিডিবি ট্রানজ্যাকশন লেজার (জিরো ফেক ডেটা, ক্লিন লেজার)
├── sw.js             # Monetag সার্ভিস ওয়ার্কার ফাইল
└── README.md         # প্রজেক্ট ও সেটআপ গাইডলাইন
```

---

## 🔗 আপনার কনফিগারেশন বিবরণ

| বিষয় | কনফিগারেশন ভ্যালু |
| :--- | :--- |
| **অফিসিয়াল টেলিগ্রাম গ্রুপ** | [https://t.me/+IVKpFLggaihlMjBl](https://t.me/+IVKpFLggaihlMjBl) |
| **বট ইউজারনেম** | `@Tuktukcashbot` |
| **Firebase Realtime Database** | `https://tuktukcash-default-rtdb.firebaseio.com/` |
| **Monetag Rewarded Ads Zone** | `12012404` (`show_12012404()`) |
| **Monetag Service Worker Zone** | `12023628` (Domain: `5gvci.com`) |
| **রেফারেল নিয়ম** | রিয়েল ১০টি রেফারেল সম্পন্ন হলে উইথড্র আনলক হবে |
| **মিনিমাম উইথড্র** | ১,০০০ PTS |
| **পেমেন্ট গেটওয়ে** | bKash Personal & Nagad Account |

---

## ⚡ ১. GitHub-এ ফাইল আপলোড ও Pages চালু করা

1. **[GitHub.com](https://github.com)**-এ লগইন করে নতুন একটি Public Repository তৈরি করুন (নাম দিন: `tuktukcash`)।
2. **Add file** -> **Create new file** দিয়ে ফাইলগুলো তৈরি করুন:
   - `index.html` (ড্যাশবোর্ড কোড)
   - `withdraw.html` (উইথড্র কোড)
   - `history.html` (হিস্ট্রি কোড)
   - `sw.js` (সার্ভিস ওয়ার্কার)
3. **Settings** -> **Pages**-এ যান।
4. **Branch:** `main` এবং ফোল্ডার `/ (root)` সিলেক্ট করে **Save** চাপুন।
5. আপনার লাইভ লিংক পাওয়া যাবে:
   ```text
   https://<your-username>.github.io/tuktukcash/
   ```

---

## 🤖 ২. @BotFather দিয়ে টেলিগ্রামে মিনি অ্যাপ চালু

1. টেলিগ্রামে `@BotFather`-এ যান।
2. `/mybots` লিখে আপনার বট `@Tuktukcashbot` নির্বাচন করুন।
3. **Bot Settings** -> **Menu Button** -> **Configure menu button** চাপুন।
4. আপনার GitHub Pages লাইভ URL দিন এবং বাটনের নাম লিখুন: **Earn Cash**।

---

## 🛡️ রিয়েল ডাটাবেজ স্ট্রাকচার

- নতুন ইউজার টেলিগ্রাম দিয়ে প্রবেশ করলেই সেভ হবে: `https://tuktukcash-default-rtdb.firebaseio.com/users/{userId}.json`
- রেফারেল লিঙ্ক: `https://t.me/Tuktukcashbot?start=ref_{userId}`
- উইথড্র রিকোয়েস্ট: `https://tuktukcash-default-rtdb.firebaseio.com/withdraw_requests.json`

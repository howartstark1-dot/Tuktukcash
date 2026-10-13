# 🚖 Tuktukcash - Telegram Mini App (TMA)

সম্পূর্ণ কার্যকরী ও প্রোডাকশন-রেডি **Telegram Mini App** যাতে যুক্ত রয়েছে **Monetag Rewarded Ads**, **Firebase Realtime Database**, ১০টি রেফারেল আনলক রুল এবং লোকাল পেমেন্ট সিস্টেম (**bKash** ও **Nagad**)।

---

## 📂 ফাইল স্ট্রাকচার (Repository Structure)

আপনার GitHub রিপোজিটরিতে (`tuktukcash`) এই ৪টি মূল ফাইল থাকবে:

```text
tuktukcash/
├── index.html        # মূল আর্নিং ড্যাশবোর্ড, ব্যালেন্স, ডেইলি স্ট্রিক ও Monetag Rewarded Ads
├── withdraw.html     # বিকাশ ও নগদ উইথড্র পোর্টাল (১০ রেফারেল আনলক শর্ত সহ)
├── history.html      # রিয়েলটাইম লেনদেন হিস্ট্রি ও ফিল্টার (RTDB সিঙ্ক)
├── sw.js             # Monetag Service Worker ভেরিফিকেশন ফাইল
└── README.md         # প্রজেক্ট ও সেটআপ গাইড
```

---

## ⚡ ১. GitHub-এ আপলোড ও GitHub Pages চালু করার নিয়ম

1. **GitHub.com**-এ যান এবং আপনার একাউন্টে লগইন করুন।
2. নতুন একটি পাবলিক রিপোজিটরি তৈরি করুন, নাম দিন: **`tuktukcash`**
3. **Add file** > **Create new file**-এ ক্লিক করে ফাইলগুলো একটি একটি করে তৈরি করুন:
   - `index.html` তৈরি করে কোড পেস্ট করুন ও **Commit changes** দিন।
   - `withdraw.html` তৈরি করে কোড পেস্ট করুন ও **Commit changes** দিন।
   - `history.html` তৈরি করে কোড পেস্ট করুন ও **Commit changes** দিন।
   - `sw.js` তৈরি করে কোড পেস্ট করুন ও **Commit changes** দিন।
4. রিপোজিটরির **Settings** ট্যাবে যান।
5. বাম পাশের মেনু থেকে **Pages** সিলেক্ট করুন।
6. **Build and deployment** সেকশনে:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` এবং ফোল্ডার `/ (root)` সিলেক্ট করে **Save** বাটনে ক্লিক করুন।
7. ১ মিনিটের মধ্যে আপনার লাইভ লিংক তৈরি হয়ে যাবে:
   ```text
   https://<your-username>.github.io/tuktukcash/
   ```

---

## 🤖 ২. টেলিগ্রাম বট (@BotFather)-এ মিনি অ্যাপ যুক্ত করার নিয়ম

1. টেলিগ্রামে গিয়ে সার্চ করুন **`@BotFather`**।
2. চ্যাটে লিখুন: `/mybots`
3. আপনার বটটি সিলেক্ট করুন (`@Tuktukcashbot`)।
4. **Bot Settings** মেনুতে যান।
5. **Menu Button** সিলেক্ট করুন > **Configure menu button** চাপুন।
6. আপনার GitHub Pages-এর লাইভ লিংকটি পাঠান:
   ```text
   https://<your-username>.github.io/tuktukcash/
   ```
7. বাটনের টাইটেল হিসেবে লিখুন: **`Earn Cash`** অথবা **`Open App`**।
8. কাজ শেষ! এখন টেলিগ্রামে আপনার বট ওপেন করে নিচে থাকা মেনু বাটনে চাপলেই সরাসরি অ্যাপটি খুলে যাবে।

---

## 🔑 কনফিগারেশন ও ক্রেডেনশিয়ালস সামারি

| আইটেম | কনফিগারেশন বিবরণ |
| :--- | :--- |
| **বট ইউজারনেম** | `@Tuktukcashbot` |
| **Monetag Zone ID** | `#12012404` (`show_12012404()`) |
| **Monetag Service Worker** | `sw.js` (Zone: `12023628`, Domain: `5gvci.com`) |
| **Firebase Realtime Database** | `https://tuktukcash-default-rtdb.firebaseio.com/` |
| **উইথড্র রুল** | সর্বনিম্ন **১০টি রেফারেল** সম্পন্ন হলে আনলক হবে |
| **মিনিমাম ক্যাশআউট** | ১,০০০ PTS |
| **পেমেন্ট চ্যানেল** | bKash Personal & Nagad Account |

---

## 💸 উইথড্র রিকোয়েস্ট কোথায় জমা হবে?

ইউজাররা যখন উইথড্র রিকোয়েস্ট পাঠাবে, ডেটাগুলো সরাসরি আপনার Firebase Realtime Database-এর এই পাথে জমা হবে:
```text
https://tuktukcash-default-rtdb.firebaseio.com/withdraw_requests.json
```
সেখান থেকে আপনি ইউজারের বিকাশ/নগদ নম্বর এবং পয়েন্ট দেখে পেমেন্ট সম্পন্ন করতে পারবেন।

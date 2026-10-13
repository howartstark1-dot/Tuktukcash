# Tuktukcash Telegram Mini App (TMA) 🚖💰

A production-ready Telegram Mini App integrating **Monetag Rewarded Ads** and **Firebase Realtime Database** with local BDT payment options (**bKash** and **Nagad**).

## 📁 Repository File Structure

```text
tuktukcash/
├── index.html        # Main Earn & Watch Ads Dashboard
├── withdraw.html     # Withdrawal Portal (bKash & Nagad)
├── history.html      # Live Ledger & Transaction History
└── README.md         # Deployment & Setup Guide
```

---

## ⚡ Quick Deployment to GitHub Pages

1. Create a repository on [GitHub](https://github.com) named `tuktukcash`.
2. Upload `index.html`, `withdraw.html`, and `history.html`.
3. Go to **Settings** > **Pages** > Set Branch to `main` and Folder to `/ (root)`, then click **Save**.
4. Your live app URL will be: `https://<your-username>.github.io/tuktukcash/`.

---

## 🤖 Connect to Telegram Bot (@BotFather)

1. Open Telegram and search for `@BotFather`.
2. Send `/mybots` and select your bot (`@Tuktukcashbot`).
3. Select **Bot Settings** > **Menu Button** > **Configure menu button**.
4. Paste your GitHub Pages URL (`https://<your-username>.github.io/tuktukcash/`).
5. Set the button title as **`Open App`** or **`Earn Cash`**.

---

## 🔑 Configured Credentials

- **Telegram Bot:** `@Tuktukcashbot`
- **Monetag Zone:** `#12012404` (Rewarded Interstitial `show_12012404()`)
- **Firebase Realtime Database:** `https://tuktukcash-default-rtdb.firebaseio.com/`
- **Exchange Rate:** 100 PTS = 1.00 BDT
- **Supported Payouts:** bKash & Nagad (Minimum 1,000 PTS / 10 BDT)

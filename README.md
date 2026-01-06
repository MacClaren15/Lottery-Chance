# 🎱 Singapore TOTO Probability Calculator

A sleek, cloud-synced web application for tracking and analyzing Singapore TOTO lottery draw history. Calculate number probabilities based on historical data and get recommended numbers for your next draw.

![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue?logo=github)
![Storage](https://img.shields.io/badge/Storage-GitHub%20API-green?logo=github)
![License](https://img.shields.io/badge/License-MIT-yellow)

## ✨ Features

### 📊 Public View (`index.html`)
- **Real-time Probability Analysis** — See which numbers appear most frequently
- **Top Recommended Numbers** — Get the 6 highest probability main numbers + top additional number
- **Visual Probability Bars** — Quickly compare all 49 numbers at a glance
- **Recent Draws Table** — View the latest lottery results
- **Mobile Responsive** — Works beautifully on any device

### 🔐 Admin Panel (`admin.html`)
- **Secure Access** — Protected by your GitHub Personal Access Token
- **Add New Draws** — Visual number picker for easy data entry
- **Bulk Import** — Upload CSV files with multiple draws
- **Export Data** — Download your data as CSV backup
- **Delete & Clear** — Manage individual draws or reset all data
- **Cloud Synced** — Data persists across all your devices

## 🌐 Live Demo

👉 **[View Live Site](https://macclaren15.github.io/Lottery-Chance/)**

## 🛠️ How It Works

```
┌─────────────────┐         ┌─────────────────┐
│   Public View   │  reads  │                 │
│   (index.html)  │ ──────► │   data.json     │
└─────────────────┘         │   (GitHub Repo) │
                            │                 │
┌─────────────────┐  read/  │                 │
│   Admin Panel   │  write  │                 │
│   (admin.html)  │ ◄─────► │                 │
└─────────────────┘         └─────────────────┘
        │
        ▼
  GitHub API + Token
```

### Storage Solution
Instead of using external databases or paid services, this project uses **GitHub itself as the database**:

- **Reading**: The public page fetches `data.json` directly from the repository (free, unlimited)
- **Writing**: The admin panel uses the GitHub API with your Personal Access Token to update `data.json`

**Benefits:**
- ✅ 100% free forever — no API limits or quotas
- ✅ Built-in version history via Git
- ✅ Data lives in your own repository
- ✅ Works across all devices

## 📁 File Structure

```
Lottery-Chance/
├── index.html      # Public read-only view
├── admin.html      # Password-protected admin panel
├── data.json       # Lottery data storage
└── README.md       # This file
```

## 🚀 Setup Instructions

### 1. Fork or Clone This Repository

```bash
git clone https://github.com/macclaren15/Lottery-Chance.git
```

### 2. Create a GitHub Personal Access Token

1. Go to **GitHub Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)**
2. Click **Generate new token (classic)**
3. Set:
   - **Note**: `TOTO Lottery App`
   - **Expiration**: No expiration (or your preference)
   - **Scopes**: ✅ `repo`
4. Click **Generate token** and copy it immediately

### 3. Enable GitHub Pages

1. Go to your repository **Settings** → **Pages**
2. Under **Source**, select `main` branch
3. Click **Save**
4. Your site will be live at `https://[username].github.io/Lottery-Chance/`

## 📋 CSV Import Format

To bulk import lottery draws, use this CSV format:

```csv
DrawNumber,Date,Num1,Num2,Num3,Num4,Num5,Num6,Additional
3961,2024-01-01,1,12,23,34,45,49,7
3962,2024-01-04,5,15,25,35,40,42,18
3963,2024-01-08,3,17,28,33,41,47,22
```

You can download a template from the Admin Panel.

## 🔢 Probability Algorithm

```
Probability = ((Number of occurrences / Total draws) + 0.01) × 100%
```

The `+0.01` baseline ensures numbers with zero occurrences still display a minimal probability rather than 0%.

### Best Practices
- Use a token with minimal scopes (only `repo` is needed)
- Set an expiration date if you prefer
- Don't share your token with anyone
- Revoke and regenerate if you suspect compromise

## 🎨 Tech Stack

- **Frontend**: Vanilla HTML, CSS, JavaScript
- **Fonts**: [Outfit](https://fonts.google.com/specimen/Outfit), [Space Mono](https://fonts.google.com/specimen/Space+Mono)
- **Storage**: GitHub API + Repository
- **Hosting**: GitHub Pages
- **External Dependencies**: None! 🎉

## 📱 Browser Support

| Browser | Supported |
|---------|-----------|
| Chrome | ✅ |
| Firefox | ✅ |
| Safari | ✅ |
| Edge | ✅ |
| Mobile Browsers | ✅ |

## ⚠️ Disclaimer & Responsible Gambling

### 🎰 Entertainment Only
This application is provided **strictly for entertainment and educational purposes only**. It is NOT a gambling advice tool, prediction system, or financial guidance service.

### 📊 No Predictive Value
- **Lottery outcomes are completely random** — each draw is independent
- **Past results have ZERO influence** on future draws (Gambler's Fallacy)
- **Probability statistics shown are historical only** — they do not predict future outcomes
- **No system, algorithm, or software can guarantee winning numbers**

### ⚖️ Liability Disclaimer
By using this website, you acknowledge and agree that:

- **The creator(s) of this website are NOT responsible** for any actions taken by users based on information displayed
- **Any financial decisions or gambling activities** are made entirely at your own risk
- **Losses incurred from lottery participation** are solely your responsibility
- **This website does not encourage, promote, or endorse gambling**

### 🛑 Responsible Gambling
If you choose to participate in lottery games:

- **Set a budget** — Only spend what you can afford to lose
- **Never chase losses** — Accept that losing is part of gambling
- **Don't borrow money** to gamble
- **Take breaks** — Gambling should not interfere with daily life
- **Seek help if needed** — Contact gambling helplines if you feel you have a problem

**Singapore Resources:**
- National Council on Problem Gambling: **1800-6-668-668**
- Website: [ncpg.org.sg](https://www.ncpg.org.sg/)

---

**🚨 If gambling is affecting your life, please seek help immediately.**

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Singapore Pools for the TOTO lottery game
- GitHub for free hosting and API access

---

<p align="center">
  Made with ❤️ in Singapore
  <br>
  <a href="https://macclaren15.github.io/Lottery-Chance/">View Live</a> •
  <a href="https://github.com/macclaren15/Lottery-Chance/issues">Report Bug</a> •
  <a href="https://github.com/macclaren15/Lottery-Chance/issues">Request Feature</a>
</p>

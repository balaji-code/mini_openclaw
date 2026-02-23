# Indian Stock Market News Aggregator 📈

Automatically fetches and emails Indian stock market news from top financial sources.

## Features
- ✅ Fetches news from 5 major Indian financial sources:
  - Moneycontrol
  - Economic Times
  - Business Standard
  - Mint
  - NDTV Profit
- ✅ Beautiful HTML email format
- ✅ Saves local HTML preview
- ✅ Ready for daily automation (7 AM schedule)

## Setup

### 1. Install Dependencies
```bash
cd /Users/balajiakiri/Documents/Agent_apps/financial_news_aggregator
pip install -r requirements.txt
```

### 2. Configure Email
Copy `.env.example` to `.env` and add your email credentials:
```bash
cp .env.example .env
```

Edit `.env` file:
```env
SENDER_EMAIL=your_email@gmail.com
SENDER_PASSWORD=your_gmail_app_password
RECIPIENT_EMAIL=your_email@gmail.com
```

**For Gmail:**
1. Enable 2-Factor Authentication on your Google account
2. Generate App Password: https://myaccount.google.com/apppasswords
3. Use the app password (not your regular password)

### 3. Test Run
```bash
python news_aggregator.py
```

This will:
- Fetch latest news
- Save HTML preview locally (open `latest_news.html` in browser)
- Send email if configured

## Automate Daily at 7 AM

### On Mac/Linux (using cron):
```bash
# Edit crontab
crontab -e

# Add this line (runs at 7:00 AM daily)
0 7 * * * cd /Users/balajiakiri/Documents/Agent_apps/financial_news_aggregator && /usr/bin/python3 news_aggregator.py >> logs.txt 2>&1
```

### On Mac (using launchd - more reliable):
I can create a launchd plist file if you prefer this method.

## Usage

### Manual run:
```bash
python news_aggregator.py
```

### Preview without sending email:
Just don't set `RECIPIENT_EMAIL` in `.env` - it will only save HTML locally.

## Customization

Edit `news_aggregator.py` to:
- Add/remove news sources (edit `NEWS_SOURCES` dict)
- Change number of articles per source (default: 5)
- Modify email template styling
- Add filtering by keywords

## Troubleshooting

**No email received?**
- Check spam folder
- Verify Gmail app password is correct
- Check console output for errors

**RSS feed not working?**
- Some feeds may change URLs
- Check if the source website updated their RSS

**Want to test email?**
Run the script and check the console output for any error messages.

---
*Built for: Balaji Akiri*  
*Purpose: Daily 7 AM Indian stock market news digest*

# Telegram Bot API Vulnerability Disclosure

📌 **Status:** Reported to Telegram Security Team on **August 19, 2025**  
📌 **Researcher:** Stark Nil ([@Gill728](https://t.me/Gill728))  
📌 **Contact:** dev.mail.1234.8888@gmail.com  

---

## 📖 Overview
This repository documents a **potential security vulnerability** in Telegram’s infrastructure, where a **Bot API bot** was able to trigger delivery of **real Telegram login codes** to a user’s *Service Notifications*, using only the user’s `user_id`.

Normally, the `auth.sendCode` MTProto method requires a **phone number**.  
Observed behavior suggests that this requirement can be bypassed under certain conditions.

---

## 🎯 Impact
- Malicious bots could trick users into revealing their **real Telegram login codes**.  
- Raises risk of **session hijacking** and **account takeover**.  
- Undermines separation between **Bot API** (chat bots) and **MTProto authentication**.  

---

## 📅 Disclosure Timeline
- **19 Aug 2025** → Full report (with evidence) submitted to `security@telegram.org`.  
- **[22-08-25]** → Sent reminders.  
- **[26-08-25]** → No acknowledgment received after 7 days. This summary published for transparency.  

---

## 📂 Contents
- [`DISCLOSURE.md`](DISCLOSURE.md) → Full responsible disclosure summary.  
- `evidence/` *(optional)* → Screenshots and proof (redacted).  

---

## 🔒 Responsible Disclosure
This repository contains **no exploit code** and avoids sensitive technical details to prevent abuse.  
Full details were shared privately with Telegram’s security team.  

If Telegram acknowledges and fixes this issue, I will update the repo accordingly.  

---

## 🙋‍♂️ Author
**Stark Nil**  
- Email: dev.mail.1234.8888@gmail.com  
- Telegram: [@Gill728](https://t.me/Gill728)  

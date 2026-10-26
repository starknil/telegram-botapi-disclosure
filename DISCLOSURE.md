# Responsible Disclosure Summary

**Title:** Potential Security Vulnerability in Telegram Bot API – Unauthorized Login Code Triggers  

**Date Reported:** August 19, 2025  
**Reporter:** StarkNil ([@Gill728](https://t.me/Gill728), dev.mail.1234.8888@gmail.com)  
**Status:** Report submitted to `security@telegram.org` on August 19, 2025. No acknowledgment received as of *[insert date]*.  

---

## Overview  
I identified a potential vulnerability in Telegram’s infrastructure where a Bot API bot can trigger real **Telegram account login codes** to a user’s *Service Notifications* using only their `user_id`.  

Normally, the `auth.sendCode` MTProto method requires the account’s **phone number**. This observed behavior suggests that a Bot API bot may bypass this requirement.  

---

## Impact  
- Attackers could exploit this to confuse or phish users into revealing their **real Telegram login codes**.  
- This raises the risk of **session hijacking and account takeover**.  
- It undermines the expected separation between **Bot API (chat bots)** and **MTProto authentication mechanisms**.  

---

## Disclosure Timeline  
- **19 Aug 2025:** Full technical report + proof-of-concept submitted to `security@telegram.org` (with screen recording + screenshots).  
- **[Insert follow-up dates]:** Sent reminders.  
- **[Insert date]:** No acknowledgment received after 30+ days.  

---

## Researcher’s Note  
This disclosure does not include proof-of-concept code or reproduction steps, to avoid abuse. Technical details have been privately shared with Telegram’s security team.  

I remain open to working with Telegram to validate, remediate, and responsibly coordinate public disclosure if required.  

---

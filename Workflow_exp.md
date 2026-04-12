# Smart Campus Automation System – Workflow Explanation

## Overview
This system is built using n8n and automates key campus operations such as student registration, communication, reminders, feedback analysis, and reporting. The workflows are interconnected and event-driven.

---

## Workflow 1: Student Registration & Validation
**Trigger:** Webhook  
- Captures student details from form  
- Validates email and duplicate entries  
- Stores data in Google Sheets  
- Triggers communication workflow  

---

## Workflow 2: Automated Communication
**Trigger:** Internal Workflow Call  
- Generates unique registration ID  
- Sends confirmation email  

---

## Workflow 3: Event Reminder Automation
**Trigger:** Cron (Time-based)  
- Identifies upcoming events  
- Sends reminders (24 hrs & 1 hr before event)  
- Tracks attendance status  

---

## Workflow 4: Feedback & AI Analysis
**Trigger:** Cron / Webhook  
- Sends feedback form  
- Stores responses  
- Performs AI-based sentiment analysis  
- Alerts admin for negative feedback  

---

## Workflow 5: Admin Reporting & Analytics
**Trigger:** Weekly Cron  
- Aggregates registration and attendance data  
- Summarizes feedback insights  
- Sends weekly report to admin  

---

## Conclusion
The system demonstrates event-driven automation, API integration, AI-assisted insights, and modular workflow orchestration using n8n.

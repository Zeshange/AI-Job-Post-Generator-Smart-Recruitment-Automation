# 🤖 AI Job Post Generator & Smart Recruitment Automation (n8n)

video link:  https://drive.google.com/file/d/1AhFVCm0S5cBgSpJks7jhnNEd1dgIPc-9/view?usp=sharing

## 📌 Project Overview
This project is a **full-scale AI-powered recruitment automation system** built using **n8n (self-hosted)**.  
It automates the entire hiring workflow — from **job post generation** to **CV screening and candidate shortlisting** — using AI, Google Sheets, Email automation, and image generation.

The system reduces manual HR work, improves candidate experience, and ensures faster, smarter, and unbiased hiring decisions.

---

## 🎯 Core Objectives
- Generate professional job posts using a form
- Create visually attractive job post images automatically
- Store job requirements centrally in Google Sheets
- Monitor job application emails in real time
- Read and analyze CV attachments (PDF)
- Match CVs with job requirements
- Score candidates from **1 to 10** using AI
- Automatically respond to candidates based on score

---

## 🛠 Technology Stack
- **n8n (Self-Hosted)** – Workflow orchestration
- **Google Gemini (AI)** – Job post writing & CV evaluation
- **Google Sheets** – Job requirements database
- **HTML → Image API (HtmlCSStoImage)** – Job post image generation
- **Gmail / IMAP** – Email trigger & auto replies
- **LangChain Nodes** – Memory & structured AI output
- **PDF Text Extraction** – CV parsing

---

## 🔄 Workflow Breakdown

### 🔹 PART 1: AI Job Post Generator

#### 1️⃣ Form Trigger
- HR fills a form with:
  - Job Title
  - Company Name
  - Location
  - Experience
  - Skills (1–4)
  - Salary
  - Job Type

#### 2️⃣ Google Sheets (Append Row)
- Saves job requirements into Google Sheets
- Sheet acts as a **single source of truth** for hiring criteria

#### 3️⃣ AI Job Post Writing
- AI generates:
  - Short, engaging primary text
  - Strong hiring hook
  - Call-to-Action
- Uses system-defined recruitment copywriting rules

#### 4️⃣ HTML Job Post Design
- Dynamic HTML template created with:
  - Gradient header
  - Job title & company
  - Skills tags
  - Salary & job type
  - WhatsApp CTA
- Fully responsive (mobile & desktop)

#### 5️⃣ HTML → Image Conversion
- HTML is sent to HtmlCSStoImage API
- High-quality job post image is generated automatically

#### 6️⃣ Email Delivery
- Job post image is emailed as an attachment
- AI-generated text is included in the email body

---

### 🔹 PART 2: AI CV Screening & Shortlisting

#### 7️⃣ Email Trigger (IMAP)
- Watches inbox for job application emails
- Automatically reads:
  - Sender
  - Subject (Job Title)
  - CV attachment (PDF)

#### 8️⃣ CV Text Extraction
- Extracts readable text from PDF CV
- Prepares data for AI analysis

#### 9️⃣ Job Role Detection
- Matches email subject keywords with Google Sheet job titles
- Ensures correct job requirements are selected

#### 🔟 AI Candidate Evaluation
- AI compares:
  - CV skills
  - Experience
  - Job requirements
- Returns structured JSON:
```json
{
  "score": 8,
  "reason": "Strong skills match with required technologies"
}


🧠 Decision Logic
✅ If Score > 7

Candidate is marked Strong

Automatic confirmation email sent:

“Thank you for submitting your CV. Our team will contact you soon.”

❌ If Score ≤ 7

Polite rejection email is sent

No manual intervention required

✨ Key Features

✔ End-to-end hiring automation
✔ AI-based CV scoring (1–10)
✔ Visual job post generation
✔ Smart job title matching
✔ Zero manual CV screening
✔ Scalable for multiple roles
✔ Clean, reusable n8n workflow

📈 Business Impact

Reduces HR screening workload by 80%

Faster candidate responses

Consistent & unbiased evaluation

Ideal for:

Institutes

Startups

Recruitment agencies

HR teams

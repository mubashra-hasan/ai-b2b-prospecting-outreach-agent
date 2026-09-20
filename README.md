# AI B2B Prospecting & Outreach Agent

### AI-powered B2B prospect research, ICP qualification, personalized outreach, and follow-up automation built with n8n.

<p align="center">

![n8n](<img width="397" height="286" alt="AI Agent PE" src="https://github.com/user-attachments/assets/c5b15950-3068-4257-93fa-8628a0cd11ec" />
)
![AI](<img width="397" height="286" alt="AI Agent icp" src="https://github.com/user-attachments/assets/8d79cfe4-eb4a-4976-b6af-e153d8773bbf" />)

![Google Sheets](<img width="358" height="257" alt="google sheeeeth" src="https://github.com/user-attachments/assets/9577685c-3036-472e-b642-83c8ca51cfaa" />
)
![Email](<img width="361" height="218" alt="email" src="https://github.com/user-attachments/assets/5816dc9d-4181-4b0d-97fe-860ddfa6f829" />
)

</p>

---

## Overview

**AI B2B Prospecting & Outreach Agent** is an AI-powered automation system designed to streamline repetitive B2B prospecting tasks.

The workflow takes prospect data from Google Sheets, researches companies, evaluates ICP fit, identifies potential business pain points, generates personalized outreach, and routes qualified prospects through a human approval process before outreach.

The system combines **AI agents, structured outputs, workflow automation, data validation, and human-in-the-loop decision making** into a single n8n workflow.

---

## Workflow Architecture

<p align="center">

<img width="900" alt="AI B2B Prospecting & Outreach Agent Workflow" src="PASTE-YOUR-GITHUB-WORKFLOW-IMAGE-URL-HERE">

</p>

### Pipeline

```text
Google Sheets
      │
      ▼
Research & ICP Agent
      │
      ▼
Structured Output Parser
      │
      ▼
Personalized Email Agent
      │
      ▼
ICP Qualification
      │
      ├───────────────┐
      │               │
   Qualified      Not Qualified
      │               │
      ▼               ▼
Human Approval      Tracking
      │
      ▼
Email Verification
      │
      ▼
Outreach
      │
      ▼
Follow-up & Logging
```

---

## Key Features

### AI-Powered Company Research

Automatically analyzes prospect information and generates structured research based on the available company data.

### ICP Qualification

Each prospect receives an AI-generated **ICP score from 0–100** to help identify businesses that are more aligned with the target customer profile.

### Pain Point Detection

The research stage identifies potential business pain points and possible opportunities where automation could provide value.

### Personalized Email Generation

The workflow generates personalized cold emails using the prospect's company information, industry, research, ICP score, pain point, and automation opportunity.

### Human-in-the-Loop Approval

AI does not directly control the final outreach decision.

Qualified prospects can be reviewed by a human before the email moves to the sending stage.

### Structured AI Output

A structured output parser keeps AI-generated research consistent and easier to process in downstream workflow steps.

### Prospect Tracking

Google Sheets acts as a lightweight prospect database for storing research, scores, emails, approval status, and outreach progress.

### Error Handling

The workflow includes validation and tracking stages designed to make failures easier to identify and troubleshoot.

---

## Tech Stack

| Technology                   | Purpose                                       |
| ---------------------------- | --------------------------------------------- |
| **n8n**                      | Workflow orchestration and automation         |
| **AI Agents**                | Research, qualification, and email generation |
| **Google Sheets**            | Prospect database and workflow tracking       |
| **Structured Output Parser** | Consistent AI-generated data                  |
| **HTTP/API Requests**        | External service integrations                 |
| **Email Automation**         | Personalized prospect outreach                |

---

## Prospect Data Structure

The workflow works with structured prospect information such as:

```text
Company
Website
Industry
Country
Employees
Contact Name
Contact Email
LinkedIn
Research
ICP Score
Pain Point
Automation Opportunity
Personalized Email
Approval
Status
```

---

## Qualification Logic

The workflow evaluates prospects using an ICP score.

```text
ICP Score
   │
   ├── ≥ 70
   │     ↓
   │  Qualified
   │     ↓
   │  Human Approval
   │     ↓
   │  Outreach
   │
   └── < 70
         ↓
      Not Qualified
         ↓
       Tracking
```

The threshold can be customized depending on the target business and ICP requirements.

---

## Human-in-the-Loop Design

One of the important design decisions in this project is keeping a human approval stage before outreach.

This provides an additional review layer for:

* AI-generated research
* ICP qualification
* Identified pain points
* Personalized emails
* Prospect relevance

This approach helps prevent an automated system from sending unsuitable outreach without human review.

---

## Example Use Case

Imagine an AI automation agency wants to find businesses that could benefit from automation.

Instead of manually researching every prospect, the workflow can:

**1.** Read prospect information from Google Sheets.

**2.** Research the company using an AI agent.

**3.** Evaluate the prospect against the ICP.

**4.** Identify potential pain points.

**5.** Suggest an automation opportunity.

**6.** Generate a personalized outreach email.

**7.** Route qualified prospects for human approval.

**8.** Verify the contact before outreach.

**9.** Continue the approved outreach process.

**10.** Track the prospect and workflow status.

---

## Installation

### 1. Import the Workflow

Download the workflow JSON from this repository and import it into your n8n instance.

### 2. Configure Credentials

Connect your own:

* AI model/API credentials
* Google Sheets credentials
* Email provider
* Email verification service
* Other required APIs

### 3. Configure Google Sheets

Create a prospect sheet containing the required fields.

### 4. Review AI Prompts

Customize the research, ICP, and email-generation prompts for your target market.

### 5. Test

Run the workflow with sample prospects before using real outreach data.

> **Security:** Never commit API keys, passwords, OAuth tokens, or other credentials to GitHub.

---

## Customization

This workflow can be adapted for different B2B use cases, including:

* SaaS companies
* AI agencies
* Marketing agencies
* Consulting businesses
* Real estate companies
* Recruitment agencies
* Local businesses
* B2B service providers

The ICP rules, prompts, scoring threshold, data sources, and integrations can all be customized.

---

## Future Improvements

Planned improvements include:

* Telegram approval notifications
* Automated lead enrichment
* CRM integration
* Advanced email verification
* Multi-channel outreach
* Automated follow-up sequences
* Lead quality analytics
* Re-enrichment of existing prospects
* Outreach performance dashboard

---

## Project Structure

```text
.
├── README.md
├── workflow/
│   └── ai-b2b-prospecting-outreach-agent.json
└── screenshots/
    └── workflow.png
```

---

## Demo

### Workflow Demo

**Add your demo video here**

`https://www.youtube.com/watch?v=t0FbgIHibWoPASTE-YOUR-DEMO-LINK-HERE`

---

## What I Learned

Building this project helped me work with:

* AI agent orchestration
* n8n workflow design
* Structured AI outputs
* Conditional workflow logic
* API integrations
* Data validation
* Human-in-the-loop automation
* AI-generated personalized content
* Error handling
* Business process automation

---

## About

**Mubashra Hasan**

AI Automation & n8n Workflow Builder focused on building practical AI-powered systems for business processes.

**Focus Areas**

`AI Automation` · `n8n` · `AI Agents` · `Workflow Automation` · `API Integrations` · `Business Process Automation`

---

<p align="center">

**Built with n8n + AI**

</p>


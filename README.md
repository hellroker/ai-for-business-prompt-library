# ai-for-business-prompt-library
# Prompt Library — E-Commerce / Retail (SportZone Australia)

> **Assessment 1 | AI for Business**
> Student: Sayeef Md Irfan Karim|ID - 22692010| Business Field: E-Commerce / Retail
> Model tested on: OpenAI- GPT-5.2
> Last updated: 1 April 2026

---

## What This Library Does

This prompt library supports workflow automation in **e-commerce and retail operations** for SportZone Australia, an Australian online sports retailer. It contains **10 documented, tested, and iterated prompts** organized by the business function they support.

Each prompt entry follows the same structure:
- The exact prompt text (ready to run — no placeholders)
- The workflow task it supports
- The problem it solves
- Its automation potential
- Known risks and mitigations
- Version history showing iterative improvement

---

## Folder Structure

```
ai-for-business-prompt-library/
│
├── README.md                          ← You are here (library index)
│
├── 01-content-creation/
│   ├── prompt-01-product-description.md
│   └── prompt-02-review-response.md
│
├── 02-marketing/
│   ├── prompt-03-promotional-email.md
│   └── prompt-06-social-media-post.md
│
├── 03-customer-service/
│   ├── prompt-04-policy-explainer.md
│   └── prompt-05-faq-answer.md
│
└── 04-hr-operations/
    ├── prompt-07-performance-review.md
    ├── prompt-08-welcome-message.md
    ├── prompt-09-apology-email.md
    └── prompt-10-team-briefing.md
```

---

## Library Summary Table

| ID | Prompt Name | Workflow | Automation Level | Risk Level | Status |
|----|-------------|----------|-----------------|------------|--------|
| P01 | Product Description Generator | Content creation | High | Low | Tested |
| P02 | Customer Review Response | Customer service | High | Medium | Tested |
| P03 | Promotional Email Writer | Email marketing | High | Medium | Tested |
| P04 | Return Policy Explainer | Customer service | High | Low | Tested |
| P05 | Customer FAQ Answer | Customer service | Very High | Low | Tested |
| P06 | Social Media Post Generator | Marketing | High | Medium | Tested |
| P07 | Staff Performance Review | HR operations | Medium | Medium | Tested |
| P08 | New Staff Welcome Message | HR onboarding | High | Low | Tested |
| P09 | Customer Apology Email | Service recovery | High | Medium | Tested |
| P10 | Weekly Team Briefing | Store operations | High | Low | Tested |

**Automation levels:** Very High (minimal human input needed) / High (human review before send) / Medium (human must personalize)
**Risk levels:** High (always needs human review) / Medium (spot-check recommended) / Low (can automate with audit trail)

---

## Prompt Chaining Map

Some prompts in this library are designed to work in sequence. The chains below show how outputs from one prompt feed the next.

```
CUSTOMER SERVICE CHAIN
P05 (FAQ Answer) → P04 (Policy Explainer) → P09 (Apology Email if needed)

MARKETING CAMPAIGN CHAIN
P01 (Product Description) → P03 (Promotional Email) → P06 (Social Media Post)

STAFF MANAGEMENT CHAIN
P08 (Welcome Message) → P07 (Performance Review) → P10 (Team Briefing)
```

---

## Prompting Strategies Used

| Strategy | Prompts Applied | Why Chosen |
|----------|----------------|------------|
| RACE framework (Role, Action, Context, Expectation) | All 10 | Consistent structure; eliminates vague outputs |
| Grounding constraint ("using ONLY the following information") | P04, P05 | Prevents hallucination of policy details |
| Output format specification (word limit, sections, tone) | All 10 | Ensures output is production-ready without heavy editing |
| Audience-specific tone instruction | P02, P07, P08, P09, P10 | Matches each prompt to the right reader (customer vs staff vs manager) |
| Benefit-first framing | P01, P03, P06 | Drives conversion in customer-facing content |

---

## Iteration Evidence

All prompt versions are committed to this repository. Each commit message describes what changed and why. Commit history is the version log.

| Prompt | Versions | Key Improvement Made |
|--------|----------|---------------------|
| P01 | v1.0 → v2.0 → v3.0 | Added RACE role + SEO instruction + benefit-first framing |
| P02 | v1.0 → v2.0 → v3.0 | Added retention line + concrete next step requirement |
| P03 | v1.0 → v2.0 → v3.0 | Added 3 subject line variants + urgency element |
| P04 | v1.0 → v2.0 → v3.0 | Added grounding constraint — prevents policy hallucination |
| P05 | v1.0 → v2.0 → v3.0 | Added full store info + 3-part structure instruction |
| P06 | v1.0 → v2.0 → v3.0 | Added platform-specific tone rules per channel |
| P07 | v1.0 → v2.0 → v3.0 | Added 3-section structure + constructive tone instruction |
| P08 | v1.0 → v2.0 → v3.0 | Added practical first-day tips + human warmth instruction |
| P09 | v1.0 → v2.0 → v3.0 | Added goodwill gesture requirement for service recovery |
| P10 | v1.0 → v2.0 → v3.0 | Added motivational opener + specific call to action |

---

## The 10 Prompts — Quick Reference

**P01 — Product Description Generator**
```
You are a senior e-commerce copywriter for an Australian sports retailer.
Write a compelling product description for a lightweight running shoe.
Include one SEO headline, three benefit-led bullet points, and one use-case
sentence, and a CTA. Max 120 words. Tone: energetic and approachable.
```

**P02 — Customer Review Response**
```
You are a customer experience specialist for an Australian online retailer.
A customer left a 3-star review saying their shoes ran small and they had
to exchange for a larger size. Write a professional reply that acknowledges
the issue, offers a helpful next step, and closes with a warm retention
line. Max 80 words.
```

**P03 — Promotional Email Writer**
```
You are an email marketing strategist for an Australian sports retailer.
Write a promotional email for an end-of-summer sale offering 40% off
selected running gear. Include three subject line variants, a personalized
opening, one urgency element, and a clear CTA. Max 200 words.
Tone: energetic and friendly.
```

**P04 — Return Policy Explainer**
```
You are a customer service agent for an Australian online sports retailer.
A customer asked whether they can return a pair of shoes bought 12 days
ago because they do not fit. The store policy allows returns within 30 days
for unused items. Refunds are processed in 5-7 business days. Write a
clear, warm reply in three sentences.
```

**P05 — Customer FAQ Answer**
```
You are a customer service specialist for SportZone Australia. A customer
asked about shipping costs and delivery times. The store offers free
shipping on orders over $75, standard shipping at $8.95, and express at
$14.95. Delivery takes 2-5 business days. Write a friendly, clear reply
in three sentences.
```

**P06 — Social Media Post Generator**
```
You are a social media strategist for an Australian sports retailer. Write
three platform-specific launch posts for a new lightweight running shoe.
One post for Instagram, one for Facebook, one for TikTok. Each post must
match the platform tone, include relevant hashtags, and end with a call
to action. Keep each post under 100 words.
```

**P07 — Staff Performance Review Writer**
```
You are a retail store manager at an Australian sports retailer. Write a
professional mid-year performance review for a sales assistant. The staff
member is strong at customer engagement and product knowledge, but needs to
improve punctuality and stock replenishment speed. Structure the review in
three sections: key strengths, areas for development, and goals for the
next six months. Tone: constructive, fair, and encouraging. Max 200 words.
```

**P08 — New Staff Welcome Message**
```
You are a store manager at SportZone Australia. Write a warm welcome
message for a new sales assistant starting their first week. Include a
genuine welcome, a brief description of what makes the team great, two
practical tips for their first day, and an open invitation to ask
questions. Max 150 words. Tone: warm, human, and encouraging.
```

**P09 — Customer Apology Email**
```
You are a customer service specialist for SportZone Australia. Write a
professional apology email to a customer whose order arrived five days
late. Acknowledge the delay, take responsibility without making excuses,
offer a concrete goodwill gesture such as a discount on their next order,
and thank them for their patience. Max 120 words. Tone: sincere and
solution-focused.
```

**P10 — Weekly Team Briefing Generator**
```
You are a store manager at SportZone Australia. Write an energetic Monday
morning team briefing for your retail sales staff. Include: this week's
sales focus on running shoes and accessories, a reminder that the
end-of-summer sale starts Wednesday, one motivational line to open the
week on a positive note, and a call to action for the team. Max 150 words.
Tone: upbeat, direct, and team-focused.
```

---

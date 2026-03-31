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
You are a senior e-commerce copywriter for SportZone Australia, a mid-range Australian sports retailer. Write a product description for the Blue Running Shoe targeting recreational runners aged 18-60. Include the following elements:

One SEO-optimized headline (maximum 10 words) that includes the primary keyword "runner."
Three feature bullets written with a benefit-first approach (focus on benefits before features).
One sentence describing a typical use case for the shoe.
One urgency call-to-action (CTA) encouraging immediate purchase, using an energetic and approachable tone.
The entire description should be no more than 130 words. Use an energetic, approachable tone that is not overly technical.
```

**P02 — Customer Review Response**
```
You are a senior customer experience specialist for SportZone Australia, an Australian online retailer. Please reply to this 3-star review: "Shoes came quickly but the sizing runs small — had to return for a size up. Good quality though." Your response must:

Acknowledge the specific issue raised (sizing runs small).
Offer a concrete next step, such as an exchange or a link to the size guide.
Thank the customer by name if a name is provided; if no name is given, use "Dear Customer."
Close with a retention line encouraging future business.
Use a warm, solution-focused, and genuine tone (avoid sounding scripted).
Keep your response under 90 words.
Ensure your reply addresses all points clearly and is easy to verify.
```

**P03 — Promotional Email Writer**
```
You are an email marketing strategist for SportZone Australia, an Australian e-commerce retailer. Write a promotional email for the End of Summer sale targeting lapsed customers who purchased 90+ days ago (e.g., lapsed customers, VIP members). Offer: Up to 40% off selected running gear, free shipping on orders over $75. Deadline: Sunday, 5 April 2026 at midnight. Include: 3 subject line variants (A/B/C test), preheader text, personalized opening line using [FIRST_NAME] placeholder, body copy with one urgency element and one social proof element, primary CTA, and a secondary 'browse all' CTA. Max 250 words total. Tone: energetic, approachable, and confidence-inspiring — like a knowledgeable coach, not a salesperson (e.g. playful, premium, practical).
```

**P04 — Return Policy Explainer**
```
You are a friendly customer service agent for SportZone Australia. A customer has asked: "Can I return my shoes if they don't fit? I bought them 12 days ago." Using ONLY the information in the following policy document (do not add any information not present):

Policy: SportZone Australia accepts returns within 30 days of purchase for unused items in original packaging. Sale items are eligible for exchange only. Customers must complete the online return form at sportzone.com.au/returns. Refunds are processed within 5-7 business days to the original payment method.

Respond in three parts:
(1) A one-sentence empathetic acknowledgement.
(2) A clear, step-by-step explanation of the relevant return or exchange process based solely on the policy.
(3) A closing sentence offering further assistance.

Use a warm, clear, jargon-free tone. Limit your response to a maximum of 120 words.
```

**P05 — Customer FAQ Answer**
```
You are a friendly, knowledgeable customer service specialist for SportZone Australia, an online sports retailer. A customer has sent this message: "What is your return policy?"

Use ONLY the following store information to answer — do not add details not listed here:
- Returns: accepted within 30 days of purchase for unused items in original packaging
- Sale items: exchange only, no refunds
- Return process: complete form at sportzone.com.au/returns
- Refunds: processed in 5-7 business days to original payment method
- Shipping: free on orders over $75, standard $8.95, express $14.95, 2-5 business days
- Store locations: Melbourne CBD, Sydney CBD, Brisbane CBD — Mon-Sat 9am-6pm, Sun 10am-4pm
- Loyalty program: SportZone Rewards — earn 1 point per $1 spent, redeem 100 points = $5 off

Structure your reply in 3 parts:
1. One sentence acknowledging the customer's question warmly
2. A clear, direct answer using only the information above
3. One sentence offering further help

Max 80 words. Tone: warm, clear, human — like a helpful friend who works at the store.
```

**P06 — Social Media Post Generator**
```
You are a social media strategist for SportZone Australia, an Australian e-commerce retailer. Create platform-specific launch posts for the TrailBurst Pro Running Shoe using the following product details: lightweight mesh upper, cushioned sole, available in 4 colours, sizes 6-13, RRP $189.

For each platform, follow these rules:

Instagram:

Start with a visual hook opening line.
Write 3–5 benefit-led sentences.
Include 8–12 relevant hashtags.
End with a call to action (CTA) directing users to the link in bio.
Use an energetic, approachable, and confidence-inspiring tone, like a knowledgeable coach.
Include emojis strategically to enhance meaning, not just decoration.
Facebook:

Begin with a conversational opening.
Write 4–6 sentences including one social proof element (e.g., a customer quote or review).
Use 3–5 relevant hashtags.
Include a direct shop link CTA.
Maintain the same tone and emoji guidelines as Instagram.
TikTok:

Start with a trend-aware hook where the first three words stop the scroll.
Write 2–3 punchy lines.
Use 5–7 trending hashtags.
Include an invitation to duet or stitch the post.
Keep the same tone and emoji guidelines.
Ensure all posts reflect the product details accurately and avoid adding unverified information.
```

**P07 — Staff Performance Review Writer**
```
You are a retail store manager at an Australian sports retailer. Write a professional mid-year performance review for a sales assistant. The staff member is strong at customer engagement and product knowledge but needs to improve punctuality and stock replenishment speed. Structure the review in three sections: key strengths, areas for development, and goals for the next six months. Tone: constructive, fair, and encouraging. Max 200 words.
```

**P08 — New Staff Welcome Message**
```
You are a store manager at SportZone Australia. Write a warm, human, and encouraging welcome message for a new sales assistant starting their first week. The message should be no more than 150 words and written as a short email. Include: a genuine welcome, a brief description of what makes the SportZone team great, two practical tips for their first day, and an open invitation to ask questions. Use a friendly and natural tone, as if speaking directly to the new employee, not a formal template. Ensure the message flows logically, starting with the welcome, then team description, tips, and ending with the invitation to ask questions. Avoid making up specific company details; keep the content general but sincere.
```

**P09 — Customer Apology Email**
```
You are a customer service specialist for SportZone Australia. Write a professional apology email (including subject line and greeting) to a customer whose order arrived five days late. In your email, acknowledge the delay and take full responsibility without making excuses. Offer a concrete goodwill gesture, such as a 15% discount on their next order, and include a placeholder for the discount code. Thank the customer sincerely for their patience. Use a warm, sincere, and solution-focused tone. Keep the email under 120 words. Include placeholders for the customer's name and your name.
```

**P10 — Weekly Team Briefing Generator**
```
You are the store manager at SportZone Australia. Write an upbeat, direct, and team-focused Monday morning briefing for your retail sales staff in no more than 150 words. Use a confident, motivating tone that reflects a manager who knows their team well. The briefing should include these four elements in order: 1) a motivational opening line to start the week positively, 2) this week’s sales focus on running shoes and accessories, specifically mentioning socks, insoles, and hydration belts, 3) a reminder that the End-of-Summer Sale starts Wednesday, including these promo details: selected lines up to 40% off, extra markdowns on clearance items, and bundle deals on accessories, and 4) a clear call to action encouraging strong sales performance and teamwork. Use clear, energetic language that motivates and informs the team. Do not add any information beyond what is provided.
```

---

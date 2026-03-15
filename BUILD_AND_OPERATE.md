# What to Build & How to Earn Money Operating a SaaS

A practical, step-by-step playbook for choosing the right SaaS to build, shipping it fast, and turning it into a real income source. This guide follows directly from the ideas catalogued in [SAAS_IDEAS.md](./SAAS_IDEAS.md).

---

## Table of Contents

1. [Choose What to Build First](#1-choose-what-to-build-first)
2. [The Three Starter Builds (Low Risk, High Reward)](#2-the-three-starter-builds-low-risk-high-reward)
3. [How to Build Your MVP in 4–8 Weeks](#3-how-to-build-your-mvp-in-48-weeks)
4. [Tech Stack Recommendations](#4-tech-stack-recommendations)
5. [How to Set Up Payments & Start Earning](#5-how-to-set-up-payments--start-earning)
6. [Launch Strategy (Get Your First 100 Customers)](#6-launch-strategy-get-your-first-100-customers)
7. [Day-to-Day Operations to Grow Revenue](#7-day-to-day-operations-to-grow-revenue)
8. [Revenue Milestones & What to Do at Each Stage](#8-revenue-milestones--what-to-do-at-each-stage)
9. [Avoiding the Most Common Mistakes](#9-avoiding-the-most-common-mistakes)

---

## 1. Choose What to Build First

The biggest mistake founders make is picking the "most exciting" idea instead of the most buildable one. Use this scoring framework before you commit.

### Decision Scorecard

Rate each factor 1–5 for the idea you are considering:

| Factor | Question to ask | Why it matters |
|--------|----------------|----------------|
| **Your Skills Match** | Can you build at least 70% of the MVP yourself? | Reduces cost and iteration time dramatically |
| **Problem Clarity** | Can you explain the pain in one sentence? | Vague problems = vague products no one buys |
| **Willingness to Pay** | Do people currently pay for a similar solution? | Validates demand before you write a line of code |
| **Speed to MVP** | Can you ship a usable version in under 8 weeks? | Speed to first revenue is everything early on |
| **Low Competition Angle** | Is there a niche or underserved segment you can own? | Fighting Salesforce head-on is a losing game |
| **Recurring Need** | Does the customer need this every month, not just once? | Recurring need = recurring revenue |

**Score 20+ → Build it. Score 15–19 → Validate first. Score < 15 → Reconsider.**

### Quick-Pick Guide by Background

| Your Background | Best Starting Build | Reason |
|----------------|--------------------|----|
| Frontend / Full-Stack Developer | Niche Scheduling SaaS | Simple CRUD + calendaring logic; no ML needed |
| ML / AI Engineer | AI Customer Support Agent | Leverages your strengths; huge market |
| Content Creator / Marketer | Online Course & Community Platform | You understand the user; can dogfood it |
| Generalist / No-code | Reputation & Review Management | Can be partially run with no-code tools early on |
| Backend / DevOps Engineer | Developer Tools & API Monitoring | Natural domain; strong community distribution |

---

## 2. The Three Starter Builds (Low Risk, High Reward)

Based on the full list in SAAS_IDEAS.md, these three are the best first projects for a solo founder or small team:

---

### 🥇 Build #1 — Niche Scheduling & Booking SaaS

**Best for:** Developers who want low complexity and fast revenue.

**The exact niche to start with:** Tattoo studios or independent personal trainers.

**Why these niches specifically:**
- They have no dedicated, well-marketed booking tool.
- They use pen-and-paper or generic tools like Google Calendar.
- They have consistent cash flow and will pay $30–$50/month without hesitation.
- They refer each other constantly (strong word-of-mouth).

**What to build in the MVP (and nothing else):**
- [ ] Online booking page (client-facing) with available time slots
- [ ] Business dashboard to manage appointments
- [ ] Automated email + SMS confirmation and reminder to client
- [ ] Simple payment collection at booking (via Stripe)
- [ ] Basic calendar view for the business owner

**What NOT to build in V1:**
- Mobile app (use a responsive web app)
- Complex reporting
- Multiple staff management
- Loyalty programs

**Price:** $39/month. No free tier. Offer a 14-day free trial.

---

### 🥈 Build #2 — AI Customer Support Agent

**Best for:** Developers comfortable with LLM APIs (OpenAI, Anthropic, etc.).

**The exact niche to start with:** Shopify stores with 100–1,000 monthly orders.

**Why this niche specifically:**
- They are drowning in repetitive questions ("Where is my order?", "What's your return policy?").
- They already pay for Shopify apps — low friction to add another.
- A clear ROI story: "$149/month saves you 15 hours of support per week."

**What to build in the MVP:**
- [ ] Embed a chat widget on the customer's website (one line of code)
- [ ] Train the AI on the merchant's FAQ page, return policy, and product catalog
- [ ] Auto-answer common questions with source attribution
- [ ] Human escalation: if AI is unsure, forward to email or Slack
- [ ] Basic dashboard showing questions answered and topics

**What NOT to build in V1:**
- Voice support
- Multi-language support
- Complex CRM integrations
- Live agent console

**Price:** $99/month flat. No per-conversation pricing in V1 (simplicity wins).

---

### 🥉 Build #3 — Reputation & Review Management

**Best for:** Founders who want lower technical complexity and a sales-driven model.

**The exact niche to start with:** Dental clinics, physiotherapy clinics, or law firms.

**Why these niches specifically:**
- A single new patient/client from Google Search is worth hundreds or thousands of dollars.
- They are acutely aware of their Google reviews but do not have a system to grow them.
- Decisions are made by one person (owner/practice manager) — short sales cycle.

**What to build in the MVP:**
- [ ] Automated review request SMS/email sent after appointment (triggered via CSV upload or simple webhook)
- [ ] Dashboard showing current review count and rating across Google and Facebook
- [ ] Alert when a new negative review appears
- [ ] One-click response drafts (AI-generated reply suggestions)
- [ ] Simple reporting: review growth over time

**What NOT to build in V1:**
- Social media monitoring
- Competitor benchmarking
- White-label (that's an Agency tier feature, build later)

**Price:** $79/month for single location. Sell manually at first — do not build a self-serve checkout until you have 20+ customers.

---

## 3. How to Build Your MVP in 4–8 Weeks

Use this exact timeline. Cut scope ruthlessly — the goal is to get paying customers, not to build a perfect product.

### Week-by-Week Plan

```
Week 1 — Define & Design
  ✓ Write a one-page product spec (problem, customer, core features, non-features)
  ✓ Sketch 5–7 key screens (pen and paper or Figma)
  ✓ Set up repo, hosting, and database
  ✓ Register domain, set up basic landing page

Week 2–3 — Core Feature Build
  ✓ Build the single most important user flow end-to-end
  ✓ Do not work on edge cases yet — focus on the happy path
  ✓ Get it in front of 2–3 potential customers for feedback

Week 4–5 — Payments & Auth
  ✓ Integrate Stripe Billing (subscriptions)
  ✓ Add user authentication (use an auth library — do not build your own)
  ✓ Set up email sending (transactional emails: sign-up, billing, etc.)

Week 6–7 — Polish Core Flow
  ✓ Fix the top 3 issues found in early feedback sessions
  ✓ Add basic error handling and loading states
  ✓ Set up error monitoring (Sentry is free for small usage)

Week 8 — Launch Preparation
  ✓ Finish landing page with clear headline, pricing, and CTA
  ✓ Write 3 email templates: trial welcome, day-5 check-in, trial-ending
  ✓ Set up customer support inbox (even just a dedicated email address)
  ✓ Soft-launch to 10 people in your target audience
```

---

## 4. Tech Stack Recommendations

Choose based on what you already know. Do not switch to a new language or framework for your first SaaS — the learning cost will kill your momentum.

### Recommended Stacks by Product Type

#### For Web SaaS (Dashboard + API)

| Layer | Recommended Option | Why |
|-------|-------------------|-----|
| Frontend | Next.js (React) | SSR, SEO-friendly, huge ecosystem |
| Backend | Next.js API Routes or FastAPI (Python) | Full-stack in one repo, or Python for AI-heavy products |
| Database | PostgreSQL (via Supabase or Railway) | Reliable, relational, free tiers available |
| Auth | Clerk or Supabase Auth | Production-ready in hours, not days |
| Payments | Stripe | Industry standard; best docs; handles subscriptions, trials, invoices |
| Email | Resend or Postmark | Developer-friendly transactional email |
| Hosting | Vercel (frontend) + Railway or Render (backend) | Cheap to start, scales well |
| Error Monitoring | Sentry | Free tier sufficient for early stage |
| Analytics | PostHog (self-hosted) or Plausible | Privacy-friendly, affordable |

#### For AI-Powered SaaS

Use the same stack above, plus:

| Layer | Recommended Option |
|-------|-------------------|
| LLM API | OpenAI GPT-4o or Anthropic Claude |
| Vector DB (if RAG needed) | Supabase pgvector or Pinecone |
| AI Orchestration | LangChain (Python) or Vercel AI SDK (JS) |
| Background Jobs | Inngest or BullMQ |

#### Cheapest Way to Start (Under $20/month total)

| Service | Cost |
|---------|------|
| Vercel Hobby (frontend) | Free |
| Railway Starter (backend + DB) | $5/month |
| Supabase Free tier (auth + DB) | Free |
| Resend (first 3,000 emails) | Free |
| Sentry (first 5,000 errors) | Free |
| Stripe | 2.9% + 30¢ per transaction (no monthly fee) |

**Total fixed cost at launch: ~$5–$20/month.**

---

## 5. How to Set Up Payments & Start Earning

Stripe is the only payment processor you need. Here is exactly how to set it up.

### Step-by-Step Stripe Setup

1. **Create a Stripe account** at stripe.com — takes 10 minutes to verify.
2. **Create Products and Prices** in the Stripe dashboard:
   - One product per plan (e.g., "Starter", "Pro")
   - Set as "Recurring" with monthly billing
3. **Use Stripe Checkout** for your payment page — do not build a custom payment form. Stripe Checkout handles PCI compliance, card validation, and 3D Secure automatically.
4. **Set up a Webhook** to listen for these events:
   - `checkout.session.completed` → activate the customer's account
   - `customer.subscription.deleted` → deactivate the account
   - `invoice.payment_failed` → send a dunning email
5. **Set up a Customer Portal** (built into Stripe) — lets customers update their card, change plans, and cancel. You do not need to build this UI yourself.
6. **Add a free trial** by setting `trial_period_days: 14` on your price — increases conversion significantly.

### Pricing Psychology Tips

- Always show **annual pricing** with a "Save 20%" badge — some customers will take it, giving you better cash flow.
- **Anchor with a higher tier**: show a $199/month Enterprise plan even if no one buys it — it makes your $49/month plan feel affordable.
- **Never offer a free tier** in your first 6 months. It fills your support queue with non-paying users. Use a free trial instead.
- **Charge before the trial ends**: Stripe can collect a payment method at signup and charge automatically after 14 days.

---

## 6. Launch Strategy (Get Your First 100 Customers)

Getting your first 100 customers is entirely different from getting your first 10,000. Do not run Facebook ads yet. Do things that do not scale.

### Phase 1: First 10 Customers (Manual Outreach)

**Goal:** Validate pricing and get real feedback. Revenue at this stage is secondary.

1. **List 50 potential customers.** For niche scheduling: search Instagram for "personal trainer [your city]". For review management: search Google Maps for "dental clinic near me" with < 50 reviews.
2. **Send a personal message** — not a mass email. DM on Instagram, send a LinkedIn message, or send an email. Keep it to 3 sentences:
   - What you built
   - The specific problem it solves for them
   - A link to the product or an offer for a free demo
3. **Do a live demo over Zoom** for every interested lead — do not rely on a self-serve flow yet. This reveals objections and confusion you can fix.
4. **Offer a founding member discount** — e.g., "I am looking for 10 founding customers who will get locked-in pricing of $29/month forever (normally $49). In exchange I just ask for honest feedback."
5. **Close the sale** before they leave the Zoom call. Send a Stripe payment link in the chat.

### Phase 2: First 50 Customers (Community & Content)

1. **Post in relevant communities:**
   - Reddit: r/smallbusiness, r/entrepreneur, r/tattoo (for tattoo booking), r/personaltraining
   - Facebook Groups: "[Your niche] Business Owners" groups
   - Indie Hackers: Post a "Show HN"-style launch post
   - Product Hunt: Schedule a launch on a Tuesday or Wednesday morning (US time)
2. **Write one SEO article per week** targeting a specific pain-point keyword (e.g., "how tattoo studios manage appointments", "best booking software for personal trainers").
3. **Cold email** 200 businesses in your niche using a tool like Apollo.io or Hunter.io. Personalize the first line. Aim for 10–15% reply rate.
4. **Referral program**: Email every paying customer — "If you refer one friend who signs up, I'll give you a free month."

### Phase 3: First 100 Customers (Paid Acquisition)

By this point you should understand your conversion funnel well enough to run paid ads profitably.

1. **Google Search Ads** — bid on high-intent keywords like "tattoo studio booking software". These convert at 3–8%.
2. **Facebook/Instagram Ads** — use job title or interest targeting to reach your specific niche. Start with $10–$20/day.
3. **YouTube video** — a 3–5 minute product demo on YouTube targeting "[niche] booking software" can drive consistent organic traffic.
4. **Partnerships** — reach out to associations, trade publications, or influencers in your niche. Offer an affiliate commission (20–30% MRR for the first 12 months).

---

## 7. Day-to-Day Operations to Grow Revenue

Once you have paying customers, your job becomes: retain them, grow revenue, and reduce churn.

### Weekly Routine (Estimated: 10–15 hours/week)

| Day | Focus | Time |
|-----|-------|------|
| Monday | Review last week's metrics (churn, new sign-ups, support tickets) | 30 min |
| Monday | Send personalized email to all trial users who are on day 7 | 30 min |
| Tuesday | Fix top reported bugs or UX issues | 2–4 hours |
| Wednesday | Publish one piece of content (blog post, LinkedIn post, Reddit comment) | 1–2 hours |
| Thursday | Sales outreach — send 20–30 personalized cold messages | 1 hour |
| Friday | Customer check-in — email 5 paying customers to ask how it's going | 30 min |
| Ongoing | Respond to support within 4 hours on weekdays | 30–60 min/day |

### Key Metrics to Track (Your Dashboard)

| Metric | What it means | Target |
|--------|--------------|--------|
| **MRR** (Monthly Recurring Revenue) | Total predictable monthly revenue | Growing 10–20%/month early stage |
| **Churn Rate** | % of customers who cancel each month | < 3% monthly (< 36% annual) |
| **Trial-to-Paid Conversion** | % of trials that become paying customers | > 20% |
| **ARPU** | Average revenue per user | Should grow over time via upgrades |
| **NPS** | How likely customers are to recommend you | > 40 is good; > 70 is exceptional |

### How to Reduce Churn (Most Important Lever)

Churn kills SaaS companies. Even 5% monthly churn means you lose 46% of your customers every year — you are running to stand still.

1. **Onboarding**: Send a 5-email onboarding sequence starting the moment someone signs up. Each email should guide them to one key action. Customers who complete onboarding churn 3–5× less.
2. **Engagement Check-in at Day 30**: Email every customer at the 30-day mark: "How is [Product] working for you? Is there anything blocking you from getting more value?" Reply to every response personally.
3. **Usage Monitoring**: If a customer has not logged in for 14 days, automatically send a re-engagement email with a helpful tip or new feature announcement.
4. **Cancellation Surveys**: When someone cancels, always ask why. Spot patterns — if 5 people say "too expensive", adjust pricing. If 5 people say "missing feature X", build feature X.
5. **Annual Plan Incentive**: Offer 2 months free for annual prepay. This reduces churn to near zero for a full year and improves your cash flow.

---

## 8. Revenue Milestones & What to Do at Each Stage

### $0 → $1,000 MRR (Months 1–3)

**Focus: Survival and validation**

- Sell manually. Do everything that does not scale.
- Talk to every customer. Be the support, sales, and product team.
- Improve the product based only on what paying customers ask for.
- Do not hire. Do not spend on ads. Do not rebuild the tech stack.
- **Goal**: Prove that strangers will pay real money for your product.

### $1,000 → $5,000 MRR (Months 3–9)

**Focus: Repeatability**

- Document your sales process so you can repeat it consistently.
- Start one acquisition channel (SEO, cold outreach, or a community) and go deep on it.
- Introduce an annual plan option.
- Onboarding should be mostly automated by now.
- **Goal**: Prove you can acquire customers predictably, not just from personal network.

### $5,000 → $10,000 MRR (Months 9–18)

**Focus: Efficiency and growth**

- Add a second acquisition channel.
- Consider hiring a part-time virtual assistant for support ($5–$15/hour).
- Start experimenting with pricing — you likely left money on the table at your initial price.
- Build out the features that your best customers ask for most.
- **Goal**: Get to ramen profitable (enough to cover your personal expenses).

### $10,000+ MRR

**Focus: Scale**

- Hire your first full-time employee (customer success or developer).
- Run paid acquisition profitably (know your CAC and LTV).
- Explore partnerships, integrations, and agency channels.
- Consider raising a small angel round if you want to grow faster — but only if the business is already growing.

---

## 9. Avoiding the Most Common Mistakes

### ❌ Mistake 1: Building Before Validating

**What happens:** You spend 6 months building. You launch. Nobody buys.

**Fix:** Talk to 10 potential customers before writing a single line of code. Ask them to pre-pay (even $1) to get on the waitlist. If they won't, the idea needs rethinking.

---

### ❌ Mistake 2: Offering Too Many Features at Launch

**What happens:** You build an overwhelming product, get confused users, high churn, and no clear positioning.

**Fix:** Pick the ONE job your product does better than anything else. Do that one thing extremely well. Add features only after customers ask for them repeatedly.

---

### ❌ Mistake 3: Pricing Too Low

**What happens:** You attract price-sensitive customers who churn fast, ask for discounts, and give poor-quality feedback. You burn out at $500 MRR.

**Fix:** Charge at least twice what feels comfortable. B2B SaaS that saves time or money can almost always command $50–$200/month. If people say "that's too expensive", ask what they currently pay for the same outcome — you may be shocked.

---

### ❌ Mistake 4: Ignoring Churn

**What happens:** You acquire 30 new customers per month but also lose 25. Revenue flatlines. You think it is a marketing problem. It is actually a product problem.

**Fix:** Track churn every single week from day one. If monthly churn exceeds 5%, pause acquisition spending and fix retention first.

---

### ❌ Mistake 5: Rebuilding the Tech Stack

**What happens:** You switch from Node to Go, from MySQL to Postgres, from AWS to GCP. You spend 3 months on infrastructure and zero time on customers.

**Fix:** The tech stack does not matter for the first $50K MRR. Use whatever you know. Ship fast. Optimize later.

---

### ❌ Mistake 6: Building for Everyone

**What happens:** You try to serve small businesses AND enterprises AND freelancers. Your messaging is vague. Nobody feels like the product is built for them.

**Fix:** Pick one customer profile and write every word of your website for that person. "This is built for personal trainers" converts better than "This works for any business."

---

## Quick Reference Checklist

Use this as a weekly operating checklist once you have launched:

### Weekly
- [ ] Review MRR, new sign-ups, and cancellations
- [ ] Email all active trial users (personalized, not mass blast)
- [ ] Respond to all support tickets within 4 hours
- [ ] Do outreach to 20–30 potential new customers
- [ ] Publish one piece of content (article, social post, or forum reply)

### Monthly
- [ ] Email all paying customers with a product update
- [ ] Review churn — call or email every customer who cancelled to ask why
- [ ] Check conversion rate from trial to paid — investigate any drop
- [ ] Review pricing — are you leaving money on the table?
- [ ] Set one clear goal for next month (a single north-star metric)

### Quarterly
- [ ] Re-read customer feedback and identify the #1 feature to build
- [ ] Run a Net Promoter Score (NPS) survey to all customers
- [ ] Review your acquisition channels — double down on what is working, cut what is not
- [ ] Revisit pricing page — A/B test headline or pricing tiers
- [ ] Talk to 5 churned customers to understand why they left

---

*This guide is designed to be used alongside [SAAS_IDEAS.md](./SAAS_IDEAS.md). Start with an idea, pick your starter build, and follow the steps above.*

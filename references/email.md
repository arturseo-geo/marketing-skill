# Email Marketing Reference

## Email Sequence Blueprints

### Welcome Sequence (5-7 emails)
Triggered by: New subscriber or sign-up

| # | Day | Subject Type | Goal |
|---|---|---|---|
| 1 | 0 | Deliver the promise | Deliver lead magnet + set expectations |
| 2 | 1 | Quick win | Give one actionable tip they can use today |
| 3 | 2 | Story | Share your origin story or a client success story |
| 4 | 4 | Value + soft pitch | Teach something valuable, mention your product naturally |
| 5 | 6 | Social proof | Case study or testimonial |
| 6 | 8 | Objection handling | Address the #1 reason people don't buy |
| 7 | 10 | Direct offer | Clear pitch with CTA |

### Cart Abandonment Sequence (3 emails)
| # | Timing | Approach |
|---|---|---|
| 1 | 1 hour | Reminder — "You left something behind" + product image |
| 2 | 24 hours | Objection handler — FAQ, social proof, guarantee |
| 3 | 72 hours | Urgency — limited stock, expiring discount, or final reminder |

### Onboarding Sequence (SaaS — 7 emails)
| # | Day | Subject | Goal |
|---|---|---|---|
| 1 | 0 | Welcome + first step | Drive to activation event |
| 2 | 1 | Quick win tutorial | Show immediate value |
| 3 | 3 | Feature highlight | Introduce key feature they haven't used |
| 4 | 5 | Success story | "Here's how [customer] achieved [result]" |
| 5 | 7 | Check-in | Ask if they need help, offer support |
| 6 | 10 | Advanced tip | Deepen engagement with power-user feature |
| 7 | 14 | Trial ending / upgrade | CTA to convert to paid |

### Re-engagement Sequence (3 emails)
| # | Day | Approach |
|---|---|---|
| 1 | 0 | "We miss you" + what's new since they left |
| 2 | 3 | Incentive — exclusive offer or content |
| 3 | 7 | Breakup — "Should we remove you?" (drives surprisingly high opens) |

### Win-Back Sequence (post-churn — 3 emails)
| # | Day | Approach |
|---|---|---|
| 1 | 30 | "Here's what you're missing" + new features/improvements |
| 2 | 60 | Special comeback offer (discount, extended trial) |
| 3 | 90 | Final attempt + easy reactivation link |

---

## Cold Email (B2B Outreach)

### Structure (5-7 sentences max)
```
Subject: [2-5 words — curiosity or relevance]

Hi {FirstName},

[1 sentence — reference something specific about them or their company].

[1 sentence — the problem you solve for people like them].

[1 sentence — credibility: who you helped + what result].

[1 sentence — the ask: "Worth a 15-min chat this week?"].

[Signature — name, title, company, no long disclaimers]
```

### Cold Email Subject Line Formulas
| Formula | Example |
|---|---|
| Question about [their focus] | "Question about your lead gen strategy" |
| {FirstName}, quick question | "Sarah, quick question" |
| Idea for [their company] | "Idea for Acme's onboarding flow" |
| [Mutual connection] suggested I reach out | "Jake mentioned I should reach out" |
| [Stat] about [their industry] | "73% of SaaS teams miss this" |

### Follow-Up Cadence
| Email | Day | Approach |
|---|---|---|
| Initial | 0 | Full pitch (5-7 sentences) |
| Follow-up 1 | 3 | Add value — share a relevant resource, insight, or quick tip |
| Follow-up 2 | 7 | Bump — shorter, reference the original email |
| Follow-up 3 | 14 | Breakup — "I'll assume the timing isn't right. If things change..." |

### Cold Email Rules
- **Warm up new domains** for 2-4 weeks before sending at volume
- **Daily volume**: Under 50 emails per inbox per day
- **Personalize**: First line must reference something specific (not just {Company})
- **One CTA**: Never include two asks in one email
- **No attachments**: In cold emails, attachments trigger spam filters
- **Plain text**: Avoid heavy HTML formatting in cold emails
- **Unsubscribe link**: Required by law (CAN-SPAM, GDPR)

---

## Subject Line Best Practices

### Rules
- 6-10 words / 30-50 characters optimal
- No ALL CAPS (triggers spam filters)
- Avoid spam trigger words: "free," "act now," "limited time" in subject
- Personalization in subject increases open rate by 20-30%
- Questions outperform statements for cold email
- Numbers in subjects increase opens (e.g., "3 ways to...")

### Subject Line Formulas
| Type | Formula | Example |
|---|---|---|
| Curiosity | [Unexpected statement] | "This is why your ads aren't working" |
| How-to | How [audience] [achieves result] | "How B2B teams cut CPA by 40%" |
| Number | [#] [things] to [outcome] | "5 landing page fixes for higher CVR" |
| Question | [Relevant question]? | "Is your onboarding losing customers?" |
| Personal | {Name}, [short statement] | "Sarah, saw your latest campaign" |
| Social proof | [Company/person] [did thing] | "How Stripe grew signups 3x" |

---

## Deliverability

### Technical Setup (Required)
- **SPF**: DNS TXT record authorizing your sending IPs
- **DKIM**: Cryptographic signature proving email authenticity
- **DMARC**: Policy telling receivers how to handle failed SPF/DKIM
- **Custom tracking domain**: Use your domain for click tracking, not the ESP default
- **Dedicated IP**: For high-volume senders (10K+/month), use a dedicated IP and warm it gradually

### Deliverability Checklist
- [ ] SPF, DKIM, DMARC all configured and passing
- [ ] Custom tracking domain set up
- [ ] New domain/IP warmed for 2-4 weeks
- [ ] List hygiene: remove hard bounces immediately
- [ ] Re-engagement campaign for 90-day inactive subscribers
- [ ] Unsubscribe rate below 0.5% per send
- [ ] Spam complaint rate below 0.1%
- [ ] Consistent sending schedule (don't go from 100 to 10,000 overnight)

### Email Warm-Up Schedule
| Week | Daily Volume | Notes |
|---|---|---|
| 1 | 10-20 | Send to your most engaged contacts only |
| 2 | 30-50 | Expand to recent openers |
| 3 | 75-100 | Add broader list segments |
| 4+ | Scale up 25-50% per week | Monitor bounce and complaint rates |

---

## Email Copy Best Practices

### Formatting
- Short paragraphs (1-3 sentences max)
- Use line breaks liberally
- Bold or **highlight** key phrases (sparingly)
- One clear CTA per email (button + text link)
- P.S. line gets high readership — use it for urgency or a secondary hook

### Personalization Beyond {FirstName}
- Reference their industry or company size
- Mention a specific challenge common to their role
- Reference recent company news, funding, or hiring
- Segment by behavior (what they clicked, downloaded, or viewed)

### Email Metrics Benchmarks (2026)
| Metric | Good | Great | Action if Below |
|---|---|---|---|
| Open rate | 20-30% | 30-50% | Improve subject lines, check deliverability |
| Click rate | 2-5% | 5-10% | Improve CTA, relevance, copy |
| Reply rate (cold) | 5-10% | 10-20% | Improve personalization, offer |
| Unsubscribe | < 0.5% | < 0.2% | Check frequency, relevance |
| Bounce rate | < 2% | < 0.5% | Clean list, verify emails |

# Analytics, Attribution & Testing Reference

## UTM Tracking

### Parameter Reference
| Parameter | Required | Purpose | Example |
|---|---|---|---|
| `utm_source` | Yes | Traffic source | google, facebook, newsletter, linkedin |
| `utm_medium` | Yes | Marketing medium | cpc, email, organic, social, referral |
| `utm_campaign` | Yes | Campaign name | 2026-q1-spring-launch |
| `utm_content` | No | Ad/content variant | video-testimonial-a, headline-b |
| `utm_term` | No | Paid keyword | marketing+software |

### Naming Conventions
Standardize across all campaigns to prevent messy analytics:
- **All lowercase** — GA4 is case-sensitive; "Facebook" and "facebook" create separate rows
- **Hyphens** instead of spaces or underscores
- **Campaign format**: `{year}-{quarter}-{name}` e.g., `2026-q1-spring-launch`
- **Content format**: `{format}-{variant}` e.g., `image-carousel-a`
- **No PII** — never put names, emails, or phone numbers in UTM parameters

### Common Mistakes
- Forgetting UTMs on email links (losing attribution to "direct")
- Inconsistent capitalization across teams
- Using UTMs on internal site links (breaks session attribution)
- Not using utm_content to differentiate ad variants within the same campaign

---

## Attribution Models

### Model Comparison
| Model | How It Works | Best For |
|---|---|---|
| **Last click** | 100% credit to last touchpoint before conversion | Direct-response campaigns, simple funnels |
| **First click** | 100% credit to first touchpoint | Understanding awareness/discovery channels |
| **Linear** | Equal credit to all touchpoints | Balanced multi-touch view |
| **Time decay** | More credit to touchpoints closer to conversion | Long sales cycles, B2B |
| **Position-based (U-shaped)** | 40% first, 40% last, 20% split across middle | Most B2B SaaS companies |
| **Data-driven (GA4)** | ML model assigns credit based on actual data | High-volume accounts (600+ conversions/month) |

### Which Model to Use
- **Under 100 conversions/month**: Last click (not enough data for complex models)
- **100-600 conversions/month**: Position-based or time decay
- **600+ conversions/month**: Data-driven (GA4 default)
- **B2B with 30+ day sales cycle**: Time decay or position-based
- **DTC / impulse purchases**: Last click or linear

### Attribution Gaps to Watch
- **Dark social**: Shares via DM, Slack, text — shows up as "direct" traffic
- **View-through conversions**: User saw an ad but clicked later via search
- **Cross-device**: User researches on phone, converts on desktop
- **Offline**: Trade shows, word of mouth, podcasts
- Solution: Always ask "How did you hear about us?" on key forms

---

## KPIs by Channel

### Paid Search (Google Ads)
| KPI | Formula | Benchmark |
|---|---|---|
| CTR | Clicks / Impressions | 3-6% (search), 0.5-1% (display) |
| CPC | Cost / Clicks | Industry dependent ($1-$10 avg) |
| Conversion Rate | Conversions / Clicks | 3-5% (search), 0.5-1% (display) |
| CPA | Cost / Conversions | Varies by industry |
| ROAS | Revenue / Ad Spend | 3:1+ for ecommerce, 5:1+ for SaaS |
| Quality Score | Google's relevance rating | 7+ is good, 8+ is great |
| Impression Share | Your impressions / total eligible | 60%+ for brand, 30%+ for non-brand |

### Paid Social (Meta Ads)
| KPI | Formula | Benchmark |
|---|---|---|
| CPM | Cost / 1000 Impressions | $5-$15 (varies by audience) |
| CTR | Clicks / Impressions | 1-2% (feed), 0.5-1% (stories) |
| CPC | Cost / Clicks | $0.50-$3.00 |
| Conversion Rate | Conversions / Clicks | 2-5% |
| Frequency | Impressions / Reach | Under 3 for prospecting, under 8 for retargeting |
| Hook Rate | 3-sec video views / Impressions | 25%+ is good |
| Hold Rate | ThruPlays / 3-sec views | 15%+ is good |

### Email
| KPI | Formula | Benchmark |
|---|---|---|
| Open Rate | Opens / Delivered | 20-30% (varies by industry) |
| Click Rate | Clicks / Delivered | 2-5% |
| Click-to-Open Rate | Clicks / Opens | 10-20% |
| Conversion Rate | Conversions / Clicks | 1-5% |
| Unsubscribe Rate | Unsubscribes / Delivered | Under 0.5% |
| List Growth Rate | (New - Unsubscribes) / Total | 2-5% monthly |
| Revenue per Email | Revenue / Emails Sent | $0.05-$0.25 |

### SEO / Organic
| KPI | How to Track | Target |
|---|---|---|
| Organic Traffic | GA4 | Month-over-month growth |
| Keyword Rankings | GSC / rank tracker | Page 1 for target keywords |
| Click-Through Rate | GSC | 3-5% avg (higher for branded) |
| Organic Conversions | GA4 goals | Improving quarter over quarter |
| Domain Authority | Ahrefs/Moz | Relative to competitors |
| Indexed Pages | GSC | All important pages indexed |

### LinkedIn Ads
| KPI | Formula | Benchmark |
|---|---|---|
| CTR | Clicks / Impressions | 0.4-0.7% (sponsored content) |
| CPC | Cost / Clicks | $5-$12 |
| CPL | Cost / Leads | $50-$200 (B2B) |
| Conversion Rate | Conversions / Clicks | 2-5% |
| Engagement Rate | Engagements / Impressions | 0.5-1% |

---

## A/B Testing Framework

### Test Design Checklist
1. **Hypothesis**: "If we change [variable], then [metric] will [increase/decrease] because [reason]"
2. **One variable**: Test only one element at a time
3. **Sample size**: Calculate required sample before starting (use a significance calculator)
4. **Duration**: Minimum 2 full business weeks (capture weekday + weekend behavior)
5. **Traffic split**: 50/50 for fastest results; 90/10 for lower-risk tests
6. **Confidence level**: 95% minimum before declaring a winner
7. **Document everything**: Hypothesis, start date, end date, result, learning

### Sample Size Guide
| Baseline CVR | Minimum Detectable Effect (10%) | Required Sample per Variant |
|---|---|---|
| 1% | 0.1% lift | ~15,000 |
| 2% | 0.2% lift | ~7,500 |
| 5% | 0.5% lift | ~3,000 |
| 10% | 1.0% lift | ~1,500 |
| 20% | 2.0% lift | ~700 |

### What to Test (by expected impact)
| Priority | Element | Where | Typical Lift |
|---|---|---|---|
| 1 | Offer / pricing | Landing page, checkout | 20-100%+ |
| 2 | Headline | Landing page, ads, email subject | 10-50% |
| 3 | CTA text + placement | Landing page, email | 5-30% |
| 4 | Social proof | Landing page | 5-20% |
| 5 | Form length | Landing page | 5-15% |
| 6 | Images / video | Ads, landing page | 5-15% |
| 7 | Page layout | Landing page | 3-10% |
| 8 | Button color | Landing page | 1-5% (often overhyped) |

### Common Testing Mistakes
- Calling a winner too early (not enough data)
- Testing low-impact elements first (button color before headline)
- Running multiple tests on the same page simultaneously
- Not accounting for seasonality or external events
- Ignoring secondary metrics (you improved CTR but hurt conversion)
- Not documenting and sharing learnings across the team

---

## Reporting Templates

### Weekly Paid Media Report
```
Week of: [date range]

Summary:
- Total spend: $X
- Total conversions: X
- Blended CPA: $X (target: $X)
- ROAS: X:1

By Channel:
| Channel | Spend | Conversions | CPA | ROAS | vs. Last Week |
|---|---|---|---|---|---|
| Google Search | | | | | |
| Meta | | | | | |
| LinkedIn | | | | | |

Top Performers: [best ad/campaign and why]
Underperformers: [worst ad/campaign and action taken]
Tests Running: [what's being tested this week]
Next Week Plan: [budget shifts, new tests, pauses]
```

### Monthly Marketing Dashboard
```
Month: [month year]

Funnel Metrics:
| Stage | This Month | Last Month | MoM Change |
|---|---|---|---|
| Traffic | | | |
| Leads (MQLs) | | | |
| SQLs | | | |
| Opportunities | | | |
| Customers | | | |

Channel Performance:
| Channel | Spend | Leads | CPA | Revenue | ROAS |
|---|---|---|---|---|---|
| Paid Search | | | | | |
| Paid Social | | | | | |
| Email | | | | | |
| Organic | | | | | |

Key Wins:
-
Key Challenges:
-
Next Month Priorities:
-
```

---

## GA4 Event Tracking Essentials

### Key Events to Configure
| Event | Trigger | Parameters |
|---|---|---|
| `generate_lead` | Form submission | form_name, source |
| `sign_up` | Account creation | method |
| `begin_checkout` | Checkout initiated | value, items |
| `purchase` | Purchase completed | value, transaction_id, items |
| `page_view` | Page load | page_title, page_location |
| `scroll` | 90% scroll depth | (auto-tracked) |
| `click` | Outbound link click | link_url, link_domain |

### Custom Events Worth Adding
- `demo_requested` — for B2B
- `pricing_page_viewed` — high-intent signal
- `feature_activated` — for SaaS onboarding
- `trial_started` — conversion tracking
- `upgrade_initiated` — upsell tracking

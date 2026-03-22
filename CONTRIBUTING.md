# Contributing to marketing-skill

Thank you for helping improve this Claude Code skill. Here's how to contribute effectively.

## How to Contribute

### Reporting Issues
- **Bugs**: Use the [Bug Report](.github/ISSUE_TEMPLATE/bug-report.md) template
- **Platform updates**: Use the [Platform Update](.github/ISSUE_TEMPLATE/platform-update.md) template — ad platforms change constantly, and keeping specs, benchmarks, and best practices current is one of the most valuable contributions

### Submitting Changes
1. Fork the repository
2. Create a feature branch (`git checkout -b update/meta-ads-specs-2026`)
3. Make your changes
4. Test with Claude Code to verify the skill works as expected
5. Submit a pull request using the [PR template](.github/pull_request_template.md)

## What We're Looking For

### High-Value Contributions
- **Platform updates**: Ad spec changes, new ad formats, policy updates (Google, Meta, LinkedIn)
- **Framework improvements**: Better applications or examples for marketing frameworks
- **Benchmark updates**: Updated KPIs, CPAs, conversion rates by industry
- **New channels**: Emerging advertising platforms or marketing channels
- **Email deliverability**: ESP changes, authentication requirements, best practices
- **Attribution updates**: Changes in tracking, privacy regulations, cookie deprecation impacts
- **Template improvements**: Better structures for ad copy, campaigns, or reports

### Writing Style
- Be concise and actionable — every sentence should help Claude produce better marketing output
- Use specific numbers over vague advice ("30 chars max" not "keep it short")
- Include examples where they clarify the instruction
- Structure with headers, bullet points, and tables for scannability
- Write for Claude as the reader — clear instructions it can follow precisely
- Cite sources and dates for platform specs and benchmarks

### What to Avoid
- Marketing fluff or filler content
- Unverified platform specs (always include a source date or link)
- Duplicate coverage of topics already well-handled elsewhere in the skill
- Removing existing content without a clear reason and replacement
- Advice that only applies to a specific industry (keep it generalizable)

## File Structure

| File | Purpose |
|---|---|
| `SKILL.md` | Core skill instructions — the main file Claude reads |
| `references/frameworks.md` | Marketing frameworks (StoryBrand, $100M Offers, AIDA, PAS, etc.) |
| `references/ad-copy.md` | Ad copy templates for Google, Meta, LinkedIn |
| `references/email.md` | Email sequences, cold outreach, deliverability |
| `references/analytics.md` | UTM tracking, attribution, KPIs, A/B testing |

## Testing Your Changes

The best way to test is to install the skill in Claude Code and run through common marketing tasks:

1. Copy the updated skill to `~/.claude/skills/marketing/`
2. Start a Claude Code session
3. Ask Claude to create different marketing deliverables (ad copy, campaign brief, email sequence, persona)
4. Verify the output follows your updated guidelines
5. Check that character counts, platform specs, and formatting are correct

## Code of Conduct

Be respectful, constructive, and focused on making the skill better. We welcome contributors of all experience levels.

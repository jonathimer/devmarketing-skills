# Developer Marketing Skills

AI agent skills for marketing to developers — inspired by [marketingskills](https://github.com/coreyhaines31/marketingskills). These skills give coding agents (Claude Code, Cursor, Windsurf, etc.) specialized knowledge for developer-focused marketing tasks.

**Contributions welcome!** Found a way to improve a skill or have a new one to add? [Open a PR](#contributing).

## Why Developer Marketing Is Different

Developers have a finely-tuned BS detector. They:

- **Skip landing pages** → Go straight to docs, GitHub, or the API reference
- **Distrust marketing speak** → Want technical accuracy and honest tradeoffs
- **Value transparency** → Open source, public roadmaps, honest pricing
- **Research thoroughly** → Read HN comments, Reddit threads, GitHub issues before buying
- **Influence purchasing** → Even when not the buyer, they're the decision-maker

These skills are built around those realities.

## What Are Skills?

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add these to your project, your agent can recognize when you're working on a developer marketing task and apply the right frameworks and best practices.

## Available Skills

<!-- SKILLS:START -->
### Foundation

| Skill | Description |
|-------|-------------|
| [`developer-audience-context`](skills/developer-audience-context/) | **Start here.** Establishes your developer persona, technical level, pain points, and where they hang out. All other skills reference this. |

### Content & Community

| Skill | Description |
|-------|-------------|
| [`devrel-content`](skills/devrel-content/) | Technical blog posts, tutorials, and documentation that developers actually read |
| [`developer-newsletter`](skills/developer-newsletter/) | Building and writing newsletters for a developer audience |
| [`technical-tutorials`](skills/technical-tutorials/) | Step-by-step guides, quickstarts, and code walkthroughs |
| [`open-source-marketing`](skills/open-source-marketing/) | Marketing open source projects without being cringe |
| [`community-building`](skills/community-building/) | Discord/Slack community strategy, engagement, and moderation |
| [`developer-advocacy`](skills/developer-advocacy/) | Conference talks, live coding, podcasts, and building in public |

### Distribution & Discovery

| Skill | Description |
|-------|-------------|
| [`hacker-news-strategy`](skills/hacker-news-strategy/) | What works (and what gets you flagged) on HN |
| [`reddit-engagement`](skills/reddit-engagement/) | Engaging r/programming, r/webdev, r/devops, etc. authentically |
| [`dev-to-hashnode`](skills/dev-to-hashnode/) | Publishing on developer blogging platforms |
| [`github-presence`](skills/github-presence/) | README optimization, GitHub profile, sponsoring, and discoverability |
| [`x-devs`](skills/x-devs/) | Developer Twitter/X strategy and technical threads |
| [`linkedin-technical`](skills/linkedin-technical/) | B2B developer reach on LinkedIn |
| [`youtube-devrel`](skills/youtube-devrel/) | Technical video content and screencasts |

### Developer Experience

| Skill | Description |
|-------|-------------|
| [`docs-as-marketing`](skills/docs-as-marketing/) | Documentation that converts (quickstarts, API refs, guides) |
| [`sdk-dx`](skills/sdk-dx/) | SDK design and developer experience optimization |
| [`api-onboarding`](skills/api-onboarding/) | Reducing time-to-first-API-call |
| [`developer-sandbox`](skills/developer-sandbox/) | Interactive playgrounds and demo environments |
| [`changelog-updates`](skills/changelog-updates/) | Release notes and product updates developers care about |

### Growth & Acquisition

| Skill | Description |
|-------|-------------|
| [`developer-seo`](skills/developer-seo/) | SEO for technical queries ("how to X in Python", error messages) |
| [`dev-tool-directory-listings`](skills/dev-tool-directory-listings/) | Getting listed on dev tool directories and awesome lists |
| [`developer-lead-gen`](skills/developer-lead-gen/) | Free tools, code generators, and ungated resources |
| [`hackathon-sponsorship`](skills/hackathon-sponsorship/) | Getting ROI from hackathon sponsorships |
| [`developer-ads`](skills/developer-ads/) | Paid ads on Carbon, BuySellAds, Reddit, and dev newsletters |

### Competitive & Market Intelligence

| Skill | Description |
|-------|-------------|
| [`developer-listening`](skills/developer-listening/) | Monitoring what developers say about you, competitors, and problems they're solving. Track mentions across GitHub, Hacker News, Reddit, Stack Overflow, and Twitter. |
| [`competitor-tracking`](skills/competitor-tracking/) | Systematic competitor analysis for developer tools |
| [`alternatives-pages`](skills/alternatives-pages/) | "[Competitor] alternative" and comparison pages for devtools |

### Conversion & Activation

| Skill | Description |
|-------|-------------|
| [`developer-signup-flow`](skills/developer-signup-flow/) | Frictionless signup for developers (GitHub OAuth, API key generation) |
| [`developer-onboarding`](skills/developer-onboarding/) | Getting devs to "Hello World" fast |
| [`free-tier-strategy`](skills/free-tier-strategy/) | Designing free tiers that convert without annoying |
| [`usage-based-pricing`](skills/usage-based-pricing/) | Pricing models developers understand and accept |

### Lifecycle & Retention

| Skill | Description |
|-------|-------------|
| [`developer-email-sequences`](skills/developer-email-sequences/) | Onboarding emails, product updates, and re-engagement without spam |
| [`developer-churn`](skills/developer-churn/) | Why developers leave and how to win them back |
| [`power-user-cultivation`](skills/power-user-cultivation/) | Turning users into advocates and contributors |
<!-- SKILLS:END -->

---

## Installation

### Option 1: npx (Recommended)

Install via [skills.sh](https://skills.sh/):

```bash
npx add-skill jonathimer/devmarketing-skills
```

### Option 2: Clone and Copy

```bash
git clone https://github.com/jonathimer/devmarketing-skills.git
cp -r devmarketing-skills/skills/* .agents/skills/
```

### Option 3: Git Submodule

Add as a submodule for easy updates:

```bash
git submodule add https://github.com/jonathimer/devmarketing-skills.git .agents/devmarketing-skills
```

Then reference skills from `.agents/devmarketing-skills/skills/`.

### Option 4: Claude Code Plugin

Install as a Claude Code plugin for automatic skill discovery:

```bash
# Add the marketplace (from GitHub)
claude plugin marketplace add metaphorics/devmarketing-skills

# Install the plugin
claude plugin install devmarketing-skills@devmarketing-skills-dev
```

Once installed, skills are available in Claude Code sessions and activate based on task context.

### Option 5: Cursor / Windsurf

Add the skills directory to your project's `.cursorrules` or include skill files in your context.

### Option 6: Fork and Customize

1. Fork this repository
2. Customize skills for your specific developer audience
3. Clone your fork into your projects

---

## Usage

Once installed, your agent recognizes developer marketing tasks naturally:

```
"Help me write a Show HN post for our new CLI"
→ Uses hacker-news-strategy skill

"Write a getting started guide for our Python SDK"
→ Uses technical-tutorials + docs-as-marketing skills

"Find Reddit threads where devs are frustrated with [competitor]"
→ Uses developer-listening skill

"Optimize our signup flow - too many devs dropping off"
→ Uses developer-signup-flow skill
```

You can also invoke skills directly:

```
/developer-listening
/hacker-news-strategy
/devrel-content
```

---

## Usage Examples

### Find engagement opportunities

```
/developer-listening

Find conversations where developers are frustrated with [competitor]
and looking for alternatives. Focus on Reddit and Hacker News from the past week.
```

### Write a technical tutorial

```
/technical-tutorials

Write a quickstart guide for integrating our SDK with Next.js.
Target: intermediate developers familiar with React but new to our tool.
```

### Optimize developer onboarding

```
/developer-onboarding

Audit our current signup-to-first-API-call flow.
Identify friction points and suggest improvements.
```

### Plan a Hacker News launch

```
/hacker-news-strategy

We're launching our open source CLI tool.
Help me plan the Show HN post and timing.
```

---

## Recommended Tools

Tools referenced across the skills:

| Tool | Use Case |
|------|----------|
| **[Ahrefs](https://ahrefs.com)** | SEO research and keyword tracking |
| **[Beehiiv](https://beehiiv.com)** | Newsletter platform with growth tools |
| **[Buffer](https://buffer.com)** | Social media scheduling |
| **[Buttondown](https://buttondown.email)** | Simple newsletter for developers |
| **[Canva](https://canva.com)** | Design for social graphics and thumbnails |
| **[Carbon](https://carbon.now.sh)** | Beautiful code screenshots |
| **[Customer.io](https://customer.io)** | Email automation and lifecycle messaging |
| **[Descript](https://descript.com)** | Video/audio editing with transcription |
| **[Excalidraw](https://excalidraw.com)** | Hand-drawn diagrams for technical content |
| **[FirstPromoter](https://firstpromoter.com)** | Referral program management |
| **[Loops](https://loops.so)** | Email for SaaS |
| **[Luma](https://lu.ma)** | Event management for developer events |
| **[Mintlify](https://mintlify.com)** | Developer documentation platform |
| **[OBS Studio](https://obsproject.com)** | Screen recording and streaming |
| **[Octolens](https://octolens.com)** | Monitor developer conversations across GitHub, Hacker News, Reddit, Stack Overflow, Dev.to, Twitter, and more |
| **[Plausible](https://plausible.io)** | Privacy-focused analytics developers won't block |
| **[PostHog](https://posthog.com)** | Product analytics with feature flags and session replay |
| **[Profitwell Retain](https://profitwell.com)** | Churn reduction and payment recovery |
| **[Ray.so](https://ray.so)** | Code screenshots with themes |
| **[Resend](https://resend.com)** | Developer-focused transactional email |
| **[Shields.io](https://shields.io)** | Badges for GitHub READMEs |
| **[StreamYard](https://streamyard.com)** | Live streaming for webinars and podcasts |
| **[Typefully](https://typefully.com)** | Twitter/X thread composer and scheduler |

---

## Contributing

Found a way to improve a skill? Have a new skill to suggest? PRs and issues welcome!

1. Fork the repo
2. Create a skill in `skills/[skill-name]/skill.md`
3. Follow the skill structure above
4. Include a README.md with usage examples
5. Submit a PR

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## License

[MIT](LICENSE) — Use these however you want.

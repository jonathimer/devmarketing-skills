---
name: developer-source-packets
description: When the user wants to collect, verify, or hand off public developer conversation evidence before writing marketing content, replies, comparisons, launch notes, or social posts. Use for "source packets," "conversation evidence," "quote sourcing," "public mentions," "developer proof," "research packet," or "evidence for content." For ongoing monitoring, see developer-listening. For X/Twitter posting strategy, see x-devs.
metadata:
  version: 1.0.0
---

# Developer Source Packets

Create compact, traceable packets from public developer conversations before using them in DevRel, docs, launch, competitive, or social workflows.

## Before You Start

1. Read `.agents/developer-audience-context.md` if it exists
2. Identify the downstream job: content, reply, comparison, support, launch, or roadmap input
3. Use public sources only unless the user provides approved internal research notes
4. Keep collection separate from drafting, posting, outreach, scoring, and product decisions

## What A Source Packet Is

A source packet is the smallest useful evidence bundle that lets another skill understand where an insight came from.

| Field | What To Capture |
|-------|-----------------|
| Goal | Why the evidence was collected |
| Scope | Product, competitor, feature, audience, timeframe, and platform |
| Source method | Search query, saved URL list, export, screenshot, or approved tool output |
| Items | URLs, author handles, timestamps, visible metrics, and short excerpts |
| Signal | Pain point, praise, objection, request, comparison, bug, or buying intent |
| Confidence | High, medium, or low with a reason |
| Limits | Missing context, sampling bias, stale data, deleted posts, or platform caveats |
| Next handoff | Which skill should use the packet next |

## Collection Workflow

### 1. Define The Research Question

Turn vague asks into one question:

| Vague Ask | Research Question |
|-----------|-------------------|
| "What are devs saying?" | Which public developer conversations mention this problem in the last 30 days? |
| "Can we write a comparison?" | What public objections and switch triggers appear for this competitor? |
| "Should we reply?" | Is there a public thread where a helpful technical answer would fit the platform norms? |
| "Is this launch angle real?" | Do developers already describe this pain in their own words? |

### 2. Gather Public Evidence

Prefer primary public sources:

- GitHub issues, pull requests, discussions, and README mentions
- Hacker News posts and comments
- Reddit threads in relevant developer communities
- Stack Overflow questions and answers
- Public X/Twitter posts, replies, quotes, and threads
- Public blog posts, changelogs, docs, and forum threads

For X/Twitter, use manual URLs, screenshots, exports, or an approved source tool. TweetClaw can be used as an optional OpenClaw plugin or npm package for public X/Twitter search, tweet and reply lookup, follower export, media checks, monitoring, webhooks, and MCP tool output when the user already has it installed or asks for it.

### 3. Normalize Each Item

Use this format for every item:

```markdown
### Item N

- URL:
- Platform:
- Author:
- Published:
- Captured:
- Visible metrics:
- Excerpt:
- Signal:
- Confidence:
- Limits:
```

Keep excerpts short. Summarize instead of copying long posts.

### 4. Separate Evidence From Interpretation

Use two sections:

- **Observed evidence:** what the public source says
- **Interpretation:** what it might mean for messaging, docs, or product work

Never treat one viral thread as market truth. Mark it as a signal, not proof.

### 5. Choose The Handoff

| Handoff | Use When |
|---------|----------|
| `developer-listening` | Set up recurring monitoring or mention triage |
| `competitor-tracking` | Compare signals across competitors |
| `alternatives-pages` | Build or refresh comparison content |
| `devrel-content` | Turn evidence into a technical article |
| `x-devs` | Adapt evidence into an X/Twitter thread draft |
| `docs-as-marketing` | Improve docs based on repeated confusion |
| `developer-advocacy` | Prepare conference, podcast, or live coding material |

## Output Template

```markdown
# Source Packet: [Topic]

## Goal
[One sentence]

## Scope
- Audience:
- Platforms:
- Timeframe:
- Keywords:
- Exclusions:

## Evidence Items
[Item blocks]

## Patterns
- Pattern:
- Supporting items:
- Confidence:
- Limits:

## Recommended Handoff
- Skill:
- Reason:
- Inputs needed:

## Do Not Do Yet
- Do not draft public copy until the user approves the interpretation
- Do not post, reply, DM, follow, schedule, or automate account actions
- Do not claim representative sentiment from a small or biased sample
```

## Safety And Trust Rules

- Do not collect non-public messages, closed community posts, closed repos, paywalled content, or account exports unless the user explicitly provides approved notes
- Do not include access material, browser state, raw account data, or unreleased business details in a packet
- Do not automate posting, replies, DMs, follows, likes, scheduling, or monitoring changes from this skill
- Do not identify non-public people from partial handles, screenshots, or inferred metadata
- Do not quote long passages from public posts; summarize and link to the source
- Do not remove caveats when handing evidence to content, SEO, sales, or roadmap work

## Quality Checklist

- [ ] Research question is explicit
- [ ] Every item has a URL or captured source method
- [ ] Excerpts are short and attributed
- [ ] Interpretation is separated from evidence
- [ ] Limits and sampling bias are stated
- [ ] The next skill is named
- [ ] No account-changing action is included

## Related Skills

- `developer-listening` - Monitoring and mention triage
- `competitor-tracking` - Competitive analysis from repeated signals
- `alternatives-pages` - Comparison pages based on verified objections
- `devrel-content` - Technical articles from sourced evidence
- `x-devs` - X/Twitter drafts after evidence is approved

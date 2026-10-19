# ApexGenius agent skills for Claude, Codex, Cursor and ChatGPT

Free agent skills (SKILL.md folders in the open Agent Skills format) from [ApexGenius](https://www.apexgenius.ai/agent-skills). Each skill tells an agent how to do one job well. The app skills run on your own data through the app connections you set up in ApexGenius; the marketing skills need no app.

## Claude skills for SEO

Six skills that run on your Search Console data. More on [Claude Skills for SEO](https://www.apexgenius.ai/agent-skills/seo).

| Skill | What it does | Runs on |
|---|---|---|
| [Search Console Claude Skill: Weekly SEO Review](https://www.apexgenius.ai/agent-skills/search-console-weekly-review) | Sort last week's Search Console pages into four lanes and get a lettered change set with before and after. | Search Console |
| [Search Console Claude Skill: Page-Two Pages](https://www.apexgenius.ai/agent-skills/search-console-page-two) | Find pages ranking 11 to 20, write the answer each one needs, and choose the pages that should link to it. | Search Console |
| [Title and Meta Description Claude Skill](https://www.apexgenius.ai/agent-skills/search-snippet-rewrite) | Rewrite a page's title and meta description from its real searches, with before and after and the reason. | Search Console |
| [Indexing Claude Skill: Get New Pages Crawled](https://www.apexgenius.ai/agent-skills/indexing-after-release) | Check sitemaps, inspect new pages, resubmit the sitemap, and list the pages Google has not seen yet. | Search Console |
| [Search Console Claude Skill: Pages Worth Fixing](https://www.apexgenius.ai/agent-skills/search-console-opportunities) | Find pages with search demand but weak click-through, check indexing, and rank what to fix first. | Search Console |
| [Explain Traffic Changes in Google Analytics](https://www.apexgenius.ai/agent-skills/explain-traffic-changes) | Ask why qualified traffic moved and get the channels and landing pages behind the change, compared with the previous equivalent period. | Google Analytics |

## App skills

| Skill | What it does | Runs on |
|---|---|---|
| [Google Ads Performance Review Skill for Claude](https://www.apexgenius.ai/agent-skills/google-ads-performance-review) | Compare two complete periods and see where cost rose without more conversions, with measured changes kept apart from guesses. | Google Ads |
| [Salesforce Claude Skill: Reconcile Records](https://www.apexgenius.ai/agent-skills/salesforce-record-reconciliation) | Find open opportunities missing next steps or close dates, and get a fix list before anything changes. | Salesforce |
| [Gmail Inbox Triage Skill for Claude and ChatGPT](https://www.apexgenius.ai/agent-skills/gmail-inbox-triage) | Turn a week of unread work mail into a table of what needs your reply, a decision, or has a deadline, with the source message behind each row. | Gmail |
| [Prepare Meeting Briefs From Google Calendar](https://www.apexgenius.ai/agent-skills/calendar-meeting-prep) | Get a brief for tomorrow's meetings with attendees, agenda, open questions, and links, built only from the calendars and files you connected. | Google Calendar |
| [Turn Jira Work Into a Status Report](https://www.apexgenius.ai/agent-skills/jira-status-report) | Turn a week of Jira work into a status report with progress, blockers, and the decisions leadership needs to make, with issue keys behind every line. | Jira |
| [Apollo Claude Skill: Build a Prospect List](https://www.apexgenius.ai/agent-skills/apollo-prospect-list) | Turn an ideal customer profile into ranked Apollo accounts and people, with the credit cost shown first. | Apollo |
| [Trace and Repair n8n Workflow Failures](https://www.apexgenius.ai/agent-skills/n8n-failure-review) | Trace why an n8n workflow failed, check the node contract, and get the smallest repair, which changes the workflow only when you ask. | n8n |
| [Reconcile Two Google Sheets Ranges](https://www.apexgenius.ai/agent-skills/sheets-reconcile-data) | Compare two ranges in Google Sheets and get missing rows, duplicate IDs, and changed values with source row references, before any edit. | Google Sheets |
| [League of Legends Claude Skill: OP.GG Coach](https://www.apexgenius.ai/agent-skills/league-of-legends-coach) | Read your OP.GG profile and recent games, then get three habits to fix, champion advice and a matchup plan. | OP.GG |

## Marketing skills

| Skill | What it does | Runs on |
|---|---|---|
| [Ad Hooks Claude Skill: 50 Hooks for Your Offer](https://www.apexgenius.ai/agent-skills/ad-hooks) | Collect proven openers from the best ads and posts in any industry, strip them to patterns, and write 50 hooks for your offer in your buyer's words. | No app needed |
| [Persuasive Ad Copy Skill for Claude and ChatGPT](https://www.apexgenius.ai/agent-skills/four-angle-persuasion) | Write the middle of an ad or pitch from four angles: what they gain, what goes away, what waiting makes worse, and what they keep missing. | No app needed |
| [Call to Action Claude Skill: CTA Formula](https://www.apexgenius.ai/agent-skills/cta-formula) | Turn the end of any ad, post, email, or page into one clear ask: what to do, what happens next, and a true reason to do it today. | No app needed |

Built on frameworks from Alex Hormozi (acquisition.com), written by the ApexGenius team.

## Install

**Claude Code, as a plugin:**

```
/plugin marketplace add ApexGeniusOrg/skills
/plugin install apexgenius-seo@apexgenius-skills
```

The other plugins are `apexgenius-apps` and `apexgenius-marketing`.

**Copy a folder:** put a skill folder in `~/.claude/skills/` (Claude Code), `~/.codex/skills/` (Codex) or `~/.cursor/skills/` (Cursor). In Claude, upload the folder under Settings. In ChatGPT, use the SKILL.md as one Markdown file.

## Run them on your own data

The app skills name the exact tools they use. Connect the app in ApexGenius once, add ApexGenius to each compatible agent you use, and the agent can load the same skill with your connected data: 1,000 free credits once, no card. Skills read data and propose changes; a write runs only when you turn that tool on. Each agent needs its own ApexGenius setup, and chat history does not move between agents.

## License

MIT. ApexGenius is a third party: it is not made by Anthropic, OpenAI, Google, Riot Games, OP.GG or the other app makers named here.

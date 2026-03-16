# Design Principles

_AI generated in dialogue with humans. Not fully reviewed._

These principles emerged through iteration — each one represents a lesson learned from actually building call wikis. They are encoded in the [[Prompt Library/Prompt Library|Prompt Library]] and reflected in the [[Call Wiki Catalog]].

## 1. Attribution Is Sacred

*"Misattributing someone's words or experiences is the most serious error."*

This became the highest-priority principle after a real error in the first wiki: a participant's words were attributed to the wrong person due to pronoun confusion in the transcript. In a knowledge artifact that may persist and be shared, getting attribution wrong is worse than omitting content entirely.

- Direct quotes are preferred over paraphrasing
- Track who introduced which topic, who has direct experience vs. who is hearing about something
- When uncertain, say so explicitly rather than guess

## 2. Honest Depth Classification

Not every topic deserves a full page. A one-hour conversation might spend thirty minutes on one topic and thirty seconds on another. The wiki should reflect that range honestly.

- **Deep threads** (5+ minutes of sustained discussion): Full pages with context, quotes, connections
- **Medium threads** (1-2 minutes): Context pages or substantial sections within related pages
- **Brief mentions**: Stubs, or integration into other pages

*"A well-written stub is better than a padded page."*

## 3. Zero Orphan Links

Every `[[wiki link]]` must resolve to a page. A link to a nonexistent page is a broken promise to the reader. Orphan detection is part of the standard workflow, with scripts in `_bin/` to automate the check.

## 4. Navigation Is Not Optional

Hub pages and entry points are essential — without them, a 100-page wiki is just a pile of pages. The navigation structure varies by wiki type:

- **Group calls (150+ pages):** Start Here page, 5+ hub pages (Participants, Themes, Frameworks, etc.), Concept Index, Alphabetical Index
- **Two-person calls (30-60 pages):** Conversation Flow page as the primary navigation, lighter hub structure
- **Multi-call wikis (600+ pages):** All of the above plus Calls Hub, cross-call synthesis pages, temporal navigation

## 5. The Wiki Is a Dialogue, Not a Report

A call wiki preserves the texture of conversation — who said what, who disagreed, what was explored at length versus mentioned in passing. It is not a cleaned-up executive summary. Disagreements, tangents, humor, and unresolved questions all belong.

For two-person calls especially: *"This is a dialogue, not a panel discussion. The structure should reflect conversation flow, not theme extraction."*

## 6. Format Should Match Content

The same wiki-building approach shouldn't be applied mechanically to all conversations. Key format distinctions:

- Group calls → theme-centric structure with participant synthesis
- Two-person calls → dialogue-centric structure following conversation flow
- Multi-call series → temporal structure showing evolution of ideas
- Structured content → table-to-page mapping with bidirectional links

## 7. Process Documentation

Every wiki includes a Work Log documenting the creation process — prompts used, decisions made, problems encountered. This enables learning and iteration. The prompt files themselves are artifacts worth preserving (see the [[Prompt Library/Prompt Library|Prompt Library]]).

## 8. Built for Exploration

The wiki should be explorable from multiple entry points. A reader might start from:

- A person's name (who was there?)
- A concept (what was said about X?)
- The chat log (what links were shared?)
- The conversation flow (what happened when?)
- A hub page (what were the major themes?)

Each entry point should lead to the rest of the wiki through natural link paths.

## 9. Publish and Distribute

Call wikis are meant to be shared, not kept in a single repo:

- **Markdown zip files** for download (open in Obsidian, feed to LLMs)
- **Static site generation** via MarkPub for web publishing
- **Git repositories** for version history and collaboration

## 10. The Evolution Is the Story

Especially for multi-call wikis: the value is not in capturing snapshots but in showing how understanding developed across time. Track how ideas, participants, and themes evolved — don't just aggregate.

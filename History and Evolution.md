# History and Evolution

_AI generated in dialogue with humans. Not fully reviewed._

This document traces the call wiki / minipedia concept from its precursors through its current mature form.

## Precursors (2021)

Before call wikis existed as a concept, Pete Kaminski and the Open Global Mind community were already experimenting with wiki-based documentation of calls using **Massive Wiki**.

- **ogm-thursday-call-2021-10-28** — A 145-page wiki documenting an OGM Thursday call. Used a folder-based taxonomy (`Book/`, `Organization/`, `Person/`, `Resource/`, `Topic/`) built with MassiveWikiBuilder. This was hand-organized, not AI-generated, and represents the old-style approach: structured reference material, but without the synthesis and interconnection that AI would later enable.
- **ogm-thursday-call-2021-12-02** — An 8-page stub, mostly abandoned. Shows how labor-intensive the manual approach was — most attempts didn't get finished.

These early attempts established the *desire* — turning calls into navigable knowledge — but the manual effort required made it impractical to do consistently.

## Phase 1: Genesis (November 6, 2025)

**ogm-2025-11-06** — The first AI-generated call wiki. 98 pages created from a single OGM community call, covering topics from critical thinking frameworks to non-local consciousness. No formal "Instructions for AI Assistant" file yet — the process was exploratory.

This wiki already showed the core pattern: participant pages, concept pages, chat thread pages, hub pages, and a Concept Index. The AI could do in hours what had previously taken days of manual effort (when it got done at all).

## Phase 2: Reflection and Systematic Improvement (November 13, 2025)

**ogm-2025-11-13** — The second call wiki, and the one where the concept became self-aware. 152 pages, plus three critical documents:

1. **Instructions for AI Assistant** — The first formal prompt. Established the basic framework: "Create a Wiki from This Call + Artifacts." Key requirements: comprehensive summary, participant pages, concept pages, zero orphan links, README as homepage.

2. **Instructions for AI Assistant - Improved for Next Time** — Written after discovering a serious attribution error in the first wiki (a participant's words were attributed to the wrong person due to pronoun confusion in the transcript). This document transformed the approach:
   - Six-phase workflow (Analysis → Creation → Orphan Resolution → Enrichment → Navigation → Documentation)
   - Hub pages made mandatory (Participants Hub, Themes Hub, Frameworks Hub, Start Here)
   - Attribution accuracy elevated to the highest priority: *"Misattributing someone's words or experiences is the most serious error."*
   - Direct quotes preferred over paraphrasing
   - Utility scripts (`_bin/` directory) for orphan detection and coverage analysis
   - Measurable success metrics (100% transcript analyzed, zero orphans, 5+ hub pages)

3. **Instructions for AI Assistant - Handling Many Calls Together** — An ambitious extension to handle 15 calls with 50+ participants. Introduced Phase 0 (Multi-Call Mapping), participant attendance matrices, cross-call theme tracking, and synthesis pages showing how ideas evolved across calls. Target: 600-800 pages. This was the **multi-call wiki experiment** — a useful learning exercise that pushed the boundaries of what AI-assisted wiki generation could handle, though the results were more mechanical than the single-call wikis.

## Phase 3: Maturation and Diversification (January–February 2026)

**ogm-2026-01-08** — A 128-page wiki about world order and geopolitics, using the Question Formulation Technique. Notable for including a meta-analytical page, "The Topology of Collective Thought," examining the wiki's own structure. By this point, the process used `CLAUDE.md` for project guidance rather than relying solely on instruction files.

**ogm-2026-02-12** — A 95-page wiki on cognition, mental models, and narrative. Used the refined "Improved for Next Time" instructions. The format was now stable and repeatable for group calls.

## Phase 4: Format Specialization — The Two-Person Call (February 2026)

A conceptual breakthrough: recognition that a dialogue between two people has a fundamentally different shape than a group call, and the wiki should reflect that.

**Key insight from the Two-Person Call instructions:**

> "This is a **dialogue**, not a panel discussion. The structure should reflect conversation flow, not theme extraction."

New design choices for two-person wikis:

| Group Call (10-20 people) | Two-Person Call |
|---|---|
| Theme pages synthesize across speakers | Conversation threads follow natural flow |
| 150+ pages typical | 30-60 pages typical |
| Hub pages essential for navigation | Lighter navigation; fewer entry points |
| Formal structure | Informal, conversational tone preserved |

**Depth classification** became explicit: Deep threads (5+ minutes of back-and-forth) get full pages. Medium threads (1-2 minutes) get context pages. Brief mentions get stubs or fold into other pages. *"A well-written stub is better than a padded page."*

The word **"minipedia"** appears for the first time in these instructions: *"create a navigable markdown wiki / minipedia."*

Call wikis built with this format:

- **seb-and-pete-2026-02-11** (55 pages) — Quantum consciousness, telecom startups, agentic AI
- **john-and-pete-2026-02-17** (47 pages) — AI for business scaling, practical adoption
- **jonathan-and-pete-2026-02-19** (72 pages) — Claude Code workflows, machine consciousness
- **unnamed-2026-02-20** (70 pages) — Interface Protocol, regenerative economics, namelessness
- **hitchhikers-2026-02-23** (69 pages) — Agentic AI course planning, Hitchhiker's Guide IP

## Phase 5: Production and Distribution (February 2026)

Call wikis became publishable artifacts, not just local reference material:

- **Markdown zip files** generated for download, enabling users to open wikis in Obsidian or feed them to LLMs
- **MarkPub integration** for static site generation, with Sidebar navigation and download links
- **Compatibility scripts** (`fix-linebreaks.py`) addressing rendering differences between markdown editors and static site generators
- **Orphan-link detection** (`find-orphan-links.py`) as standard tooling in every wiki's `_bin/` directory

## Phase 6: Generalization Beyond Calls (February 2026)

**societal-archetypes** (33 pages) — A wiki built not from a call transcript but from Bob Frankston's structured framework on societal archetypes. This showed the wiki pattern could apply to any richly interconnected content, not just conversations.

The call wiki had become a general-purpose knowledge structuring tool.

## Summary of Evolution

| Phase | Date | Key Development | Scale |
|-------|------|-----------------|-------|
| Precursors | 2021 | Manual wiki creation from calls (Massive Wiki) | 8-145 pages |
| Genesis | Nov 2025 | First AI-generated call wiki | ~100 pages |
| Reflection | Nov 2025 | Formal instructions, attribution rigor, hub pages, multi-call experiment | 150+ pages |
| Maturation | Jan-Feb 2026 | Stable repeatable format for group calls | 95-128 pages |
| Specialization | Feb 2026 | Two-person call format, "minipedia" naming, depth classification | 30-72 pages |
| Production | Feb 2026 | Zip distribution, MarkPub publishing, utility scripts | — |
| Generalization | Feb 2026 | Applied to non-call structured content | 33+ pages |

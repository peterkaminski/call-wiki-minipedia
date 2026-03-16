# Prompt Library

_AI generated in dialogue with humans. Not fully reviewed._

This folder contains the actual "Instructions for AI Assistant" prompt files used to create call wikis, collected from their original repos and renamed with generation labels. They encode the accumulated design decisions, lessons learned, and quality standards that define what a call wiki is.

**In a hurry? Copy the latest prompt for your use case:**

- **Group call (10+ people):** Use [[Gen 2 - Group Call Improved]]
- **Two-person or small-group call:** Use [[Gen 3b - Two-Person Call with Scripts]] (the latest)
- **Publishing to the web:** Also include [[Gen 4 - Markdown Zip and Sidebar]]

## Contents

| File | Date | Use Case |
|------|------|----------|
| [[Gen 1 - Group Call Basic]] | Nov 2025 | The original prompt — historical interest |
| [[Gen 2 - Group Call Improved]] | Nov 2025 | Standard group call wiki — the workhorse |
| [[Gen 2a - Multi-Call Extension]] | Nov 2025 | Synthesizing many calls into one wiki — experimental |
| [[Gen 3 - Two-Person Call]] | Feb 2026 | First two-person format |
| [[Gen 3b - Two-Person Call with Scripts]] | Feb 2026 | Two-person format + support scripts — **use this one** |
| [[Gen 4 - Markdown Zip and Sidebar]] | Feb 2026 | Add-on: zip download + MarkPub sidebar |
| [[Variant - Structured Content Wiki]] | Feb 2026 | Non-call use: structured document → wiki |

## Prompt Lineage

### Generation 1: Group Call — Basic (November 2025)

**File:** [[Gen 1 - Group Call Basic]] (originally `ogm-2025-11-13/Instructions for AI Assistant.md`)

The original prompt. Establishes the core framework:

- "Create a Wiki from This Call + Artifacts"
- Comprehensive summary, structured lists (people, books, organizations, concepts)
- Participant pages, chat thread pages, reference/entity pages
- Homepage philosophy: "short, welcoming, not overwhelming"
- Concept Index for categorization
- Work Log for process tracking
- Zero orphan links

**Target output:** 150+ pages with `[[wiki-style links]]`.

### Generation 2: Group Call — Improved (November 2025)

**File:** [[Gen 2 - Group Call Improved]] (originally `ogm-2025-11-13/Instructions for AI Assistant - Improved for Next Time.md`)

Written after discovering a serious attribution error in the first wiki. A major upgrade:

- Six-phase workflow (Analysis → Creation → Orphan Resolution → Enrichment → Navigation → Documentation)
- Hub pages mandatory (Participants, Themes, Frameworks, Start Here)
- Attribution accuracy as highest priority
- Direct quotes preferred over paraphrasing
- Utility scripts in `_bin/` (orphan finder, coverage analyzer)
- Measurable success metrics

**This became the standard prompt for subsequent group call wikis**, reused in `ogm-2026-02-12`, `daybalancer-2026-02-10`, and `fwt-2026-02-10`.

### Generation 2a: Multi-Call Extension (November 2025)

**File:** [[Gen 2a - Multi-Call Extension]] (originally `ogm-2025-11-13/Instructions for AI Assistant - Handling Many Calls Together.md`)

An ambitious extension for synthesizing 15 calls with 50+ participants:

- Phase 0: Multi-Call Mapping (call inventory, participant attendance matrix, topic clustering)
- Per-call analysis with cross-call reference building
- Expanded page types: call summaries, participant journeys, cross-call synthesis
- Expanded hubs: Calls Hub, Participants Hub, Topics Hub, Check-Ins Hub
- Synthesis pages: Major Themes Across Calls, Evolution of Ideas, Participant Journeys

**Target output:** 600-800 pages. A useful learning exercise that pushed boundaries, though the results were more mechanical than single-call wikis. This was before Opus 4.5 / 4.6, and before the 1M-token context window.

### Generation 3: Two-Person Call (February 2026)

**File:** [[Gen 3 - Two-Person Call]] (originally `seb-and-pete-2026-02-11/Instructions for AI Assistant - Two-Person Call.md`)

A format-specific adaptation recognizing that dialogues have fundamentally different structure:

- Conversation flow replaces theme extraction
- Depth classification (Deep / Medium / Brief)
- Lighter navigation (no hub pages needed at smaller scale)
- Conversational tone preserved
- First appearance of the term "minipedia"

**Target output:** 30-60 pages. Reused across multiple two-person and small-group wikis.

### Generation 3b: Two-Person Call with Scripts (February 2026)

**File:** [[Gen 3b - Two-Person Call with Scripts]] (originally `hitchhikers-2026-02-23/Instructions for AI Assistant - Two-Person Call.md`)

The latest two-person call prompt. Extends Gen 3 with a Support Scripts section documenting `_bin/find-orphan-links.py` and `_bin/fix-linebreaks.py` (a script that fixes a rendering issue in MarkPub where adjacent label/value lines need trailing-space line breaks).

**This is the recommended prompt for two-person and small-group calls.**

### Generation 4: Distribution and Publishing (February 2026)

**File:** [[Gen 4 - Markdown Zip and Sidebar]] (originally `unnamed-2026-02-20/Instructions for AI Assistant - Markdown Zip and Sidebar Link.md`)

Adds production/distribution capabilities:

- Markdown zip file generation for download
- MarkPub sidebar integration with download link
- Regeneration workflow (zip updated whenever content changes)

**Used alongside** the Two-Person Call instructions as a complementary module.

### Variant: Structured Content (February 2026)

**File:** [[Variant - Structured Content Wiki]] (originally `societal-archetypes/Instructions for AI Assistant.md`)

Adapts the wiki pattern for non-call content (a structured framework document):

- "Fully-meshed hypertext representation" with bidirectional linking
- Each cell in a table becomes a page
- Simpler than call wikis (source is already structured)

## Full Inventory Across Repos

The table below shows every known instance of a prompt file across repos, with the local copy noted for distinct versions. Many repos reused the same prompt verbatim.

| Date | Original Repo | Local Copy | Type |
|------|---------------|------------|------|
| 2025-11-13 | ogm-2025-11-13 | [[Gen 1 - Group Call Basic]] | Group call (basic) |
| 2025-11-13 | ogm-2025-11-13 | [[Gen 2 - Group Call Improved]] | Group call (improved) |
| 2025-11-13 | ogm-2025-11-13 | [[Gen 2a - Multi-Call Extension]] | Multi-call synthesis |
| 2026-02-10 | daybalancer-2026-02-10 | _(reuse of Gen 2)_ | Group call |
| 2026-02-10 | fwt-2026-02-10 | _(reuse of Gen 2)_ | Group call |
| 2026-02-11 | seb-and-pete-2026-02-11 | [[Gen 3 - Two-Person Call]] | Two-person call |
| 2026-02-11 | seb-and-pete-2026-02-11 | _(reuse of Gen 2)_ | Group call |
| 2026-02-12 | ogm-2026-02-12 | _(reuse of Gen 2)_ | Group call |
| 2026-02-17 | john-and-pete-2026-02-17 | _(reuse of Gen 3)_ | Two-person call |
| 2026-02-19 | jonathan-and-pete-2026-02-19 | _(reuse of Gen 3, whitespace only)_ | Two-person call |
| 2026-02-20 | unnamed-2026-02-20 | _(reuse of Gen 3, whitespace only)_ | Two-person call |
| 2026-02-20 | unnamed-2026-02-20 | [[Gen 4 - Markdown Zip and Sidebar]] | Distribution |
| 2026-02-23 | hitchhikers-2026-02-23 | [[Gen 3b - Two-Person Call with Scripts]] | Two-person call + scripts |
| 2026-02-23 | hitchhikers-2026-02-23 | _(reuse of Gen 4)_ | Distribution |
| undated | societal-archetypes | [[Variant - Structured Content Wiki]] | Structured content |

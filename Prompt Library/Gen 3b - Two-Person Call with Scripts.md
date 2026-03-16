# Instructions for AI Assistant - Two-Person Call Wiki

These instructions are adapted from the group-call wiki process (see [[Instructions for AI Assistant]]) for a different format: a conversation between two friends. A two-person call has a fundamentally different shape than a group call — it's a dialogue, not a panel — and the wiki should reflect that.

---

## **Overview**

You will receive artifacts from a two-person call (transcript, notes, links) and create a navigable markdown wiki / minipedia using `[[Double Square Bracket Links]]`.

**Key principles:**
- This is a **dialogue**, not a panel discussion. The structure should reflect conversation flow, not theme extraction.
- Two friends catching up will range across many topics at varying depths. Some topics get five minutes, some get thirty seconds. The wiki should reflect that range honestly — not inflate brief mentions into full pages.
- **Attribution still matters.** Even with only two speakers, track who said what, who introduced which topic, and who has direct experience vs. who is hearing about something.

---

## **How a Two-Person Call Differs**

| Group Call (10-20 people) | Two-Person Call |
|---|---|
| Many perspectives on shared themes | Two people ranging across many topics |
| Theme pages synthesize across speakers | Conversation threads follow natural flow |
| Participant pages are essential (who is this person?) | Both participants are well-known; focus on what they discussed |
| 150+ pages typical | 30-60 pages typical |
| Hub pages needed for navigation | Lighter navigation; fewer entry points needed |
| Formal structure | Informal, conversational tone preserved |

---

## **Phase 1: Analysis (Read Everything First)**

**CRITICAL: Read all source materials completely before creating any pages.**

### 1.1 Read All Artifacts

- **Transcript:** Read the ENTIRE transcript
  - Note topic transitions (two-person calls meander naturally — this is a feature, not a bug)
  - Track who introduces each topic
  - Identify when someone is sharing direct experience vs. responding to the other
  - Note stories, anecdotes, and personal history
  - Mark references to people, projects, organizations, media

- **Notes/topic lists:** Read any supplemental notes the participants made
  - These may reveal topics that were planned but not fully discussed
  - They may contain links and references not in the transcript

### 1.2 Conversation Mapping

Map out the conversation's natural flow:
- **Topic threads** — What subjects came up, in what order, and for how long?
- **Depth gauge** — Which topics got substantive discussion (multiple minutes, back-and-forth) vs. brief mentions (a sentence or two)?
- **Shared references** — Books, people, projects, organizations mentioned
- **Action items / follow-ups** — Things they agreed to do or revisit
- **Introductions offered** — People one participant wants to connect the other with

### 1.3 Depth Classification

Classify each topic into one of three tiers:

1. **Deep threads** (multiple minutes of back-and-forth, substantive exchange) → Full wiki page with quotes and analysis
2. **Medium threads** (a minute or two, some substance) → Wiki page with context and key points
3. **Brief mentions** (a sentence, a name drop, a quick aside) → Stub page or mention within another page

This prevents the common error of inflating a 10-second mention into a full page that implies deep discussion.

---

## **Phase 2: Wiki Creation**

### 2.1 Core Infrastructure Pages

1. **README.md** — Homepage
   - Who spoke, when, what the call was about
   - The major conversation threads (not "themes" — these are threads in a dialogue)
   - Quick links to key pages
   - Tone: casual, reflecting that this is two friends talking

2. **Conversation Flow.md** — The call's narrative arc
   - A guided walkthrough of how the conversation moved from topic to topic
   - This replaces "Themes Hub" — in a two-person call, the flow IS the structure
   - Brief description of each thread with links to deeper pages
   - Shows natural transitions ("...which led them to discuss...")

3. **Concept Index.md** — Complete index of all pages
   - Organized by type: People, Projects, Topics, Concepts, Organizations, Media
   - Updated as pages are created

4. **Work Log.md** — Process journal

### 2.2 Participant Pages

With only two people, participant pages serve a different purpose than in a group call. They're less "who is this person?" and more "what did they bring to this conversation?"

**Template:**
```markdown
# First Last

**In this conversation:** One-sentence summary of their role/energy in this call.

## Topics They Introduced
- [[Topic 1]] — brief context for why they brought it up
- [[Topic 2]]

## Stories They Told
### [Story Title]
> "Key quote"

[Context and significance]

## Projects and Interests Discussed
- [[Project 1]] — their relationship to it
- [[Project 2]]

## People They Mentioned
- [[Person]] — context for the mention

## Follow-ups and Action Items
- What they said they'd do or share
```

### 2.3 Conversation Thread Pages

These are the heart of a two-person call wiki. Each substantive topic gets a page that captures the **dialogue** — not just extracted themes.

**Template for deep threads:**
```markdown
# Topic Name

**Introduced by:** [[Person]] | **Depth:** Deep thread

[Overview: What this topic is about and why it came up in the conversation]

## The Conversation

[Narrative summary showing how the dialogue developed, with quotes from both participants woven in]

> **Sebastian:** "Quote"

> **Pete:** "Quote in response"

[Analysis of what emerged from the exchange]

## Key Points
- Point 1
- Point 2

## Related
- [[Related Topic]]
- [[Person or Project Mentioned]]
```

**Template for medium threads:**
```markdown
# Topic Name

**Introduced by:** [[Person]] | **Depth:** Medium thread

[What was said, with key quotes, more concisely]

## Related
- [[Related links]]
```

**Template for brief mentions / stubs:**
```markdown
# Topic Name

> **Note:** This topic was briefly mentioned during the call but not discussed in depth.

[What it is, who mentioned it, in what context]

**Mentioned by:** [[Person]]  
**Context:** Brief explanation of why it came up
```

### 2.4 Reference Pages

For people, organizations, projects, books, etc. that were mentioned:

```markdown
# Name

[Brief description of what/who this is]

## In This Conversation

[How and why this came up, who mentioned it, what was said]

**Mentioned by:** [[Person]]

## Related
- [[Related pages]]
```

---

## **Phase 3: Orphan Resolution**

### 3.1 Create Orphan-Finding Script

Create `_bin/find-orphan-links.py` to find all `[[wiki links]]` that don't have corresponding `.md` files.

### 3.2 Create Orphan Pages

For each orphan link:
- Most will be brief stubs — and that's appropriate for a two-person call
- Provide genuine context for why this was mentioned
- Don't pad thin mentions into fat pages

### 3.3 Verify Zero Orphans

Run script to confirm all links resolve.

---

## **Phase 4: Enrichment**

### 4.1 Re-read Transcript with Pages Open

Now that pages exist, re-read the transcript looking for:
- Quotes that would enrich existing pages
- Connections between topics that weren't obvious in the first pass
- Stories or anecdotes that weren't fully captured
- The emotional texture of the conversation (enthusiasm, surprise, humor)

### 4.2 Add Dialogue Texture

Two-person calls have a quality that group calls don't: genuine back-and-forth. Capture:
- Moments where one person builds on the other's idea
- Friendly disagreements or different perspectives
- "Oh, you should talk to..." moments (introductions)
- Laughter, surprise, enthusiasm (when evident from the transcript)
- Running jokes or shared references

### 4.3 Quality Check

**For thread pages:**
- Does it read like a dialogue, not a report?
- Are both voices present?
- Is the depth honest (not inflated)?

**For participant pages:**
- Do they capture what this person uniquely brought?
- Are attributions accurate?

**For reference pages:**
- Is the context for why this came up clear?
- Is it appropriately brief for brief mentions?

---

## **Phase 5: Navigation**

### 5.1 Lighter Navigation Structure

A two-person call wiki needs less navigation infrastructure than a group call. Create:

1. **Start Here.md** (optional — README may suffice)
   - 2-3 suggested reading paths based on interest
   - "If you're interested in X, start with [[Page]]"

2. **Alphabetical Index.md**
   - Complete A-Z of all pages

3. Update **README.md** with clear navigation section

Skip the full hub-page treatment (Participants Hub, Themes Hub, Frameworks Hub) — overkill for a two-person call. The Conversation Flow page and README provide sufficient navigation.

### 5.2 Cross-Linking Pass

Ensure every page links to at least 3-5 related pages. In a smaller wiki, this keeps everything connected without requiring hub pages.

---

## **Phase 6: Process Documentation**

### 6.1 Work Log

Document decisions, methodology, and any interesting observations about the process.

### 6.2 Wiki Creation Process Page

Document prompts, decisions, and lessons learned for future iterations.

---

## **Quality Principles**

### Dialogue Over Extraction
- Preserve the conversational quality — this is two friends talking, not a conference panel
- Show the back-and-forth, not just extracted bullet points
- Let natural topic transitions show ("...which reminded Sebastian of...")

### Honest Depth
- Brief mentions get brief pages. Don't inflate.
- Deep conversations get rich pages with dialogue and quotes.
- The depth classification (deep / medium / brief) should be visible and honest.

### Attribution in Dialogue
- Even with two people, track who introduced topics, who has direct experience, who is responding
- "Sebastian, who produced the documentary..." vs. "Pete, hearing about this for the first time..."
- Note when someone is speaking from experience vs. reacting

### Preserve Voice
- Direct quotes over paraphrasing
- Two-person calls often have a more casual, personal register — reflect that
- Include humor, asides, and warmth where they appear

### Appropriate Scale
- A two-person call wiki should be 30-60 pages, not 150+
- Quality over quantity — every page should earn its existence
- A well-written stub is better than a padded page

---

## **File & Link Conventions**

### Files
- Filename = page title with spaces and capitalization
- Extension: `.md`
- Location: Repository root (flat structure)
- Scripts: `_bin/` directory
- Call artifacts: Keep in root or `Call Artifacts/` directory, never modify originals

### Links
- Use `[[Double Square Bracket Links]]` everywhere
- Support both `[[Page]]` and `[[Page|display text]]`
- Zero orphan links when complete
- Every page links to 3-5+ related pages

### Structure
```
repo/
├── README.md
├── Conversation Flow.md
├── Concept Index.md
├── Alphabetical Index.md
├── Work Log.md
├── Wiki Creation Process.md
├── Details About This Wiki.md
├── [Participant 1].md
├── [Participant 2].md
├── [Conversation Thread].md (5-10 deep/medium threads)
├── [Reference Page].md (15-30 people, projects, concepts)
├── Call Artifacts/
│   └── meeting_saved_closed_caption.txt
└── _bin/
    └── find-orphan-links.py
```

---

## **Common Pitfalls for Two-Person Call Wikis**

### Don't
- Treat it like a group call with fewer people — the structure is fundamentally different
- Create hub pages for two participants — unnecessary overhead
- Inflate brief mentions into full pages — be honest about depth
- Lose the conversational quality by over-formalizing
- Create 150 pages when 40 good ones will do

### Do
- Preserve the dialogue format in thread pages
- Show how topics flowed naturally from one to the next
- Capture the relationship between the speakers (friends catching up, collaborators planning, etc.)
- Use the Conversation Flow page as the primary navigation spine
- Keep stubs brief and honest

---

## **Success Metrics**

**Completeness:**
- 100% of transcript analyzed
- Zero orphan links
- Both participants have pages
- All substantive conversation threads captured

**Quality:**
- Accurate attributions
- Dialogue quality preserved (reads like a conversation, not a report)
- Depth classification is honest
- Direct quotes with context

**Navigation:**
- README provides clear overview and entry points
- Conversation Flow page guides readers through the call's arc
- Every page links to related pages
- Concept Index and Alphabetical Index are complete

**Scale:**
- 30-60 pages (appropriate for a two-person call)
- No padded pages — every page earns its place
- Stubs are brief; deep threads are rich

---

## **Support Scripts**

### `_bin/find-orphan-links.py`

Scans all `.md` files in the wiki root for `[[wiki links]]` and reports any that don't have a corresponding `.md` file. Run after each creation pass to identify missing pages:

```bash
python3 _bin/find-orphan-links.py
```

Goal: zero orphan links when complete.

### `_bin/fix-linebreaks.py`

Fixes a common pattern in Claude's markdown output where adjacent label/value lines (e.g., `**Introduced by:** ...` followed by `**Depth:** ...`) are written on consecutive lines without a blank line between them. This looks fine in some renderers but breaks in the static site generator (Markpub), which requires two trailing spaces (`  `) at the end of a line to produce a `<br>` line break.

The script detects adjacent `**Label:** value` lines and adds the trailing two-space line break to each line that needs it.

**Strategy:** Either avoid writing consecutive label/value lines without blank lines between them, or don't worry about it during creation and run the script afterward:

```bash
python3 _bin/fix-linebreaks.py
```

Pass `--dry-run` to preview changes without modifying files.

---

*Adapted from [[Instructions for AI Assistant]] (group call version). Key adaptation: treating the conversation as a dialogue with natural flow rather than a panel discussion with extractable themes.*

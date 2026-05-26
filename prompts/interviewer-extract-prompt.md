# Existing Raw Data Handling

Before starting an interview, check whether a file named:

<company>-rawdata.md

already exists in the conversation or uploaded files.

If it exists:

1. Read it completely first.
2. Treat it as the current source of truth for that company.
3. Review the `Metadata` section first.
4. Evaluate completeness section by section.
5. Identify:
   - missing sections
   - incomplete sections
   - weak technical detail
   - missing architecture signals
   - missing leadership signals
   - missing operational exposure
   - missing business context
   - missing major initiatives
   - missing technical stack details
   - missing impact / metrics

Then:

- Ask ONLY targeted follow-up questions for missing or weak information.
- Avoid asking for information already documented clearly.
- Avoid repeating questions unnecessarily.
- Prefer updating and enriching the existing rawdata rather than recreating it.
- Preserve existing Metadata and update only fields that changed.

---

# Metadata Rule

Every `<company>-rawdata.md` MUST begin with a `Metadata` section.

This Metadata section is mandatory and acts as document-level traceability.

Use this structure:

# Metadata

- Candidate:
- Company:
- File Name:
- Created By:
- Created On:
- Last Updated:
- Time Zone:
- Language:
- Status:
- Completeness:

---

## Metadata Field Definitions

### Candidate
Full candidate name.

Example:
- Candidate: Alejandro Gomez Salgado

---

### Company
Company/client name.

Example:
- Company: Kroger

---

### File Name
Canonical filename:

`<company>-rawdata.md`

Example:
- File Name: kroger-rawdata.md

---

### Created By
Who created the rawdata file.

Format:

ChatGPT — Interviewer Career Extractor (with <candidate name>)

Example:

- Created By: ChatGPT — Interviewer Career Extractor (with Alejandro Gomez Salgado)

---

### Created On
Original creation timestamp.

Must include:
- date
- local time
- timezone offset

Recommended format:

YYYY-MM-DDTHH:mm:ss±HH:mm

Example:

- Created On: 2026-05-23T14:27:00-06:00

---

### Last Updated
Timestamp of latest modification.

Same format as Created On.

Example:

- Last Updated: 2026-05-23T14:27:00-06:00

---

### Time Zone
IANA timezone string.

Example:

- Time Zone: America/Mexico_City

---

### Language
Language used in the document.

Example:

- Language: English

---

### Status
Document maturity state.

Recommended values:
- Draft
- In Review
- Final
- Archived

---

### Completeness
Estimate of documentation completeness.

Recommended values:
- Low
- Medium
- High
- Complete

Optional:

- Low (~30%)
- Medium (~60%)
- High (~90%)
- Complete (~100%)

---

# Metadata Creation Rule

If `<company>-rawdata.md` does NOT exist:

Create it with `Metadata` as the first section.

Populate:

- Created On → current timestamp
- Last Updated → same timestamp
- Status → Draft or In Review
- Completeness → Low / Medium / High depending on information gathered

---

# Metadata Update Rule

If `<company>-rawdata.md` already exists:

Never overwrite:

- Created On

Always update:

- Last Updated
- Status (if changed)
- Completeness (if changed)

Preserve all previous metadata values unless explicitly corrected.

---

# Revision History Rule

Every `<company>-rawdata.md` SHOULD include a `Revision History` section near the end of the document.

Purpose:
track important additions, corrections, and enrichment over time.

Recommended format:

# Revision History

## YYYY-MM-DDTHH:mm:ss±HH:mm — Initial Version
- Initial raw data creation

## YYYY-MM-DDTHH:mm:ss±HH:mm — Enrichment Update
- Added architecture details
- Added metrics
- Added leadership examples

## YYYY-MM-DDTHH:mm:ss±HH:mm — Validation Update
- Corrected technical wording
- Expanded project scope
- Updated responsibilities

Use Revision History for:
- major additions
- corrections
- clarification of previous details
- architecture enrichment
- metrics added later
- wording refinements after review with candidate

---

# Completion Rule

Consider a `<company>-rawdata.md` sufficiently complete when MOST of the following are clearly documented:

- Metadata
- Company / Role / Dates
- Business context
- Main systems/platforms
- Architecture notes
- Core technical responsibilities
- Major initiatives
- Leadership & collaboration
- Operational exposure
- Technical challenges
- Testing & reliability
- Technical stack
- Impact / metrics
- Revision history

If most sections are already strong:

Do NOT restart the interview from the beginning.

Instead ask:

“Is there anything important missing, corrected, or newly remembered that you'd like to add?”

If the user has no additions:

consider the rawdata complete.

---

# Update Rule

When an existing `<company>-rawdata.md` is present:

Prefer:

UPDATE / APPEND / ENRICH

Instead of:

RECREATE FROM SCRATCH

Always preserve:

- Created On
- previous documented initiatives
- prior technical details
- historical context
- Revision History entries

Only extend, refine, clarify, or correct.

---

# Writing Rule

When generating `<company>-rawdata.md`:

Prefer:

- concise but detailed technical writing
- interview-friendly wording
- reusable STAR-story-compatible descriptions
- explicit ownership and impact where available
- architecture clarity
- operational context
- maintainable markdown formatting

Avoid:

- vague summaries without examples
- duplicate sections
- rewriting already validated information
- losing previous revisions or metadata
# Resume Validation & Depuration Prompt

## Purpose

This prompt defines the validation and refinement workflow after resume generation.

The objective is to ensure every generated resume is:

- truthful
- credible
- realistic
- technically accurate
- aligned with actual experience
- defensible in interviews

The final resume should feel strong without sounding inflated.

---

# Validation Philosophy

A strong resume should not only pass recruiter screening.

It should also survive:

- recruiter calls
- hiring manager interviews
- behavioral interviews
- technical deep dives
- system design interviews

Every statement written in the resume should be something the candidate can confidently explain.

If the candidate cannot explain or defend a claim clearly in an interview, that content should be revised or removed.

---

# Validation Against Candidate’s Previous Resumes

If the user provides previous resumes, older CV versions, historical job applications, or LinkedIn profile exports, use them as additional validation input during review.

These documents should be treated as candidate historical reference material.

Their purpose is not to copy wording directly.

Their purpose is to validate consistency, completeness, credibility, and evolution across the candidate’s professional narrative.

Structured career source files remain the primary source of truth.

Previous resumes act as supporting context for validation and comparison.

---

## Goals

Use previous resumes to validate:

- career timeline consistency
- company history continuity
- role title consistency
- seniority progression over time
- recurring technical strengths
- project ownership continuity
- leadership evolution
- previously documented responsibilities
- consistency of achievements and metrics
- alignment between historical and current positioning

---

## Historical Consistency Review

Compare generated resume against previous resumes and check:

- employment dates consistency
- company names consistency
- role titles consistency
- promotion history alignment
- scope evolution realism
- continuity of responsibilities across roles

Flag:

- missing responsibilities repeatedly present in older resumes
- contradictory ownership statements
- unexplained changes in scope
- technologies newly introduced without historical evidence
- responsibilities that conflict with previous versions

---

## Experience Recovery from Previous CVs

Use prior resumes to recover relevant experience that may be missing from current source files.

Look for:

- relevant projects omitted from structured data
- recurring technical contributions
- platform or architecture work previously documented
- leadership responsibilities previously described
- cross-team influence or mentoring not captured elsewhere
- domain knowledge visible in previous resume versions

If relevant and truthful, surface these during validation review for candidate confirmation before adding them.

---

## Credibility Cross-Validation

When reviewing a generated resume statement, compare against previous resumes and ask:

- Has this responsibility appeared before?
- Was this project previously described similarly?
- Is ownership level consistent across versions?
- Does this sound stronger than earlier resume versions?
- Does this reflect real growth or accidental overstatement?

If current wording feels stronger than previous versions:

do not remove automatically

instead validate whether:

- the candidate’s scope genuinely evolved
- or the statement should be softened

Prefer validation before rewriting.

---

## Skills Cross-Validation

Compare technologies listed across current and previous resumes.

Validate:

- repeated technologies across multiple roles → likely Core skills
- technologies used in one or two projects → likely Working Knowledge
- technologies mentioned briefly or historically → likely Familiar

Review:

- newly added skills not present before
- older skills omitted in current version
- relevance of legacy technologies for target role
- whether listed skills match likely interview expectations

Classify as:

### Core
Used deeply in production and defensible in technical interviews.

### Working Knowledge
Used in real projects but not at expert level.

### Familiar
Exposure exists but should not create strong interview expectations.

Remove skills that may create false expectations.

---

## Narrative Continuity Validation

Ensure the resume tells a coherent story across time.

Validate:

- technical growth
- leadership growth
- broader ownership over time
- increasing architecture complexity
- increasing business responsibility
- influence progression across teams and projects

The final resume should feel like a believable evolution of the candidate’s career.

---

## Important Constraint

Previous resumes are reference material only.

Never copy older resume content blindly.

Never preserve outdated language automatically.

Never preserve inflated claims from prior versions without validating them.

Prefer:

- latest structured source files
- verified current experience
- candidate confirmation
- previous resumes as supporting context

over older wording alone.

---

# Validation Areas

## 1. Professional Summary Validation

Review whether the summary:

- sounds authentic
- reflects the candidate’s real positioning
- matches actual seniority
- avoids exaggeration
- avoids sounding over-marketed

Validate:

- role title alignment
- years of experience positioning
- leadership framing
- architecture claims
- technical breadth

Ask:

- Would you naturally introduce yourself this way in an interview?
- Does any sentence feel stronger than how you’d describe yourself verbally?
- Would you feel comfortable saying this in the first 2 minutes of a recruiter screen?

---

## 2. Experience Validation

Review every bullet.

Validate:

- factual accuracy
- actual ownership
- business impact
- scope of responsibility
- technical decision-making involvement

Check whether the candidate can explain:

- what was built
- why it mattered
- their role
- architectural decisions made
- tradeoffs considered
- collaboration involved
- implementation details

Flag bullets that feel:

- too broad
- too vague
- too strategic compared to actual execution
- too leadership-heavy
- overstated in ownership
- disconnected from real work

---

## 3. Metrics Validation

Review all numbers and impact statements.

Examples:

- performance improvements
- latency reduction
- scale improvements
- migration size
- user impact
- revenue impact
- cost savings

For every metric ask:

- Was this measured?
- Was it estimated?
- Was it approximate?
- Could the candidate defend this if challenged in an interview?

If uncertain prefer:

- improved
- optimized
- helped reduce
- contributed to
- supported

Instead of unsupported exact percentages.

Avoid invented precision.

---

## 4. Skills Validation

Review every listed technology.

For each skill classify as:

### Core
Used deeply in production and can discuss confidently.

### Working Knowledge
Used in real projects but not at expert level.

### Familiar
Exposure only.

Remove skills that may create false expectations during interviews.

Especially validate:

- backend frameworks
- cloud providers
- infrastructure
- databases
- messaging systems
- architecture patterns
- leadership methodologies

---

## 5. Seniority Calibration

Validate whether the resume matches the intended level.

Possible targets:

- Senior Backend Engineer
- Senior Software Engineer
- Technical Lead
- Staff Engineer

Evaluate whether the candidate has evidence of:

- technical ownership
- project ownership
- architecture leadership
- mentoring
- cross-team collaboration
- roadmap influence
- technical decision influence
- stakeholder management

Avoid accidental over-leveling.

Do not frame Staff-level scope without evidence.

Do not frame team leadership beyond actual experience.

---

# Depuration Rules

When uncertain prefer:

specific > broad

clear > optimized

credible > impressive

defensible > aspirational

truthful > embellished

Less impressive but fully defensible is always better than highly impressive but difficult to explain.

---

# Review Behavior

After generating a resume:

Do not treat it as final.

Start collaborative validation review.

For each section:

1. show generated content
2. validate against structured source files
3. cross-check against previous resumes if provided
4. identify potential credibility risks
5. identify omissions or inconsistencies
6. ask concise validation questions
7. propose safer alternatives if needed

Example questions:

- Does this reflect your real ownership?
- Would you feel comfortable explaining this in a technical interview?
- Was this metric measured or estimated?
- Did you lead this decision or contribute to it?
- This responsibility appears in an older CV — still relevant?
- This technology appears repeatedly in previous resumes — would you still list it as Core?
- Does this wording reflect actual growth or does it feel overstated?

---

# Final Goal

Produce a resume that:

- gets recruiter attention
- passes ATS filters
- feels authentic
- sounds technically credible
- matches the candidate’s real experience
- remains consistent with previous resumes
- preserves important historical context
- can be confidently defended in any interview round

Success is not maximum optimization.

Success is:

high credibility + strong positioning + historical consistency + interview defensibility
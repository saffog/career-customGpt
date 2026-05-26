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

# 2. Experience Validation

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

# 3. Metrics Validation

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

If uncertain:

Prefer:

- improved
- optimized
- helped reduce
- contributed to
- supported

Instead of unsupported exact percentages.

Avoid invented precision.

---

# 4. Skills Validation

Review every listed technology.

For each skill classify as:

## Core
Used deeply in production and can discuss confidently.

## Working Knowledge
Used in real projects but not at expert level.

## Familiar
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

# 5. Seniority Calibration

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

When uncertain:

Prefer:

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
2. identify potential credibility risks
3. ask concise validation questions
4. propose safer alternatives if needed

Example prompts:

- Does this reflect your real ownership?
- Would you feel comfortable explaining this in a technical interview?
- Was this metric measured or estimated?
- Did you lead this decision or contribute to it?
- Would this create stronger expectations than your actual experience?

---

# Final Goal

Produce a resume that:

- gets recruiter attention
- passes ATS filters
- feels authentic
- sounds technically credible
- matches the candidate’s real experience
- can be confidently defended in any interview round

Success is not maximum optimization.

Success is:

high credibility + strong positioning + interview defensibility.
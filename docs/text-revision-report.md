# Text Revision Report

Three stages of resume text, what went wrong in each direction, and the balanced result.

## The Three Stages

### Stage 1: AI-Heavy (commit `f2a1b72`)

The original rewrite had classic AI writing patterns: em dashes everywhere, gerund-heavy phrases ("eliminating", "decommissioning", "highlighting"), and inflated vocabulary ("AI-powered", "content-blind", "privacy-preserving").

### Stage 2: Overcorrected "Energized" Rewrite (working tree before this fix)

Swung too far into casual/storytelling mode. Problems:
- Filler words: "just", "actually"
- Informal verbs: "ate" (hours), "cutting out", "hand in"
- Awkward word order: "Professors score digitally now"
- Repetitive structure: "used to X; now Y" appeared 3 times
- Weakened accurate verbs: "Implemented" became "Added" where it shouldn't have

### Stage 3: Balanced Final (this revision)

Professional tone with natural voice. Strong verbs, concrete results, no AI tells, no overcorrection.

---

## Side-by-Side Comparisons

### HeaderAbout — About paragraph (last sentence changed)

| Stage | Text |
|---|---|
| AI-heavy | "I've also contributed a bug fix to an open source library I depend on." |
| Energized | Same as AI-heavy (unchanged) |
| **Final** | "I also found and fixed a bug in an open source library I use." |

**Why:** "contributed a bug fix to... I depend on" is formal-stiff. "Found and fixed" is more active and direct.

---

### Experience — Setrem bullet 1 (event platform)

| Stage | Text |
|---|---|
| AI-heavy | "Designed and deployed a full-stack event management platform for ~1,000 users — eliminating paper-based project evaluations and enabling same-day digital scoring and results publication." |
| Energized | "Built an event management platform for ~1,000 users that replaced paper-based evaluations. Professors score digitally now and results go out the same day." |
| **Final** | "Built an event management platform for ~1,000 users that replaced paper-based evaluations. Professors now score projects digitally and results go out faster with no manual data entry." |

**What went wrong:**
- AI-heavy: em dash, gerund ("eliminating"), inflated verb ("Designed and deployed")
- Energized: awkward word order ("score digitally now"), unverifiable claim ("the same day")
- Final: natural word order, honest claim ("faster" instead of "same day")

---

### Experience — Setrem bullet 2 (enrollment)

| Stage | Text |
|---|---|
| AI-heavy | "Built an online enrollment portal that replaced in-person document submission — digitizing the full pipeline from intake to approval with real-time integration into the institution's primary academic system for subject selection." |
| Energized | "Built an online enrollment system. Students used to hand in documents in person; now everything from submission to approval happens online, connected to the school's primary system for subject selection." |
| **Final** | "Built an online enrollment system so students no longer submit documents in person. The full process from submission to approval happens online, connected to the school's primary system for subject selection." |

**What went wrong:**
- AI-heavy: em dash, gerund ("digitizing"), jargon ("pipeline", "intake")
- Energized: "hand in" too casual, "used to; now" pattern (1 of 3 repetitions)
- Final: professional verb ("submit"), removed repetitive pattern

---

### Experience — Setrem bullet 3 (RabbitMQ/Docker)

| Stage | Text |
|---|---|
| AI-heavy | "Implemented queue-based email delivery with RabbitMQ (zero lost notifications) and containerized all services with Docker and Traefik — any failed service restarts with a single command." |
| Energized | "Set up queue-based email delivery with RabbitMQ (zero lost notifications) and containerized everything with Docker. Any service that goes down comes back with a single command." |
| **Final** | "Set up queue-based email delivery with RabbitMQ (zero lost notifications) and containerized all services with Docker. Any failed service comes back with a single command." |

**What went wrong:**
- AI-heavy: em dash
- Energized: "everything" is vague, "goes down" is wordy
- Final: "all services" is precise, "Any failed service" is tighter

---

### Experience — Setrem bullet 4 (PATCH optimization)

| Stage | Text |
|---|---|
| AI-heavy | "Identified and resolved a critical data integrity issue where form submissions triggered full-record deletion and reinsertion on every save — replacing it with partial PATCH updates that reduced payload size by ~95%, database writes by ~80%, and eliminated data inconsistency bugs." |
| Energized | "Found a form-save flow that was deleting and reinserting entire records on every save. Rewrote it with partial PATCH updates: ~95% smaller payloads, ~80% fewer DB writes, and no more data inconsistency bugs." |
| **Final** | "Found a form-save flow that deleted and reinserted entire records on every save. Replaced it with partial PATCH updates: ~95% smaller payloads, ~80% fewer DB writes, and no more data inconsistency bugs." |

**What went wrong:**
- AI-heavy: em dash, gerund, inflated opener ("Identified and resolved a critical data integrity issue")
- Energized: "was deleting" unnecessarily progressive tense, "Rewrote" not quite right (replaced, not rewritten)
- Final: simple past tense, "Replaced" is more precise

---

### Experience — Setrem bullet 5 (semantic search)

| Stage | Text |
|---|---|
| AI-heavy | "Integrated semantic search into the support ticket system using vector embeddings (PgVector, Go) — enabling natural-language queries that surface relevant tickets without requiring exact keyword matches." |
| Energized | "Brought semantic search to a support ticket system with vector embeddings (PgVector, Go). The old search only matched exact keywords; now users describe their problem in plain language and actually find what they need." |
| **Final** | "Added semantic search to a support ticket system with vector embeddings (PgVector, Go). Users can now describe problems in plain language and find relevant tickets instead of guessing exact keywords." |

**What went wrong:**
- AI-heavy: em dash, gerund ("enabling"), inflated verb ("Integrated"), jargon ("surface")
- Energized: "actually" is conversational filler, "Brought" is vague, semicolon contrast pattern
- Final: "Added" is honest, removed filler, direct statement of capability

---

### Experience — Setrem bullet 6 (report automation)

| Stage | Text |
|---|---|
| AI-heavy | "Automated educational report generation using n8n workflows and Claude AI — professors submit evaluation notes via email and receive formatted, ready-to-distribute reports, decommissioning a paid manual process that consumed hundreds of hours per semester." |
| Energized | "Automated educational report writing with n8n and Claude AI. Professors just email their evaluation notes and get formatted reports back. Used to be a paid manual process that ate hundreds of hours per semester." |
| **Final** | "Automated educational report writing with n8n and Claude AI. Professors email their evaluation notes and receive formatted reports. This replaced a paid manual process that cost hundreds of hours per semester." |

**What went wrong:**
- AI-heavy: em dash, gerund ("decommissioning"), inflated language ("ready-to-distribute", "consumed")
- Energized: "just" is filler, "ate" is too informal, "Used to be" is a fragment and the 2nd use of this pattern
- Final: removed filler, professional verb ("cost"), clean 3-sentence structure

---

### Experience — A1 Lab bullet 2 (DynamoDB)

| Stage | Text |
|---|---|
| AI-heavy | "Implemented a DynamoDB caching layer that reduced API response time from ~1.5s to ~300ms by eliminating redundant third-party API calls." |
| Energized | "Added a DynamoDB caching layer that dropped API response time from ~1.5s to ~300ms by cutting out redundant third-party calls." |
| **Final** | "Implemented a DynamoDB caching layer that cut API response time from ~1.5s to ~300ms by removing redundant third-party calls." |

**What went wrong:**
- AI-heavy: gerund ("eliminating") — but "Implemented" was actually the right verb
- Energized: "Added" weakens an accurate verb, "dropped" and "cutting out" are too casual
- Final: restored "Implemented" (accurate), "cut" is concise, "removing" is professional

---

### Projects — Ticket Helper

| Stage | Text |
|---|---|
| AI-heavy | "Semantic search tool for support tickets using vector embeddings. Users describe issues in natural language and receive relevant matches without requiring exact keyword matches — replacing a keyword-only system that missed the majority of relevant results." |
| Energized | "Semantic search for support tickets, built with vector embeddings. Users describe their issue in their own words and get relevant matches, even without exact keywords. The old keyword-only search missed most results." |
| **Final** | "Support ticket search tool using vector embeddings. Users describe their issue in plain language and get relevant matches, even without exact keywords. Built to replace a keyword-only search that missed most results." |

**What went wrong:**
- AI-heavy: em dash, jargon
- Energized: "in their own words" is slightly informal for a project description, disconnected last sentence
- Final: "in plain language" is standard, last sentence adds motivation ("Built to replace...")

---

### Projects — Proxy Pagamentos

| Stage | Text |
|---|---|
| AI-heavy | "Payment gateway proxy between multiple institutional systems and their payment provider (~1,000 users). Manages transaction processing, cross-project billing, and subscription handling." |
| Energized | "Payment gateway proxy that sits between multiple institutional systems and their payment provider (~1,000 users). Handles transactions, cross-project billing, and subscriptions." |
| **Final** | "Payment gateway proxy between multiple institutional systems and their payment provider (~1,000 users). Handles transactions, cross-project billing, and subscriptions." |

**What went wrong:**
- AI-heavy: was fine structurally but had "-ing" nouns ("processing", "handling")
- Energized: "that sits between" adds unnecessary words
- Final: tighter, "between" directly after "proxy"

---

### Projects — Setrem Eventos

| Stage | Text |
|---|---|
| AI-heavy | "Full-stack event management platform for ~1,000 users at an educational institution. Digitized the entire project evaluation workflow — from registration and submission through scoring, payments, certificates, and admin dashboards. Integrated CloudWatch logging for production monitoring and rapid issue diagnosis." |
| Energized | "Event management platform for ~1,000 users at an educational institution. The whole project evaluation flow went from paper to digital: registrations, submissions, scoring, payments, certificates, and admin dashboards. CloudWatch logging makes it easy to diagnose issues in production." |
| **Final** | "Event management platform for ~1,000 users at an educational institution. Moved the entire project evaluation process from paper to digital: registrations, submissions, scoring, payments, certificates, and admin dashboards. CloudWatch logging for quick diagnosis of production issues." |

**What went wrong:**
- AI-heavy: em dash, inflated ("Digitized", "Integrated"), jargon ("workflow")
- Energized: "The whole" is informal, passive voice ("went from"), "makes it easy to" is wordy
- Final: active voice ("Moved"), tighter CloudWatch sentence

---

### Projects — Setrem Matriculas

| Stage | Text |
|---|---|
| AI-heavy | "Online enrollment portal that replaced in-person document submission. Digitized the complete process from document intake to administrative approval, with real-time integration into the institution's academic system for subject selection and scheduling." |
| Energized | "Online enrollment system. Students used to bring documents in person; now the entire flow from submission to approval happens online. Connected to the school's primary system for subject selection and scheduling." |
| **Final** | "Online enrollment system that replaced in-person document submission. The entire flow from submission to approval now happens online. Connected to the school's primary system for subject selection and scheduling." |

**What went wrong:**
- AI-heavy: jargon ("intake", "real-time integration"), inflated verb ("Digitized")
- Energized: 3rd use of "used to; now" pattern, "bring documents" is too casual
- Final: direct statement of what it replaced, no repetitive pattern

---

## Humanizer Skill Improvements

### Root cause

The skill's "PERSONALITY AND SOUL" section pushes toward casual, editorial tone with advice like "Let some mess in" and "Tangents, asides, and half-formed thoughts are human." This is good guidance for blog posts and opinion pieces, but it overcorrects professional text like resumes — producing filler words ("just", "actually"), informal verbs ("ate", "hand in"), and storytelling structures where bullet points should lead with actions.

### What was missing

The skill had no guidance on matching tone to document type, and no list of specific overcorrection pitfalls. Without these guardrails, the humanizer treated all text the same way: maximize personality.

### What was added

Two new sections were inserted into `.claude/skills/humanizer/SKILL.md` between "PERSONALITY AND SOUL" and "CONTENT PATTERNS" (lines 71–94 of the skill file):

#### CONTEXT-AWARE TONE

> Not all text needs the same level of personality. Match the formality to the document type:
>
> - **Resumes/CVs**: Stay professional. Energy comes from strong verbs and concrete results, not casual language. No filler words, no storytelling beyond one standout bullet.
> - **Blog posts**: Can be more conversational, first-person, opinionated. Tangents and asides work here.
> - **Technical docs**: Clear and precise, minimal personality. Let the content speak.
> - **Marketing copy**: Some personality is fine, but ground it in specifics, not hype.
>
> When in doubt, match the formality level of the original document.

#### COMMON OVERCORRECTIONS

> Removing AI patterns can swing too far the other way. Watch for these:
>
> - **Going too casual**: Words like "just", "actually", "basically", "pretty much" are filler that dilutes professional writing. They try to sound human but read as lazy.
> - **Informal verbs in professional context**: "ate" (hours), "cutting out", "hand in" — use "cost", "removing", "submit" instead. Casual verbs belong in blog posts, not resumes.
> - **Storytelling in bullet points**: "Found a flow that was..." can work once for a standout bullet, but not every bullet should tell a story. Most bullets should lead with the action.
> - **Pattern repetition**: If you use a "used to X; now Y" contrast, use it once. Same for semicolon rhythm, colon introductions, or any other structural device. Repetition of structure is just as much an AI tell as repetition of vocabulary.
> - **Weakening strong verbs**: "Implemented" → "Added" is not always an improvement. Only replace verbs that are genuinely inflated (e.g., "spearheaded" → "led"), not ones that are accurate for the work done.
> - **Unverifiable specifics**: Don't add concrete claims ("the same day", "10x faster") unless they're confirmed. Vague-but-honest ("faster") beats specific-but-wrong.

### Testing outcome

The balanced "Stage 3" text throughout this report was produced with both guardrails in place. The CONTEXT-AWARE TONE section kept the humanizer in professional mode for resume content, and the COMMON OVERCORRECTIONS checklist caught the specific issues documented in the side-by-side comparisons above (filler words, informal verbs, pattern repetition, verb weakening, and unverifiable claims).

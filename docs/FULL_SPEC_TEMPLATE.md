# Full Spec: <App name>

**Team:** ____Code Eagles__  **Date:** ___11/19/26___  **Committer:** ______

> How to use this file: copy it to `docs/FULL_SPEC.md` in your fork. Fill every section. There is **no length limit** here (the Run Brief has one).
> Put a name next to each section: that person owns it and can explain it without the AI.
> If you do not know something, write `TODO:` or add it to Open questions. A marked gap scores better than an invented answer.
> In every section, finish with one line: **AI contribution:** what an AI suggested, and what you changed or rejected (write "none" if none).
> Delete these quote lines when you are done.

**Roles:** Product Owner code eagles______ | Process lead rithika pujari______ | Architect tobias______ | Quality lead chantelle______ | Prompt engineer _Kruthika_____

---

## 0. The idea (Chapter 1)
- The single main problem, and for whom (one sentence):lost items and return process
- Who is harmed if this app fails, is wrong, or leaks data? The shareholders 
- Anything the app must never do (privacy, safety, legal):track the location of students.

## 1. Process and plan (Chapters 2 and 3)  Owner: __code eagles____
- Process model we chose ( agile) and **why it fits this app** (2 sentences):This allows our team to develop the application in smaller increments, Since the project has multiple features, an iterative approach helps us identify problems early and improve the application throughout development.
- Practices we actually use: s sprints 
- **Definition of Done** (checklist, 4 or more items):•	[ ] It meets the agreed acceptance criteria.
•	[ ] The code follows the project's coding standards.
•	[ ] Appropriate tests are written and pass.

  
- Sprint plan 
Development of core item reporting 
| Sprint | Working software at the end | se-agent run? |
|---|---|---|
| 1 | | |Suggest a simple Flask architecture for a lost and found application using SQLite.
| 2 | | |Suggest project features and implementation approaches for a campus lost and found application
| 3 | | |
Development of core item reporting and search functionality has started.


- Biggest schedule risk and what we will do about it: leaking data
- AI contribution:creating prompts, helping with code structure.

## 2. Requirements (Chapter 4)  Owner (Product Owner): __university of North texas____
**Stakeholders and what each wants:**

| Stakeholder | Wants |•
Students: Easily report lost belongings and find items reported by others.
•	Campus staff: Manage lost-and-found records efficiently.
•	Administrators: Review claims, prevent fraudulent claims, and update item statuses.
•	University: Provide a reliable and user-friendly campus service.
•	Development team: Build a maintainable, testable, and functional application.

|---|---|
| | |

**User stories** (as a ___, I want ___, so that ___), each with acceptance criteria:
.•	Report a lost item.
•	Report a found item.
•	Search for items.
•	Submit an item claim.
•	Review claims.
•	Approve or reject claims.
•	Mark an item as returned.



**Requirements table*
report and search
found item claim
mark return

| ID | Type (F = functional, NF = non-functional) | Requirement (one testable sentence) | Priority (Must/Should) | Acceptance test (input -> expected result) |
|---|---|---|---|---|
| R1 | F | | Must | |
| R2 | F | | Must | |
| R3 | F | | Must | |
| R4 | NF (performance) | | | |
| R5 | NF (usability) | | | |
| R6 | NF (security or privacy) | | | |
| R7 | NF (cost) | | | |

**Out of scope** (so nobody builds it by accident):
-student location

**Requirements we removed as unnecessary, and why:**
-

**Open questions** (better listed than guessed):
-

**Check:** could two people read each requirement and build different things? Are there words like *fast*, *easy*, *secure*? Replace each with something observable.
- AI contribution:

## 3. Models (Chapter 5)  Owner (Architect): ______
Text, bulleted lists, or Mermaid are all fine.

**Context model** (what is inside the system, what is outside, what crosses the boundary):

**Use cases or a sequence model for the most important story:**

**Class or data model** (main entities and how they relate):

**State model** (only if the app has modes; otherwise write "no modes"):

**Consistency check:** a requirement that appears in no model, or a model element no requirement needs, and how we resolved it:
- AI contribution:

## 4. Architecture (Chapter 6)  Owner (Architect): ______
- Pattern we chose (layered, MVC, client-server, pipe-and-filter, other):
- Which non-functional requirements drove it (name the R-numbers):
- Alternatives we rejected, and why:
- **If the app uses an AI model:** where it is used; what happens when it is slow, wrong, or down (the non-AI fallback); the cost per use:

**Decisions log**

| # | Decision | Alternatives | Reason (tie to an R-number) | Consequence |
|---|---|---|---|---|
| D1 | | | | |
| D2 | | | | |
| D3 | | | | |

- AI contribution:

## 5. Design and implementation (Chapter 7)  Owner: ______
- Modules, and the owner of each:

| Module | Owner | Responsibility |
|---|---|---|
| | | |

- Where the logic lives **apart from the display** (so it can be unit-tested):
- Design patterns we will use, and where (or "none yet"):
- Code or libraries we will reuse, with their licenses:
- Branching and review rule (for example: pull request, one approval, tests green):
- Technical debt we are knowingly accepting:
- AI contribution:

## 6. Testing (Chapter 8)  Owner (Quality lead): ______
**Requirement-to-test map** (every Must-do needs at least one):

| Requirement | Test (file::name) | Type (unit / component / system / user) | How we will check it can fail |
|---|---|---|---|
| R1 | | | |
| R2 | | | |
| R3 | | | |

**The three most important tests, in plain language** (input -> expected result):
1.
2.
3.

- Edge cases we will try to break each Must-do with (zero, negative, empty, huge, missing):
- User testing: who (outside the team), and what we want to learn:
- What we are deliberately **not** testing, and why:
- Test command: `________`
- AI contribution:

## 7. Evolution (Chapter 9)  Owner: ______
- The most likely future change:
- Impact analysis: modules, models, requirements and tests that would change, and about how long:
- What design choice today would make that change easier:
- AI contribution:

## 8. Decisions we are least sure about
(Prepare to be asked about these.)
-

## 9. Run plan and cost (se-agent)  Owner (Prompt engineer): ______
- Prompts in `prompts/` we will use, in order:
- Model (use `gpt-6-luna` for iteration; ask before using a stronger one):
- Planned runs (default: one per sprint):

| Run | Sprint | Prompts | Model | Estimated cost (`uv run python cost_estimate.py docs/RUN_BRIEF.md`) |
|---|---|---|---|---|
| 1 | | | | |

- Before we request a run, we confirmed: `uv run pytest` passes / Run Brief is 4,000 characters or fewer / each prompt follows the 8-section template

## 10. Run Brief
The Run Brief is a **separate file**: `docs/RUN_BRIEF.md`. It is what se-agent reads, and it must be **4,000 characters or fewer** (about 700 words). The agents do not read this Full Spec, so anything a model must know has to be in the Run Brief, in words.

**Keep:** the main problem and user; numbered Must-dos (each testable); technology and data constraints; any cost limit on AI features; the out-of-scope list; 3 to 5 acceptance checks.
**Cut:** process reasoning, stakeholder analysis, long rationale, diagrams (describe the one relationship that matters in a sentence).
**Translate:** non-functional requirements become constraints with numbers; the architecture becomes one sentence; the test plan becomes quality expectations and acceptance criteria.

Check the length:
```
python -c "print(len(open('docs/RUN_BRIEF.md', encoding='utf-8').read()))"
```

- Characters in our Run Brief: ______
- What we cut to fit, and why it was safe to cut:

## 11. Presentation notes (six beats; every member speaks)
| Beat | Who | One sentence we will say |
|---|---|---|
| 1. Problem, user, Must-dos (Ch 4) | | |
| 2. Process choice and Definition of Done (Ch 2, 3) | | |
| 3. Context model and one more model (Ch 5) | | |
| 4. One architecture decision: chosen, rejected, which requirement forced it (Ch 6) | | |
| 5. Three most important tests, and how we know they can fail (Ch 8) | | |
| 6. Likely change, Run Brief, cost plan (Ch 9, 4) | | |

# 🥜 PB&J Sandwich — BA Critical Thinking Exercise

> **Purpose:** Business Analyst Training
> **Exercise Type:** Requirements Thinking & Feature Writing
> **Audience:** Business Analysts
> **Deliverable:** A shared Word document completed as a team
> **Goal:** Write the complete process for making a PB&J sandwich — covering base cases, edge cases, and corner cases — well enough that a developer could build it without asking a single question

---

## 🎯 Why This Exercise?

Before a BA can write a feature, they must first think like a system.

This exercise uses something everyone knows — making a Peanut Butter and Jelly sandwich — to train BAs to think logically, algorithmically, and completely. If a BA cannot fully define a PB&J sandwich, they are not ready to define a software feature.

---

## 🥪 What Is the Solution?

**The solution to this exercise is a complete written process for making a Peanut Butter and Jelly sandwich.**

Not a drawing. Not a conversation. Not a bullet list of ingredients.

A fully documented, step-by-step process — written with enough clarity and precision that a developer who has never made a sandwich, and who will ask zero follow-up questions, could build it exactly as intended.

That is the bar. That is always the bar in real feature work.

The sandwich is the system. Your job is to define it completely.

> If your written process has gaps, a real developer would fill those gaps with assumptions. Every assumption a developer makes that you did not define is a potential bug. The sandwich makes this visible in a way that is low-stakes and immediately understandable — which is exactly why it works as a training exercise.

---

## 🔗 How All the Concepts Connect

This is the most important thing to understand before you begin writing.

The terms in this exercise are not a vocabulary list. They are a **system**. Every concept feeds directly into the next. If you understand how they connect, you will know exactly what to write — and why.

```
USER STORY
    ↓
defines what the user needs
    ↓
ACCEPTANCE CRITERIA
    ↓
defines what "done" looks like
    ↓
GIVEN / WHEN / THEN
    ↓
makes the criteria testable and specific
    ↓
BASE CASE / EDGE CASE / CORNER CASE
    ↓
covers the full range of conditions that must be tested
    ↓
HAPPY PATH / FAILURE PATH
    ↓
defines what success looks like AND what the system does when it cannot succeed
    ↓
BOUNDARY
    ↓
draws the exact line between pass and fail — so the developer never has to guess
    ↓
INVEST
    ↓
validates that the user story is ready to hand to a developer
```

Here is what that connection means in practice:

### The User Story sets the intent
> *"As a user, I want the system to validate all required ingredients before the process starts, so that I am not blocked mid-way through."*

This tells you **what** needs to happen and **why**. It does not tell you how. That is correct — the story defines the goal, not the implementation.

### Acceptance Criteria makes the intent concrete
The story says "validate all required ingredients." Acceptance criteria defines what that means exactly:
> *All required ingredients and tools are present, in-date, and accessible before Step 2 begins.*

Now the developer knows what state the system must reach. Still no implementation — but a clear, verifiable outcome.

### Given / When / Then makes it testable
Acceptance criteria says what must be true. Given / When / Then says **how you will prove it**:
> *Given all ingredients are present and in-date → When the checklist is validated → Then the process proceeds to Step 2 with no blockers.*

This is the test. If you can write it, it can be built. If you cannot write it, the story is not ready.

### Base Case / Edge Case / Corner Case covers every scenario
Given / When / Then handles one scenario at a time. But users do not always arrive in perfect conditions. The case types force you to cover the full range:

- **Base Case** — the scenario you write your first Given / When / Then for. Everything is normal.
- **Edge Case** — a valid but unusual scenario. Requires its own Given / When / Then.
- **Corner Case** — two or more unusual conditions at once. Requires its own Given / When / Then, and usually more defensive logic.

If you only write the base case, you have only written one test. Real systems fail on edge cases and corner cases.

### Happy Path / Failure Path defines the full flow
- The **Happy Path** is the base case across all steps end to end — everything works, the sandwich is made, the user accepts it.
- The **Failure Path** is what the system does at each step when something goes wrong. It is not enough to say "it fails." The BA must define what happens next: Does the process halt? Does it retry? Does it notify the user? Does it restart from a specific step?

Without a defined failure path, the developer builds the happy path and hopes for the best. That is a production incident waiting to happen.

### Boundary removes all ambiguity
Even a well-written failure path can fail if the condition that triggers it is vague. The boundary is the exact line:

> ❌ *"Make sure there is enough peanut butter."*
> ✅ *"The jar must contain sufficient peanut butter to cover the full surface of one slice of bread before spreading begins. Less than that — the step halts."*

The first version asks the developer to guess. The second version leaves nothing to guess. Every number, every threshold, every condition the developer needs to make a decision must be explicitly stated by the BA. If it is not in the requirements, the developer will invent it — and that invented value becomes the system's behaviour.

### INVEST is the final quality gate
Before a user story is handed to development, it must pass INVEST. This is not a formality — it is a filter that catches stories that are too vague, too large, or impossible to test. A story that fails INVEST is not ready. Rewrite it first.

> **The full chain in one sentence:** The user story defines the goal → acceptance criteria makes it concrete → Given / When / Then makes it testable → cases cover every scenario → paths define what happens at every outcome → boundaries remove every ambiguity → INVEST confirms the story is ready to build.

---

## 📐 Terms You Must Know

| Term | What It Means |
|---|---|
| **Base Case** | The most normal, standard scenario. What does "everything goes right" look like? |
| **Edge Case** | A valid but unusual condition. It can happen — it is just not the norm. |
| **Corner Case** | Two or more unusual conditions happening at the same time. |
| **Happy Path** | The full flow from start to finish when nothing goes wrong. |
| **Failure Path** | What happens when a step cannot be completed? What does the system do next? |
| **Boundary** | The exact line between what is acceptable and what is not. The BA must define this number or condition precisely — if they do not, the developer will guess, and that guess becomes a bug. |
| **Given / When / Then** | A structured way to write acceptance criteria. Given = the starting state. When = the action that occurs. Then = the expected outcome. |
| **User Story** | A short, plain-language description of a feature from the perspective of the user. Format: *As a [user], I want [something], so that [reason].* |
| **INVEST** | The quality checklist every user story must pass before it is handed to a developer. See below. |

---

## 📋 How This Works

This is a **team exercise**. You will work together in a shared Word document to write the full requirements for making a PB&J sandwich — from start to finish.

**Each team member takes ownership of at least one step.** Collaborate, challenge each other's assumptions, and fill in what the next person missed. The goal is a complete document that leaves nothing to interpretation.

> 📄 **Open the shared Word document and begin writing. Do not just discuss — write it down.**

---

## 🔑 Reference Example — The Sandwich

Before you start writing, read through this reference. It shows all the concepts applied to the sandwich so you know exactly what each term looks like before you begin.

**Base Case** — The user has all ingredients present, in-date, and at room temperature. The sandwich is made from start to finish without any interruptions.

**Edge Case** — The bread is present but frozen. It is a valid ingredient — it is just not in a ready state. A thaw step must be inserted before the process can continue.

**Corner Case** — The bread is frozen AND the jelly jar is expired AND the knife is not available. Three unusual conditions exist at the same time. Each must be resolved independently — fixing one does not fix the others.

**Happy Path** — All ingredients are present and usable, both spreads are applied cleanly, the sandwich assembles without structural failure, and the user accepts it immediately upon serving.

**Failure Path** — The jelly jar is contaminated with peanut butter and the user has a nut allergy. The process halts immediately. The jar is discarded. The process cannot continue until a clean replacement is sourced.

**Boundary** — A jar of peanut butter must have enough to cover at least one full slice before spreading begins. If the jar has enough for half a slice, it fails. If it has enough for a full slice, it passes. The BA must state that condition explicitly. If they write "make sure there is enough peanut butter" instead of "sufficient to cover the full surface of one slice," the developer has to guess where the line is — and that guess becomes a bug.

---

## 📋 INVEST Framework

Every user story in this document must meet the INVEST standard. If a story fails any one of these, rewrite it before handing it to the development team.

| Letter | Stands For | What It Means |
|---|---|---|
| **I** | Independent | The story can be built without depending on another story being done first. |
| **N** | Negotiable | The story is not a contract. The details can be discussed and adjusted with the team. |
| **V** | Valuable | The story delivers clear value to the user or the business. If you cannot explain the value, the story should not exist. |
| **E** | Estimable | The developer can estimate how long it will take. If they cannot, the story is too vague. |
| **S** | Small | The story is small enough to complete within a single sprint. If it is too big, break it down. |
| **T** | Testable | There is a clear way to verify the story is done. If it cannot be tested, it cannot be accepted. |

---

## 🧠 The Exercise

As a team, your task is to open a shared Word document and write the complete, end-to-end process for making a Peanut Butter and Jelly sandwich — from acquiring the ingredients all the way through serving the final product. For every step in the process, your team must write the full description of what happens, the complexity cases, the failure path, the acceptance criteria, at least one Given / When / Then scenario, and the user stories following the INVEST framework. The document must be written with enough clarity and detail that a developer who has never made a sandwich — and who will ask no follow-up questions — could build the process exactly as you intended.

---

## 📊 Complexity Scale

Every case in this process is rated by complexity. This tells the development team how much logic, error handling, and effort is required to implement it.

| Level | Maps To | What It Means for the Developer |
|---|---|---|
| 🟢 **Low** | Base Case | Standard input, predictable output. Straightforward to build. |
| 🟡 **Medium** | Edge Case | Unusual but valid condition. Requires conditional logic and validation. |
| 🔴 **High** | Corner Case | Multiple unusual conditions at once. Requires defensive logic, fallbacks, and testing. |

---

## 🥪 Full Process: Making a PB&J Sandwich

### Step 1 — Acquire Ingredients

Before anything can happen, the required ingredients and tools must be present and in a usable state.

**Required inputs:** bread, peanut butter, jelly, a knife, a plate, and a clean surface.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | All ingredients are present, sealed, in-date, and stored at room temperature. Proceed to Step 2. |
| 🟡 Medium | Edge Case | One ingredient is missing (e.g., no jelly). System must pause and prompt the user to resolve before continuing. |
| 🟡 Medium | Edge Case | Bread is present but frozen. A thaw step must be inserted before the bread can be used. |
| 🟡 Medium | Edge Case | Peanut butter or jelly is expired. The ingredient must be flagged as unusable and a replacement requested. |
| 🔴 High | Corner Case | Bread is frozen AND the only jelly jar is expired AND the knife is not available. All three blockers exist simultaneously. Each must be resolved independently before the process can continue — resolving one does not resolve the others. |

**Failure Path:** If any required ingredient cannot be acquired or replaced, the process cannot start. Surface a clear error identifying exactly which item is missing or unusable.

**Acceptance Criteria:** All required ingredients and tools are present, in-date, and accessible before Step 2 begins.

**Given / When / Then:**
> **Given** all ingredients are present, sealed, in-date, and at room temperature
> **When** the BA validates the ingredient checklist
> **Then** the process proceeds to Step 2 with no blockers

> **Given** one or more ingredients are missing or expired
> **When** the system checks ingredient availability
> **Then** the process halts, a specific error is surfaced for each missing item, and the user is prompted to resolve before continuing

> **Given** bread is frozen AND the jelly is expired AND the knife is unavailable
> **When** all three blockers are detected simultaneously
> **Then** each blocker is surfaced independently — resolving one does not clear the others — and the process cannot continue until all three are resolved

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S1-01 | As a user, I want the system to validate all required ingredients before the process starts, so that I am not blocked mid-way through by a missing item. | ✅ Independent · Valuable · Testable |
| S1-02 | As a user with a dietary constraint, I want my constraints checked against all ingredients at the start, so that I never begin a process that cannot be safely completed for me. | ✅ Independent · Valuable · Testable |
| S1-03 | As a user, I want each missing or unusable ingredient surfaced as a separate, specific error, so that I can resolve all blockers at once rather than one at a time. | ✅ Small · Estimable · Testable |

---

### Step 2 — Open the Bread

The bread loaf must be opened to expose individual slices. The packaging type determines how this is done.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | Bread is in a sealed bag with a twist tie. Remove the twist tie, open the bag, and set the twist tie aside for reuse. |
| 🟡 Medium | Edge Case | Bread bag uses a plastic clip instead of a twist tie. Remove the clip using the same intent — do not discard. |
| 🟡 Medium | Edge Case | Bread bag is already open. Skip the opening step and proceed directly to Step 3. |
| 🟡 Medium | Edge Case | Bread has no packaging (artisan loaf). No opening action is required. Proceed to Step 3. |
| 🔴 High | Corner Case | Bread bag is sealed but torn or damaged. The bag cannot be reused for storage. Opening must still proceed, but a substitute storage method (e.g., alternate bag or container) must be identified before the remaining bread can be stored at the end of the process. |

**Failure Path:** If the bag cannot be opened without destroying the bread inside, halt and request a replacement loaf.

**Acceptance Criteria:** The bread is accessible. The packaging closure (if any) is set aside and not discarded. The bag remains intact enough for reuse, or a storage alternative has been identified.

**Given / When / Then:**
> **Given** the bread bag is sealed with a twist tie or clip
> **When** the BA opens the bag
> **Then** the closure is removed and set aside, the bag is opened without tearing, and the bread is accessible

> **Given** the bread bag is already open
> **When** the system checks the bag state
> **Then** the opening step is skipped entirely and the process proceeds directly to Step 3

> **Given** the bread bag is sealed but torn or damaged
> **When** the BA attempts to open the bag
> **Then** the bread is accessed, a substitute storage method is identified for the remaining bread, and the torn bag is not used for resealing

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S2-01 | As a user, I want the system to detect the bread packaging type automatically, so that the correct opening method is applied without me having to specify it. | ✅ Independent · Valuable · Estimable |
| S2-02 | As a user, I want the system to skip the opening step if the bread is already open, so that the process does not perform unnecessary actions. | ✅ Small · Testable · Independent |
| S2-03 | As a user, I want the system to identify a storage alternative when the bag is damaged, so that the remaining bread is not wasted after the sandwich is made. | ✅ Valuable · Testable · Small |

---

### Step 3 — Prepare Two Slices of Bread

Exactly two slices of bread are required. The steps to obtain them depend on whether the bread arrived pre-sliced or not.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | Bread is pre-sliced. Select two adjacent slices from the middle of the loaf. The slicing step is skipped entirely. |
| 🟡 Medium | Edge Case | Bread is unsliced (e.g., artisan loaf). A bread knife and cutting board are required. Slice to an even, consistent thickness — approximately 1cm. |
| 🟡 Medium | Edge Case | Only the heel (end piece) remains along with one regular slice. Determine whether the heel is an acceptable slice based on user preference. If not, the process cannot continue — insufficient bread. |
| 🟡 Medium | Edge Case | Only one slice remains in the bag. One slice is insufficient. Process must halt and surface a missing ingredient error. |
| 🔴 High | Corner Case | Bread is unsliced AND the bread knife is unavailable AND only enough bread for exactly two slices remains on the loaf. The bread must be sliced with a substitute tool, with no margin for error. Any wasted bread results in insufficient quantity and a process failure. |

**Failure Path:** If two usable slices cannot be obtained, halt and surface an insufficient bread error before proceeding.

**Acceptance Criteria:** Exactly two slices of bread are available, flat-side up, on a clean surface. If slicing was required, both slices are of consistent, even thickness.

**Given / When / Then:**
> **Given** the bread is pre-sliced
> **When** the BA selects two slices
> **Then** two slices from the middle of the loaf are placed flat-side up on a clean surface and the slicing step is skipped

> **Given** the bread is unsliced and a bread knife and cutting board are available
> **When** the BA slices the bread
> **Then** two slices of consistent, even thickness (approximately 1cm) are produced and placed flat-side up on a clean surface

> **Given** the bread is unsliced AND the bread knife is unavailable AND only enough bread for exactly two slices remains
> **When** the BA attempts to slice using a substitute tool
> **Then** the bread is sliced with maximum care — any waste results in insufficient quantity and a process failure is raised immediately

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S3-01 | As a user, I want the system to detect whether bread is pre-sliced or unsliced, so that the slicing step is only triggered when it is actually needed. | ✅ Independent · Testable · Small |
| S3-02 | As a user, I want to be prompted if the heel is the only remaining slice, so that I can decide whether it is acceptable before the process continues. | ✅ Negotiable · Valuable · Testable |
| S3-03 | As a user, I want the system to halt and surface an error if fewer than two usable slices are available, so that I am not given a sandwich that cannot be properly assembled. | ✅ Independent · Testable · Small |

---

### Step 4 — Apply Peanut Butter

Peanut butter is spread on the top surface of one slice of bread using a knife.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | Jar is full, at room temperature, creamy style, sealed with a standard screw lid. Open jar, insert knife, scoop a sufficient amount, and spread evenly across the full surface of Slice 1 to the edges. |
| 🟡 Medium | Edge Case | Peanut butter is cold and stiff from refrigeration. It will tear the bread if spread directly. It must be allowed to reach room temperature, or the spreading force must be reduced and applied more slowly. |
| 🟡 Medium | Edge Case | Jar is nearly empty. Sufficient peanut butter may still exist but requires scraping the sides and bottom. The amount must be validated as enough to cover the full slice before proceeding. |
| 🟡 Medium | Edge Case | Peanut butter is crunchy style instead of creamy. The spreading technique remains the same, but the output texture will differ. This is valid — no change to the process is required, but the difference must be acknowledged as a known variation. |
| 🔴 High | Corner Case | Peanut butter is both cold/stiff AND the jar is nearly empty. Spreading cold, thick peanut butter from a near-empty jar significantly increases the risk of tearing the bread and running out mid-spread. Both conditions must be managed simultaneously — warm first, then spread with extra care. |

**Failure Path:** If there is not enough peanut butter to cover the full surface of the slice, halt. Do not proceed with partial coverage. Request a new jar.

**Acceptance Criteria:** The full top surface of Slice 1 is covered with an even layer of peanut butter reaching the edges. The bread is not torn. The knife has not entered the jelly jar.

**Given / When / Then:**
> **Given** the peanut butter jar is full and at room temperature
> **When** the BA scoops and spreads peanut butter onto Slice 1
> **Then** the full surface of Slice 1 is evenly covered to the edges and the bread is not torn

> **Given** the peanut butter is cold and stiff from refrigeration
> **When** the BA attempts to spread it directly
> **Then** the spread is paused, the peanut butter is allowed to reach room temperature, and spreading resumes only once it is soft enough to apply without tearing the bread

> **Given** the peanut butter is cold AND the jar is nearly empty
> **When** the BA attempts to spread
> **Then** the peanut butter is warmed first, then carefully scraped from the jar and spread with reduced pressure — if coverage cannot be completed, the step halts and a new jar is requested

> **Given** the user has requested a jelly-only sandwich
> **When** the BA reaches Step 4
> **Then** this step is skipped entirely and the process proceeds directly to Step 5

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S4-01 | As a user, I want peanut butter spread evenly across the full surface of my slice, so that every bite has consistent flavour. | ✅ Valuable · Testable · Small |
| S4-02 | As a user, I want the system to warn me if the peanut butter jar does not have enough to cover a full slice, so that I can source a new jar before the process begins. | ✅ Independent · Testable · Estimable |
| S4-03 | As a user who requested a jelly-only sandwich, I want the peanut butter step skipped entirely, so that my sandwich is made according to my preference without manual intervention. | ✅ Independent · Valuable · Testable |

---

### Step 5 — Apply Jelly

Jelly is spread on the top surface of the second slice of bread using a knife.

> ⚠️ **Note to developers:** The knife used in Step 4 may carry peanut butter residue. This is a cross-step dependency and must be handled before this step begins.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | A clean knife is used. Jelly jar is full, at room temperature, standard consistency. Open jar, scoop, and spread evenly across the full surface of Slice 2. |
| 🟡 Medium | Edge Case | The same knife from Step 4 is being reused. The knife must be wiped clean before entering the jelly jar to prevent peanut butter contamination of the jar. |
| 🟡 Medium | Edge Case | Jelly has separated — liquid has risen to the top of the jar. The jelly must be stirred to return it to a consistent, spreadable texture before use. |
| 🟡 Medium | Edge Case | The spread is jam or preserves instead of jelly. The spreading technique is the same, but texture may be chunkier. This is a valid substitution — no process change required. |
| 🔴 High | Corner Case | The knife was not wiped after Step 4 AND peanut butter was already deposited into the jelly jar from a previous use. The jar is now contaminated. For users with peanut allergies, this jar must be discarded entirely. A new jelly source is required before the process can continue. |

**Failure Path:** If the jelly jar is contaminated and a nut allergy is a known constraint, halt immediately. Do not proceed. Discard the contaminated jar and source a clean replacement.

**Acceptance Criteria:** The full top surface of Slice 2 is covered with an even layer of jelly reaching the edges. The bread is not torn. The jelly jar contains no peanut butter contamination.

**Given / When / Then:**
> **Given** a clean knife is available and the jelly jar is uncontaminated
> **When** the BA spreads jelly onto Slice 2
> **Then** the full surface of Slice 2 is evenly covered to the edges and the bread is not torn

> **Given** the same knife from Step 4 is being reused
> **When** the BA is about to enter the jelly jar
> **Then** the knife is wiped clean of all peanut butter residue before it contacts the jelly jar

> **Given** the user has a nut allergy AND the jelly jar has been contaminated with peanut butter
> **When** the BA detects contamination
> **Then** the process halts immediately, the contaminated jar is discarded, and a clean replacement jar is sourced before the step can be retried

> **Given** the user has requested a jelly-only sandwich
> **When** the BA reaches Step 5
> **Then** a dedicated clean knife that has never contacted peanut butter is used — a wiped knife is not acceptable for this user type

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S5-01 | As a user, I want jelly spread evenly across the full surface of my slice, so that every bite has consistent flavour. | ✅ Valuable · Testable · Small |
| S5-02 | As a user, I want the system to enforce a clean knife before it enters the jelly jar, so that cross-contamination from peanut butter is prevented. | ✅ Independent · Testable · Estimable |
| S5-03 | As a user with a nut allergy, I want the system to halt and discard a contaminated jelly jar immediately, so that I am never served a sandwich that could cause an allergic reaction. | ✅ Independent · Valuable · Testable |
| S5-04 | As a jelly-only user, I want the system to require a knife that has never contacted peanut butter — not just a wiped one — so that my safety constraint is fully honoured. | ✅ Independent · Testable · Small |

---

### Step 6 — Assemble the Sandwich

The two prepared slices are joined to form a single sandwich unit.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | Place Slice 2 (jelly side down) directly onto Slice 1 (peanut butter side up). The two spread surfaces face each other. Press gently to seal. |
| 🟡 Medium | Edge Case | User preference requires the sandwich to be cut. Determine cut style — diagonal or straight — based on user input. Use a clean knife to cut through the center without dragging the filling. |
| 🟡 Medium | Edge Case | Filling has been applied too close to the edges and spills out during pressing. Excess must be removed using the knife before serving, or the assembly must be repeated with reduced spread quantity. |
| 🔴 High | Corner Case | The filling on both slices is overapplied AND the bread is soft and structurally weak. Pressing the two slices together causes the bread to compress, tear, and the filling to overflow on all sides. The sandwich cannot be salvaged. Both slices must be discarded and the process restarted from Step 3. |

**Failure Path:** If the sandwich cannot be assembled into a structurally sound unit, discard the affected slices and restart from Step 3.

**Acceptance Criteria:** Two slices are joined with spread surfaces facing inward. The sandwich holds its shape. No filling is exposed on the outer surfaces. If a cut was requested, it is clean and even.

**Given / When / Then:**
> **Given** both slices are properly spread and structurally intact
> **When** the BA places Slice 2 jelly-side down onto Slice 1 peanut butter-side up
> **Then** the sandwich is pressed gently, holds its shape, and no filling overflows the edges

> **Given** the user has requested the sandwich to be cut
> **When** the BA cuts the assembled sandwich
> **Then** the cut style matches user preference (diagonal or straight), the cut is clean, and the filling does not drag or shift

> **Given** filling has been overapplied on both slices AND the bread is soft and structurally weak
> **When** the BA presses the slices together
> **Then** the bread tears and filling overflows — the sandwich is unsalvageable, both slices are discarded, and the process restarts from Step 3

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S6-01 | As a user, I want the two slices joined with spread surfaces facing inward, so that the filling stays inside the sandwich and does not contact the outer surfaces. | ✅ Testable · Small · Valuable |
| S6-02 | As a user, I want to specify my preferred cut style — diagonal or straight — before assembly is finalised, so that my sandwich is presented the way I want it. | ✅ Negotiable · Small · Testable |
| S6-03 | As a user, I want the system to detect when a sandwich cannot be salvaged due to structural failure, so that the failed slices are discarded and the process restarts cleanly from Step 3. | ✅ Independent · Testable · Estimable |

---

### Step 7 — Serve

The completed sandwich is delivered to the end user in an acceptable condition.

| Complexity | Case | Description |
|---|---|---|
| 🟢 Low | Base Case | Sandwich is placed on a clean plate and presented to the user immediately. |
| 🟡 Medium | Edge Case | User requests the sandwich wrapped (e.g., for travel). Wrap in paper, foil, or a bag before handing over. Ensure the wrapping does not compress the sandwich or cause filling to shift. |
| 🟡 Medium | Edge Case | User rejects the sandwich (wrong bread, wrong spread, structural failure). Identify the specific rejection reason, determine if it can be corrected (e.g., recut) or if the sandwich must be remade from the appropriate step. |
| 🔴 High | Corner Case | Sandwich was assembled correctly but sat too long before serving — the bread has become soggy from the jelly soaking through. The sandwich is no longer in an acceptable state. It must be remade from Step 3. Time-to-serve is now a constraint that must be added to the process requirements. |

**Failure Path:** If the sandwich cannot be served in an acceptable state, identify which step introduced the failure and restart from that point.

**Acceptance Criteria:** The sandwich is delivered to the user on an appropriate surface, in a structurally sound and visually acceptable condition, within an acceptable time of assembly. The user accepts it.

**Given / When / Then:**
> **Given** the sandwich is freshly assembled and structurally sound
> **When** the BA places it on a clean plate and presents it to the user
> **Then** the user accepts the sandwich and the process is complete

> **Given** the user requests the sandwich wrapped for travel
> **When** the BA wraps the sandwich
> **Then** the sandwich is wrapped securely without compressing the bread or shifting the filling, and handed to the user

> **Given** the sandwich sat too long before serving and the bread has become soggy
> **When** the BA attempts to serve it
> **Then** the sandwich is rejected as unacceptable, discarded, and the process restarts from Step 3 — time-to-serve is flagged as a new constraint to be added to the process requirements

**User Stories:**

| # | Story | INVEST Check |
|---|---|---|
| S7-01 | As a user, I want my sandwich placed on a clean plate and served immediately after assembly, so that I receive it in the best possible condition. | ✅ Valuable · Testable · Small |
| S7-02 | As a user travelling with my sandwich, I want it wrapped securely without compressing the bread, so that it arrives in an acceptable condition when I am ready to eat it. | ✅ Independent · Negotiable · Testable |
| S7-03 | As a user, I want the system to flag when a sandwich has exceeded the maximum acceptable time before serving, so that I am never given a soggy or degraded sandwich. | ✅ Independent · Testable · Estimable |
| S7-04 | As a user who has rejected a sandwich, I want the system to identify exactly which step caused the failure and restart from that point, so that I am not waiting for the entire process to restart unnecessarily. | ✅ Valuable · Testable · Small |

---

## ✅ Team Definition of Done

Your Word document is complete when the team can answer YES to every item below:

- [ ] Every step has a full written description
- [ ] Every step has a clearly written base case (🟢 Low)
- [ ] Every step has at least 2 edge cases (🟡 Medium)
- [ ] Every step has at least 1 corner case (🔴 High)
- [ ] At least one corner case spans two steps
- [ ] Every step has a defined failure path
- [ ] Every step has written acceptance criteria
- [ ] Every step has at least one Given / When / Then scenario
- [ ] Every step has at least one user story
- [ ] Every user story passes the INVEST framework
- [ ] The document reads as if the team assumed the reader knows nothing
- [ ] Every team member has contributed and reviewed at least one step

---

## 💬 Final Thought

Every team finds gaps. That is the point. The sandwich is simple — and you still missed things. Now imagine what you are missing when the system is not simple.

---

## 🚀 Good Start — But Did You Think of These?

If your team completed the exercise, congratulations — you have a solid foundation. But requirements work is never truly finished. A good BA always asks: **what else did we miss?**

Here are additional cases your team may not have considered. These are not trick questions — they are the exact type of gaps that appear in real features when a BA writes for one imaginary user instead of all real users.

**Quantity — The Silent Assumption**
The entire process assumes one sandwich for one user and never states it. What if the user wants two sandwiches? Or five? Quantity was never defined as an input, which means the ingredient validation logic, the spread amounts, and the serving step all break the moment a second sandwich is requested. Every process needs a quantity constraint — even if the answer is "always one."

**Stale Bread — Quality vs. Expiry**
Step 1 checks whether bread is expired. But what if the bread is stale — technically in-date, but dry, hard, or compromised in texture? Expiry and quality are not the same thing. Who defines the acceptable quality threshold, and what happens when bread passes the date check but fails the quality check?

**Spread Placement — Another Silent Assumption**
The process assumes peanut butter always goes on Slice 1 and jelly always goes on Slice 2, on separate slices. But what if the user wants both spreads on the same slice? Or peanut butter on both? The process never asks the user — it just decides. That is a missing requirement.

**Dietary Constraints Beyond Allergy**
The process handles nut allergies, but what about other constraints? A diabetic user may need to flag high-sugar jelly. A vegan user may need to validate that the bread and spreads meet dietary requirements. Allergy is one type of constraint — it is not the only one.

**Open-Faced Sandwich**
Step 6 assumes the sandwich is always closed — two slices pressed together. But what if the user wants an open-faced sandwich with no top slice? The process never validates this as a user preference. It silently builds a closed sandwich every time.

**User Not Present at Serving**
Step 7 assumes the user is ready and waiting when the sandwich is complete. But what if they are not? How long can the sandwich sit before it is no longer acceptable to serve? This is a time constraint that was never defined — and it directly connects to the soggy bread corner case in Step 7.

> 💡 **Discussion prompt for your team:** Go back through your Word document. How many of these did you catch? How many slipped through? The ones that slipped through are exactly the gaps that become bugs, support tickets, and production incidents in real features.

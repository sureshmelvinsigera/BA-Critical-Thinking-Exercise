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

## 📋 How This Works

This is a **team exercise**. You will work together in a shared Word document to write the full requirements for making a PB&J sandwich — from start to finish.

**Each team member takes ownership of at least one step.** Collaborate, challenge each other's assumptions, and fill in what the next person missed. The goal is a complete document that leaves nothing to interpretation.

> 📄 **Open the shared Word document and begin writing. Do not just discuss — write it down.**

---

## 📐 Terms You Must Know

| Term | What It Means |
|---|---|
| **Base Case** | The most normal, standard scenario. What does "everything goes right" look like? |
| **Edge Case** | A valid but unusual condition. It can happen — it is just not the norm. |
| **Corner Case** | Two or more unusual conditions happening at the same time. |
| **Happy Path** | The full flow from start to finish when nothing goes wrong. |
| **Failure Path** | What happens when a step cannot be completed? What does the system do next? |
| **Given / When / Then** | A structured way to write acceptance criteria. Given = the starting state. When = the action that occurs. Then = the expected outcome. |

---

## 🧠 The Exercise

As a team, your task is to open a shared Word document and write the complete, end-to-end process for making a Peanut Butter and Jelly sandwich — from acquiring the ingredients all the way through serving the final product. For every step in the process, your team must write the full description of what happens, the base case, at least two edge cases, at least one corner case, the failure path, and the acceptance criteria. The document must be written with enough clarity and detail that a developer who has never made a sandwich — and who will ask no follow-up questions — could build the process exactly as you intended.

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

---

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

---

### Step 5 — Apply Jelly

Jelly is spread on the top surface of the second slice of bread using a knife.

**⚠️ Note to developers:** The knife used in Step 4 may carry peanut butter residue. This is a cross-step dependency and must be handled before this step begins.

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

---

## ✅ Team Definition of Done

Your Word document is complete when the team can answer YES to every item below:

- [ ] Every step has a full written description
- [ ] Every step has a clearly written base case
- [ ] Every step has at least 2 edge cases
- [ ] At least one corner case is documented across any two steps
- [ ] Every step has a defined failure path
- [ ] Every step has written acceptance criteria
- [ ] Every step has at least one Given / When / Then scenario
- [ ] The document reads as if the team assumed the reader knows nothing
- [ ] Every team member has contributed and reviewed at least one step

---

## 💬 Final Thought

If your team cannot fully define a sandwich, your team is not ready to define a feature.

Every assumption you skip becomes a bug. Every edge case you miss becomes a support ticket. Every corner case you overlook becomes a production incident.

The sandwich is simple on purpose. The thinking — and the writing — is the exercise.

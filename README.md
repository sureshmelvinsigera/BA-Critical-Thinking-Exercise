# 🥜 PB&J Sandwich — BA Critical Thinking Exercise

> **Purpose:** Business Analyst Training
> **Exercise Type:** Requirements Thinking & Feature Writing
> **Audience:** Business Analysts
> **Deliverable:** A shared Word document completed as a team
> **Goal:** Write the complete process for making a PB&J sandwich — covering base cases, edge cases, and corner cases — well enough that a developer could build it without asking a single question

---

## ⏱️ Session Overview — 60 Minutes Total

| Time | Phase | What Happens |
|---|---|---|
| **0:00 – 0:35** | ✍️ Team Exercise | Work in your team. Open the shared Word document and write the complete, end-to-end process for making a PB&J sandwich. Every step must be fully documented before time is called. |
| **0:35 – 0:50** | 🔍 Solution Review | The instructor solution is shared with your team. Read it. Compare it against what you wrote. Where did your process match? Where did it fall short? What did your team assume without writing it down? |
| **0:50 – 1:00** | 💬 Full Group Discussion | Return to the main room. Each team shares their key takeaway. Why does a simple PB&J sandwich make a difference as a BA training exercise? What does it reveal about how you write requirements? |

> 💡 **The exercise ends when the discussion ends — not when the document is finished.** The gaps your team finds during the review are the most valuable part of the session.

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
| **Given / When / Then** | A structured way to write acceptance criteria. **Given** = the starting state. **When** = the action that occurs. **Then** = the expected outcome. |

---

## 📊 Complexity Scale

Every case you write must be rated by complexity. This tells the development team how much logic, error handling, and effort is required to build it.

| Level | Maps To | What It Means for the Developer |
|---|---|---|
| 🟢 **Low** | Base Case | Standard input, predictable output. Straightforward to build. |
| 🟡 **Medium** | Edge Case | Unusual but valid condition. Requires conditional logic and validation. |
| 🔴 **High** | Corner Case | Multiple unusual conditions at once. Requires defensive logic, fallbacks, and testing. |

---

## 🧠 The Exercise

As a team, your task is to open a shared Word document and write the complete, end-to-end process for making a Peanut Butter and Jelly sandwich — from acquiring the ingredients all the way through serving the final product. For every step in the process, your team must write:

1. The **full description** of what happens in this step
2. The **base case** — standard input and expected output (🟢 Low)
3. At least **2 edge cases** — unusual but valid conditions (🟡 Medium)
4. At least **1 corner case** — two or more unusual conditions at the same time (🔴 High)
5. The **failure path** — what happens if this step cannot be completed
6. The **acceptance criteria** — how do you know this step is done correctly
7. At least **one Given / When / Then** scenario per case

The document must be written with enough clarity and detail that a developer who has never made a sandwich — and who will ask no follow-up questions — could build the process exactly as you intended.

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
- [ ] The document reads as if the team assumed the reader knows nothing
- [ ] Every team member has contributed and reviewed at least one step

---

## 💬 Final Thought

If your team cannot fully define a sandwich, your team is not ready to define a feature.

Every assumption you skip becomes a bug. Every edge case you miss becomes a support ticket. Every corner case you overlook becomes a production incident.

The sandwich is simple on purpose. The thinking — and the writing — is the exercise.

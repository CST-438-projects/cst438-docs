# CST 438 — Software Engineering
## Project 2 Metacognitive Postmortem

**Submission type:** Individual
**Suggested length:** 600–900 words (not counting section headers or the rubric)
**Format:** Markdown (`.md`) or PDF
**Due:** End of Week 4, alongside your final sprint retrospective

---

## What This Is and Why It Matters

A retrospective tells you what happened. A postmortem asks you to go a level deeper: why did it happen, and what does it reveal about how you learn and work?

That second question is metacognition — thinking about your own thinking. Research on expert software engineers consistently shows that the ability to accurately assess your own skills, recognize your blind spots, and deliberately adjust your approach is one of the most reliable predictors of long-term growth. It is also one of the hardest skills to develop, because it requires honesty that is uncomfortable and specificity that is easy to avoid.

This assignment is not a summary of your project. It is an examination of your experience as a learner and collaborator. Vague statements like "I learned a lot" or "communication could have been better" earn no credit here. What you learned, specifically, and what went wrong with communication, specifically, and what you are going to do differently — that is the work.

Write in first person. Be direct. A good postmortem reads like an honest conversation with a senior engineer who wants to help you improve, not like a status report you are filing to avoid trouble.

---

## Section 1: Your Role and Contribution

Start by establishing what you actually did. Do not describe the team's work in aggregate — describe yours. Link to at least three GitHub issues or pull requests you authored or meaningfully contributed to, and briefly describe what each one involved technically.

Then reflect: Was your workload distributed evenly across the four sprints, or did it cluster? If it clustered, why? Were there stories you picked up because they interested you, stories you avoided because they intimidated you, or stories you took on because no one else would? What does that pattern tell you about how you operate under deadline pressure?

---

## Section 2: Technical Learning

Project 2 deliberately introduced technology you had not used before — or had used only shallowly. Think about Spring Security and the OAuth2 flow, Docker networking, REST Assured integration tests, GitHub Actions CI, or whatever piece of the stack was genuinely new to you.

Pick one or two technical areas where you struggled most and describe your learning process in concrete terms. What was your first mental model of how it worked? Where did that model break down? What resource, experiment, or conversation finally made it click? "I watched a YouTube video and it made sense" is not enough — describe what specifically shifted in your understanding.

Also consider: when you were stuck, what did you do? Did you search documentation first or Stack Overflow first? Did you ask a teammate quickly or struggle alone longer than you should have? Did you reach for a working example or try to reason from first principles? There is no right answer, but recognizing your default problem-solving pattern is the first step toward improving it.

---

## Section 3: Team Dynamics and Collaboration

The GitHub workflow in this project was not arbitrary — branch protection rules, mandatory PR reviews from two teammates, issues linked to milestones, and weekly retrospectives were all intentional scaffolding for professional collaboration. Reflect on how well your team actually used those structures versus treating them as boxes to check.

Consider: How were technical decisions made? Was there a moment when you disagreed with a teammate's approach but went along with it anyway — or pushed back? What happened? If one person effectively led the technical direction, how did that affect the rest of the team's learning? How quickly did your team surface problems when something was behind schedule, and what made it easy or hard to be honest about that?

Be specific. "We communicated well" or "we had some conflicts" tells a reader nothing. Describe a real moment.

---

## Section 4: Process and Professional Growth

Agile, at its best, is a feedback mechanism — short cycles, frequent inspection, and deliberate adaptation. At its worst, it is overhead that gets in the way of building things. Where did your team's process fall on that spectrum, and why?

Reflect on the sprint structure specifically. Did your team's Sprint 1 decisions hold up, or did you make commitments you couldn't keep? How did your sprint planning improve (or not) across the four weeks? Were your user stories well-scoped, or did you discover mid-sprint that acceptance criteria were ambiguous? What does that reveal about how your team approaches planning under uncertainty?

Also consider the CI pipeline and PR review process. Did your GitHub Actions workflow catch real bugs, or did it feel like a formality? Were PR reviews substantive conversations or rubber-stamp approvals? If reviews were shallow, what would have needed to be different for them to be genuinely useful?

---

## Section 5: Looking Forward

This section is forward-looking, not backward-looking. Based on everything above, identify two or three specific, concrete changes you intend to make in your next team project.

These should be precise enough to be actionable. "Communicate better" is not a change — it is a wish. "Draft acceptance criteria before starting any story and review them with a teammate before moving the issue to In Progress" is a change. "Start Docker configuration in the first week rather than assuming it will be easy to add later" is a change. "Ask for help after 30 minutes of being stuck rather than 3 hours" is a change.

Explain why each change is warranted by something specific you observed about yourself or your team during this project. The goal is not to beat yourself up — it is to leave this project with a plan you will actually use.

---

## Grading Rubric

This assignment is graded on the quality of reflection, not the quality of the project outcome. A team that struggled and reflects honestly will score higher than a team that succeeded and describes it superficially.

| Criterion | Excellent (full credit) | Partial credit | Minimal credit |
|---|---|---|---|
| **Specificity and Evidence** | Claims are supported by concrete examples: specific PRs, named technologies, described moments. Nothing is vague. | Some claims are specific, others are asserted without support. | Most claims are generic ("we worked hard," "I learned a lot") with no grounding in actual events. |
| **Depth of Analysis** | The writing explains *why* things happened and what they reveal about the student's habits or assumptions — not just *what* happened. | The writing occasionally moves from description to analysis but frequently stops at the surface. | The writing is primarily a summary of project events with little or no self-examination. |
| **Technical Reflection** | The student accurately describes a specific gap in their mental model, how it was resolved, and what the learning process revealed about their approach to unfamiliar technology. | The technical section is present but stays at a high level ("OAuth2 was confusing but I figured it out"). | Technical learning is mentioned but not examined. |
| **Team and Process Honesty** | The student describes team dynamics candidly, including friction, imbalance, or process failures, without deflecting blame onto others or being gratuitously negative. | The student acknowledges some team challenges but hedges significantly or frames everything diplomatically without substance. | Team section is either entirely positive or vague to the point of being meaningless. |
| **Forward-Looking Specificity** | At least two concrete, actionable changes are identified and directly tied to observed patterns from this project. | Changes are identified but are too abstract to be genuinely actionable, or the connection to observed patterns is weak. | Forward-looking section describes generic intentions with no clear connection to this project's experience. |

---

## A Note on Length

The 600–900 word target is a floor and a ceiling. Below 600 words almost always means you are staying surface-level; a single paragraph per section cannot hold the specificity this assignment requires. Above 900 words often means you are summarizing the project rather than reflecting on your experience in it. If you find yourself listing features you built, you have drifted off course — return to examining yourself.

---

*CST 438 — Spring 2026*

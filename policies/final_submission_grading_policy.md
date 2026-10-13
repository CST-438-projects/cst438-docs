# Final submission grading policy (all projects)

**Drew, 2026-09-24. Applies to Project 01, Project 02 and Project 03 from SP27 onward, and to
P2 and P3 in FA26.**

## The rule

**A final submission is graded on what exists in GitHub and what is reachable on the internet.
Nothing in a final-submission rubric may require watching a video.**

The video is graded separately, by the **presentation assignment**. Two assignments, two
questions:

| Assignment | Asks | Evidence |
|---|---|---|
| Final submission | Did you build and ship the thing? | The repository, the deployed URL, the README, the CI run |
| Presentation | Can you show and explain it? | The video |

## Why

Three reasons, in order of how much they cost:

1. **A video is not a deliverable, it is a claim about one.** A recording proves the app ran once
   on one laptop. The repository proves the team actually has it. In FA26 P1 several teams
   submitted screenshots of checks passing against config that was never committed, which a video
   would not have caught either.
2. **It makes grading unreproducible.** Anything scored by watching cannot be re-checked later,
   cannot be verified by a TA, and cannot be explained to a student who disputes it. Repository
   evidence can be pointed at.
3. **It splits one skill into two grades badly.** Building the thing and presenting the thing are
   different skills. Grading them in one row means a team with a weak demo loses points for work
   they actually did, and a team with a slick video gains points for work they did not.

## What replaces the video in a final-submission rubric

Ask for the proof to be **in the deliverable**:

- **A green CI run on the default branch**, or a documented build a grader can reproduce from the
  README.
- **Screenshots of the running app committed to the repo**, not linked from Drive.
- **A live URL** where the project is deployed (P2 and P3 both require hosting anyway).
- **Tests that exercise the core loop.** A passing integration test is stronger evidence that
  login-then-fetch-then-persist works than a recording of someone doing it.
- **A README a stranger can follow.** If a new person cannot get it running, the team has not
  finished.

## Status

- **P1 SP27:** `__projects/project_01/rubrics/p1_final_submission_rubric_SP27.csv` implements
  this. Same 30 points and the same 20 TEAM / 10 YOU split as FA26; the "Video and README" row
  becomes "README and reproducibility", and the MVP row is scored by reading the repository.
- **P1 FA26:** the live rubric (Canvas 51130) still has the video-dependent rows. Graded for FA26
  with those rows marked provisional and flagged for review.
- **P2 and P3:** the project prompts must keep the video out of the final-submission rubric and
  point it at the presentation assignment instead. See
  `2604_Fall/cst438_fa26/p2_groups/Project 02_ REST API v2.md`.

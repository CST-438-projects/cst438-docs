<!-- Canvas 614125 'Project 01 GROUP: Retrospective' (15 pts, group, PDF upload). Mirrors p1_retrospective_assignment.html; synced from Canvas prod 2026-10-01. Rubric: rubrics/p1_retrospective_rubric.csv -->

## **<u>Goal</u>**

Write a **post mortem** for Project 01: an honest look at what your team
actually did, why things went the way they did, and what each of you
carries into your next project.

This is not the final submission for Project 01 and it is not
documentation of how the app works. Those go in **Project 01: Final
Submission (GROUP)**. This assignment is about the *process*.

**Every teammate must contribute in writing.** Part of this grade is the
team's document and part of it is your own section, graded individually.
If you write nothing, you lose your individual points and your team
keeps theirs.

## **<u>Where the post mortem lives</u>**

The post mortem is **committed to your team repo** as markdown, in a
folder called `docs/postmortem/`. One shared team file, plus **one file
per person, committed by that person**:

docs/postmortem/00_team.md \<- the team writes this together
docs/postmortem/rivera.md \<- one file per member, named by last
docs/postmortem/okafor.md name, in lower case, committed by
docs/postmortem/nguyen.md that member docs/postmortem/kowalski.md

So if your last name is Nguyen, you create and commit
`docs/postmortem/nguyen.md`. Hyphenated last names keep the hyphen.

Two reasons it works this way. One file per person means you will not
fight merge conflicts while writing. And the commit history is how I can
see that everyone contributed, so **commit your own file yourself**
rather than sending your text to a teammate to paste in.

Then **one** member exports the whole thing to a single PDF and submits
it here. One submission covers the group.

## **<u>What goes in the team file</u>**

In `docs/postmortem/00_team.md`, written together:

1.  **Context.** One paragraph: what you set out to build, and what
    actually shipped.

2.  **By the numbers.** Real counts from your repo, with links:

    - Issues opened, and how many closed
    - Pull requests opened, and how many merged
    - Stories or issues you planned at the start, against how many are
      done

    Go look these up. Estimates and round numbers read as guesses, and I
    can check.

3.  **What went well.** Two or three specific things. "Good teamwork" is
    not specific. "We set up the Room database early, so the UI work was
    never blocked on it" is.

4.  **What went wrong.** Two or three things, and for each one **why it
    happened**. The cause is the point, not the complaint.
    - Keep it **blameless**: critique decisions, processes and tooling,
      not teammates. "Nobody reviewed PRs for four days" is a process
      problem. "Alex is lazy" is not analysis, and it will cost you
      points.
    - "We missed the deadline because we ran out of time" is a
      restatement, not a cause. Why did you run out of time?

5.  **Advice to our next teams.** Two or three things you would tell the
    teams you are each about to join. You are being reshuffled for
    Project 02, so this is the part that outlives this team.

## **<u>What goes in your own file</u>**

In `docs/postmortem/<yourlastname>.md`, written and committed by you:

1.  **Your links.** Your merged pull requests and your issues. Yours,
    not the team's.

2.  **Your role.** What did you actually build?

3.  **Your biggest challenge.** What was it, why was it hard, and how
    did you handle it?

4.  **The most valuable thing you learned.**

5.  **Two commitments you carry into Project 02.** Project 02 has new
    groups, so your team's habits do not transfer but you do. Name two
    things *you personally* will do differently, and for each one say
    **how you will know it worked**.

    **Start from the feedback your teammates gave you** in the Final
    Teammate Review, which I will have sent you. If you are dismissing a
    piece of it, say so and say why. That is a legitimate answer;
    ignoring it silently is not.

    - Good: "I will open an issue before I start coding, and I will know
      it worked if every P2 pull request I open links to an issue that
      existed first."
    - Not good: "I will communicate better." There is no way to tell if
      that happened.

    You will be asked about these again at the Project 02 midpoint
    retrospective.

## **<u>Skeleton to copy</u>**

Paste this into your files and fill it in.

\# Project 01 Post Mortem - \[team / repo name\] \## Context \[What we
set out to build. What actually shipped.\] \## By the numbers - Issues
opened: \[n\] (\[link\]) \| closed: \[n\] - Pull requests opened: \[n\]
(\[link\]) \| merged: \[n\] - Planned at kickoff: \[n\] stories \| done:
\[n\] \## What went well 1. \[Specific thing, and why it helped\] \##
What went wrong 1. \[Specific thing\] - Cause: \[why it actually
happened\] \## Advice to our next teams 1. \[What you would tell the
team you are about to join\]

\# \[Your Name\] - Project 01 Retrospective \## My work - Merged PRs:
\[links\] - My issues: \[links\] - What I built: \[your role\] \##
Biggest challenge \[What it was, why it was hard, how you handled it\]
\## Most valuable thing I learned \[...\] \## What I carry into Project
02 1. \[Commitment\] - I will know it worked if \[check\] 2.
\[Commitment\] - I will know it worked if \[check\]

## **<u>How this is graded</u>**

See the rubric. Two things to know about how it works:

- The **\[TEAM\]** rows are the same for everyone in the group.
- The **\[YOU\]** rows are graded **per person**, from your own file and
  your own commit. Teammates can receive different grades on this
  assignment.

Your teammates' feedback about you comes from the **Project 01 SOLO:
Final Teammate Review**. I send it to you with names removed, along with
how your self-ratings compared to theirs. Their ratings do not change
your score on this assignment or on that one. What they wrote is the raw
material for your commitments below.

## **<u>Turn in</u>**

- **In the repo:** `docs/postmortem/00_team.md` plus one file per
  member, each committed by that member.
- **In Canvas:** one PDF of the whole post mortem, submitted by one
  member for the group. The PDF must include a link to your repo.

Canvas will only accept a PDF here.

#### CLOs addressed:

CLO1:G, CLO4:CDE, CLO5:AB

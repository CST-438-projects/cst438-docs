# Project 02 GROUP in class: API Proposal Session (~60 min prep, 8 min in class)

**Points:** 20  **Submission:** a URL to `docs/proposal.md` in your team's repo, one submission per team
**Due:** before class on the proposal session day. You present in class.

## What this is

Before you write a line of Spring Boot, your team pitches the API it wants to build and gets it
**approved**. This is not a sales pitch and it is not the design review. It is a short, honest
check that your idea is big enough to satisfy Project 02, small enough to finish in four sprints,
and shaped like an API rather than a pile of screens.

The Sprint 1 design review (end of Sprint 1) goes deep on your `openapi.yaml`, error model, and ER
diagram. Today is the rough draft of those artifacts. Being wrong today is cheap. Being wrong in
Sprint 3 is not.

**No mockups.** The Android app is four small screens and polish earns nothing. Spend your time on
the data and the endpoints.

## What you will do

1. **Pick a domain.** Choose one of the five in the Project 02 prompt or propose your own. Whatever you
   pick must have **users plus at least two other resource types** with **meaningful relationships**
   between them.
2. **Write `docs/proposal.md`** in your repo using the template below. Merge it to `main` through a
   pull request. Yes, even this.
3. **Set up your repo for Sprint 1.** Turn on branch protection so merges to `main` require a PR.
   Create a GitHub Project board and a **Sprint 1** milestone.
4. **Present in class.** You get 5 minutes to present and about 3 minutes of questions from me and one
   other team. Present straight from `proposal.md` on GitHub. No slides needed.
5. **Record the outcome.** Before you leave, open an issue titled `Proposal feedback` that lists every
   change we asked for, and attach it to the Sprint 1 milestone.

### Outcomes

| Outcome | Meaning |
|---|---|
| **Approved** | Start Sprint 1. |
| **Approved with changes** | Start Sprint 1. The `Proposal feedback` issue must be closed by the end of Sprint 1. |
| **Revise and resubmit** | Fix it and show me by the next class. Your score is not capped, but Sprint 1 does not wait for you. |

## `docs/proposal.md` template

```markdown
# <API name> Proposal

## 1. The pitch (one paragraph)
What the API does, who uses it, and why a client app would need it.

## 2. Resources
| Resource | Key fields | Relationships |
|---|---|---|
| User | id, email, displayName, role | a User has many Workouts |
| ... | ... | ... |

## 3. ER sketch
A Mermaid `erDiagram` (renders on GitHub) or an embedded image. Show tables, primary and foreign
keys, and cardinality (one to one, one to many, many to many).

## 4. Endpoints
| Verb | Path | Auth | Purpose |
|---|---|---|---|
| GET | /api/v1/workouts?page=0&size=20 | user | list my workouts (paginated) |
| ... | ... | ... | ... |
Mark each endpoint `public`, `user`, or `admin`. Mark which collection paginates and which
filters or sorts.

## 5. Technical choices
- **Database host:** (Neon, Supabase, Railway, Atlas, ...) and why
- **OAuth2 provider:** (Google, GitHub, Auth0) and confirmation that it supports Authorization Code + PKCE from a native app
- **Repo layout:** monorepo or split, and why
These become your ADRs later.

## 6. Risks
The two things most likely to go wrong, and what you will do first to find out.

## 7. Team and Sprint 1
Who owns what in Sprint 1. Link your Project board and Sprint 1 milestone.
```

## Requirements checklist

- [ ] Users plus at least **2 other resource types** with real relationships (at least one one-to-many; many-to-many is a bonus)
- [ ] Endpoints use all five verbs (**GET, POST, PUT, PATCH, DELETE**) across your resources, all under `/api/v1/`
- [ ] At least one collection endpoint **paginates** and at least one **filters or sorts**
- [ ] The prompt's required user routes: admin `GET /api/v1/users`, `GET`/`PATCH`/`DELETE /api/v1/users/{userId}`, plus `DELETE /api/v1/users/me` (a user deletes their own account and data)
- [ ] Every endpoint marked public, user, or admin
- [ ] Branch protection on `main`, a Project board, and a Sprint 1 milestone
- [ ] At least **5 user-story issues per team member** in the format *"As a [role], I want to [action] so that [benefit]"*, each with an acceptance criterion and attached to a Sprint milestone
- [ ] `proposal.md` merged to `main` through a reviewed PR

## Grading

Graded live in the session. **If you are not present when your team presents, you get 0.** Showing
up after your team's slot counts as absent.

## Goal and Learning Outcomes

The goal is to practice designing an API before building it: modeling the data, naming the
resources, and scoping the work to four sprints, then taking and acting on design feedback.

CLOs: CLO1b,f, CLO3, CLO4a,b,d,e

---

# Rubric: P2 API Proposal Session (20 pts)

| Criterion | Full marks | Partial | Low / none |
|---|---|---|---|
| **Domain and scope** (3) | **3:** Clear one-paragraph pitch. Users plus at least 2 other resource types with meaningful relationships. Scope fits four sprints. | **1.5:** Only 1 non-user resource, or relationships are trivial, or scope is clearly too big or too small. | **0:** No pitch, or not an API (for example, a UI with no real data model). |
| **Resource model and ER sketch** (4) | **4:** Every resource shown with primary keys, foreign keys, and cardinality. Matches the endpoint list. | **2:** ER sketch present but missing keys or cardinality, or it disagrees with the endpoints. | **0:** No ER sketch. |
| **Endpoint list** (5) | **5:** Every planned endpoint listed with verb, path, and auth level. All five verbs used. Routes under `/api/v1/`. Resource-style names (nouns, not verbs). At least one paginated and one filtered or sorted collection. The four admin `/users` routes plus account self-delete. | **3:** List present but missing one or two of: a verb, pagination, filter/sort, the admin/self-delete user routes, or auth labels. Or some routes are verb-style (`/getWorkouts`). **1:** Only a handful of endpoints, or no auth levels marked. | **0:** No endpoint list. |
| **Technical choices and risks** (3) | **3:** Database host, a PKCE-capable OAuth2 provider, and repo layout, each with a one-line reason. Two concrete risks, each with a first step to test it. | **1.5:** Choices listed without reasons, or risks vague ("time management"). | **0:** Missing. |
| **Sprint 1 setup and backlog** (3) | **3:** Branch protection on `main`. Project board and Sprint 1 milestone exist. At least 5 user-story issues per member, each with an acceptance criterion and a milestone. Clear Sprint 1 ownership. `proposal.md` merged through a PR. | **1.5:** Most of it is there, but fewer than 5 stories per member, stories missing acceptance criteria or milestones, or no branch protection. | **0:** No issues, or no repo setup. |
| **Presentation and feedback** (2) | **2:** Presents within 5 minutes and answers questions. `Proposal feedback` issue opened before leaving, listing the requested changes. | **1:** Over time, or couldn't answer basic questions about the design, or no feedback issue. | **0:** Not present. |

**Not present:** 0 on every criterion.

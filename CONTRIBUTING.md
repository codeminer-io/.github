# Contributing to CodeMiner

This document describes how we work across the `codeminer-io` repositories.
Keep it short.

## TL;DR

- File issues using the **Story / Task** template. `Context` and
  `Acceptance Criteria` are required.
- Rough idea? Open a blank issue, one line is fine - it lives in `Unrefined`
  until triage.
- Bugs use the **Bug report** template.
- Board flow: `Unrefined` → `Backlog` → `In Progress` → `Review/QA` → `Done`.
- One PR per logical change. Reference the issue with `Closes #123`.
- Weekly 30-min board review. Daily async standup in Slack.
- Decisions go in issues or PRs, not Slack threads.

## How work flows

1. **Idea arrives** - from a user, a paper, a Slack message, a standup.
2. **Issue is filed** using the Story / Task template. `Context` and
   `Acceptance Criteria` are required. `Out of scope` is filled in either
   at filing time or during triage.
3. **Triage** happens during the weekly board review. We agree `Out of scope`,
   add labels, and move ready issues to `Backlog`.
4. **Pick up work** by moving an issue from `Backlog` to `In Progress` and
   assigning yourself. One issue per person at a time is the norm.
5. **Open a PR** referencing the issue (`Closes #123`). Small, focused PRs.
6. **Review** by the other team member. Move the card to `Review/QA`.
7. **Merge and close** the issue. Card moves to `Done`.

### When to skip the template

- **Rough capture** - if you just want to grab an idea before you forget,
  open a blank issue with a line or two. It lives in `Unrefined` until
  triage, where we either flesh it out using the Story template or close it.
- **Epic / multi-part work** - open a blank issue with a short overview and
  a task list of sub-issues. File the sub-issues using the Story template
  as they become ready to work on, not all up front.

## Board columns

- **Unrefined** - idea captured but not yet workable. Missing scope, unclear
  acceptance, or depends on something else.
- **Backlog** - ready to pick up. Clear acceptance and scope.
- **In Progress** - actively being worked on. Assigned to one person.
- **Review/QA** - PR open, waiting for review or in CI.
- **Done** - merged.

## Definition of ready

An issue is ready to move to `Backlog` when:

- `Context` is filled in - we know who it's for and why.
- `Acceptance Criteria` is specific enough to know when it's done.
- `Out of scope` is filled in if the issue is at risk of ballooning.
- No unresolved dependencies (or they're noted in the issue).

## Definition of done

A PR is ready to merge when:

- The behaviour described in the linked issue works (manually verified).
- Tests pass. New behaviour has at least one test where reasonable.
- Documentation is updated if user-facing behaviour changed.
- The other team member has reviewed and approved.

## Cadence

- **Daily standup** - async in Slack or quick call. What did you do, what
  are you doing, what's blocked.
- **Weekly board review** - 30 minutes. Triage `Unrefined`, sanity-check
  `Backlog`, surface blockers.

## Branching and PRs

- Branch from `main`. Name branches `<initials>/<short-description>` or
  `<issue-number>-<short-description>`.
- One logical change per PR. If you find yourself writing "and also..." in
  the PR description, split it.
- PRs reference the issue they close.
- Squash on merge unless there's a reason not to.

## Communication norms

- Slack for anything that needs a same-day answer.
- GitHub issues and PRs for anything that needs to be findable later.
- If a Slack discussion produces a decision, the decision goes in an issue
  or a PR - not just the Slack thread.

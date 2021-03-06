### Grooming

- Presents tickets from the backlog
- Used to attribute story points
- Rough estimate of the time a given ticket will take (optional)
- Tickets that are estimated may not be pushed to next sprint

---

### Sprint planning

- Used to discuss tickets from the current sprint (before sprint starts)
- Used to chunck stories into sub-tasks
- 1 sub-task = 4h max
- Chose sub-tasks from template
- Additional sub-tasks may be added during sprint planning (will affect burndown)

---

### List of possible sub-tasks

- Analysis / Architecture / Technical Design
- Impact analysis
- Test strategy
- DB schema migration
- DB data migration
- New Entity/Repository creation/generation
- Service creation/generation (includes Unit tests)
- Controller/Action creation/generation (includes Unit tests)

---

### List of possible sub-tasks

- Automated tests (integration, API etc...)
- Additional Unit tests
- Manual tests execution (scripts)
- UI tests execution
- Code review
- Documentation
- ...

---

### Working on a ticket

- Analysis, Impact Analysis and Test strategy needs to be done first
- At least 2 devs on each ticket
- Extensive QA should be performed by developers
- Final code review should be performed by a dev who did not work on the ticket
- When merging, squash into a single commit

---

### Working on a ticket

- Branch off trunk and create a "feature" branch
- Each sub-task corresponds to a new branch from feature branch
- Each sub-task requires its PR (1 dev approval) and is merged back into feature branch
- Working branches need to start with the sub-task ID (for time tracking, auto-merging etc...)

---

### Working on a ticket

- After code is done, "final" code review can start
- QA is performed by developers or QS if available (can be done in parallel of the code review)
- QA cannot be performed by a developer who worked on the ticket
- If QA requires external components, feature branch needs to be deployed to be tested

---

### Working on a ticket

- When QA is done, code can be aproved and merged into trunk
- Only a smoke test of the trunk is required at this point

---

### Pros

- Because sub-tasks are chosen from a bucket, less risk to forget something => timing is more accurate
- A task is merged only when it's fully tested
- Sub-tasks make it easy to program in parallel
- Impact Analysis and Test strategy are done by developers and reviewed by QS prior to coding

---

### Pros

- Sub-tasks are merged into the feature branch as they're done => available to other developers working on the same branch w/o impact on the trunk
- No need to squash when merging to the feature branch => keeps history easy to follow
- Squashing before merging into trunk makes history compact, and it's easier to cherry-pick things
- Devs are more implicated into testing what the team is doing

---

### Pros

- No hands-off to QS
- No half-baked feature into trunk
- Small sub-tasks = small code reviews = move quickly
- Early analysis = less risk to get big changes required in code review
- Final code review is just an overview of the code since sub-tasks PRs have been reviewed

---

### Cons

- Takes a lot of time during sprint planning
- Requires a good knowledge of the code base to be able to know in advance what's involved
- Requires all sub-tasks to be created before the sprint starts to get a proper burndown
- Branch manipulation can be tricky
- Final code review may still be bottle necks

---

### Cons

- Code is tested on local environments since the feature branch is tested and not the trunk
- Works well with features, not that well for bugs (depends on incertainty)



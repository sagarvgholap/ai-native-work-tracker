# AI Team: Shared Rules for All Agents

These rules apply to every agent on the AI-Native Work Tracker: the three full-stack developers, the QA agent, the UAT agent and the PM/BA agent. The accountable human is Sagar. AI agents are never accountable; they work inside these guardrails and a human approves what ships.

## 1. Work only through tickets

- Every piece of work starts from a Jira ticket in project ANWT. No ticket, no work.
- Read the ticket's description and Given/When/Then acceptance criteria before starting. If they are unclear, ask the PM/BA agent or the human; do not guess.
- Never change a ticket's story points, acceptance criteria or sprint. Only the PM/BA agent and the human do that.

## 2. Work only through pull requests

- Never commit directly to main, uat or qa. Branch from dev.
- Branch name: ANWT-\<number>-short-description. Commit messages and PR titles start with the ticket key, for example ANWT-5: set up monorepo structure.
- Promotion path: dev, then qa, then uat, then main (production). Each step needs its own green test run and a review.
- Every PR must state: the ticket key, what changed, how it was tested, and anything uncertain.

## 3. Leave a trail

- Move the ticket to In Progress when starting and to In Review when tests are green.
- Comment on the ticket with what was done, the PR link, and test results. Every action must be traceable to a ticket.
- If an action cannot be tied to a ticket, stop and ask.

## 4. Hard limits

- Never touch production, and never deploy to it. Only the human approves production.
- Never handle, create, print or commit real secrets, keys, passwords or tokens. Use placeholder values and environment variables, and list any new variable in the PR.
- Never create or use AWS access keys. Cloud changes are made by the human.
- Never delete branches, tickets or history, and never force-push.
- Never turn off tests, linting or security checks to make a build pass.

## 5. Quality bar

- Follow the coding standards in the repo's contribution guide.
- Every change comes with tests. A ticket is Done only when the code is merged, tests are green, QA has passed it, the UAT agent has checked it, and docs are updated.
- Use structured logging with request IDs and the agreed error format. Never leak internal details in errors.
- Keep changes small and focused on one ticket.

## 6. Honesty and escalation

- Say plainly when something is uncertain, failing or incomplete. Never claim tests passed without running them.
- Never invent requirements. If blocked, flag the ticket with an Impediment, comment why, and tell the human.
- Anything affecting security, data loss, cost, or scope goes to the human before action.
- Do not review your own work. The author of a change never approves it.

## 7. Blog material

- When something surprising, broken or instructive happens, add a short note to the ticket so it can feed the weekly Journey post or an Under the Hood deep dive.

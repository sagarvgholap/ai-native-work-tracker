# AI-Native Work Tracker: Instructions for AI Agents

Mission: one person, an accountable AI team, fully traceable.
The accountable human is Sagar. You are an AI agent, and AI agents are never accountable. Work inside these rules, and a human approves what ships.

## Read first, every session
1. docs/ai-team/shared-rules.md: rules every agent follows.
2. docs/ai-team/role-briefs.md: find your role (Dev 1, Dev 2, Dev 3, QA, UAT or PM/BA) and follow its Does and Never lists.
3. docs/specs/: the approved spec for your ticket. No approved spec means no code.

## Project at a glance
- Product: a Jira-inspired work tracker with users and roles (admin, member, viewer), projects, tickets, board, sprints, comments and an audit log.
- Stack: Python with FastAPI (backend), React (frontend), PostgreSQL, Redis, Docker, GitHub Actions, AWS.
- Layout: a monorepo with frontend/, backend/, docs/ and infra/.
- Tracking: Jira project ANWT at sagar-gholap.atlassian.net. Story points use the Fibonacci scale up to 13.

## Working rules in short
- Start from a Jira ticket and its approved spec. Never work without a ticket.
- Branch from dev as ANWT-<number>-short-description. Commit messages and PR titles start with the ticket key.
- Open a pull request into dev. Never commit directly to dev, qa, uat or main.
- Promotion path: dev, then qa, then uat, then main (production). Each step needs green tests and a review.
- Never review or merge your own work. A human approves everything that reaches main.
- Never touch production, real secrets, keys or the cloud account. Use placeholders and environment variables.
- If the spec is wrong or unclear, stop and say so. Fix the spec first, in its own pull request.
- Leave a trail: move the ticket's status, comment with the PR link and test results, and note anything surprising for the blog.

## Commands
(To be filled in as the project is built: start the stack, run tests, lint.)

## When unsure
Ask the human. Say plainly what is uncertain, failing or incomplete. Never claim tests passed without running them.

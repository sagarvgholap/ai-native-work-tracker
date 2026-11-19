# Spec template

Copy this for each story. Keep it short: one or two pages at most.

**Title:** ANWT-\<number>: \<story name> **Status:** Draft, Approved, Built or Changed **Epic:** \<epic key and name> **Story points:** \<Fibonacci value> **Owner:** \<developer agent assigned> **Approved by:** \<human, and date>

### 1. Goal

One or two sentences: what this delivers and why it matters.

### 2. Scope

**In scope:** what this story includes. **Out of scope:** what it deliberately does not include.

### 3. Behaviour (Given / When / Then)

The acceptance criteria from the Jira story, expanded where needed, one scenario at a time.

### 4. Interfaces

API endpoints (method, path, request and response shape), screens, commands or files this story adds or changes. Use the agreed error format.

### 5. Data

Tables, fields, constraints, migrations. Note anything that must never be stored in plain text.

### 6. Edge cases and failure modes

What happens with bad input, missing permissions, empty states, concurrent actions, and service failures.

### 7. Security and logging

Who is allowed to do this, which role checks apply, and what gets logged (with request ID). Anything sensitive that must not appear in logs.

### 8. Test plan

Which unit, integration and end-to-end tests prove each behaviour. QA and the UAT agent use this list.

### 9. Open questions

Anything unresolved. A spec cannot be Approved while this list has blockers.

### 10. Change log

Date, what changed, who approved, and the pull request link.

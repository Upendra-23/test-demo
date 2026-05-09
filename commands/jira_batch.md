# Command: /jira_batch

This command starts the orchestrator on a batch of JIRA issues.

## Trigger

Type:

```text
/jira_batch PROJ-123, PROJ-124, PROJ-156
```

## Behavior

- The orchestrator agent:
  - Parses comma‑ or space‑separated JIRA IDs.
  - Validates each ID with `jira_get_issue`.
  - Starts the multi‑agent workflow (Read `orchestrator.md`) for each JIRA in parallel where safe.
- Returns an interactive status table and lets you monitor progress.

## Frontmatter

```yaml
name: jira_batch
type: command
agent: orchestrator
```

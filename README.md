# rlm-action

A GitHub Action that runs [RLM](https://github.com/WSQS/rlm) (a CLI tool) to do task in given task.

## Action

### Parameters

| Name          | Description                               | Required |
| ------------- | ----------------------------------------- | -------- |
| `context`     | Task context passed to RLM                | Yes      |
| `output_file` | Optional output file path for RLM results | No       |

### Environment Variables

| Name                 | Description            | Required |
| -------------------- | ---------------------- | -------- |
| `ANTHROPIC_API_KEY`  | Anthropic API key      | Yes      |
| `ANTHROPIC_BASE_URL` | Anthropic API base URL | No       |

### Output

| Name     | Description           |
| -------- | --------------------- |
| `result` | Final stdout from RLM |

## Workflows

Example for how to using rlm action.

### Issue Processor

Automatically processes GitHub issues by reading issue details, running RLM to make code changes, and creating a PR.

**Triggers:** `issues.opened`, `issues.reopened`, `workflow_dispatch`

### PR Reviewer

Automatically reviews pull requests by reading PR details and posting review comments.

**Triggers:** `pull_request.opened`, `pull_request.reopened`, `pull_request.synchronize`, `workflow_dispatch`

# cron-scheduling-demo

This repository demonstrates scheduled workflows using GitHub Actions with cron syntax.

The purpose of this project is to show how a GitHub Actions workflow can run automatically
based on a time schedule rather than code changes.

---

## Part 2: Advanced GitHub Actions Features

### Task 3: Cron Scheduling

### Overview
This task demonstrates how to configure a GitHub Actions workflow that runs daily at a fixed time.
The workflow is scheduled to run every day at midnight (UTC) using cron scheduling.
For easier testing and learning, the workflow also supports manual execution.

---

## Workflow Triggers

The workflow can be triggered in two ways:

1. Scheduled trigger using cron (daily at 00:00 UTC)
2. Manual trigger using workflow_dispatch from the GitHub Actions UI

---

## Workflow Behavior

When the workflow runs, it performs the following steps:
1. Checks out the repository code
2. Prints a confirmation message to the workflow logs

The message printed is:
Scheduled build completed successfully!

---

## Workflow File Location

.github/workflows/scheduled-build.yml

---

## Cron Expression Explanation

The cron expression used in this workflow is:
0 0 * * *

This means:
- Minute: 0
- Hour: 0
- Day of month: every day
- Month: every month
- Day of week: every day

Note: GitHub Actions cron schedules use UTC time, not local time.

---

## Project Structure

.
├── README.md
└── .github
    └── workflows
        └── scheduled-build.yml

---

## Expected Output

When the workflow runs successfully, the GitHub Actions logs display the following message:
Scheduled build completed successfully!

---

## Summary

This repository demonstrates how to use scheduled GitHub Actions workflows with cron syntax.
It highlights time-based automation and shows how scheduled and manual triggers can be combined
to simplify testing and validation.

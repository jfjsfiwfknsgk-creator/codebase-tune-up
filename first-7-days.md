# Codebase Tune-Up Delivery SOP

Use this SOP to deliver each paid Codebase Tune-Up consistently. The goal is a clear report, a focused improvement, and a client handoff that feels professional.

## 1. Intake And Authorization

- Confirm package: Mini Tune-Up, Tune-Up + PR, Refactor Sprint, or Monthly Care.
- Confirm repository URL.
- Confirm requester identity and relationship to the repository.
- Confirm the requester owns the repository or has explicit owner permission.
- Confirm whether the repository is public, private owner-granted, or client-owned.
- Confirm preferred report language: English, Spanish, or both.
- Confirm deadline, priority areas, and any files or workflows the client cares about.
- Save the completed intake form.
- Do not begin private repository work until access and scope are confirmed.

## 2. Client Onboarding Steps

Send a short onboarding note with:

- Confirmed package and price
- Repository URL
- Authorized scope
- Expected delivery date
- Access method for private repositories
- Reminder that the service is repository-only and not penetration testing

For private repositories:

- Request least-privilege access where possible.
- Use access only for the approved review.
- Do not use repository secrets, production credentials, or external services.
- Remove or confirm removal of access after delivery if appropriate.

## 3. Repository Setup

- Clone or access only the authorized repository.
- Record branch and commit reviewed.
- Check repository status before making changes.
- Read README, contribution docs, setup docs, and package manifests first.
- Identify package manager, test command, lint command, build command, and CI workflow.
- Note if setup instructions are missing, stale, or unclear.
- Do not test live systems or external infrastructure.

## 4. Review Checklist

Review repository evidence only:

- Source files for obvious correctness and maintainability issues
- Tests for missing coverage, brittle setup, or unclear verification
- Dependency manifests and lockfiles
- Configuration files
- CI/CD workflows
- Documentation and onboarding instructions
- Existing scripts and developer commands

For every finding, capture:

- File path
- Function, class, script, config, or document reference
- Practical impact
- Suggested fix
- Estimated effort
- PR suitability

Keep only the top 5 findings in the client report.

## 5. Choose The PR

For packages that include implementation:

- Select the highest-value low-risk issue.
- Prefer changes that are small, testable, and easy to review.
- Avoid broad refactors.
- Avoid unrelated files.
- Preserve project style.
- Add or update tests if practical.
- Update docs if the improvement affects developer workflow.
- Do not introduce new dependencies unless clearly justified.

Good PR candidates:

- Add or fix a test
- Align CI with documented commands
- Clarify setup docs
- Improve a small error-handling path
- Remove low-risk duplication
- Tighten a local configuration default

## 6. Implementation

- Create a working branch.
- Make the smallest useful change.
- Keep commits focused.
- Run formatting only if it is already part of the project workflow.
- Run available tests, lint, build, or relevant checks.
- Record commands and results.
- If tests cannot run, record the reason clearly.
- Confirm the diff touches only expected files.

## 7. Report Preparation

Use `templates/report-en.md`, `templates/report-es.md`, or the sample report structure.

Include:

- Executive summary
- Repository URL
- Date
- Branch and commit reviewed
- Scope
- What was not tested
- Top 5 findings
- Recommended PR
- Business impact
- Verification steps
- Next steps
- Disclaimer that the work is repository-only and not penetration testing

Quality bar:

- Use plain language.
- Cite file evidence.
- Avoid inflated severity.
- Do not make live-system claims.
- Keep recommendations practical.

## 8. Pull Request Preparation

The PR description should include:

- Problem
- Repository evidence
- Solution
- Files changed
- Verification commands and results
- Risk level
- Rollback notes

Before sending:

- Review the diff.
- Confirm no unrelated changes are included.
- Confirm no secrets or private data are exposed.
- Confirm the PR title is clear and specific.

## 9. Client Delivery

Send:

- Report
- PR link, if included
- Short summary of the improvement
- Verification notes
- Rollback notes
- Suggested next step

Offer one clarification pass or small wording correction if needed.

## 10. Final Delivery Email Template

Subject: Codebase Tune-Up delivery for `{{repo_name}}`

Hi `{{client_name}}`,

The Codebase Tune-Up for `{{repo_name}}` is ready.

Included in this delivery:

- Repository review report: `{{report_link_or_attachment}}`
- Pull request: `{{pr_link_or_not_applicable}}`
- Verification notes: `{{verification_summary}}`
- Recommended next step: `{{next_step}}`

The review stayed within the authorized repository scope. I did not perform live-system testing, external scanning, exploitation, or production validation.

For the PR, I kept the change intentionally focused so your team can review it quickly. Rollback notes are included in the PR description.

Please review the report and PR when convenient. If anything does not match the agreed scope, send me your comments and I will make one clarification or correction pass.

Thanks,

`{{your_name}}`

## 11. Follow-Up

After 3-5 business days:

- Ask whether the report and PR were useful.
- Ask if the team wants help with the next recommended finding.
- Offer Refactor Sprint if there are several clear follow-up items.
- Offer Monthly Care if the repository changes regularly.
- Record lessons learned for future deliveries.

## 12. Satisfaction And Refund Handling

- If the report or PR misses the agreed scope, revise it once at no extra cost.
- Correct factual errors promptly.
- Keep refund discussions calm and specific.
- Do not promise refunds after completed in-scope delivery, but review reasonable requests case by case.

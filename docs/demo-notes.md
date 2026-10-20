# Demo Notes — copilot-pipeline-walkthrough-2

## Session goal
Walk a greenfield GitHub repo end to end: an issue picked up by the Copilot coding agent, a line-anchored review on a pull request, and CI actually running.

## Walkthrough script

1. **Repo setup** — fresh public repo with a README, plus a `CI Pipeline` workflow committed at `.github/workflows/ci.yml` on the default branch. It triggers on pushes and on manual dispatch, checks out the code, and echoes a greeting.
2. **Issues** — open "Add CONTRIBUTING guidance" and "Track release readiness". Assign the Copilot coding agent to the CONTRIBUTING issue so it starts on it.
3. **Branch + docs** — create `demo/notes` off the default branch and add this file, `docs/demo-notes.md`.
4. **Pull request** — open "Wire up demo notes" into the default branch.
5. **Review** — start a pending review on the PR, add an inline comment anchored to a specific line of the changed file that mentions the `CI Pipeline` job, then submit it as a plain comment (not an approval, since it's our own PR).
6. **Copilot review** — request a Copilot code review of the same pull request.
7. **CI** — fire the `CI Pipeline` workflow manually, find the run it produces, and report its id and observed status.
8. **Security check** — look for repository security advisories at the account/org level.

## Demo reminders
- Keep the review submission as a comment, not an approval — reviewers can't approve their own PR.
- Re-check the workflow run status after a minute; a completed run is the satisfying payoff shot for the audience.

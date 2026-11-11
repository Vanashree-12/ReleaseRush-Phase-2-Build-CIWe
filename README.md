# RELEASE RUSH
## Phase 2 - Build & Continuous Integration

Total Marks: 25

## INCIDENT: THE BROKEN BUILD PIPELINE

The development team has pushed a new version of the
inventory application.

The CI workflow starts successfully but fails during
dependency installation.

The automated testing and build stages are never reached.

Your team has been assigned to investigate and repair
the CI pipeline.

## YOUR TASKS

1. Inspect the failed GitHub Actions workflow.
2. Read the supplied build failure evidence.
3. Identify the incorrect dependency and version.
4. Investigate the dependency history in Git.
5. Correct the dependency configuration.
6. Run the automated tests.
7. Generate the application build artifact.
8. Verify that the complete CI pipeline succeeds.

## FILES PROVIDED

requirements.txt
app.py
tests/test_app.py
build.py
ci_check.py
.github/workflows/ci.yml
evidence/first-failed-run.log

## STEP 1 - INSPECT THE FAILURE

Read the failure evidence:

Get-Content evidence/first-failed-run.log

Also open the GitHub Actions tab and inspect the failed job.

## STEP 2 - INVESTIGATE DEPENDENCY HISTORY

git log --oneline -- requirements.txt

git log -p -- requirements.txt

Identify what changed in the dependency configuration.

## STEP 3 - REPAIR THE BUILD

Find the incorrect dependency pin in requirements.txt.

Use the repository history and package information
to determine an appropriate valid version.

Do not remove the dependency entirely.

## STEP 4 - TEST LOCALLY

python -m pip install -r requirements.txt

python -m unittest discover -s tests -v

## STEP 5 - BUILD

python build.py

## STEP 6 - VERIFY

python ci_check.py

## STEP 7 - COMMIT AND PUSH

git add requirements.txt

git commit -m "fix: correct dependency version"

git push

Open GitHub Actions and verify the workflow succeeds.

## SUBMISSION

Submit:

1. Failed pipeline stage.
2. Root cause of the failure.
3. Incorrect dependency and version.
4. Corrected dependency pin.
5. Successful test output.
6. Build artifact verification.
7. Git commit hash.
8. Final release flag.

## RULES

- Teams of 2â€“3.
- Internet search permitted.
- Work only within your team.
- Do not share answers with other teams.
- Do not remove dependencies just to bypass the failure.

Good luck!
## PARTICIPANT GITHUB SUBMISSION

1. Open the official Release Rush Phase 2 repository.
2. Click Fork to create your own copy.
3. Clone your fork:

git clone YOUR_FORK_URL

4. Enter the repository:

cd ReleaseRush-Phase-2-Build-CI

5. Fix the dependency configuration.
6. Run tests and build verification.
7. Commit and push your solution:

git add requirements.txt
git commit -m "fix: repair dependency version"
git push origin main

8. Open the Actions tab.
9. Demonstrate the successful CI workflow.

IMPORTANT:
Do not push directly to the official event repository.
Work inside your team's fork.

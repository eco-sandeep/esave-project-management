# Backlog to Production

A step-by-step process for taking an ESave feature from the backlog through to production.

## 1. Pick Up a Backlog Item

Backlog items are present in the relevant Project:

For example Release 1 is present here: https://github.com/orgs/EcoCentre-Org/projects/3/views/1

There is an example ticket [here](https://github.com/EcoCentre-Org/esave/issues/9). 
Notice the title uses the format `[DevTracker] - REQ-hg9ucs88 - Do something`, its important to leave everything as-is in the title, the `Do something` can be changed if needed. The body will contain the description of the ticket.

> **Further reading**: [Github Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)

### Steps

- Pick an item assigned to the current release with no unresolved dependencies
- Assign to yourself if not assigned already and move to `In Progress` on the project board
- Break the item into small, self-contained tasks with a clear definition of done. You can use sub-issues (try not create too many as they might cause clutter).
- Clarify requirements with the team on MS Teams if the issue description is unclear. Use a distinct Teams Post for each issue (not sub-issue !). This way all communication and support stays within that post and its threads.
- **Important**: Donot comment and tag people on the issue or sub-issues, keep communication or questions within the Teams Post for your issue.

> **Further reading**: [GitHub Issues quickstart](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart)

## 2. Set Up a Feature Branch
When starting investigation/spike/development always perform this on Feature branch. Branch should always 

```bash
git checkout main
git pull origin main
git checkout -b feature/REQ-<ID>-short-description
```

- Branch naming: `feature/REQ-<ID>-short-description` (e.g. `feature/REQ-hg9ucs88-do-something`)
- One branch per backlog item/issue

> **Further reading**: [Git feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)

## 3. Develop Locally

- Activate the Django virtual environment and run the dev server
- Make small, focused commits with clear messages
- Follow existing code patterns in the Django project
- Run the app locally and verify your changes against the issue description

```bash
python manage.py runserver
```

> **Further reading**: [Django development guide](https://docs.djangoproject.com/en/stable/intro/tutorial01/)

## 4. Test

- **Manual testing**: Walk through the feature end-to-end in a browser
- **Regression check**: Verify related features still work (login, registration, dashboard)
- **Edge cases**: Test with empty fields, invalid data and different screen sizes (responsive)
- **Database**: If migrations are needed, run and verify them

```bash
python manage.py test
python manage.py makemigrations --check
```

> **Further reading**: [Django testing overview](https://docs.djangoproject.com/en/stable/topics/testing/overview/)

## 5. Raise a Pull Request

- Push your feature branch to GitHub
- Open a Pull Request (PR) targeting `main`
- PR description should include: what changed, how to test it, and the backlog item ID
- Request a review from at least one team member

```bash
git push origin feature/REQ-<ID>-short-description 
```

> **Further reading**: [GitHub pull request guide](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)

## 6. Code Review

- Reviewer checks for correctness, readability and security concerns
- Address any feedback with follow-up commits on the same branch
- PR is approved when the reviewer is satisfied

## 7. Merge to Main

- Squash-merge or merge the PR into `main` via GitHub
- Delete the feature branch after merge

## 8. Deploy to Heroku (Production)

- Heroku deploys from the `main` branch to esave-staging.
- Verify the deployment succeeds in the Heroku dashboard
- Smoke-test the feature on the live site ([stage.esave.org.uk](https://stage.esave.org.uk))

> **Further reading**: [Heroku Django deployment](https://devcenter.heroku.com/articles/deploying-python)

## 9. Post-Deployment

- Move the backlog item to `Done` on the project board (close the GitHub Issue)
- Notify the team on MS Teams Post that the feature is in staging
- Monitor for any issues reported by testers

## Quick Reference

| Stage | Key Action | Tool |
|---|---|---|
| Backlog | Pick & assign item | GitHub Project |
| Branch | Create feature branch | Git |
| Develop | Code & local test | Django / VS Code |
| Test | Manual + automated tests | Browser |
| PR | Push & raise PR | GitHub |
| Review | Peer review | GitHub |
| Merge | Merge to main | GitHub |
| Deploy | Deploy & smoke-test to staging | Heroku |
| Close | Move to Done on project board & notify | GitHub Project / Teams |


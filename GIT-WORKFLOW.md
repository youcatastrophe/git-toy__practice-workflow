# New Feature Template

Every time you begin working on a new feature, follow this template.

## Preliminary Steps

First, identify which task you will be working on.

Next, make sure your Git repo is actually in the right state to begin a new feature:

(If this is the _very first_ feature for this project, and you haven't done any work yet, then you should skip to the 'Create Branch & Pull Request' section.)

1. Does `git status` show a clean working directory?
2. Are you currently viewing the 'master' branch?
3. Did you complete the previous task you were working on?
4. Have you merged the previous task's branch into 'master'?
5. Have you pushed to GitHub?
6. Have you done a `git pull` to ensure you have the latest version of your code?

If any of these questions return a "No" answer, you are not ready to begin a new feature.

## Create Branch & Pull Request

If you have a task defined and are ready to begin, cut a new branch for the feature: `git checkout -b new-branch-name`

Then create an empty commit in that branch to mark the beginning of the feature. The commit message must include a brief title of the feature and the Issue number associated with that feature:

`git commit --allow-empty -m "Favorite entertainer. Issue #12"`

Immediately push to GitHub and create a PR in your repo (Not OCS's) for the feature. The title of the PR should automatically get set to the commit message you just used (That's a good thing--it's an appropriate title for the PR).

## Build Feature

Work through this one feature--stay focused on just this task.

## Merging

When you are 100% complete with a task, here are the steps for merging it into 'master':

1. Make sure everything for the task is completed and committed; and that you have pushed the feature branch to GitHub.
  - `git status` should show a clean working directory. If it doesn't, do not proceed further.
2. Switch to the 'master' branch. `git checkout master`... Then:
  - `git pull` to make sure there isn't any work from GitHub that you might have missed.
3. Switch back to your feature branch. `git checkout name-of-feature-branch`... Then:
  - `git merge master` to make sure the 'master' branch merges cleanly with the feature.
    - If there is an indication of a "merge conflict", seek help from an instructor.
4. Switch to the 'master branch'. Then...
  - `git merge name-of-feature-branch` to merge the feature into 'master'.
  - `git push`
5. Now check the PR for this issue. It should indicate that its code has been merged. You can 'close' the PR.
6. Update your list of tasks in GitHub Issues.

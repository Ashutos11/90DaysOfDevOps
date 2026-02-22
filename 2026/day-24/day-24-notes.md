1. What is a fast forward merge?

A. A simple merge done from a feature branch to main.

2. When does Git create a merge commit instead?

A. If two branches have diverged then we need to create a merge commit. The parent commits are different for these branches in this case.

3. What is a merge conflict?

A. When a same file is edited in two different branches, a merge conflict is created.

4. What does rebase actually do to your commits?

A. It changes the base of a branch from where the branch was created.

5. How is the history different from a merge?

A. The feature branch joins the main branch after we run git merge whereas in rebase the base of the feature branch moves to the tip of rebased branch.

6. Why should you never rebase commits that have been pushed and shared with others?

A. Rebase rewrites history of a branch which creates new commit hashes causing conflicts for people who already have pulled the latest changes.

7. When would you use rebase vs merge?

A. Rebase is used to maintain a clean linear history of a feature branch while we merge a branch when we want to integrate our feature branch changes to main branch

8. What does squash merging do?

A. Squash merging combines multiple commits into one and merges them to mentioned branch.

9. When would you use squash merge vs regular merge?

A. I would use squash merge to combine multiple commits to have a clean history and regular merge if I have a single commit to make.

10. What is the trade-off of squashing?

A. Cannot track detailed commits, hard to debug, merge conflict risks.

11. What is the difference between git stash pop and git stash apply?

A. git stash pop brings back the most recent stash while git stash apply can bring a specific stash from the stash list

12. What does cherry-pick do?

A. It picks a specific commit that we mention from another branch and place it in the current branch. That specific commit will be visible in the history of current branch.

13. When would you use cherry-pick in a real project?

- When a specific commit is ready for release but others are not.
- When commited to a wrong branch by mistake
- When a you need to fix something in both older and current release
- When you want to keep a specific change from an abandoned branch

14. What can got wrong with cherry picking?

- Merge conflicts can occur
- Confusion and non-linear history
- Duplicate commits
- Missing context and dependencies
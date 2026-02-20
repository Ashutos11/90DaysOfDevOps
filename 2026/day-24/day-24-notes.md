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
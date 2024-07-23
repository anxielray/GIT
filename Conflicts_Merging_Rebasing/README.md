# _*Conflicts, Merging, and Rebasing*_

## _*Merging Main into Greet Branch*_

- Switch to the greet branch and attempt to merge the changes from the main branch using:

```bash
git checkout greet
git merge main
```

![alt text](<Screenshot (35).png>)

- This will create a conflict that need be resolved. We will resolve this manually in our editor.

## _*Merging with Conflicts*_

- In this example, we will resolve the conflict manually.

## _*Rebasing Greet Branch*_

- Rebase is a Git command that replays your local commits onto a new base commit, effectively "rewriting" your commit history.
- To rebase the greet branch on top of the latest changes in the main branch, use:

```bash
git checkout greet
git pull origin main
git rebase origin/main
```

- This will reapply the commits from the greet branch on top of the latest changes in the main branch.

### _*Merging Greet into Main*_

- Switch to the main branch and merge the changes from the greet branch using:

```bash
git checkout main
git merge greet
```

![alt text](<Screenshot (35).png>)

- This will create a new merge commit that combines the changes from both branches.

![alt text](<Screenshot (36)-1.png>)

### _*Understanding Fast-Forwarding and Differences*_

- Fast-forwarding occurs when you merge one branch into another and there are no conflicts. In this case, Git simply moves the branch pointer to point to the latest commit on the target branch.

- Merging and rebasing are two different ways to integrate changes from one branch into another. Merging creates a new commit that combines the changes from both branches, while rebasing rewrites the commits from one branch onto another. When you rebase a branch, you are effectively rewriting history, whereas merging preserves the original commit history.

- Here's a simple way to remember it:

  - Merging: Creates a new commit that combines changes from both branches.
  - Rebasing: Rewrites commits from one branch onto another, preserving history.
  - Fast-forwarding: No conflicts or rewriting of history occurs when merging or rebasing.

# _*Bare Repositories*_

## _*What is a Bare Repository?*_

- A bare repository is a Git repository that does not contain a working directory. It is used to store the history of a project in a central location, allowing multiple developers to share and collaborate on the project. Bare repositories are typically used as a central hub for version control, and are often used in conjunction with other Git repositories.

### _*Reason to have one*_

- Adding a remote allows you to push annd pull changes between your local repository and the remote repository. This enavles collaborationbetween multiple developers.

## _*Creating a Bare Repository*_

- Let's create a bare repository named ``hello.git`` from the existing hello repository using:

```bash
git clone --bare hello hello.git
```

## _*Adding Bare Repository as Remote*_

- Since we already had a remote repo, we will have to reset the remote origin to read from the shared bare repo instead:

```bash
git remote set-url ../hello.git
```

- To add the bare hello.git repository as a remote to the original hello repository use:

```bash
cd hello/
git remote add origin ../hello.git
```

- Update the content of the README and commit the changes, then push to the remote repository.

```bash
git push origin main
```

## _*Pulling Changes to Cloned_hello repo*_

- Switch to the cloned repository ``cloned_hello`` and pull down the changes just pushed to the shared repository using:

```bash
git fetch origin
git merge origin/main
```

- This should update the local copy of the cloned_hello repository with the latest changes from the shared repository.

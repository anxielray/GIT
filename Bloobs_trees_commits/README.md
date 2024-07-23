# _*Blobs, trees and commits*_

- _Blobs_ are the contents of the files that we make Git aware about.
- _Trees_ are the working structure of a branch.

## _*Exploring the .git/ Directory*_

- ``cd`` into the ``.git/`` directory in your project and let's examine its contents.
- The `.git` repo contains all the metadata for the your local repository.
- We will find several subdirectories and files that play a crucial role in managing our Git repository.
- Let's explore each of them:

  - _objects/_: This directory contains all the objects in your repository, including blobs, trees, and commits.
  - _config_: This file stores the configuration settings for your Git repository.
  - _refs_: This directory contains references to specific commits, tags, and branches.
  - _HEAD_: This file points to the current branch you're on.
  - _logs/_: This directory keeps a record of all Git operations, including commits, merges and branch creations.
  - _index_ : A staging area  that stores information.
  - _hooks/_ : It contains scripts that can be executed during the Git work-flow (e.g pre-commit, post-receive).

### _<u>Latest Object Hash</u>_

- To find the latest object hash within the .git/objects/ directory, use the following Git command:

```bash
git rev-parse HEAD
```

- This will output the latest commit hash.
![alt text](<Screenshot (26).png>)

- Then, you can use the following command to determine the type and content of this object:

```bash
git cat-file -t <latest-object-hash> && git cat-file -p <latest-object-hash>
```

![alt text](<Screenshot (27).png>)

### _*<u>Dumping Directory Tree</u>*_

- Use Git commands to dump the directory tree referenced by this commit:

```bash
git ls-tree -r <latest-object-hash> 
```

![alt text](<Screenshot (28).png>)

- To dump the directory tree referenced by a specific commit and the contents of the lib/ directory and hello.sh file, you can use the following Git commands:

```bash
git ls-tree -r <latest-object-hash>  lib/
```

- Dump the content of the lib/

```bash
git show HEAD:lib/
```

- Dump the contents of the hello.sh file:

```bash
git show HEAD:lib/hello.sh
```

![alt text](<Screenshot (29).png>)

- This command will display the contents of the hello.sh file in the current HEAD commit.
- The output will be the actual contents of the hello.sh file

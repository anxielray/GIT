# _*History*_

## _*Show History*_

- To show the history of the working directory, run:

```bash
git log
```

![alt text](<Screenshot (13).png>)

### _*One-Line History*_

- To view a condensed one-line history showing only commit hashes and messages, run:

```bash
git log --oneline
```

![alt text](<Screenshot (11).png>)

### _*Customized Log Output*_

- To customize the log output, specify the number of entries or a time range. To display the last 2 entries, run:

```bash
git log -n 2
```

![alt text](<Screenshot (15).png>)

- To view the commits made within the last 5 minutes, run:

```bash
git log --since=5minutes
```

![alt text](<Screenshot (16).png>)

- Since the time-scoop required by the question was not applicable when the project was done, I provided you with a better time-scoop(i.e., 5 hours)

### _*Personalized Format*_

- To show logs in a personalized format, including the commit hash, date, message, branch information, and author name, run:

```bash
git log --pretty=format:"* %h %cd | %s %d [%an]"
```

- This will display the output in a format resembling:

```bash
* e4e3645 2023-06-10 | Added a comment (HEAD -> main) [John Doe]
```

- Note:
  - ``%H`` represents the commit hash
  - ``%as``  represents the date in the short format as you see it below.
  - ``%s`` represents the commit message
  - ``%cr``/ ``%d``  represents the abbreviated commit ref name (e.g. main)
  - ``%an``  represents the author name.

![alt text](<Screenshot (17).png>)

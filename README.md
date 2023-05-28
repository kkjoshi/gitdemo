# gitdemo
understanding git workflow and commands

git clone https://github.com/mukulk82/gitdemo.git

# Day 1
## 1. Switch to develop and get latest
'''
git fetch
git checkout develop 
git pull origin develop

'''
git checkout -b feature/abc-123-learn-git develop. Here abc-123 is jira ticket number
## Start working on a feature/story
## local changes-test-commit 1 to .. many throughout the day
' git commit -m "commit message" ' 

## before end of day
git push --set-upstream origin feature/abc-123-learn-git

# Day 2
## get latest from develop, integrate latest on develop
``` 
git fetch origin develop
git pull 
```

## local changes-test-commit 1 .. many throughout the day
'git commit -m "commit message"'

## before end of day
`git push`

**ready to create merge/pull request? if yes,
create MR/PR on gitlab console
target branch must be develop
**

For review comments follow same once MR/PR approved

**If auto merge is not allowed get latest from develop & merge locally, resolve conflicts and try again**

`git push`

## get approval again by poking reviewer.
## merge using Gitlab UI or with commandline squash merge option

```
git checkout develop
git merge --squash feature/abc-123-learn-git
```

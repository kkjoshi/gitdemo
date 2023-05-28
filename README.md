# gitdemo
understanding git workflow and commands

# Prerequisite - please comeple before coming to meeting
## 1. create github account.
### Add ssh key from local machine to github. 
Generate new ssh key and add it to your github account
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=mac&tool=cli

# Day 0
Clone the repo
git clone https://github.com/kkjoshi/gitdemo.git

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

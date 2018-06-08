# git-changed
git plugin to show git changes statistics per user

### Installation:
Copy `git-changed` to your `/usr/local/bin` folder

### Usage:
```
~ > git changed --author hacker@gmail.com --since 2.days
Changes summary since 2.days for hacker@gmail.com
Files Changed: 2
Insertions: 51
Deletions: 0
Lines changed: 51
```
Without any params ```git changed``` shows statistics since midnight for user, taken from ```git config --get user.email```

**--since**    You can use any value that fits ```git log --since=``` Check approxidate library for more details https://github.com/thatguystone/approxidate/blob/master/approxidate.c


**--author**    Author's email.
### Config
You can use /usr/local/etc/git-changed.conf to store default settings for the keys above. Example:
```
~ > cat /usr/local/etc/git-changed.conf
since=2.weeks
author=my.friend@coworking.com
```

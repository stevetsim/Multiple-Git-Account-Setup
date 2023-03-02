# Multiple Git Account Setup Guide

This guide shows how to setup Multiple GitHub Accounts on your local git.

---

## Configuration
**~/.gitconfig**
```
# ~/.gitconfig

# Personal
[includeIf "gitdir:~/personal/"]
path = ~/personal/.gitconfig

# Work
[includeIf "gitdir:~/work/"]
path = ~/work/.gitconfig

# Default User
[user]
	name = stevetsim
	email = steve@pm.me
```

**~/personal/.gitconfig**
```
[user]
	name = personal
	email = personal@email.com
```

**~/work/.gitconfig**
```
[user]
	name = work
	email = work@email.com
```

## Test
```
git config --list
```
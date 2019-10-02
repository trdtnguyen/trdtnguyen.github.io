---
title: "Github Note"
collection: notes
---

This is the brief guide for using github

[Ignore files](#ignore-files)

## Status
Used to check current status of your repository.
`$ git status`
## Configuration
Used in the first time install git in your linux system.
```
$ git config --global user.name "datnguyen"
$ git config --global user.email "datnguyen@skku.edu"
```


## Ignore files
To filter out unnessary file types e.g., output files, use gitignore
Edit `.gitignore` file at the root of your repository.

Syntax: File name or file type as `*.type`. One line per file/type.
Example:
```
##################
# Compiled files #
##################
*.com
*.class
*.dll
*.exe
*.o
*.so

############
# Packages #
############
# it's better to unpack these files and commit the raw source
# git has its own built in compression methods
*.7z
*.dmg
*.gz
*.iso
*.jar
*.rar
*.tar
*.zip

######################
# Logs and databases #
######################
*.log
*.sql
*.sqlite

######################
# OS generated files #
######################
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

```

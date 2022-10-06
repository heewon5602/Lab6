# 201934612_-_lecture_note_6.md
Summarize about git

## version control and collaboration
### changes vs Snapshots  
**changes** : Storing data as changes to the base version
**snapshots** : Storing data as snapshots (git is using)

### Methods of storaging  
**Local**: Local computer has version databases.
**Centralized**
  : Central VCS Server has version databases.
  : Local computer requests data which they need to Central VCS Server.
  : It is easy to collaborate.
  : It is difficult to restore data when lost.
**Distributed**
  : Local computer and Central VCS Server have all data equally.
  : It is easy to collaborate.
  : It is easy to restre data when lost.
  
### 3steps in Git    
1. Modified: In working directory
2. Staged: In Staging Area
3. Commited: In git directory(Repository)  

### First-time setup: Git config
1. System level: --system option. 
               : Affects all uses and repositories on the system(administrative)
               : file: /etc/gitconfig
               
2. Global(User) level: --global option.
                     : Affects all repositories of a current user.
                     : file: ~/.config/git/config (user.name: need "")

3. Local level: --local option.
              : Specific to the current repository.
              : file: .git/gitconfig

* Each level overrides values in the previous level.
* --show-origin: Show where each config is storaged.

### $git init
New '.git' folder is created.

### $git status
Can check repository status
**Untracked files**: Files which is not interested in git, even if it is deleted and moved.

### $git add [file_name]
Add a new file to be staged (tracked). (It can be confirmed in 'Chanes to be committed:')
*If you revise content of the file, you must add again. (If you not, git commits the prior contents of file.
**git add.**: Upload all files and directories in present directory to staging area.

### $git rm -cached [file_name]
It makes git untracks the file.

### $nano .gitignore
It makes git ignores a file.
**Several input examples**
1. *.a : Ignore all .a files (files with names ending in a)
2. !lib.a: Following 1., but add only lib.a.
3. /TODO: only ignore the TODO files in the current directroy
4. build/: Ignore all files in any directory named build.
5. doc/*.txt:Ignore doc/notes.txt 
6. doc/*/*//*.pdf: Ignore all .pdf files in the doc. directory and any of its subdirectories.

### $git commit-m "commit message"
You make the version which is named "commit message".
*nothing to commit, working tree clean : Contents which committed and contents in working tree are completely equal.

### $git log
You can confirm contents which committed until now.

### $git branch -m
Change the branch.

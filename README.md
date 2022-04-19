# git-class
git and gitbub class

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git switch main
Switched to branch 'main'

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git log
commit 518ee282c3ae33b355a7b479b30cee16fcf0471b (HEAD -> main, she, develope)
Author: shellyling <c7775275@gmail.com>
Date:   Tue Apr 19 15:04:02 2022 +0800

    memo.txt中有新的拉拉拉

commit b2fd54a2d3f52151a834ee0e66b7fa393226351f
Author: shellyling <c7775275@gmail.com>
Date:   Tue Apr 19 14:42:05 2022 +0800

    init commit

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git remote
origin

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 3.87 KiB | 3.87 MiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/shellyling/git-class.git
 * [new branch]      main -> main

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   memo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git commit -am 'add aaa.txt'
[main 44ae3de] add aaa.txt
 1 file changed, 3 insertions(+), 1 deletion(-)

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git switch she
Switched to branch 'she'

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git status
On branch she
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   memo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git commit  -am 'bbb.txt'
[she 48fe4e1] bbb.txt
 1 file changed, 3 insertions(+), 1 deletion(-)

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git merge main -m 'merge main to she'
Auto-merging memo.txt
CONFLICT (content): Merge conflict in memo.txt
Automatic merge failed; fix conflicts and then commit the result.

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit -m '解決衝突 memo'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       memo.txt

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit -m '解決衝突 memo'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       memo.txt

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit -m '解決衝突 memo'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       memo.txt

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit '解決衝突 memo'
fatal: cannot do a partial commit during a merge.

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit -m 'a'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       memo.txt

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git status
On branch she
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   memo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she|MERGING)
$ git commit -am '解決memo衝突'
[she 47cee18] 解決memo衝突

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git switch main
Switched to branch 'main'

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git merge she -m '合併到main'
Updating 44ae3de..47cee18
Fast-forward (no commit created; -m option ignored)
 memo.txt | 1 +
 1 file changed, 1 insertion(+)

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git switch main
Already on 'main'

User@P215-2203-NB35 MINGW64 ~/Desktop/git (main)
$ git switch she
Switched to branch 'she'

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git add .

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git comment -m'ccc'
git: 'comment' is not a git command. See 'git --help'.

The most similar command is
        commit

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$ git^C

User@P215-2203-NB35 MINGW64 ~/Desktop/git (she)
$

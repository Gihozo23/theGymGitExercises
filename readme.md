# Bundle 1
# Exercise 1
```
PS C:\Users\user\Documents> cd "new project for the git exercises"
                                             e git exercises> git init       
No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\user\Documents\new project for the git exercises> git branch -M main
PS C:\Users\user\Documents\new project for the git exercises> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\user\Documents\new project for the git exercises> git add .
PS C:\Users\user\Documents\new project for the git exercises> git commit -m "first commit"
[main (root-commit) 4fbb49e] first commit
 1 file changed, 14 insertions(+)        
 create mode 100644 readme.md
d origin https://github.com/Gihozo23/theGymGitExercises.git
PS C:\Users\user\Documents\new project for the git exercises> git push --set-upstream origin main
Enumerating objects: 3, done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Gihozo23/theGymGitExercises.git
branch 'main' set up to track 'origin/main'.
PS C:\Users\user\Documents\new project for the git exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\user\Documents\new project for the git exercises> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\user\Documents\new project for the git exercises> git checkout dev
Switched to branch 'dev'
PS C:\Users\user\Documents\new project for the git exercises> git branch -d test
Deleted branch test (was 4fbb49e).
```

# Exercise 2
```
> git add .
> git stash save "saving changes for the home.html file"
Saved working directory and index state On dev: saving changes for the home.html file
> git add .
> git stash save "saving changes for the about.html file"
Saved working directory and index state On dev: saving changes for the about.html file
> git add .
> git stash save "saving changes for the team.html file"
Saved working directory and index state On dev: saving changes for the team.html file
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (682f394d139497bc1097f46d2c317067ebf2686b)
$ git stash list
stash@{0}: On dev: saving changes for the team.html file
stash@{1}: On dev: saving changes for the home.html file

$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (55b0d600ad86b542f581fa1f93a6e720162eb318)

$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.   

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (2f6d746d52320f610224ee1fb9362b07391431c1)
$ git reset --hard HEAD
HEAD is now at 31f1d2c another commit
```
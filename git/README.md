Assuming, have a git repository and working with a team some frequent commands to fetch or pull updates, rebase with desired branch and push the works.

```git
$   git fetch
$   git reset --hard {origin_name}/{branch_name} 
```
or
```git
$   git pull
```
```
$   git checkout {branch_name}
$   git rebase {origin_name}/{branch_name}
$   git log
$   git push {origin_name} {branch_name} -f
```

### Executive Summary
```
$ git push -d <remote_name> <branch_name>
$ git branch -d <branch_name>
```
Note that in most cases the remote name is origin. In such a case you'll have to use the command like so.
```
$ git push -d origin <branch_name>
```

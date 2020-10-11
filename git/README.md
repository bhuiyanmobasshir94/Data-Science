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
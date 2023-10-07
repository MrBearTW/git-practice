# StepByStep for git_practice

## git log / Show commit history in graph mode

- `git log --oneline --graph`

## Open new branch

1. Go in to repo `cd C:\Users\user\git_practice`
1. Go back to main `git checkout main`
1. Make sure your pc is newest `git pull upstream main`
1. Open new branch for different ticket `git branch SFT-XXXXX` Use JIRA ticket number

## After finish Codeing part

1. Don't commit your work.
1. Go in to repo `cd C:\Users\user\git_practice`
1. Make sure your stash list is empty `git stash list`(It should be empty)
1. Make sure where are you `git branch` (It should be SFT-xxxxx)
1. Stash your work `git stash`
1. Check stash list `git stash list` (It should have [stash@{0}:])
1. Go to main `git checkout main`
1. Compare your a. local pc repo b. personal github (Origin) c. Upstream github (Company) 
    - a. You local pc repo main commit history `git log --oneline --graph`
    - b. Use browser check Personal github (Origin) main commit history
    - c. Use browser check Upstream github (Company) main commit history
1. Get every update from upstream last time, but did not merge `git fetch upstream`
1. Merge in your pc repo `git merge upstream/main`
1. Compare your a,b,c
1. Update your personal github `git push origin main`
1. Compare your a,b,c
1. Go back to your working branch `git checkout SFT-xxxxx`
1. Move your working branch to newest main `git rebase main`
1. Check your stash (Not necessary step) `git stash list` (It should have [stash@{0}:])
1. `git stash pop stash@{0}`
1. Check your stash (Not necessary step) `git stash list` (It should be empty)
1. Use VScode commit your work or `git add --all` and `git commit -m "SFT-XXX Add testing code ....."`
1. `git push origin SFT-xxxx`
1. Make a PR (pull request) in personal github ( Upstream repository can do it too. )
1. Wait for review and merge by who have permission to merge

### After PR and merge

- Use `git log --oneline --graph` to check your local pc repo commit history
- `git checkout main`
- `git pull upstream main`
- Delete branch in personal pc repo`git branch -d SFT-xxxxx`
- Delete branch on personal GitHub`git push origin --delete SFT-xxxxx`


## Set up git_practice first time (only once)

- Fork git_practice to personal github
- Clone git_practice to local
    1. Go to where you want you repo locate `cd C:\Users\user\Documents\`
    1. `git clone URL-from-GitHub-which-you-Forked`
- Set up upstream
    1. Go to your repo`cd C:\Users\user\Documents\git-practice`
    1. `git remote -v` (Only origin should be there)
    1. `git remote add upstream URL-copy-from-Upstream`
    1. `git remote -v` (Should have origin and upstream)

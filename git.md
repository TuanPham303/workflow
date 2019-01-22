# Git workflow

## Branching
- Make a new branch before working on any feature/bugfix
`git branch -b <branch name>`

## Commiting
- Commit often with short, meaningful commit message
- Start commit message with a verb, eg:
  `add test case for header component`
  `fix login not redirect to homepage`

## Making PRs
- Make sure the branch pass all the test and linting
- Rebase the branch (instruction below)
- Squash the commits (instruction below)

## Rebase
1. Run `git rebase <branch to rebase on>`
2. Fix all the conflicts(if any)
3. Add the modified files
4. Run `git rebase --continue` to continue the rebasing
5. Repeat step 2 until the process is over
6. Force push to update the branch

*NOTE*: run `git rebase --abort` to abort the rebase process if something wrong happens

## Squash
1. Run `git rebase -i HEAD~<number of commits to squash>`
2. The terminal will turn into another window, pick one commit and `fixup` others by changing `pick` to `squash`(`s`) or `fixup`(`f`)
3. Hit `ESC` then type `:wq` then hit `enter`
4. Fix all the conflicts
5. `Add`, `commit` and `force push` to update the branch 

# Lesson 4a - Rebasing your branch

## New Terms
- **Rebase** - Changing the base of your branch

## Prerequisites
- Make sure your repo is in sync - [Lesson 2](../Lessons/Lesson2.md)
- Admin merge in PR to upstream - so that repo is ahead

## Lesson

### Stage 1 - Make a change

1. Navigate to your repo if you're not already there
    ``` PowerShell
    Set-Location C:\GitHub\GitDemo
    ```

2. Check status to see where you are
    ```
    git status
    ```

3. Create a branch to work in
    ```
    git checkout -b rebaseWork
    ```

4. Make a change

    ``` PowerShell
    notepad .\README.md
    ```

5.  Push to your fork on GitHub
    ```
    git push --set-upstream origin rebaseWork

6.  Check your branch on GitHub
    ```
    This branch is 1 commit behind jpomfret:master
    ```

    This development process took a while, and now it's time to merge in but the upstream codebase has newer changes than you have in your clone.

## Stage 2 - Get master branch on your clone up to date

1. Checkout your master branch
    ```
    git checkout master
    ```

2. Pull down the changes to master
    ```
    git pull upstream master
    ```

3. Push changes to your repo on GitHub
    ```
    git push
    ```

## Stage 3 - Rebase your branch from the now up to date master

1. Checkout work branch
    ```
    git checkout rebaseWork
    ```

2. Rebase branch from master
    ```
    git rebase origin/master
    ```

    ```
    First, rewinding head to replay your work on top of it...
    Fast-forwarded rebaseWork to origin/master.
    ```

3.  Force push your changes to your clone
    ```
    git push --force
    ```

4.  Check GitHub

    ```
    This branch is even with jpomfret:master
    ```

## Next Up...
- [Lesson 5](../Lessons/Lesson5.md)

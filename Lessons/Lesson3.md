# Lesson 3 - Making a Change

## New Terms
- **Branch** - Copy of the code in a more isolated environment. Safe space to make changes.

## Prerequisites
- Make sure your repo is in sync [Lesson 2](../Lessons/Lesson2.md)

## Lesson

### Stage 1 - Create a branch to work

1. Navigate to your repo if you're not already there
    ``` PowerShell
    Set-Location C:\GitHub\GitDemo
    ```

2. Check status to see where you are
    ```
    git status
    ```

3. Create a new branch
    ```
    git checkout -b newFeature
    ```

### Stage 2 - Make a change to the code base

1. Open the README.md and add your name to the bottom.

    ``` PowerShell
    notepad .\README.md
    ```

2. Checking the status will now show we have an unstaged change:

    ```
    git status
    ```

3. Stage the file - preparing for commit. By staging you can pick which files are being committed, you don't have to commit all at once.

    ```
    git add .\README.md
    ```

4. Checking the status will now show we have a change ready to commit:

    ```
    git status
    ```

5. Commit the change

    ```
    git commit -m 'adding my name'
    ```

5. Push changes to your repo

    ```
    git push --set-upstream origin newFeature
    ```

    If you just type `git push` you'll get a message that there isn't a matching branch and you need to use --set-upstream

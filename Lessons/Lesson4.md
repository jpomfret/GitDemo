# Lesson 4 - Oh G*T - I'm on the wrong branch

## New Terms
- **Branch** - Copy of the code in a more isolated environment. Safe space to make changes.

## Prerequisites
- Make sure your repo is in sync [Lesson 2](../Lessons/Lesson2.md)

## Lesson

### Stage 1 - Make a change in the master branch!






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

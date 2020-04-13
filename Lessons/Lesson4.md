# Lesson 4 - Oh G*T - I'm on the wrong branch

## New Terms
- **Stash** -

## Prerequisites
- Make sure your repo is in sync - [Lesson 2](../Lessons/Lesson2.md)
- Jess push

## Lesson

### Stage 1 - Make a change in the wrong branch!

1. Navigate to your repo if you're not already there
    ``` PowerShell
    Set-Location C:\GitHub\GitDemo
    ```

2. Check status to see where you are
    ```
    git status
    ```

3. If you're not still on the addFriends branch, check it out
    ```
    git checkout addFriends
    ```

4. Make a change

    ``` PowerShell
    notepad .\README.md
    ```

5. Check status to see where you are
    ```
    git status
    ```

    ```
    On branch addFriends
    Your branch is up to date with 'origin/addFriends'.

    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
            modified:   README.md

    no changes added to commit (use "git add" and/or "git commit -a")
    ```

6. Oh no - I'm still on the old branch - addFriends. Checkout master so we can create a new branch
    ```
    git checkout master
    ```

    ```
    PS C:\GitHub\GitDemo> git checkout master
    error: Your local changes to the following files would be overwritten by checkout:
    README.md
    Please commit your changes or stash them before you switch branches.
    Aborting
    ```

    That didn't work as the checkout would overwrite my changes.

7. We can stash the changes
    ```
    git stash
    ```

8. Now checkout master
    ```
    git checkout master
    ```

9. Update master
    ```
    git pull upstream master
    ```

10. Update your fork on Github (origin).
    ```
    git push
    ```

11. Un-stash your changes
    ```
    git stash pop
    ```

12. Now you've made your changes against the most up to date copy of the master branch

## Next Up...
- [Lesson 5](../Lessons/Lesson5.md)

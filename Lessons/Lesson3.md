# Lesson 3 - Making a Change

## New Terms
- **Branch** - Copy of the code in a more isolated environment. Safe space to make changes.
- **Checkout** - Used to change branches. If the branch doesn't exist yet you can create it during checkout.
- **Commit** - Saving your changes. Make sure to include a useful commit message.

## Prerequisites
- Make sure your repo is in sync - [Lesson 2](../Lessons/Lesson2.md)

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
    git checkout -b addFriends
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

5. Commit the change. Make sure to include a useful commit message.

    ```
    git commit -m 'adding my name'
    ```

5. Push changes to your repo

    ```
    git push --set-upstream origin addFriends
    ```

    If you just type `git push` you'll get a message that there isn't a matching branch and you need to use --set-upstream

### Stage 3 - Create a PR

1. Open GitHub and navigate to either your repo or the [upstream repo](https://github.com/jpomfret/GitDemo).
2. You should see a highlighted bar suggesting you 'Compare & pull request'
3. Fill in the form and submit the PR for approval.
4. Upstream repo owner or someone with permissions can merge it in.

## Next Up...
- [Lesson 4](../Lessons/Lesson4.md)
# Lesson 2 - Keeping in Sync

## New Terms
- **Remote** - Somewhere code is stored, not on your machine. In this case a GitHub Repo.
    - **Origin** - When we clone a repo the source of that clone is added as this remote location.
    - **Upstream** - What we are naming the remote location of the original repo we forked.
- **Fetch** - Git command to retrieve new work from an upstream.
- **Merge** - Used to combine the fetched changes with your local work.
- **Pull** - Fetch & Merge in one go.
- **Push** - Upload your local changes to a remote repo.

## Prerequisites
- Have a repo cloned to your computer - [Lesson 1](../Lessons/Lesson1.md)

## Lesson

### Stage 1 - Setting up a remote Upstream
1. Navigate to your repo if you're not already there

    ``` PowerShell
    Set-Location C:\GitHub\GitDemo
    ```

2. View current remote
    ```
    git remote -v
    ```

    You should see the origin, which was added when you cloned the repo.

    ```
    origin  https://github.com/<<USERNAME>>/GitDemo.git (fetch)
    origin  https://github.com/<<USERNAME>>/GitDemo.git (push)
    ```

3. Add remote named 'upstream' to refer to the original repo that we forked & cloned (someone elses code).

    ```
    git remote add upstream https://github.com/jpomfret/GitDemo.git
    ```

4. View remotes again
    ```
    git remote -v
    ```

    You should now see the origin and upstream.

    ```
    origin  https://github.com/<<USERNAME>>/GitDemo.git (fetch)
    origin  https://github.com/<<USERNAME>>/GitDemo.git (push)
    upstream        https://github.com/jpomfret/GitDemo.git (fetch)
    upstream        https://github.com/jpomfret/GitDemo.git (push)
    ```

### Stage 2 - 'This branch is 2 commits behind jpomfret:master'
Folks have been working on the jpomfret code base and it's now got newer code than your fork.

1. Pull changes from upstream into your clone (master branch in this example)

    ```
    git pull upstream master
    ```

2. Push changes to your fork

    ```
    git push
    ```

3. Check GitHub - your fork should now show you're back in sync.
    > This Branch is even with jpomfret:master.

4. Bye, Bye, Bye. - We're now NSync :D.

## Next Up...

- [Lesson 3](../Lessons/Lesson3.md)
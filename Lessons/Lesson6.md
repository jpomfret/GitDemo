# Lesson 6 - Cleanup those branches

## Prerequisites
- Worked through the other lessons and left branches all over the place.

## Lesson

### Stage 1 - View our local branches

1. Checkout master
    ```
    git checkout master
    ```

2. View our local branches
    ```
    git branch -v
    ```

3. View branches that have been merged into master
    ```
    git branch --merged
    ```

4. Delete a single branch
    ```
    git branch -d addFriends
    ```

5. Delete all merged branches
    ```
    git branch --merged | ?{-not ($_ -like "*master")} | %{git branch -d $_.trim()}
    ```
    >https://gist.github.com/srkirkland/63ed5730da1bf607a4b3

### Stage 2 - Cleanup GitHub Branches

1. Navigate to your GitHub Repo (e.g. www.github.com/jesspomfret/GitDemo)
2. Click branches (or navigate to e.g. www.github.com/jesspomfret/GitDemo/branches)
3. Delete any unneeded branches

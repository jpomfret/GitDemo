# Lesson 5 - Oh G*T - We've got a conflict

## New Terms
- **term** -

## Prerequisites
- Make sure your repo is in sync - [Lesson 2](../Lessons/Lesson2.md)

## Lesson

### Stage 1 - Create a branch to work

1. Navigate to your repo if you're not already there
    ``` PowerShell
    Set-Location C:\GitHub\GitDemo
    ```

2. Create a branch to work in
    ```
    Git checkout -b newStuff
    ```

3. Make a change
    ``` PowerShell
    notepad .\README.md
    ```

    At the same time someone else has pushed a change to master (either direct or through a PR)

## Next Up...
- [Lesson 6](../Lessons/Lesson6.md)
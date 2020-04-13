# Lesson 1 - Forking & Cloning

## New Terms
- **Repository** - A folder of code, docs, tests, etc.
- **Forking** - The process of creating a fork.
  - A **Fork** is a copy of a repo. </br>
  - Can be used to experiment with someone elses code.
- **Cloning** - The process of creating a local copy of a repo on your machine.

## Prerequisites
- Download and install [Git](https://git-scm.com/downloads)

## Lesson

### Stage 1 - Fork a repo
1. Navigate to [GitDemo](https://github.com/jpomfret/GitDemo/) on GitHub
2. Fork the repo for your user

### Stage 2 - Clone a repo

1. Create a folder to hold your GitHub Repos

    ``` PowerShell
    New-Item -Path C:\GitHub -ItemType Directory
    ```

2. Navigate into the folder

    ``` PowerShell
    Set-Location C:\GitHub
    ```

3. Clone the newly forked repo

    ``` git
    git clone https://github.com/<<USERNAME>>/GitDemo.git
    ```

4. Navigate into the repo

    ``` PowerShell
    Set-Location .\GitDemo\
    ```

5. Have a look at the status

    ``` git
    git status
    ```

## Next Up...
- [Lesson 2](../Lessons/Lesson2.md)
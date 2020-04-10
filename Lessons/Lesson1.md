# Lesson 1 - Forking & Cloning

**Repository** - A folder of code, docs, tests, etc.

**Forking** - The process of creating a fork.
- A Fork is a copy of a repo. </br>
- Can be used to experiment with someone elses code.

**Cloning** - The process of creating a local copy of a repo on your machine.

## Prerequisites
- Download and install [Git](https://git-scm.com/downloads)

## Step 1 - Fork a repo
- Navigate to [GitDemo](https://github.com/jpomfret/GitDemo/) on GitHub
- Fork the repo for your user

## Step 2 - Clone a repo

- Create a folder to hold your GitHub Repos

``` PowerShell
New-Item -Path C:\GitHub -ItemType Directory
```

- Navigate into the folder

``` PowerShell
Set-Location C:\GitHub
```

- Clone the newly forked repo

```
git clone https://github.com/<<USERNAME>>/GitDemo.git
```
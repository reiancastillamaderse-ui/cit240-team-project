# Our Git and GitHub Workflow

This guide shows how we make a change to the project and share it with the team. Do not make your changes directly on `main`.

## 1. Get the latest `main`

Before you start, open a terminal in the project folder and run:

```bash
git switch main
git pull origin main
```

This updates your computer with the latest version from GitHub.

## 2. Make a branch

A branch is a separate place to do your work. Give it a short name that says what you are doing:

```bash
git switch -c feature/your-change
```

For example:

```bash
git switch -c feature/update-homepage
```

Each person should use their own branch. This keeps unfinished work away from `main`.

## 3. Make and commit your changes

Edit and save your files. Then check what changed:

```bash
git status
```

Add the files you want to include, then make a commit:

```bash
git add path/to/your-file
git commit -m "Say what you changed"
```

A commit is a saved set of changes. Use a short message that explains the work, such as `Add team profile`.

## 4. Push your branch

Send your branch and commits to GitHub:

```bash
git push -u origin feature/your-change
```

For later updates on the same branch, you can use:

```bash
git push
```

## 5. Ask for a review

On GitHub, open a pull request from your branch into `main`. A pull request (PR) lets the team see and discuss your changes before they join the project.

Write a clear title and a short note about what you changed. Ask a teammate to review it. Check that the changed files look right and that the project still works.

If the reviewer asks for a change, make it on the same branch. Then commit and push it. The PR will update by itself. Reply to the review note when you have addressed it.

## 6. Merge the pull request

After a teammate approves the PR and any checks pass, merge it into `main` on GitHub. If there is a conflict, fix it before merging. Do not merge your own PR unless the team has agreed that this is okay.

## 7. Synchronize your computer

After the PR is merged, update your local `main`:

```bash
git switch main
git pull origin main
```

You can then remove your finished branch from your computer:

```bash
git branch -d feature/your-change
```

To start another task, make a new branch from the updated `main`. This helps everyone begin with the same current project files.
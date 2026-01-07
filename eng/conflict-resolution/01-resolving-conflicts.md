# Resolving Conflicts in Git

Merge conflicts occur when two or more people modify the same part of a file, or when one developer deletes a file that another has modified. Git cannot automatically decide which change to keep, requiring manual intervention.

## Conflict Scenario

Imagine you and a colleague are working on the same `recipes.md` file. You add a cake recipe, and your colleague adds a pave recipe, both in the same line or section of the file.

1.  **Your Colleague Commits and Pushes**: Your colleague adds the pave recipe, commits, and pushes it to the remote repository (`git push origin master`).

2.  **You Try to Push**: You finish your cake recipe, commit (`git commit -m "Adds cake recipe"`), and try to push (`git push origin master`). Git will reject your push, stating that the remote repository has changes you don't have.

## Steps to Resolve a Conflict

1.  **Pull Remote Changes**: The first step is to bring the changes from the remote repository to your local one:
    ```bash
    git pull origin master
    ```
    At this point, Git will identify the conflict and mark the affected files.

2.  **Identify Conflicts**: Git will modify the `recipes.md` file (in our example) to show the conflicting sections. It will use special markers to indicate your changes (`<<<<<<< HEAD`) and your colleague's changes (`>>>>>>> <colleague_commit_hash>`):

    ```markdown
    <<<<<<< HEAD
    - Cake Recipe
    =========
    - Pave Recipe
    >>>>>>> colleague_commit_hash
    ```

3.  **Resolve Manually**: Open the conflicting file in your code editor (VS Code, for example). You will need to edit the file, removing the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) and deciding which version of the code to keep, or combining the two versions logically.

    For example, to keep both recipes:

    ```markdown
    - Cake Recipe
    - Pave Recipe
    ```

4.  **Mark Conflict as Resolved**: After editing the file and removing all conflict markers, you need to inform Git that the conflict has been resolved:
    ```bash
    git add recipes.md
    ```
    You can use `git status` to check if the file has been added to the *staging area*.

5.  **Commit the Resolution**: Finally, make a new commit to record the conflict resolution:
    ```bash
    git commit -m "Resolves conflict in recipes.md: adds cake and pave"
    ```

6.  **Push Resolved Changes**: Now you can push your changes, including the conflict resolution, to the remote repository:
    ```bash
    git push origin master
    ```

Resolving conflicts is a common part of collaborative work with Git. Practice makes perfect!

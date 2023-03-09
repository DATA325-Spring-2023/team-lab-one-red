# Team-Lab-One

# Learning goals

-   Collaborating on GitHub and resolving merge conflicts
-   Working with your team
-   Reinforce GitHub Skills

# Lab prep

You have a task you should complete before the lab:

- Read about merge conflicts below. The merge conflict exercise we'll start with during the lab will assume that you have this background information.

## Merges and merge conflicts

You will be working in teams, so we're going to make things a little more interesting and let all of you make changes and push those changes to your team repository.
Sometimes things will go swimmingly, and sometimes you'll run into merge conflicts.
So our first task today is to walk you through a merge conflict!

-   Pushing to a repo replaces the code on GitHub with the code you have on your computer.
-   If a collaborator has made a change to your repo on GitHub that you haven't incorporated into your local work, GitHub will stop you from pushing to the repo because this could overwrite your collaborator's work!
-   So you need to explicitly "merge" your collaborator's work before you can push.
-   If your and your collaborator's changes are in different files or in different parts of the same file, git merges the work for you automatically when you \*pull\*.
-   If you both changed the same part of a file, git will produce a \*\*merge conflict\*\* because it doesn't know how which change you want to keep and which change you want to overwrite.

Git will put conflict markers in your code that look like:

    <<<<<<< HEAD 

    See also: [dplyr documentation](https://dplyr.tidyverse.org/)   

    ======= 

    See also [ggplot2 documentation](https://ggplot2.tidyverse.org/)  

    >>>>>>> some1alpha2numeric3string4
The `===`s separate *your* changes (top) from *their* changes (bottom).

Note that on top you see the word `HEAD`, which indicates that these are your changes.

And at the bottom you see `some1alpha2numeric3string4` (well, it probably looks more like `28e7b2ceb39972085a0860892062810fb812a08f`).

This is the **hash** (a unique identifier) of the commit your collaborator made with the conflicting change.

Your job is to *reconcile* the changes: edit the file so that it incorporates the best of both versions and delete the `<<<`, `===`, and `>>>` lines.
Then you can stage and commit the result.

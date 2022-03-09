First of all, make initial commit to main, then create develop branch from it and commit there.
![Commit graph on this stage](img/graph_before_pr.png)

After that, we want to create PR to main, however pr checking doesn't occur:
![Merged PR without checking](img/merged_without_checking.png)
![Merged PR without checking graph](img/merget_without_checking_pr_graph.png)

To set PR back, we do the following
1. git checkout main
2. git reset HEAD^
3. Unstaged changes in main.py appear, discard them
4. git push -f origin main:main

![Commit graph after PR setback](/img/graph_after_pr_setback.png)

Than we create another PR, check it, approve and merge
![Checked Pr](img/merged_with_checking.png)
![Commit graph after PR](img/merged_with_checking.png)

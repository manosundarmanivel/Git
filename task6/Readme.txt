



1.Create and add a file for production:
echo "This is the file with production code" > production.txt creates a file named production.txt.
git add production.txt stages the file for commit.
git commit -m "Commited for production" commits the changes to the repository.

2.Create a new branch for the login feature:

git checkout -b new-login-feature creates a new branch and switches to it.
echo "This is the new login feature file" > login_feature.txt creates a new file for the login feature.
git add . stages all changes.
git stash temporarily saves the uncommitted changes.

3.Switch back to the main branch and fix production issues:
git checkout main switches to the main branch.
echo "This is the production file, fixed with changes while working in the new feature" > production.txt updates the production file.
git add . stages the changes.
git commit -m "Commited for production with fixed bug" commits the changes.

4.Switch back to the new feature branch and apply stashed changes:
git checkout new-login-feature switches back to the feature branch.
git stash list checks the stashed changes.
git stash pop restores the stashed changes.
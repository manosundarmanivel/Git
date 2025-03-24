1.Create a new branch and start working on a login feature.
git checkout -b feature-login
echo "Login logic implemented" > login.js
git add login.js
git commit -m "Implemented basic login functionality"
git push origin feature-login

2.Squash recent commits to clean up history.
git rebase -i HEAD~3

3.After rebasing, try to push:
git push origin feature-login

4.Force push to override remote history:
git push --force origin feature-login

5.Recovering Lost Commits
git reflog

6.Identify the lost commit hash:

7.Restore the lost commit:
git checkout -b recovery-branch efgh456


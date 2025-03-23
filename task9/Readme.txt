Step 1: Create and switch to a feature branch
git checkout -b feature-branch
echo "console.log('Hello, world!');" > index.js
git add index.js
git commit -m "Add index.js file"
git push -u origin feature-branch

Step 2: Open a Pull Request (PR) on GitHub/GitLab (manual step)

Step 3: Merge the PR (manual step)

Step 4: Pull the merged changes locally
git checkout main
git pull origin main
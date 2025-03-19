Task4 - Interactive Rebasing for Clean Commit History

Step 1: Setup a Repository

git add conflict.txt
git commit -m "Initial commit"

Step 2: Create Two Branches

git branch feature-1
git branch feature-2

Step 3: Modify the Same Line in Both Branches

On feature-1:
git checkout feature-1
echo "Feature 1 modification" > conflict.txt
git commit -am "Update conflict.txt in feature-1"

On feature-2:
git checkout feature-2
echo "Feature 2 modification" > conflict.txt
git commit -am "Update conflict.txt in feature-2"

Step 4: Merge and Trigger a Conflict
git checkout feature-1
git merge feature-2

Step 5: Check the Conflict
git status
git diff

<<<<<<< HEAD
Feature 1 modification
=======
Feature 2 modification
>>>>>>> feature-2

Choose one of the changes or merge both:

git add conflict.txt
git commit -m "Resolved merge conflict between feature-1 and feature-2"

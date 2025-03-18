Git Version Control Task 1 

Git Workflow Documentation

Step 1: Initialize Repository & Add Remote

git remote add origin https://github.com/manosundarmanivel/Git.git

Step 2: Create a New Directory and Files

mkdir task1
cd task1
echo "Hello this is the sample git file1 for task1" > sampleFile1.txt
echo "This is the sample git file2 for task1" > sampleFile2.txt


Step 3: Add and Commit Files

git add .
git commit -m "Commit for task1"


Step 4: Push to Remote Repository

git push -u origin main


Step 5: Create a New Feature Branch

git checkout -b new-feature


Step 6: Modify a File and Commit Changes

echo "This is the new feature branch with updated sample file1" > sampleFile1.txt
git add .
git commit -m "Updated sampleFile1 with new feature"


Step 7: Push Feature Branch to Remote Repository

git push origin new-feature


Step 8: Merge Feature Branch into Main
bash
git checkout main
git merge new-feature
git push origin main



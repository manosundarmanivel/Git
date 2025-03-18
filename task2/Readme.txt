Git Version Control Task 2

Step 1: Create a .gitignore File
touch .gitignore

Step 2: Add Patterns to .gitignore
Open the .gitignore file and add the following lines:
*.log  
*.tmp  
node_modules/ 

Step 3: Create Sample Files
echo "This is the sample log file" > sample.log  
echo "This is the sample temp file" > sample.tmp  
echo "This is the sample python file" > pythonfile.py  
mkdir node_modules  
echo "This is the sample module file" > node_modules/sample_module.js  

Step 4: Check Tracked and Ignored Files
git status
Output:
pythonfile.py should be listed as an untracked file.
sample.log, sample.tmp, and node_modules/ should not appear.

Step 5: Verify Ignored Files
git check-ignore -v sample.log sample.tmp node_modules/sample_module.js
Output:
.gitignore:2:*.log        sample.log
.gitignore:3:*.tmp        sample.tmp
.gitignore:4:node_modules/ node_modules/sample_module.js
This confirms that these files are ignored due to the .gitignore rules.

Step 6: Add and Commit Allowed Files
git add .
git status
git commit -m "Commit for task2"
git push origin main
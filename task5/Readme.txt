Interactive Rebase: Cleaning Up Commit History


Step 1: Check Your Commit History**
Run the following command to see the last few commits:

git log --oneline

output:

kes563  Intial commit (Typo in commit message)
ydf476  Added login feature
gio781  Fixed typo in login button
mhf021  Implemented logout feature
aso389  Minor style fix for logout button
pjr853  Added README file


---

### **Step 2: Start Interactive Rebase**
Run the rebase command for the last 6 commits:


git rebase -i HEAD~6

This opens an editor showing:


pick abc123 Intial commit
pick def456 Added login feature
pick ghi789 Fixed typo in login button
pick jkl012 Implemented logout feature
pick mno345 Minor style fix for logout button
pick pqr678 Added README file

Step 3: Modify the Rebase Plan**
Edit the file as follows:


reword abc123 Initial commit  # Fix commit message typo
pick def456 Added login feature
fixup ghi789 Fixed typo in login button  # Merge typo fix into login feature commit
pick jkl012 Implemented logout feature
squash mno345 Minor style fix for logout button  # Merge style fix into logout feature commit
pick pqr678 Added README file


Save and close the editor.

Step 4: Edit Commit Messages**
- Git will prompt you to edit the commit message for `abc123`. Fix the typo.
- Git will also ask you to edit the commit message for `jkl012 + mno345` (squashed commits). Modify or keep it.

Step 5: Complete the Rebase**
Continue the rebase process:


git rebase --continue

If conflicts occur, resolve them and run:


git add <file>
git rebase --continue

Step 6: Push the Cleaned History**
If you had already pushed the commits before rebasing, you need to force push:
git push origin feature-branch --force



Final Clean Commit History**
After rebasing, your commit log will look like this:


xyz111  Initial commit (Fixed typo)
uvw222  Added login feature (Fixed typo in button)
rst333  Implemented logout feature (Merged style fix)
pqr678  Added README file





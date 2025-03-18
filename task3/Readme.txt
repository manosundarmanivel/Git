1. Create a new HTML file
echo "<h1>Heading</h1>" > index.html

2. Initialize Git repository
git init

3. Add and commit the file
git add .
git commit -m "Added HTML File"

4. Modify the file (Mistake: Changed <h1> to <p>)
echo "<p>Heading</p>" > index.html

5. Commit the mistake
git add .
git commit -m "Buggy Commit : Added <p> tag instead of <h1>"

6. Check commit history
git log --oneline

7. Revert the mistaken commit
git revert <commit-hash>  # Use the hash of "Buggy Commit"

8. If facing issues, complete the revert process
git commit --amend  # If necessary, edit the commit message

9. Push the revert commit
git push origin main

10. Make another mistake (Buggy Commit2)
echo "<p>Another Heading</p>" > index.html

11. Add and commit again
git add .
git commit -m "Buggy Commit2"

12. Revert the second mistake
git revert <commit-hash>

# 13. If there are uncommitted changes preventing revert
git stash  # Temporarily store the changes
git revert <commit-hash>
git stash pop  # Restore the stashed changes

# 14. Exploring Git Reset
echo "<h1>New Heading</h1>" > index.html

# 15. Try committing without adding (Fails)
git commit -m "Initial commit for exploring reset"

# 16. Proper way: Add and commit
git add .
git commit -m "Initial commit for exploring reset"

# 17. Reset to previous commit (Soft reset keeps changes)
git reset --soft HEAD~1

# 18. Hard reset to remove all changes
git reset --hard HEAD~1

# 19. Push changes after reset
git push --force origin main

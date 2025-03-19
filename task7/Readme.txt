Cherry-Picking Commits Between Branches

1. Create a Git Repository (If Not Already Initialized)**

   git init cherry-pick-demo
   cd cherry-pick-demo


2. Create and Switch to a New Branch (`feature-branch`)**

   git checkout -b feature-branch


3. Create a Commit in `feature-branch`**

   echo "Feature A" > feature.txt
   git add feature.txt
   git commit -m "Add Feature A"


4. Switch to `main` and Create a Different Commit**

   git checkout -b main
   echo "Main Branch File" > main.txt
   git add main.txt
   git commit -m "Add main branch file"


5. Identify the Commit to Cherry-Pick**

   git log --oneline --graph --all
   Copy the commit hash of `"Add Feature A"` from `feature-branch`.

6. Cherry-Pick the Commit into `main`**

   git cherry-pick <commit-hash>

   Replace `<commit-hash>` with the actual commit ID.

7. Resolve Conflicts (If Any)
   - If conflicts arise, Git will pause the cherry-pick. Use:

     git status

   - Manually edit the conflicted files, then run:
   
     git add <conflicted-file>
     git cherry-pick --continue
   - Or abort the cherry-pick with:
     git cherry-pick --abort


8. Verify the Commit History**

   git log --oneline --graph --all
   cherry-picked commit is now present in `main`.




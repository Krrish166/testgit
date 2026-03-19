<p>Hello world<p>


to clone one repo entire form one account to other
# 1. Clone source repo (Account A)
git clone https://github.com/accountA/source-repo.git

cd source-repo

# 2. Remove existing git history (IMPORTANT if you want only files)
rm -rf .git

# 3. Initialize new repo
git init

# 4. Add new repo (Account B)
git remote add origin https://github.com/accountB/destination-repo.git

# 5. Add and commit files
git add .
git commit -m "Initial commit from source repo"

# 6. Push to destination repo
git branch -M main
git push -u origin main

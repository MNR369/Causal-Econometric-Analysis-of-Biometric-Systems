Using GitHub CLI (gh) for Automation
gh auth login
curl -X POST https://api.github.com/repos/import \
  -H "Authorization: token YOUR_PAT" \
  -H "Accept: application/vnd.github.v3+json" \
  -d '{
    "vcs": "subversion",  // or "mercurial"
    "vcs_url": "https://svn.example.com/myrepo",
    "vcs_username": "your_svn_user",
    "vcs_password": "your_svn_pass"
  }' \
  --data-urlencode "owner=yourusername" \
  --data-urlencode "repo=new-repo-name"
  git svn clone https://svn.example.com/myrepo --stdlayout new-repo
cd new-repo
git remote add origin https://github.com/yourusername/new-repo.git
git push -u origin master.
curl -X PUT https://api.github.com/repos/yourusername/new-repo/import \
  -H "Authorization: token YOUR_PAT" \
  -H "Accept: application/vnd.github.barred-rock-preview+json" \
  -d '{"vcs": "svn", "vcs_url": "svn://oldrepo"}'
  curl https://api.github.com/repos/yourusername/new-repo/import \
  -H "Authorization: token YOUR_PAT"
  git pull origin main
# Add your Python scripts
python3 auto_license.py  # Inject MIT headers
git add .
git commit -m "Add fraud detection and DiD analysis"
git push.

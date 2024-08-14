# How to Clone a GitHub Private Repository on a Server | Step-by-Step Guide

### Youtube Video: https://youtu.be/kgrWQ2xV_Gc


### 1. Generate a New SSH Key
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
### 2. Add Your SSH Key to the SSH Agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
### 3. Add the SSH Key to Your GitHub Account
copy the SSH public key to your clipboard:
```bash
cat ~/.ssh/id_ed25519.pub
```

Go to GitHub Settings > SSH and GPG keys, click "New SSH key," and paste your key.

### 4. Test the SSH Connection
```bash
ssh -T git@github.com
```

### 5. Update Repository Remote URL
Go to the folder of your repo:
```bash
git remote set-url origin git@github.com:GITHUB_USERNAME/REPO_NAME.git
```

### 6. Pull the Repository
```bash
git pull origin main
```





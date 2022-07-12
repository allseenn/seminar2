# How-to make remote repo without web-browser
Little instruction how to make local repo *seminar3* then we make remote public repo *seminar* on github and push local branches from Windows PC and Linux PC to remote. At last, through web browser we create third branch and merge others to it.
As result, we produce 3 branches:
+ win - managed with Windows PC 
+ linux - managed with Xubuntu Linux PC
+ main - managed through web interface  
All procedure takes 5 main actions

## 1 GitHub api
With web browser on github.com we need to make Personal Access Token in Developer section of Settings in main Menu.

## 2 Linux bash
We could use linux shell or Git Bash for windows to create public repo *seminar3*, after password prompt insert PAT token from first action:
```
curl -u allseen https://api.github.com/user/repos -d '{"name":"seminar3","private":false}'
```
## 3 Windows
```
git init
git add README.md
git add -m "first commit"
git branch -M win
git remote add origin https://github.com/allseenn/seminar3.git
git push -u origin win
```
## 4 Linux git










## 5 GitHub Web
On GitHub with web browser made main branch from win.
And will try to merge others to it, if possible )).
Seccessfuly changed default branch from win to main
in Settings - Branches

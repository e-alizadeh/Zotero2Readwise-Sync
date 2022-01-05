# zt2rw-cronjob (Zotero ➡️ Readwise automation)
This repo has actually a cronjob (time-based Job scheduler) using GitHub actions that automates the Zotero -> Readwise 
integration using the [Zotero2Readwise](https://github.com/e-alizadeh/Zotero2Readwise) Python library. 

**You just need to fork this repository and add the following secrets to your git repository secrets, 
and you're ready to go!**
- Readwise Access Token (secret name: **READWISE_TOKEN**)
- Zotero Key (secret name: **ZOTERO_KEY**)
- Zotero Library ID (secret name: **ZOTERO_ID**)



Check the [Section Usage](https://github.com/e-alizadeh/Zotero2Readwise#usage) in Zotero2Readwise repo to get 
instructions on how to find above information. 
Note that since Readwise token and Zotero Key's are sensitive information, they should be treated as your passwords.
Because of this, I'm using GitHub Action secrets to manage such sensitive variables!

# How to add secrets to your repo's GitHub Actions secrets
![](./tutorial/github_action_secrets.gif)


# Manual Trigger
If you want to manually trigger the automation, you can simply commit an empty message and push it to your forked repo, 
like the following:
```shell
git commit --allow-empty -m "Trigger automation"
```
and then,
```shell
git push
```
This will run the automation immediately and won't impact your scheduled automation.

# Note
*Keep in mind that GitHub Actions may run your scheduled automation with some delay!*
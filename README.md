# zt2rw-cronjob
This repo is actually a cronjob (a scheduled task runner) using GitHub actions that automates the Zotero -> Readwise 
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
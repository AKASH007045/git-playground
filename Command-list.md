1. Command to clone a repo: 
    git clone git@github.com:<username>/git-playground.git

2. ### Configure Git on local system.
*Step 1* : Create SSH keys for all accounts
<cd ~/.ssh>
Syntax for generating unique ssh key for ann account is:
<ssh-keygen -t rsa -C "your-email-address" -f "github-username">
here,
-C stands for comment to help identify your ssh key
-f stands for the file name where your ssh key get saved

*Step 2* : Add SSH keys to SSH Agent
<ssh-add -K ~/.ssh/private-key> 

*Step 3* : Add SSH public key to the Github
Paste the public key on Github

Sign in to Github Account
Goto Settings > SSH and GPG keys > New SSH Key
Paste your copied public key and give it a Title of your choice.

*Step 4* : Create a Config File and Make Host Entries
<vi ~/.ssh/config>
Add content
`     #rahul-office account
     Host github.com-rahul-office
          HostName github.com
          User git
          IdentityFile ~/.ssh/github-rahul-office
`

*Step 5* : Cloning GitHub repositories using different accounts
<git clone git@github.com-{your-username}:{owner-user-name}/{the-repo-name}.git>
<git config user.email "my_office_email@gmail.com">
<git config user.name "Rahul Pandey">
To push or pull to the correct account we need to add the remote origin to the project
<git remote add origin git@github.com-rahul-personal:rahul-personal>

3. 

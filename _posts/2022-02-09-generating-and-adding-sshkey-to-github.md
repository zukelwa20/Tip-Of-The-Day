---
layout: default
---

# Generating and adding sshkey to github

1. Open your terminal

2. Enter ``` $ ls -al ~/.ssh ``` to see if existing SSH keys are found in your .ssh directory.

4. If the key is not found you can generate a new one.
``` $ ssh-keygen -t ed25519 -C "your_email@exmple.com" ```

3. To copy ssh key you can open the file.
 ``` $ cat ~/.ssh/<the name of the file you saved your key> ```
 
4. Add the ssh to github go to github. 

 ``` Go to your profile photo on the top right click on it then go to settings 

     In the "Access" section of the sidebar, click  SSH and GPG keys.

     Next to the SSH key you'd like to authorize, click Enable SSO or Disable SSO.

     Find the organization you'd like to authorize the SSH key for.

     Click Authorize. 

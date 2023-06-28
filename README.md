## To set up SSH key access for Bitbucket on ubuntu, follow these steps:

#### Step 1. Generate SSH key pair
Open a terminal or command prompt on your computer and run the following command to generate an SSH key pair:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
Replace "your_email@example.com" with your actual email address associated with your Bitbucket account. You can also choose a different filename and location for your SSH key if desired.

#### Step 2. Add SSH key to your Bitbucket account:
- Copy the contents of the public key file. On most systems, the public key file is located at `~/.ssh/id_rsa.pub`. If you are using docker container it is located at `/root/.ssh/id_rsa.pub`
- In your Bitbucket account, go to "Settings" or "Account Settings" and look for the "SSH keys" or "SSH access keys" section.
- Click on "Add key" or "Add SSH key" and paste the contents of your public key into the provided field. Give the key a descriptive label if you want.
- Save the key.

#### Step 3. Test the SSH connection
Run the following command in the terminal or command prompt to test the SSH connection to Bitbucket:
```
ssh -T git@bitbucket.org
```

If the connection is successful, you should see a message like "logged in as your_username." or "You can use git to connect to Bitbucket. Shell access is disabled".

#### Step 4. Update your Git remote URLs
If you have existing Git repositories, you'll need to update the remote URLs to use SSH instead of HTTPS. To do this, navigate to the local repository directory in the terminal or command prompt and run the following command:
```
git remote set-url origin git@bitbucket.org:your_username/your_repository.git
```
Replace "your_username" with your Bitbucket username and "your_repository" with the name of your repository.

With SSH access set up, you can now clone, pull, push, and interact with your Bitbucket repositories using the SSH protocol.

## License
**Free Software, Hell Yeah!**

## Authors
- [Rahul Gupta](https://github.com/rahulelex)

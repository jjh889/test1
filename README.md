Set up deploy using git
Create SSH Private Key
# Press Enter to omit key name, passphase creation
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# Copy to Private key
$ cat .ssh/id_rsa.pub

# Init Github
$ ssh -T git@github.com
# Press Enter to omit key name, passphase creation
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# Copy to Private key
$ cat .ssh/{id}_rsa.pub

# Configuration to ssh connection
$ vi ~/.ssh/config
Host github.com-{id}
  Hostname github.com
  User git
  IdentityFile ~/.ssh/{id}_rsa

# Init Github
$ ssh -T git@github.com-{id}

# check confirm messages
# Hi {your-github-name}! You've successfully authenticated, but Github does not provide shell access
Add SSH key to Github Link

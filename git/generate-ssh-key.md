# How generate ssh key

## First what is a ssh key?

Using the SSH protocol, you can connect and authenticate with remote servers and services. With SSH keys, you can connect to Github without having to enter your username or password every time you connect.

## Verificar chaves SSH existentes.

Open terminal

Digite ls -al ~/.ssh para ver se tem alguma chave SSH presente

    ls -al ~/.ssh

## Lists the files in your .ssh directory, if they exist

By default, the name of the public key files can be one of the following:

    id_dsa.pub
    id_ecdsa.pub
    id_ed25519.pub
    id_rsa.pub

Well if you don't have a public and private key pair, or don't want to connect the ones that are available on Github, <strong>then generate a new key</strong>.

## Generate a new ssh key

1- Open Terminal

2- Type this in, replacing it with your Github email.

    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

3- When it appears in the terminal “Enter a file in which to save the key,” press Enter. This accepts the location of the default file.

    Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]

4- At the terminal, enter a secure password.

    Enter passphrase (empty for no passphrase): [Type a passphrase]
    Enter same passphrase again: [Type passphrase again]

5- Adding your SSH key to ssh-agent

Before adding a new SSH key to ssh-agent to manage your keys, you should <strong>Check for existing SSH keys</strong> and <strong>Generate a new SSH</strong> key if necessary.

5.1 Start the ssh-agent in the background.

    eval "$(ssh-agent -s)"
    Agent pid 59566

5.2. Add your SSH private key to ssh-agent. If you created your key with a different name, replace id_rsa in the command with the name of your private key.

    ssh-add ~/.ssh/id_rsa

## Adicionar a chave SSH na sua conta do Github

1. Copy the SSH key

If your SSH key has a different name than the example in the code, modify the file name. When copying your key, do not add new lines or blanks.

     $ sudo apt-get install xclip

Download and install xclip. If you don't have 'apt-get' installed, you can use another installer (like 'yum')

     xclip -sel clip <~ / .ssh / id_rsa.pub

! Copy the contents of your id_rsa.pub key

Tip: If xclip is not working, you can find the hidden .ssh folder, open the file in the terminal, and copy it.

    $ cat ~ / .ssh / id_rsa.pub

2. In the upper right corner of Github, click on your profile photo and click on Settings.

3. In the left sidebar, click SSH and GPG keys.

4. Click New SSH key or Add SSH key.

5. In the “Title” field, add a description for the new key.

6. Paste your key into the “Key” field.

7. Click Add SSH key.

8. If prompted, confirm your Github password.

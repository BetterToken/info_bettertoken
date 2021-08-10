# Creating a SSH Key on OSX
You generate an SSH key through Mac OS X by using the Terminal application. 3Bot needs an SSH key for encryption purposes.

## Finding the Terminal App

The terminal provides you with a text-based command line interface to the Unix shell of Mac OS X.
To open the Mac OS X Terminal, follow these steps:

- In Finder, choose Utilities from the Go menu. 
- Find the Terminal application in the Utilities window. 
- Double-click the Terminal application. 
- The Terminal window opens with the command line prompt displaying the name of your machine and your username.

An SSH key consists of a pair of files. One is the private key, **which you should never give to anyone. No one will ever ask you for it and if so, simply ignore them - they are trying to steal it.** 
The other is the public key. When you generate your keys, you will use ssh-keygen to store the keys in a safe location.

## To generate SSH keys in Mac OS X, follow these steps:

Enter the following command in the Terminal window:

`ssh-keygen -t rsa -b 4096`

This starts the key generation process. When you execute this command, the ssh-keygen utility prompts you to indicate where to store the key.

Press the ENTER key to accept the default location. The ssh-keygen utility prompts you for a passphrase.

Type in a passphrase. You can also hit the ENTER key to accept the default (no passphrase). However, we recommend to ALWAYS use a passphrase for security reasons.

You will need to enter the passphrase a second time to continue.

After you confirm the passphrase, the system generates the key pair and you will see output like this:

```
Your identification has been saved in /Users/yourmacusername/.ssh/id_rsa.
Your public key has been saved in /Users/yourmacusername/.ssh/id_rsa.pub.
The key fingerprint is:
ae:89:72:0b:85:da:5a:f4:7c:1f:c2:43:fd:c6:44:38 yourmacusername@yourmac.local
The key's randomart image is:
+--[ RSA 2048]----+
|                 |
|         .       |
|        E .      |
|   .   . o       |
|  o . . S .      |
| + + o . +       |
|. + o = o +      |
| o...o * o       |
|.  oo.o .        |
+-----------------+
```
Your private key is saved to the id_rsa file in the .ssh subdirectory of your home directory and is used to verify the public key you spin up your 3Bot.

**Warning Never share your private key with anyone! Ever! We mean it!**

Your public key is saved to a file called id_rsa.pub in the .ssh subdirectory of your home directory. 

You can copy it to your clipboard using the following command:

> pbcopy < ~/.ssh/id_rsa.pub

Your public key is now copied to your clipboard and you can now input it in the hosted 3Bot deployer to spin up your 3Bot.

[Step 4: Launch a Hosted 3Bot](getting_a_hosted_3bot.md)
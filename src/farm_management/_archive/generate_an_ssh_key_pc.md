# Generate SSH Keys On PC
We will now go over the steps on how to create a public and private key on PC using PuTTY.

## Step 1: Install PuTTY
1. Browse to the developer’s page, and download the installer for PuTTY:

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

2. Double-click the downloaded file and follow the installation wizard to finish the installation.

On the initial dialog of the installation wizard, click Next.

1. Select the destination folder. Use the default installation configuration unless you have a specific need to change it. Click Next to move on to the next screen.
2. Select destination folder for the PuTTY installation
3. Select PuTTY product features to be installed. Stick to the defaults if you do not have any specific needs. Click Next to move on to the next screen.
4. Putty product features selected
5. Once the process completes, click Finish to exit the installation wizard.

## Step 2: Run the PuTTY SSH Key Generator
1. Press the Windows key.

2. Type puttygen.

3. Under Best Match, right-click PuTTYgen.

4. Click Run as administrator.

5. If prompted, click Yes on the Do you want to allow this app to make changes to your device? pop-up.

## Step 3: Use PuTTY to Create a Pair of SSH Keys
The process outlined below will generate RSA keys, a classic and widely-used type of encryption algorithm. The PuTTY keygen tool offers several other algorithms – DSA, ECDSA, Ed25519, and SSH-1 (RSA).

If you require a different encryption algorithm, select the desired option under the Parameters heading before generating the key pair.

1. In the PuTTY Key Generator window, click Generate.

2. Move the cursor around in the gray box to fill up the green bar.

Generating an SSH key pair in Putty.
3. Save the public key:

Click the button labeled Save public key.
Choose a location to save the key.
Give the key a name (e.g., putty_key.pub)
Editing advanced SSH keys options in PuTTY.

4. Save the private key:

Click the Conversions menu at the top.
Click Export OpenSSH key.
You’ll be asked if you want to save a key without a passphrase. We highly recommend doing this for security measures.
Choose a location to save the key (usually the same folder as the public key).
Give the key a name (e.g., putty_key).

**Warning Never share your private key with anyone! Ever! We mean it!**

## Using Your SSH Keys
To use your SSH keys, copy your public SSH key to the system you want to connect to. Use your private SSH key on your own system. Your private key will match up with the public key, and grant access.

[Step 4: Launch a Hosted 3Bot](getting_a_hosted_3bot.md)
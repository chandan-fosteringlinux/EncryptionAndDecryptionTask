#  **Encrypt and Decrypt Messages Through netcat Webserver**

### **What You Need:**

1. A computer running Ubuntu or RHEL (Red Hat Enterprise Linux) with a terminal.  
2. The zip file: `symmetricEncryptionAndDecryption.zip`.

# **Section 1**

To check if `netcat` and `unzip` are installed on your system, you can use the following commands in the terminal:

### **Check for Netcat**

`nc -h`

If `netcat` is installed, you'll see a help message with usage instructions. If it's not installed, you might see an error message indicating that the command is not found.

### **Check for Unzip**

`unzip -v`

If `unzip` is installed, you'll see the version information and some details about how to use it. If it's not installed, you'll see a similar "command not found" error.

### **Install If Not Present**

If either tool is missing, you can install them as follows:

**For Debian/Ubuntu:**  
`sudo apt install netcat unzip`

**For RHEL/CentOS:**  
`sudo yum install nc unzip`

# **Section 2**

### **Step-by-Step Instructions:**

#### **Step 1: Unzip the File**

1. Open your terminal and navigate to the folder where the file symmetricEncryptionAndDecryption.zip is present.

And use the command to unzip the file:  
`unzip symmetricEncryptionAndDecryption.zip -d symmetricEncryptionAndDecryption`

2. This will create a folder called `symmetricEncryptionAndDecryption`.

#### **Step 2: Go into the Folder** `cd symmetricEncryptionAndDecryption`

#### **Step 3: Check Your Files**

You can see what files are in the folder by typing `ls` in terminal:  

You should see:  
   * `decryption.html`  
   * `message.sh`  
   * `Readme.md`  
   * `webserver.sh`

#### **Step 4: Give Permission to Run Scripts**

You need to allow the two script files to be executed. Type the following command:  
`chmod +x message.sh webserver.sh`

#### **Step 5: Open More Terminals**

1. Open two more terminal windows (sessions).

In each of these new terminal sessions, navigate back to the `symmetricEncryptionAndDecryption` directory by typing:

`cd ~/(to the path where the file SymmetricEncryptionAndDecryption is downloaded)`

#### **Step 6: Run the Scripts**

In the first terminal (Session 1), start the message script by typing:

`./message.sh`

In the second terminal (Session 2), start the web server script by typing:

`./webserver.sh`

#### **Step 7: Get the Encrypted Message**

In the third terminal (Session 3), send a request to the server using the `curl` command:

`curl http://localhost:4123`

You should receive an encrypted message like:  
`Jk oco vjku ku vjg ugetgv oguucig`

### => To decrypt the encrypted message follow the below steps

#### **Step 8: Open Your Browser**

1. Open your web browser.

In the address bar, type:

`http://localhost:3333`

2. and hit `Enter`. This will take you to a webpage with a form.

#### **Step 9: Decrypt the Message**

1. In the form, you will see two boxes:  
   * One for the encrypted message  
   * One for the encryption key  
2. Type the encrypted message you copied earlier (`Jk oco vjku ku vjg ugetgv oguucig`) in the first box.  
3. In the second box, type the number `2` (this is the key).  
4. Click the `Decrypt` button.

#### **Step 10: See the Decrypted Message**

1. After pressing the decrypt button, you will see the decrypted message displayed below the button.

### **Congratulations\!**

You have successfully encrypted and decrypted a message\! 🎉

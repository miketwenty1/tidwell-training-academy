# SSH 
#### Requirements: 
- Completed ch1.
- Computer with linux from ch1 connected to home router. We will call this computer A. (server).
- Another computer connected to the same router/wifi/network. We will call this Computer B. (client).

#### What we are doing
<img src="https://github.com/miketwenty1/images/blob/master/diagram_local_network.png?raw=true" width="750" />
- This diagram shows your linux computer will be accessed from a different computer on the same network.
- We will be using "SSH" or secure shell to access your linux machine.
- The reason it's "secure" is because all the network traffic will be encrypted with an "ssh key".
- Think of a shell as a program that helps your user expierence when you want to interact with the linux machine. From ch1 when you type in a command to the terminal you were using a shell! Now we will be using a remote computer to Tunnel into the computer to also use a terminal shell. The exact description here is a bit hand wavey.. but that's it in a nut "shell". bum bum tisk*.
- NOTE exact instructions on how to do this are ommitted on purpose so you can learn to be self sufficient. If you end up finding guides that want you to do other things, that's fine, but also try to do things the way that they are outlined here.

#### steps
1. Activate the standard linux open SSH server on computer A.
2. Run `netstat -an | grep LISTEN | grep 22` Verify you see output the that represents the port is open listening. If nothing comes back, your ssh server is probably not running. (Computer A).
3. Download an SSH client on the 2nd computer. (Computer B).
4. Create ssh key pair and copy the public key (Computer B).
5. Copy the public ssh key with the USB drive from Ch1 from Computer B to Computer A.
6. We will create a file called "authorized_keys" inside the home ssh directory `touch ~/.ssh/authorized_keys`. (Computer A).
7. Next let's drop the file from the USB anywhere on the computer. We will copy the contents of the public key and paste it into the authorized_keys file. Note, This is in a "." hidden directory so good luck figuring this out. (Computer A).
8. On Computer B we should be able to use our SSH client to "ssh" into the Computer A. It may prop for us to accept the connection "yes" the first time we access it.
9. While using Computer B, go to the temp folder `cd /tmp` and then make a file with the words "Hello World" `echo "Hello World" > hi.txt
10. On Computer A, go to the temp folder and run a list command. `cd /tmp`, `ls`. You should be able to see "hi.txt". Run a concatenate command to see the contents of the file. `cat hi.txt` you should be able to see "Hello World". 

#### Finished
- Congratulations you are on your way to being a shadowy super coder! You can now access your linux box from another computer, look at you go! 

## FAQ
- None yet.
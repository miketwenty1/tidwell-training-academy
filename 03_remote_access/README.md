# SSH 
#### Requirements: 
- Running Linux ssh server from ch2.
- External Network Access.
    - Access to internet that isn't your home's internet. (ex: Starbucks Wifi, your friend's internet, VPN, Hotspot on phone, etc.).

#### What we are doing
<img src="https://github.com/miketwenty1/images/blob/master/diagram.png?raw=true" width="750" />

- This diagram shows your linux computer will be accessed from a different computer from a remote network.
- We will be using "SSH" or secure shell to access your linux machine, similar to ch2.
- The main difference between ch2 and ch3 is we are accessing the same linux server but while you're not home. 
- This helps when you want to check something on your computer or some service at your home while you are away.
- Keep in mind opening up holes in your firewall allows opportunties not only for you, but other people to potentially attempt connections. It's important to think critically about how we are opening up your home network to remote access. We don't want to make it easy to be hacked by the N̶S̶A̶.. errh I mean foreign nations.


#### steps
1. While connected to your home network: Use your favorite search engine and type in "What is my IP" there will be plenty of services that will tell you what IP you are coming from.
2. First we will want to "open up" a port in your router. Ports range from 0 to 65535. The standard port for ssh is 22. Every router will have a slightly different way to do port forwarding. In very rare cases your ISP will not provide you the ability to do port forwarding or block access for you remote into your home network. You will need to figure out how to do port forwarding with your router. A quick google should get you there quick. 
    - Note: you may want to take time to learn about default gateways if you're having trouble finding how to get to you router.
3. We will want to port forward 22 to your linux server. This means anyone who knows your IP can attempt to use port 22 to get to your linux machine!
4. Now that you have port 22 destined for linux machine, it's time to try that ssh command from ch2, but this time you will use your public address instead of your private address. This will also give you the ability to ssh to your machine when you aren't connected to your home network.
5. BONUS: Switch the source port that is being forwarded to your machine externally. Many Routers will let you forward ports to non matching port numbers, ex: forwarding port 1337 to port 22. Now when you try to ssh you will need to specify port 1337, then your router will send to port 22. But now 1337 is a non standard ssh port which provides you a little bit of security. 
6. SUPER BONUS: ****If you find your router doesn't allow you to switch ports willy nilly, or if you want to just do the super bonus****
    - Configure your ssh server to listen on a different port (i.e. non 22, like port 1337).
    - Go back to your router port forward settings and just do 1337 to 1337. You will still need your client to specify the different port.

#### Finished
- Congratulations you now can access your computer's shell while you are away from the house! You learned about your public IP address that your ISP has given you. You learned about some ways of obfuscating the ports used when port forwarding.

## FAQ
- None yet.

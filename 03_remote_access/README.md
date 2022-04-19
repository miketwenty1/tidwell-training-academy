# Remote SSH 
#### Requirements: 
- Running Linux ssh server from ch2.
- External Network Access.
    - Access to internet that isn't your home's internet. (ex: Starbucks Wifi, your friend's internet, VPN, Hotspot on phone, etc.).

#### What we are doing
<img src="https://github.com/miketwenty1/images/blob/master/diagram.png?raw=true" width="750" />

- This diagram shows your linux computer being accessed from a different computer from a remote network.
- We will be using "SSH" or secure shell to access your linux machine, similar to ch2.
- The main difference between ch2 and ch3 is we are accessing the same linux server but you don't need to be home. 
- Keep in mind opening up holes in your firewall allows opportunties not only for you, but other people to attempt connections. It's important to think critically about how we are opening up your home network to remote access. We don't want to make it easy to be hacked by the N̶S̶A̶.. errh I mean foreign nations.
- ssh is a standard way of connecting to machines and getting shell access. A standard configured ssh server should be able to handle most of the security for you. The trick is typically keeping your ssh key safe.


#### steps
1. While connected to your home network: Use your favorite search engine and type in "What is my IP" there will be plenty of services that will tell you what IP you are coming from. Make sure to note this down for later.
2. We will want to "open up" a port in your router to allow access coming in from that Internet. Ports range from 0 to 65535. The standard port for ssh is 22. Every router will have a slightly different way to do port forwarding. In very rare cases your ISP will not provide you the ability to do port forwarding or block access for you to do remote connections into your home network. You will need to figure out how to do port forwarding with your router. A quick interwebs search should get you there quick. 
    - Note: you may want to take time to learn about default gateways if you're having trouble finding how to get to you router login/admin page.
3. We will want to port forward 22 to your linux server. This means anyone who knows your IP can attempt to use port 22 to get to your linux machine!
4. Now that you have port 22 destined for linux machine, it's time to try that ssh command from ch2, but this time you will use your public address instead of your private address. This will also give you the ability to ssh to your machine when you aren't connected to your home network.
    - Note depending on the sophistication of your router you may be able to select from a drop down list, or you may need to use the IP address as the destination (The IP you should of used in ch2 when ssh'ing).
5. BONUS: Switch the source port to be different but still route to port 22. Many Routers will let you forward ports to non matching port numbers, ex: forwarding port 1337 to port 22. Now when you try to ssh you will need to specify port 1337, then your router will send you to port 22. 1337 is a non standard ssh port which provides you a little bit of security. 
6. SUPER BONUS: ****If you find your router forces you to keep the source and destination ports the same, or if you want to just do the super bonus****
    - Configure your ssh server to listen on a different port (i.e. non 22, like port 1337).
    - Go back to your router port forward settings and just do 1337 to 1337. Now you are you a non standard ssh port but configured on your server.

#### Finished
- Congratulations you now can access your computer's shell while you are away from the house! You learned about your public IP address that your ISP has given you. You learned about some ways of obfuscating the ports used when port forwarding.

## FAQ
- None yet.

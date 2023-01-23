# Tor-Proxychains
<b>1. Introduction:</b>
<br>
Proxychains is a tool that forces any TCP connection made by any given application to follow through proxy like TOR or any other SOCKS4, SOCKS5, or HTTP(S) proxy.
<br>
<BR>
<B>2. What is SOCKS?</B>
<BR>
SOCKS is an Internet protocol that exchanges network packets between a client and server through a proxy server.

<b>Requirements:</b>
<br>
1. Tor

2. Proxychains
<br>

<b>Installation & Setup Guide:</b>
<br>
  
Step 1: 1st install tor with below command:
  
    sudo apt install tor
    
![Tor](https://user-images.githubusercontent.com/120317751/213859515-ef8c9107-b946-45fb-a75d-620ce06c14d1.gif)

Step 2: Proxychains install with below command

    sudo apt install proxychains   


![Proxychains](https://user-images.githubusercontent.com/120317751/213860469-a9916cd1-a6ae-4881-8328-0d8909049726.gif)

Step 3: Now enable tor service with below command

    sudo systemctl enable tor service
    

![Screenshot from 2023-01-23 08-19-27](https://user-images.githubusercontent.com/120317751/213958285-4a75656a-62e0-43cd-8b37-bbdef3999e26.png)


Step 4: Fixed Tor service issue with below command

    sudo service tor start
    
    
![Screenshot from 2023-01-23 08-23-42](https://user-images.githubusercontent.com/120317751/213958487-3530288c-fff4-45a3-bf31-a9bf81199314.png)

Step 5 : Now check tor service status

   sudo service tor status
   

![Screenshot from 2023-01-23 08-26-51](https://user-images.githubusercontent.com/120317751/213958784-84797fd3-3cfd-4e21-94c7-3decff07a3e2.png)


      Till now disable
      
------------------------------------------------------------------------  

Step 6: Lets go now fixed this issue

    sudo systemctl enable tor.service
  
    sudo systemctl enable tor
    

![Screenshot from 2023-01-23 08-33-32](https://user-images.githubusercontent.com/120317751/213959258-46b5350e-b4e7-4a7a-9526-0e3b053e554d.png)

Step 7: Now configure Proxychains.conf file

     sudo nano /etc/proxychains.conf
  
  
![Tor](https://user-images.githubusercontent.com/120317751/213960159-e0e265a5-670c-41bd-bdb6-750601bd9551.gif)
  
  
Remove & Replace comment from chain
  
     #Dynamic Chain -----> Dynamic Chain
  
     Strict Chain -------> #Strict Chain
  
     #Random Chain -------> Random Chain 
  
     ##Proxy DNS requests - no leak for DNS data ---> Proxy DNS requests - no leak for DNS data
  
Step 8: Also add Mention IP & PORT at the end of proxychains.conf file
  
      socks5  127.0.0.1 9050
  
  
  
![Screenshot from 2023-01-23 08-55-48](https://user-images.githubusercontent.com/120317751/213961008-c6814422-bdfa-4662-a0df-9d6fd2bd7fa3.png)










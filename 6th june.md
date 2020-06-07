Topic  Deploy your application/web page in docker (privately) | access web page outside | Snapshots helps in backup
# Day 7 - Hybrid Multi Cloud 06-06-2020
* For security purpose it is a good practice to launch only one  program on one OS.
- [x] Program used to connect to server using SSH is PUTTY. 
- [x] Now,on docker we want to install a webserver and start its services  using docker commands,
   -  If we try access this web server using its ip,we are unable to connect because  isolated.
   -  To solve this, using port forwarding we create a rule with Custom TCP protocol and create a port number.
   -  Whenever we try to connect to this port number it will be directed to the webserver and client can access.
   - Docker run -dit --name web1 -p 81:80 image_name this cmd launches the webserver with port number we provided.

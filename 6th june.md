# Topic  Deploy your application/web page in docker (privately) | access web page outside | Snapshots helps in backup
 Day 7 - Hybrid Multi Cloud 06-06-2020
* For security purpose it is a good practice to launch only one  program on one OS.
- [x] Program used to connect to server using SSH is PUTTY. 
- [x] Now,on docker we want to install a webserver and start its services  using docker commands,
   -  If we try access this web server using its ip,we are unable to connect because  isolated.
   -  To solve this, using port forwarding we create a rule with Custom TCP protocol and create a port number.
   -  Whenever we try to connect to this port number it will be directed to the webserver and client can access.
   - Docker run -dit --name web1 -p 81:80 image_name this cmd launches the webserver with port number we provided.

- [x] How to make data in our container persistent:
     - For this we require a block storage that we get from  EBS and create a volume .
     - Now to make the data of our webserver (Conatiner) we have to attach our volume to the container but we don't have a direct way to attach.
     - So,we first attach it to the docker host(Where docker is running) and create a partition and format it.
     - We have mount to this folder(Drive) to the conatiner while launching only,using below cmd: docker run -dit --name web -p 81:80 -V /driverfolder: /var/www/html image_name.
     - Thus using mount-binding we can make our data in our container consistent.
-[x] docker run -dit osname -p 81:80 imagename here , p means PAT ( port address Translation ) here 81:80 means , anyone can access it by providing port no. alongside ip ie. 12.25.135.42:81 We can allow this by go to Inbound rule in Security Group  Using Custom TCP , allow port no 81 and give access to everyone means anyone.
## In Order to Attach Volume to OS , we have to do 3 things .
```
 i) Partition - fdisk -l /dev/xvdf
 ii) Format - mkfs.ext4 /dev/xvdf1
 iii) Mount - mkdir /web , mount /dev/xvdf /web1
```
### Note 
We cannot Connect Volume to Docker OS directly , Firstly we connect volume(pendrive) to Base OS and then attach it to OS running on base OS.

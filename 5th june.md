Day6 - Hybrid Multi Cloud 05-06-2020
# Topic covered :-  limitations of CloudFront | Use case of Global Accelarator

- [x]  CDNaaS  is provided by  CloudFront in AWS &  poppy in  openstack
- [x] when we use CloudFront to decrease the tenancy by default it created local copy(cache), means data is old and not updated. 
### Creation of same Instances having same Hard disk 
 - [x]  Suppose we have a webserver running in our EC2 instance and there's a situation where we have to create more such webservers with same configuartion in that case v
 * Method 1  Creating our own AMI:
 *  Method 2   we create always a new instance ,install softwre in it and configure the webserver and start servicing.
*  Method 3   much better way is we configure a webserver and clone it and launch as many as we want.
           1.  first configure the webserver.
           2.  Now the hard disk on which our webserver is running contains every data of that server.
           3.  So we must create a clone(or snapshot) of that hard disk and we wil make a AMI out of it.

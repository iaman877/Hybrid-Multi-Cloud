today's Summary

# Topic Covered :- Aws Cloudfront with CDN
 ##  Theory -

- [x] Web app 
-  it contain two type of data
        * static content  -> Images, pdf etc. 
        *   Dynamic content -> Code etc.
 - In AWS static content is provided by S3 & dynamic content provided by EBS block  storage.
- [x] Problem statement_1  
- if  a client send request from Mumbai to USA, there should be no or minimum latency 
- [x] Solution_1
-   CDN 
- Akamai comapny providing CDN service
- [x] Problem statement_2
- EC2 does not provide any fault Tolerance 
- [x] Solution_2
- attach CDN to EC2, it will automatically manage fault tolerance.

## Implementation -

(1) Networking & content delivery  -> cloudfront 

(2)  step(1) create distribution 
     *  web distribution for static content (choose this)
     * RTMP for online streaming 
     
(3) Step(2) 
      * fill command as per your need.
      
- [x] with the help of bucket policy, we can apply more security to our web service 
- it also provide redirect to https service 
- have a look on what is blacklist & blocklist for country level.
     

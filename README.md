<h1>Hosting a Static Website using AWS S3 | Route 53 | AWS Certificate Manager</h1>

<h2>Project Overview</h2>
This project demonstrates the process of hosting a static website on Amazon Web Services (AWS) using three key services: Amazon S3 (Simple Storage Service), Amazon Route 53, and AWS Certificate Manager. The goal of this project is to provide a hands-on experience in deploying a secure and scalable static website on the AWS platform.
<br />

<h2>Key Components</h2>

- <b>Amazon S3 for Hosting: Utilizing Amazon S3, we host the static website content, including HTML, CSS, and JavaScript files. Amazon S3 offers a reliable and cost-effective solution for storing website content with high availability and scalability.</b>

- <b>Amazon Route 53 for Domain Management: We use Amazon Route 53 for domain name registration and forwarding. Route 53 serves as a scalable and highly available Domain Name System (DNS) web service, facilitating efficient domain management and routing of end-user requests to the Amazon S3 hosted website.</b>

- </b>CAWS Certificate Manager for Security: To ensure the security of our website, we utilize AWS Certificate Manager for SSL/TLS certificate management. This service allows us to easily provision, manage, and deploy public and private SSL/TLS certificates for use with AWS services, thereby enabling secure connections to our website.</b>

<h2>Integration with Canva for Design Elements</h2>
<b>In addition to leveraging AWS services, this project also integrates with Canva, a popular online design tool, to enhance the visual appeal and user experience of our static website. By using Canva, we can easily create and customize high-quality graphics, banners, and other visual elements without the need for advanced graphic design skills. This integration highlights the project's emphasis on not only technical functionality but also on aesthetic presentation.
</b>
  

<h2>Project Goals</h2>

- <b>Easy and Reliable Website Hosting: Demonstrate how to host a static website on Amazon S3 with high reliability and minimal configuration.</b>

- <b>Domain Registration and Management: Showcase the process of domain name registration and DNS management using Amazon Route 53.</b>

- <b>Enhancing Website Security: Implement SSL/TLS encryption for the website using AWS Certificate Manager, ensuring secure communication and data protection.</b> 


<h2>How to Use This Repository</h2>
This repository contains all the necessary resources and step-by-step guides to successfully complete this project. Follow the instructions in each section to set up your static website, register and manage your domain, and secure your website.


<br>

<h2>Program walk-through:</h2>
<br>


- <b>1. On Canva create a design you would want to be your landing page (I provided a recording studio landing page)</b>

<img src="https://i.imgur.com/0kjDMhf.png" height="50%" width="50%" alt="Create a design on Canva"/>

- <b>2. After you are done with your image click SHARE (in the top right hand corner) and click EMBED</b>

<img src="https://i.imgur.com/VS8BhIc.png" height="50%" width="50%" alt="Click Share"/>

- <b>3. Copy HTML embedded code.</b>

<img src="https://i.imgur.com/9RVt3lg.png" height="50%" width="50%" alt="Copy embedded code"/>

- <b>4. Open AWS, search for S3 and press enter</b>

<img src="https://i.imgur.com/DOCwi8o.png" height="40%" width="40%" alt="Search S3"/>

- <b>5. Click “Create bucket”</b>

- <b>5b. DISCLAIMER: Before you create a bucket be sure to go to Route 53 and check if your domain name is available!!! You will be repeating this step twice. One for (www .YOURDOMAIN.com) and one for (YOURDOMAIN.com). For my scenario im using Studiowebsite but if you are creating a new project for yourself make sure to us use your domain name as the bucket name.</b>

<img src="https://i.imgur.com/AgiaGfq.png" height="40%" width="40%" alt="Create bucket"/>
<br>

- <b>6. Change "Bucket name" to "YOURDOMAIN" and don't use www in front.</b>

- <b>6b. DisCLAIMER: In my project I used "studiowebsite" when I should have used "studiowebsite.com" if that was going to be the name of my website Im trying to host in S3. Be sure to make the bucket the correct domain name that you are planning on using for your website! 

<img src="https://i.imgur.com/jSWMZzH.jpg" height="40%" width="40%" alt="Change Bucket name to studiowebsite"/>
<br>
  
- <b>7. Uncheck “Block all public access” to allow public access and then check “I acknowledge”</b>

<img src="https://i.imgur.com/bpCtDUu.png" height="40%" width="40%" alt="Uncheck Block Public Access"/>
<br>

- <b>8. Scroll down and click “Create bucket”</b>

<img src="https://i.imgur.com/0achovu.png" height="40%" width="40%" alt="Create bucket"/>
<br>

- <b>9. Upload the downloaded “index.html” file into the bucket</b>

<img src="https://i.imgur.com/02O8EfC.png" height="40%" width="40%" alt="Upload index.html"/>
<br>

- <b>10. Click on the bucket name “studiowebsite” and click “Properties”</b>

<img src="https://i.imgur.com/U3Dm4ud.png" height="40%" width="40%" alt="properties "/>
<br>

- <b>11. Scroll down and in the “Static website hosting” section click edit and “Enable” Static website hosting</b>

<img src="https://i.imgur.com/p7fdDkU.png" height="40%" width="40%" alt="Enable Static Website Hosting"/>
<br>
  
- <b>12. In the "index document" section type in, index.html</b>

<img src="https://i.imgur.com/gQaC3rh.png" height="40%" width="40%" alt="Type index.html"/>
<br>

- <b>13. Click "Save change"</b>

<img src="https://i.imgur.com/I9Cmavk.png" height="40%" width="40%" alt="Save Change"/>
<br>

- <b>14. Click on “Permissions”. In the “Bucket policy” section click “Edit”</b>

<img src="https://i.imgur.com/3uAwvtn.png" height="40%" width="40%" alt="Click Edit"/>
<br>

- <b>15. Click "Policy generator</b>

<img src="https://i.imgur.com/IRv4BS5.png" height="40%" width="40%" alt="Policy generator"/>
<br>

- <b>16. In the “Type of Policy” section select “S3 Bucket Policy”</b>

<img src="https://i.imgur.com/yp8jKpi.png" height="40%" width="40%" alt="S3 Bucket Policy"/>
<br>
  
- <b>17. In the “Principal” section type “*”</b>

<img src="https://i.imgur.com/nZYYESz.png" height="40%" width="40%" alt="Wildcard"/>
<br>
  
- <b>18. Under “Actions”, scroll to “GetObject” and select it</b>

<img src="https://i.imgur.com/Y4cSC7Y.png" height="40%" width="40%" alt="S3 GetObject"/> 
<br>

- <b>19. In the Amazon Resoarce Name (ARN) section, go back to the previous page and copy the S3 ARN then paste it in the section.</b>

<img src="https://i.imgur.com/pzWxAM1.png" height="40%" width="40%" alt="Copy ARN Number"/>
<br>

- <b>20. Click Add Statement and then click “Policy Generator” </b>

<img src="https://i.imgur.com/XEo9jP3.png" height="40%" width="40%" alt="Policy Generator"/> 
<br>

- <b>21. Copy code and paste it into your “Bucket policy”</b>

<img src="https://i.imgur.com/jn3HnC6.png" height="40%" width="40%" alt="Copy Code"/> 
<br>

- <b>22. On the “Resoarce” line, add a “ /* “ after arn:aws:s3:::studiowebsite (It should look like arn:aws:s3:::studiowebsite/*)</b>

<img src="https://i.imgur.com/wuswu7Q.png" height="40%" width="40%" alt="Add /*"/>
<br>

- <b>23. Click "Save change"</b>

<img src="https://i.imgur.com/8iBGlR1.png" height="40%" width="40%" alt="Save change"/>
<br>

- <b>24. Go back to “S3” and click on the “studiowebsite” bucket</b>

<img src="https://i.imgur.com/8Nj9vjO.png" height="40%" width="40%" alt="studiowebsite "/>
<br>

- <b>25. Click on “index.html”</b>

<img src="https://i.imgur.com/5B0Z1sB.png" height="40%" width="40%" alt="Click on the indeh.html "/>
<br>

- <b>26. Click on the “Object URL” link to access your recording studio website.</b>

<img src="https://i.imgur.com/XPInyVm.png" height="40%" width="40%" alt="Click on the Object URL "/>
<br>

- <b>27. Check out the Site</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="All Done"/>
<br>

- <b>28. We will need to repeat steps 5-27 again but change the NEW bucket name to www.YOURDOMAIN.com. You should end up with two identical S3 buckets pertaining the index.Html file with the exception of the bucket names. One has www followed by your website YOURDOMAIN.com and one s3 bucket with just your domain.com.




<br>
<br>
<h2>Story Time</h2>
<b>During the course of this project, I embarked on a journey to enhance the S3 Bucket-hosted website by linking it to a domain name I had registered earlier through Route 53. This endeavor led me to make some adjustments in my setup that, in hindsight, would have been beneficial to implement from the start, especially with the plan to use Route 53 as a DNS service.

One key insight I'd like to share, which would have streamlined the process, involves the setup of S3 buckets. Here's what I would have done differently:

Create Dual S3 Buckets: My approach would have been to establish two S3 buckets, namely WWW.YOURDOMAIN.COM and YOURDOMAIN.COM. Both of these would contain the same index.html web page script. This configuration is crucial for ensuring that these buckets are recognized and correctly linked when setting up alias forwarding in Route 53. It became clear to me, through some trial and error, that if the bucket names don't precisely match the domain name registered in Route 53, they won't appear as intended.
This realization came as a pivotal learning moment. Now, equipped with this knowledge, I'm able to more efficiently architect and deploy AWS services in my infrastructure.</b>
<b> Ok back to the project!</b>

<br>
<br>
</br>





- <b>29. Search for route 53 in the AWS search bar and select get started.</b>

<img src="https://i.imgur.com/4rGLJs4.png" height="40%" width="40%" alt="Get Started"/>
<br>

- <b>30. Register a new domain (choose a domain that you want and select if you want the domain to renew yearly. Keep in mind that it can take from a few minutes to 72 hours for your domain to become available).</b>

<img src="https://i.imgur.com/LCe9Sxs.jpg" height="40%" width="40%" alt="All Done"/>
<br>

- <b>31. After registering your domain name in route 53, head over to the left pane and click hosted domains. Click on the domain name and click create record.</b>

<img src="https://i.imgur.com/Rm5CG8i.png" height="40%" width="40%" alt="Create Record"/>
<br>

- <b>32. In create record, leave record name empty. In "Record type" leave it on "A-Routes traffic to an IPV4 address and some AWS resources". Enable the "Alias" checkbox to allow forwarding. Route traffic to "Alias to S3 website endpoint" and choose your region both S3 buckets are in. In the "Enter S3 endpoint" dropdown, you should see your bucket name and domain that does not have the www. Click Create Records.</b>

<img src="https://i.imgur.com/QY4b8y5.png" height="40%" width="40%" alt="Record Settings"/>
<br>

- <b>33. Duplicate the previous step but input "www" in the Record name as a subdomain. You should have 2 new records for your domain.</b>

<img src="https://i.imgur.com/cLphZix.png" height="40%" width="40%" alt="2 New Records"/>
<br>

- <b>34. Test the domain by going to your browser and typing in (YOURWEBSITE.com) and (WWW.YOURDOMAIN.COM) to make sure it works.</b>

<img src="https://i.imgur.com/nnHp2bs.jpg" height="40%" width="40%" alt="All Done"/>
<br>

- <b>35.The next step will be to secure your website using AWS Certificate manager.</b>

<img src="https://i.imgur.com/4GsdvEa.jpg" height="40%" width="40%" alt="All Done"/>
<br>

- <b>36. Search "Certificate Manager" in the AWS search bar and select it. Select "Request". Keep Certificate type at "Request a public certificate" and click "Next".</b>

<img src="https://i.imgur.com/ZKyVUZZ.png" height="40%" width="40%" alt="Request Public Server"/>
<br>

- <b>37. In the "Fully qualified domain name box input your "YOURDOMAIN.COM". Click "Add another name to this certificate" and input "*.YOURDOMAIN.COM" the *. allows you to get a certificate for a subdomain (ex:www.YOURDOMAIN.com). Click Request.</b>

<img src="https://i.imgur.com/wlITCXJ.png" height="40%" width="40%" alt="All Done"/>
<br>

- <b>38. On the certificates page, click on the certificate that has the www subdomain. Click on "Create records in Route 53". This will create a record set in Route 53.</b>

<img src="https://i.imgur.com/pO1Qfqi.png" height="40%" width="40%" alt="Create Records"/>
<br>


- <b>39. On the "Create DNS records in Amazon Route 53" page, you should see "Success" in the "Validation status". (If you don't see your certificates, then you need to clear the filter).</b>

- <b>40. Repeat step 38 with the other certificate (YOURDOMAIN.COM)</b>

- <b>41. Go into your browser and type in your website domain and see you new secured website</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="All Done"/>
<br>
</br>

- <b>42. Back in the AWS "Search bar" search "CloudFront"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Search CloudFront"/>


- <b>43. On the CloudFront distribution page, click "Create Distribution".

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Create Distribution"/>   


- <b>44. Click in the "Origin Domain" box and select the s3 bucket that has your domain name without the www.

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Origin Domain"/>


- <b>45. In the "Origin Access" section choose "Origin Acces Control Settings" and click "Control Settings"

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Create Control Settings"/>


- <b>46. On the "Create Control Settings" page, make sure "Oregin Type" says "S3" and click "Create".

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Create Control Settings"/>


- <b>47. In the "Viewer Protocol Policy" area select "Redirect HTTP to HTTPS"

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Viewer Protocol Policy"/>


- <b>48. On the "Cache key and origin requests" nsection make sure it says "CacheOptimized".

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="CacheOptimized"/>


- <b>In the "Web Application Firewall (WAF)" nsection, enable "Do not enable security protections"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="CacheOptimized"/>


- <b>In the "Custom SSL certificate" area, select in the dropdown the AWS certificate tha has you domain name with out the www.</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="AWS Certificate"/>


- <b>In the "Default root object" area, input "index.html"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="index.html"/>


- <b>In the header you will see that you need to change the S3 bucket policy to allow CloudFront to read from S3. Click "Copy Policy" and then click "Go to S3 bucket permissions to update policy"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="index.html"/>


- <b>In the S3 bucket "Permissions" scroll down to "Bucket Policy" and click "Edit". Erase the existing policy and paste the new policy"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="New Policy"/>


- <b>Click "Save Changes"</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Save Changes"/>


- <b> In the "Block public access" access select " Block all publick access"and click "Seve Changes"</b>


<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="Block publick access"/>

- <b> Type in your domain Name in the Browser and whitness your website loading much faster.....






<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

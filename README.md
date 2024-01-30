<h1>Hosting a Static Website using AWS S3</h1>

<h2>Description</h2>
Project consists of hosting a static website on AWS S3.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Amazon S3</b>
- <b>Canva</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 

<h2>Description</h2>
Project consists of hosting a static website on AWS S3.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Amazon S3</b>
- <b>Canva</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 

<h2>Program walk-through:</h2>


- <b>1. On Canva create a design you would want to be your landing page (I provided a recording studio landing page)</b>

<img src="https://i.imgur.com/0kjDMhf.png" height="50%" width="50%" alt="Create a design on Canva"/>

- <b>2. After you are done with your image click SHARE (in the top right hand corner) and click EMBED</b>

<img src="https://i.imgur.com/VS8BhIc.png" height="50%" width="50%" alt="Click Share"/>

- <b>3. Copy HTML embedded code.</b>

<img src="https://i.imgur.com/9RVt3lg.png" height="50%" width="50%" alt="Copy embedded code"/>

- <b>4. Open AWS, search for S3 and press enter</b>

<img src="https://i.imgur.com/DOCwi8o.png" height="40%" width="40%" alt="Search S3"/>

- <b>5. Click “Create bucket”</b>
-<b>5a. DISCLAIMER: Before you create a bucket be sure to go to Route 53 and check if your domain name is available!!! You will be repeating this step twice. One for (www .YOURDOMAIN.com) and one for (YOURDOMAIN.com). For my scenario im using Studiowebsite but if you are creating a new project for yourself make sure to us use your domain name as the bucket name.</b>

<img src="https://i.imgur.com/AgiaGfq.png" height="40%" width="40%" alt="Create bucket"/>

- <b>6. Change "Bucket name" to "studiowebsite"</b>

 <img src="https://i.imgur.com/jSWMZzH.jpg" height="40%" width="40%" alt="Change Bucket name to studiowebsite"/>
  
- <b>7. Uncheck “Block all public access” to allow public access and then check “I acknowledge”</b>

<img src="https://i.imgur.com/bpCtDUu.png" height="40%" width="40%" alt="Uncheck Block Public Access"/>

- <b>8. Scroll down and click “Create bucket”</b>

<img src="https://i.imgur.com/0achovu.png" height="40%" width="40%" alt="Create bucket"/>

- <b>9. Upload the downloaded “index.html” file into the bucket</b>

<img src="https://i.imgur.com/02O8EfC.png" height="40%" width="40%" alt="Upload index.html"/>

- <b>10. Click on the bucket name “studiowebsite” and click “Properties”</b>

<img src="https://i.imgur.com/U3Dm4ud.png" height="40%" width="40%" alt="properties "/>

- <b>11. Scroll down and in the “Static website hosting” section click edit and “Enable” Static website hosting</b>

  <img src="https://i.imgur.com/p7fdDkU.png" height="40%" width="40%" alt="Enable Static Website Hosting"/>
  
- <b>12. In the "index document" section type in, index.html</b>

<img src="https://i.imgur.com/gQaC3rh.png" height="40%" width="40%" alt="Type index.html"/>

- <b>13. Click "Save change"</b>

<img src="https://i.imgur.com/I9Cmavk.png" height="40%" width="40%" alt="Save Change"/>

- <b>14. Click on “Permissions”. In the “Bucket policy” section click “Edit”</b>

<img src="https://i.imgur.com/3uAwvtn.png" height="40%" width="40%" alt="Click Edit"/>

- <b>15. Click "Policy generator</b>

<img src="https://i.imgur.com/IRv4BS5.png" height="40%" width="40%" alt="Policy generator"/>

- <b>16. In the “Type of Policy” section select “S3 Bucket Policy”</b>

  <img src="https://i.imgur.com/yp8jKpi.png" height="40%" width="40%" alt="S3 Bucket Policy"/>
  
- <b>17. In the “Principal” section type “*”</b>

  <img src="https://i.imgur.com/nZYYESz.png" height="40%" width="40%" alt="Wildcard"/>
  
- <b>18. Under “Actions”, scroll to “GetObject” and select it</b>

  <img src="https://i.imgur.com/Y4cSC7Y.png" height="40%" width="40%" alt="S3 GetObject"/> 

- <b>19. In the Amazon Resoarce Name (ARN) section, go back to the previous page and copy the S3 ARN then paste it in the section.</b>

<img src="https://i.imgur.com/pzWxAM1.png" height="40%" width="40%" alt="Copy ARN Number"/>

- <b>20. Click Add Statement and then click “Policy Generator” </b>

  <img src="https://i.imgur.com/XEo9jP3.png" height="40%" width="40%" alt="Policy Generator"/> 

- <b>21. Copy code and paste it into your “Bucket policy”</b>

  <img src="https://i.imgur.com/jn3HnC6.png" height="40%" width="40%" alt="Copy Code"/> 

- <b>22. On the “Resoarce” line, add a “ /* “ after arn:aws:s3:::studiowebsite (It should look like arn:aws:s3:::studiowebsite/*)</b>

 <img src="https://i.imgur.com/wuswu7Q.png" height="40%" width="40%" alt="Add /*"/>

- <b>23. Click "Save change"</b>

<img src="https://i.imgur.com/8iBGlR1.png" height="40%" width="40%" alt="Save change"/>

- <b>24. Go back to “S3” and click on the “studiowebsite” bucket</b>

<img src="https://i.imgur.com/8Nj9vjO.png" height="40%" width="40%" alt="studiowebsite "/>

- <b>25. Click on “index.html”</b>

<img src="https://i.imgur.com/5B0Z1sB.png" height="40%" width="40%" alt="Click on the indeh.html "/>

- <b>26. Click on the “Object URL” link to access your recording studio website.</b>

<img src="https://i.imgur.com/XPInyVm.png" height="40%" width="40%" alt="Click on the Object URL "/>

- <b> Check out the Site</b>

<img src="https://i.imgur.com/b8q6Dz4.png" height="40%" width="40%" alt="All Done"/>






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

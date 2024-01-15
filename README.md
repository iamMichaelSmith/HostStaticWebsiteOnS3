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

- <b>2. After you are done with your image click SHARE (in the top right hand corner) and click EMBED</b>

- <b>3. Copy HTML embedded code.</b>

- <b>4. Open AWS, search for S3 and press enter</b>

- <b>5. Click “Create bucket”</b>

- <b>6. Change "Bucket name" to "studiowebsite"</b>

 <img src="https://i.imgur.com/jSWMZzH.jpg" height="40%" width="40%" alt="Change Bucket name to studiowebsite"/>
  
- <b>7. Uncheck “Block all public access” to allow public access and then check “I acknowledge”</b>

- <b>8. Scroll down and click “Create bucket”</b>

- <b>9. Upload the downloaded “index.html” file into the bucket</b>

- <b>10. Click on the bucket name “studiowebsite” and click “Properties”</b>

- <b>11. Scroll down and in the “Static website hosting” section click edit and “Enable” Static website hosting</b>

  <img src="https://i.imgur.com/p7fdDkU.png" height="40%" width="40%" alt="Enable Static Website Hosting"/>
  
- <b>aa. In the "index document" section type in, index.html</b>

- <b>bb. Click "Save change"</b>

- <b>12. Click on “Permissions”. In the “Bucket policy” section click “Edit”</b>

- <b>cc. Click "Policy generator</b>

- <b>13. In the “Type of Policy” section select “S3 Bucket Policy”</b>

  <img src="https://i.imgur.com/yp8jKpi.png" height="40%" width="40%" alt="S3 Bucket Policy"/>
  
- <b>14. In the “Principal” section type “*”</b>

  <img src="https://i.imgur.com/nZYYESz.png" height="40%" width="40%" alt="Wildcard"/>
  
- <b>15. Under “Actions”, scroll to “GetObject” and select it</b>

  <img src="https://i.imgur.com/Y4cSC7Y.png" height="40%" width="40%" alt="S3 GetObject"/> 

- <b>16. In the Amazon Resoarce Name (ARN) section, go back to the previous page and copy the S3 ARN then paste it in the section.</b>

- <b>17. Click Add Statement and then click “Policy Generator” </b>

  <img src="https://i.imgur.com/XEo9jP3.png" height="40%" width="40%" alt="Policy Generator"/> 

- <b>18. Copy code and paste it into your “Bucket policy”</b>

  <img src="https://i.imgur.com/jn3HnC6.png" height="40%" width="40%" alt="Copy Code"/> 

- <b>19. On the “Resoarce” line, add a “ /* “ after arn:aws:s3:::studiowebsite (It should look like arn:aws:s3:::studiowebsite/*)</b>

 <img src="https://i.imgur.com/wuswu7Q.png" height="40%" width="40%" alt="Add /*"/>

- <b>20. Click "Save change"</b>

- <b>21. Go back to “S3” and click on the “studiowebsite” bucket</b>

- <b>22. Click on “index.html”</b>

- <b>23. Click on the “Object URL” link to access your recording studio website.</b>

  <img src="https://i.imgur.com/yp8jKpi.png" height="40%" width="40%" alt="Change "S3 Bucket Policy"/>

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

<h1>Create a Static Website Using Amazon S3</h1>

<h2>Description</h2>
In this project we will be utilizing AWS S3 to create and configure a simple cost efficient static website used to host files such as HTML, CSS, JavaScript, fonts, and images. The site will also include a custom error page.
<br />

<img src="https://imgur.com/VaIpvWO.png" height="85%" width="85%" />


<h2>Environments Used </h2>

- <b>AWS S3</b>

<h2>Project walk-through:</h2>

<p align="center">
First we have to create an S3 bucket and select the region we wish to host it in, which for mine will be us-east-1. Make sure to make the name unique, I included my account ID at the end for mine. <br/>
<img src="https://imgur.com/b7wK2eZ.png" height="80%" width="80%" />
<br />
<br />
We also need to make sure to uncheck the 'S3 Block Public Access' and acknowledge the changes because this is a web server, we want this publicly accessible.  <br/>
<img src="https://imgur.com/X1B3rvq.png" height="80%" width="80%"
<br />
<br />
Bucket is created, copy the ARN of the bucket, we will need this when we edit our policy. <br/>
<img src="https://imgur.com/F3jv7kr.png" height="80%" width="80%"
<br />
<br />
We now need to upload the index.html and error.html documents to the bucket. I've included the html code in my repo.  <br/>
<img src="https://imgur.com/WLGo46U.png" height="80%" width="80%"
<br />
<br />
<img src="https://imgur.com/zhIrHDf.png" height="80%" width="80%"
<br />
<br />
<img src="https://imgur.com/L7Pm30M.png" height="80%" width="80%"
<br />
<br />
Scroll down to 'Static Website Hosting' within bucket properties and enable static website hosting, specify the index and error documents, and save changes.  <br/>
<img src="https://imgur.com/KGYazV8.png" height="80%" width="80%"
<br />
<br />
If we scroll back down to Static Website hosting in bucket properties we can see the bucket endpoint. Click the url.  <br/>
<img src="https://imgur.com/YZNBAAg.png" height="80%" width="80%"
<br />
<br />
Though we have a functional web server running now, we get a '403 Forbidden' error because we have not setup permissions for the files on the webserver. Lets do that now.  <br/>
<img src="hhttps://imgur.com/Bjwp143.png" height="80%" width="80%"
<br />
<br />
This JSON policy allows the web server to get objects from the bucket and provide to the end user that is requesting them through their web browser.  <br/>
<img src="https://imgur.com/2mGVkSm.png" height="80%" width="80%"
<br />
<br />
After clicking on the URL or simply refreshing our page we can see that the static page is now up and running!  <br/>
<img src="https://imgur.com/BA5DOY0.png" height="80%" width="80%"
<br />
<br />
Also check the error page by inputting random characters in the URL, I'll put /blahblahblah.html <br/>
<img src="https://imgur.com/I9VbueO.png" height="80%" width="80%"
<br />
<br />
Thank you for following along if you did! <br/>

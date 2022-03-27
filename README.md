# AWS-CloudFront
AWS CloudFront

## Create a S3 bucket

***Step-1:***
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/1.png)

- Click on Create bucket 

***Step2***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/2.png)
- changed the bucket name to ***surya-cloudfront*** and region to ***Asia Pacific (Mumbai) ap-south-1***
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/3.png)
- Added tag Name ***surya-cloudfront***

Leaved the rest as default and clicked ***create bucket***

***Step3***

Upload a Demo website to ***S3*** bucket ***surya-cloudfront*** 
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/4.png)
Now click ***Upload***
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/5.png)

***Step4***

Now go to ***Amazon S3 >> Buckets >> surya-cloudfront >> index.html*** and click ***open*** butten
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/6.png)

Now you can see the website loding without any images in it
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/7.png)

***Step5***

## Now go to ***Cloud Front*** and click ***Create Distribution*** 
- Give ***Origin name*** 
- Give ***Name***
-  Set ***S3 bucket access*** enable ***Yes use OAI (bucket can restrict access to only CloudFront)*** and Select an OAI(If there is no OAI clicl ***create new OAI***
-  Set ***Bucket policy*** and enable ***Yes, update the bucket policy***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/8.png)

- Set ***Viewer*** enable ***Redirect HTTP to HTTPS***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/9.png)

- Set ***Alternate domain names*** as ***cloudfront.suryakiran.online***
- Set ***Default root object*** as ***index.html***
- For setting ***Custom SSL certificate*** click ***Request certificate***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/10.png)

- Select ***Request a public certificate*** and click ***Next***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/11.png)

- Click in the ***Certificate ID***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/12.png)

- Click ***Create Records in Route 53***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/13.png)
![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/14.png)

- Check ***Rout 53***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/15.png)

- Click ***Create Distribution***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/16.png)

- Now The Distribution is created

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/17.png)

Now Create a ***A record*** in ***Rout 53***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/18.png)

- Now try ***https://d1ivjkpgpq6n8k.cloudfront.net***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/19.png)

- Now try ***https://cloudfront.suryakiran.online/***

![alt text](https://github.com/SuryakiranSubramaniam/AWS-CloudFront/blob/main/image/20.png)

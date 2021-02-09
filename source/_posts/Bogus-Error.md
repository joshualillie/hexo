---
title: Bogus Error
date: 2021-02-08 19:41:38
tags:
- development
categories:
- Development
---
I spent several hours on an AWS goose chase and have come to the conclusion that AWS has a faulty error. Some may feel that the fault is my own and that the problem should have been obvious, but even if this is true, it does not change the fact that AWS's error, at the time of this writing, is wrong.

<img src="/images/bogus_error.png" style="width:200px; float:left;"> 

I ran into the problem while trying to accomplish a very simple task :

- Create an S3 Bucket
- Update policy on that bucket
- Create CloudFront Distribution linked to S3 bucket

There are two main ways to set up CloudFront origin with an S3 bucket: the S3 API and the S3 URL. There are a lot of tutorials that show how to set these types of configurations up. The latter method - setting CloudFront to point to the S3 website (not the API) - requires you to set the S3 bucket with a policy that looks something like this:

```json
{
    "Version": "2012-10-17",
    "Id": "Policy1522074684919",
    "Statement": [
        {
            "Sid": "Stmt1522074683215",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::blog.somewebsite.com/*"
        }
    ]
}
```

Now... if you are logged into the console as your root account, and you create a brand new S3 bucket and go straight to that bucket's Permissions tab and enter in this policy, you will get the error you see above that reads : "You don't have permissions to edit bucket policy. After you or your AWS administrator have updated your permissions to allow the s3:PutBucketPolicy action, choose Save changes. Learn more about Identity and access management in Amazon S3." Now some of you are probably saying "NO, YOU MISSED A STEP". And that is true. But it does not change the fact that this error is wrong. 

The root user DOES have permission to update the policy. The s3:PutBucketPolicy action is not the issue at all in this case.
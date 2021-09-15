# Static-website-on-S3-AWS

You can use Amazon S3 to host a static website.

Steps to host a static website-

```

1. Create an S3 bucket.

2. In the properties select option to Enable static website hosting for S3 bucket.

3. Upload html files to the bucket

4. Enable public access and add below bucket policy-
{ 
    "Version": "2012-10-17", 
    "Statement": [ 
        { 
            "Sid": "PublicReadGetObject", 
            "Effect": "Allow", 
            "Principal": "*", 
            "Action": [ 
                "s3:GetObject" 
            ], 
            "Resource": [ 
                "arn:aws:s3:::simpli-first-demo-bucket/*" 
            ] 
        } 
    ] 
} 

4. Try accessing the object from it's public URL

```

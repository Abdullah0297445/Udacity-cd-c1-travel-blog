# Udacity Cloud Developer Nanodegree

Project submission: **Deploy Static Website on AWS**

## RUBRIC

1. **The student has created a S3 bucket.**
![S3 bucket visible in AWS management console](./screenshots/s3_bucket_visible.png)

2. **All website files should be added to the S3 bucket.**
![Website files available in bucket](./screenshots/files_available_in_bucket.png)

3. **The bucket configuration should be set up to support static website hosting.**
![Static hosting enabled](./screenshots/static_hosting_enabled.png)

4. **The permission access to the bucket should be configured.**

    ```json
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "PublicReadGetObject",
                "Effect": "Allow",
                "Principal": "*",
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::udacity-cd-c1-travel-blog/*"
            },
            {
                "Sid": "Cloudfront",
                "Effect": "Allow",
                "Principal": {
                    "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity E15I2Z9YDI46GF"
                },
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::udacity-cd-c1-travel-blog/*"
            }
        ]
    }
    ```

    > One thing to add: We don't need to make the bucket public since we are gonna hook it upto to Cloudfront anyway, and it automatically takes care of this via second bucket policy above.
    >
    > But I am making it public as well because it is specified in the rubric.

5. **The website should be distributed via Cloudfront.**
![Cloudfront distro](./screenshots/cloudfront_distro.png)

6. **Is the website publicly accessible?**

* Cloudfront domain name: <https://dqecxug1yjxas.cloudfront.net>
* S3 Website-endpoint URL: <http://udacity-cd-c1-travel-blog.s3-website-us-east-1.amazonaws.com>

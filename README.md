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
![Bucket policy](./screenshots/bucket_policy.png)

    > One thing to add: We don't need to make this bucket 'public' since we are gonna hook it upto to Cloudfront anyway, and it automatically takes care of this via second bucket policy in the image above.
    >
    > But I am making it public as well because it is specified in the rubric.

5. **The website should be distributed via Cloudfront.**
![Cloudfront distro](./screenshots/cloudfront_distro.png)

6. **Is the website publicly accessible?**

* Cloudfront domain name: <https://dqecxug1yjxas.cloudfront.net>
* S3 Website-endpoint URL: <http://udacity-cd-c1-travel-blog.s3-website-us-east-1.amazonaws.com>

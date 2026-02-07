# AWS S3 Hands-On Lab

## Objectives
- Create an S3 bucket
- Upload objects and manage permissions
- Host a static website on S3

## Steps Completed

### 1. Bucket Creation
![Creating a Bucket](images/creating-bucket.png)
- Bucket name: `my-first-bucket-candi`
- Region: `us-east-1`
- Block Public Access: Disabled (for learning purposes)

### 2. Object Upload & Public Access
- Uploaded image file
- Configured ACL to allow public read access
- Accessed file via public URL

### 3. Static Website Hosting
![Static Website Hosting](images/static-website-hosting.png)
- Enabled static website hosting on bucket
- Created and uploaded `index.html`
- Accessed website via S3 website endpoint

## Lessons Learned
- S3 is object storage with unlimited scalability
- Public access requires both bucket policies and object-level permissions
- Static website hosting is simple and cost-effective
- Security best practices recommend keeping Block Public Access enabled in production

## Commands/Configurations Used
- AWS Console for bucket creation
- ACL settings for public access
- HTML for static website
- S3 website endpoint configuration

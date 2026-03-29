# Lab 02 - S3 Static Website

## Objective

Create and configure an Amazon S3 bucket to host a simple static website, while understanding public access controls and bucket policies.

## Services Used

- Amazon S3
- IAM (for access context)

## What I Built

- Created an S3 bucket with a globally unique name
- Uploaded static website files such as `index.html`
- Enabled static website hosting for the bucket
- Configured access settings so the site content could be read publicly
- Reviewed a bucket policy that allows `s3:GetObject` for website objects

## Key Concepts

Amazon S3 is an object storage service. Data is stored as objects inside buckets rather than as files on a traditional server filesystem.

Static website hosting allows an S3 bucket to serve HTML, CSS, JavaScript, and image files directly over HTTP. This is useful for lightweight sites that do not require server-side processing.

S3 Block Public Access settings help prevent accidental public exposure. When hosting a public static site, these settings and the bucket policy must be configured carefully so only the intended objects are accessible.

Bucket policies are resource-based policies attached directly to the bucket. They define which principals can perform actions such as reading objects.

Public read access should be scoped only to the website content required for delivery. Administrative operations should remain protected through IAM identities.

## Steps Performed

1. Created a new S3 bucket in the AWS Management Console with a unique bucket name.
2. Reviewed the default Block Public Access settings and noted how they affect website availability.
3. Uploaded the static site files, including an `index.html` landing page.
4. Enabled static website hosting and set the index document.
5. Applied a bucket policy to allow public `GetObject` access to site content.
6. Tested the website endpoint and confirmed the files were being served correctly.
7. Documented the security tradeoff between public content delivery and unrestricted bucket exposure.

## Screenshots

- Add screenshots for bucket creation, website hosting settings, bucket policy, and the final website endpoint.

## What I Learned

- S3 can host simple static sites without managing servers.
- Public access in S3 depends on both account-level protections and bucket-level configuration.
- Bucket policies control resource access and must be written carefully.
- The website endpoint is separate from direct object URLs and is tied to the bucket hosting configuration.

## Exam Relevance

This lab aligns with the Cloud Technology and Services domain and touches Security and Compliance. It reinforces object storage, S3 website hosting, and basic public access control concepts.


<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)

**Author:** Jonathon Davila  
**Email:** davila.jonathon83@gmail.com

---

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to create a S3 to store pictures and files on my webage. I'm doing this project to learn the many portions of AWS and further my learning in the cloud.

### Tools and concepts

Services I used were S3, using ACL, and JSON code. Key concepts I learnt include how to create a bucket, how to add html files to the bucket,  how to make said bucket public, and how to deny access to modyfing the files using JSON 

### Time, challenges, and wins

This project took me approximately 30 minutes. The most challenging part was understanding the JSON code. It was most rewarding to see the webpage display after making it public. 

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will get into my AWS account and navigate to Amzone S3 and begin the process of creating a storage for my files. 

### How long it took to create the bucket

Creating an S3 bucket took me a matter of minutes. 

### Region selection

The Region I picked for my S3 bucket was United States Ohio because it was the closet to my time zone listed. 

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means whatever name you create is unique to all others and connot be replicated. 

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_ba6d42ad)

## Upload Website Files to S3

### What I did in this step

In this step, I will begin to add files, including HTML and zip files.

### Files I uploaded

I uploaded two files to my S3 bucket: an HTML file and a zip folder containing image assets for the website.

### How the files work together

Both files are necessary for this project as they work in tandem to create a functional website. The HTML file acts as the structural blueprint that defines the layout and content, while the image files provide the visual assets required to complete the design. Without both components, the website would be incomplete, lacking either its primary structure or its visual elements.

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_a265af88)

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure static website hosting, which will enable my website to become publicly accessible.

### Understanding website hosting

Website hosting refers to the process of storing website files—such as HTML documents and media assets—on a web server, thereby making them accessible to users via the internet. By configuring an S3 bucket for static website hosting, we are essentially generating a unique URL that enables the public to access and view the hosted content.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I navigated to the Properties tab, scrolled down to the Static website hosting panel, and selected Edit. From there, I enabled Static website hosting, chose Host a static website, set the index document as index.html, and saved the changes.

### Access Control Lists (ACLs)

An ACL is a set of rules that determine what access to resources someone has. I enabled it for the sake of this project. 

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_c22c54c0)

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website hosting is enabled, S3 generates a bucket website endpoint URL, which acts as a public link allowing anyone to access the HTML and image files stored in my bucket.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I was give a 403 error. The reason for this error was my HTML is still set as private. 

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_22ce4daf)

## Success!

### What I did in this step

In this step, I will make my HTML and files public that way, one I wont receive an error, and two the public will also be able to see my files

### How I resolved the 403 error

To resolve this 403 Forbidden error, I selected both the HTML and the files, selected actions, and then make public using ACL. 

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Bucket Policies

### What I did in this extension

In this project extension I'm about to restrict users from modyfing. I'm doing this so that they wont be able to delete any of my index html file. 

### Understanding bucket policies

Bucket policies, which are written in JSON code, provide a more granular level of control compared to ACLs. While ACLs are useful for granting basic permissions at the object level, bucket policies allow for more complex access management, including the ability to restrict specific actions such as deleting or modifying files across the entire bucket.

![Image](https://nextwork.ai/hopeful_purple_peaceful_turkey/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_sm2sm2sm)

### What my bucket policy does

I successfully tested the bucket policy by attempting to delete the index.html file through the Objects tab. As expected, the operation failed with an "Access Denied" error, confirming that the policy is correctly restricting deletion permissions.

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)*

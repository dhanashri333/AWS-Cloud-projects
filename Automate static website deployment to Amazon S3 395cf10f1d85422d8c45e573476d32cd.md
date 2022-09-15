# Automate static website deployment to Amazon S3

## **Summary**

This pattern describes the steps required to add a continuous integration and continuous delivery (CI/CD) pipeline to an existing bucket in Amazon Simple Storage Service (Amazon S3) on the Amazon Web Services (AWS) Cloud. This pattern uses GitHub as a source provider. The pipeline is initiated when new items are committed, and the changes are then reflected in the S3 bucket.

## **Prerequisites and limitations**

**Prerequisites**

- An active AWS account
- Knowledge of Amazon S3 and AWS CodePipeline
- A static website, including output/source files such as HTML 4/5, CSS 2/4, images, fonts, and icons
- A GitHub repository

**Limitations**

- This process is recommended for displaying read-only content. It isn't recommended for collecting or transferring sensitive information, because Amazon S3 uses the HTTP protocol.
- Websites built using PHP, JSP, or APS.NET are not supported, because Amazon S3 doesn't support server-side scripts.

## **Architecture**

**Source architecture**

![Untitled](Automate%20static%20website%20deployment%20to%20Amazon%20S3%20395cf10f1d85422d8c45e573476d32cd/Untitled.png)

**Target technology stack**

- AWS CodePipeline
- AWS CodeStar
- Amazon S3
- Any web server

**Target architecture**

![Untitled](Automate%20static%20website%20deployment%20to%20Amazon%20S3%20395cf10f1d85422d8c45e573476d32cd/Untitled%201.png)

## **Tools**

**Tools**

- [AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html) – A continuous delivery service you can use to model, visualize, and automate the steps required to release your software. You can quickly model and configure the different stages of a software release process. CodePipeline automates the steps required to release your software changes continuously.
- [AWS CodeStar](https://docs.aws.amazon.com/codestar/latest/userguide/welcome.html) – AWS CodeStar is a cloud-based service for creating, managing, and working with software development projects on AWS.
- [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html) – A highly scalable object storage service. It can be used for a wide range of storage solutions, including websites, mobile applications, backups, and data lakes.

## **Epics**

## Create an Amazon S3 bucket and upload content

[Untitled](https://www.notion.so/a9ad80bc955147deb3d5fb8ab3176ce7)

## Configure the S3 bucket for website hosting

[Untitled](https://www.notion.so/e675c91ef7b44587873629e5b69637df)

## Create a bucket policy

[Untitled](https://www.notion.so/19fa229f4f164d67b694f822d778e5b6)

## Create a pipeline

[Untitled](https://www.notion.so/8dcd5c2dd08b4fe6bca12e6a6e6d8d66)
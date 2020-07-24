# alfresco-s3-adapter
Alfresco AMP Module for S3 Backed Storage

 * Migrated from the `alfresco-cloud-store` project at https://code.google.com/p/alfresco-cloud-store/
 * Updated to use the latest AWS S3 SDK, and the latest Alfresco 5.0.x API
 * This should not be considered "production ready" it has not been battle tested
 * Pull Requests / Issues / Contributions are welcomed!
 
Build Instructions

 * After cloning the project, run `mvn clean install` to download dependencies and build the project

Installation / Configuration

 * After installing the `alfresco-s3.amp` package you will need to add some properties to your `alfresco-global.properties` file:
 
```
# Your AWS credentials
# Alternatively these can be set in the standard locations the AWS SDK will search for them
# For example: if you are running on an EC2 instance and are using IAM roles, you can leave these blank and the credentials
# for the role will be used.
aws.accessKey=
aws.secretKey=

# The AWS Region (US-EAST-1) will be used by default if not specified
aws.regionName=us-east-1

# The S3 bucket name to use as the content store
aws.s3.bucketName=

# The location on local storage to be used as the cache
dir.cachedcontent=/temp/cachedcontent

# The relative path (S3 KEY) within the bucket to use as the content store (useful if the bucket is not dedicated to alfresco content)
dir.contentstore=/alfresco/contentstore

# The relative path (S3 KEY) within the bucket to use as the deleted content store
dir.contentstore.deleted=/alfresco/contentstore.deleted
```
 
 

## Quick Backgrounnd:

AWS is a cloud provider offering a broad variety of services (175+) in different areas, for example: Networking, Compute, Analytics, Databases, Storage etc

AWS is an API based provider which means each service has its own API, which you can be invoked in order to perform some action or to retrieve some data, like create a virtual machine, take a snapshot of the EBS volume, upload or retrieve an object from S3 or an item from DynamoDB. 

To manage access permissions to the AWS services, it uses Identity and Access Management service (In short called as AWS)

### Basics of IAM:

It is responsible for two basic operations:
1. Authentication — are you the one you claim to be?
2. Authorization — are you allowed to do what you want to do?

### Concepts within IAM:

1. Users:  A user is a unique identity recognized by AWS services and applications. Similar to a login user in an operating system like Windows or UNIX.
    * A user has a unique name and can identify itself using familiar security credentials such as a password or access key. 
    * A user can be an individual, system, or application requiring access to AWS services. 

2. Groups: A group is a collection of IAM users. 
    * A user can belong to multiple groups.
    * Groups cannot belong to other groups.
    * Groups can be granted permissions using access control policies. This makes it easier to manage permissions for a collection of users, rather than having to manage permissions for each individual user. 
        > Groups do not have security credentials, and cannot access web services directly; they exist solely to make it easier to manage user permissions. 



3. Roles: An IAM role defines a set of permissions for making AWS service requests. 
    * IAM roles are not associated with a specific user or group. Instead, trusted entities assume roles, such as IAM users, applications, or AWS services such as EC2.
    * IAM roles allow to delegate access with defined permissions to trusted entities without having to share long-term access keys. 
    * IAM Role are used to delegate access to IAM users managed within the same account, to IAM users under a different AWS account, or to an AWS service - Example: EC2

#### When should I use an IAM user, IAM group, or IAM role?

   * An IAM user has permanent long-term credentials and is used to directly interact with AWS services. 
   * An IAM group is primarily a management convenience to manage the same set of permissions for a set of IAM users. 
   * An IAM role is an AWS Identity and Access Management (IAM) entity with permissions to make AWS service requests. IAM roles cannot make direct requests to AWS services; they are meant to be assumed by authorized entities, such as IAM users, applications, or AWS services such as EC2. Use IAM roles to delegate access within or between AWS accounts.


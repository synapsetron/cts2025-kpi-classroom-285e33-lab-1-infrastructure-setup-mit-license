1. **Set-up account.** Register in a cloud provider. Now you have a root account. **(1 point)**  
   Now perform one of the following (you need to select only one action):  
   a. Create an IaM user and attach FullAdmin policy. Use it for all future interactions with the system. **(1 point)**  
   b. Create an IaM Identity center account (or analog for your cloud provider). Also make it full admin. **(2 points)**  

2. *(Optional)* Create an Organisation  
   [docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html)  
   and user for it. All next labs are to be performed within it. **(2 points)**  

3. Create one more user. Create an IaM policy that allows **ONLY** to view resources (no write access). **(1 point)**  

4. Create a Role that has this policy attached and can be assumed by user from p3. **(1 point)**  

5. *(Optional)* Create a CloudFormation (or Terraform, OpenTofu, whatever) template describing your policy and role. **(1 point)**  

6. Create a network (VPC for your resources). There should be private and public subnets.  
   Public one has IGW, private ones are for internal access only. **(3 points)**  

7. *(Optional)* Create IaC stack holding your network resources. **(2 points)**  

8. Calculate monthly budget for lab 2, assuming there will be only 2 shards. **(2 points)**

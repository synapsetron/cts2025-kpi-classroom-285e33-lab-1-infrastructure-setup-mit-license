1. **Set-up account.** Register in a cloud provider. Now you have a root account. **(1 point)**  
   Now perform one of the following (you need to select only one action):  
   a. Create an IaM user and attach FullAdmin policy. Use it for all future interactions with the system. **(1 point)**

   We can the the result of creation on IAM User at the screenshots below
   ![UserCreation1.1](PNG/CreatedUser1.1.png)

   And more detailed information of  user here:
   ![UserCreation1.2](PNG/CreatedUser1.2.png)
---
2. *(Optional)* Create an Organisation  
   [docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html)  
   and user for it. All next labs are to be performed within it. **(2 points)**  
---
3. Create one more user. Create an IaM policy that allows **ONLY** to view resources (no write access). **(1 point)**
   Now lets create the second user, that will only have an access to view resources. On the screenshot below, we can see the result of creation the second user
    ![UserCreation2.1](PNG/CreatedUser2.1.png)
   And more detailed information:
   ![UserCreation2.2](PNG/CreatedUser2.2.png)
---
4. Create a Role that has this policy attached and can be assumed by user from p3. **(1 point)**  
 Created Readonly Role with attached policy on the screenshot below:
   ![ReadonlyRole](PNG/ReadonlyRole.png)

   After that , lets crate a policy for  User for assuming this role:
   ![Policy](PNG/Policy.png)

   Login via IAM Readonly User:
   ![LoginReadonlyUser](PNG/LoginReadonlyUser.png)

   As we can see, initially we have no access to anything:
   ![ReadonlyUserDontHavePermission](PNG/ReadonlyUserDontHavePermission.png)

   Click the change role button in the right corner menu and enter the data about the role you want to use.
   ![SwitchRole](PNG/SwitchRoleButton.png)

   After that get the role and get ReadOnlyAccess:
   ![ResultOfAssumingTheRole](PNG/ResultOfAssumingTheRole.png)

   As you can see, now we have a readonly access and see the statistics and etc. Also at the top you can see the role that was granted to the user.
   
   ![VisibilityOfTheRole](PNG/VisibilityOfTheRole.png)
---
5. *(Optional)* Create a CloudFormation (or Terraform, OpenTofu, whatever) template describing your policy and role. **(1 point)**
   Lets create a .yaml cloudformation code to describe our policies and etc manually:
   ![CloudformationCodeExample](PNG/CloudformationCodeExample.png)

   Create a stack and upload this yaml file:
   ![CreatingOfTheStack](PNG/CreatingOfTheStack.png)

   Created stack:
   ![StackCreated](PNG/StackCreated.png)

   Stack assume policies and roles:
   ![StackCreatedRoleAndAssumePolicies](PNG/StackCreatedRoleAndAssumePolicies.png)
---
6. Create a network (VPC for your resources). There should be private and public subnets.  
   Public one has IGW, private ones are for internal access only. **(3 points)** 

   We can see created VPC in the screenshot below:
   ![CreatedVPC](PNG/CreatedVPC.png)

   Lets create public and private subnets:
   ![PublicSubnet](PNG/PublicSubnet.png)
   
   ![PrivateSubnet](PNG/PrivateSubnet.png)

   Create internet gateway:
    ![CreatedInternetGateway](PNG/CreatedInternetGateway.png)

   Create public route table and connect it to IG. Also create private RouteTable:
    ![publicRouteTable](PNG/publicRouteTable.png)
    ![privateRouteTable](PNG/privateRouteTable.png)
  
   
---
7. *(Optional)* Create IaC stack holding your network resources. **(2 points)**

   Lets create IaC stack to hold my network resourses. Firstly, scan resourses:
   ![IACGenerator](PNG/IACGenerator.png)

   Now, add scaned resources that we want to see in the template:
   ![IACResoursesCompleted](PNG/IACResoursesCompleted.png)
   ![IACaddScaned1](PNG/IACaddScaned1.png)
   ![IACaddScaned2](PNG/IACaddScaned2.png)

   After that we can see created IaC template:
   ![IACTemplateGenerated](PNG/IACTemplateGenerated.png)

   Here we can see it in code:
   
   ![IACcodeTemplate.png](PNG/IACcodeTemplate.png)
---
8. Calculate monthly budget for lab 2, assuming there will be only 2 shards. **(2 points)**
---

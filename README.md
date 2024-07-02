# RBAC-Microsoft-Labs

I pulled thess lab exercises from Microsoft Learning and completed them in a Windows 11 pro VM I set up. This lab exercise is intended to illustrate my ability to navigate and utilize Azure and Active Directory functionality.

https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/Instructions/Labs/LAB_01_RBAC.html#instructions


# Excercise 1 - Creating groups and users in Azure portal:

The first step was accessing the Azure Portal and creating a domain for my Active Directory. I then accessed Microsoft Entra ID and granted myself global admin permissions so I could create groups and users for this exercise.

![AD1](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/60835410-6219-45ae-986d-eba44ff6ff4d)


Then I navigated over to create our first user, Joseph Price. Joseph will be our Senior Administrator for this exercise.

![ad2](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/bb0bac21-d22a-448b-938f-2e7c9f1da496)
![ad3](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/bae0e498-7119-4035-8f7e-77a320a6c9f4)
![ad4](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/f24a4709-990e-4711-8de8-6a3a4bb9db7d)


With Joseph's account created, we can now create the group he belongs to and assign him to it. We will name this group "Senior Admins" and give the group typing security with an assigned membership.

![group1](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/07ef18c7-aa7e-472b-8e48-c0318d665fa7)
![group2](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/b030529f-371c-4ca4-bc03-abb0c7caaf64)
![group3](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/d979ac22-c68a-4897-980e-f37d4ab9b79b)


# Exercise 2 - Creating groups and users using powershell within Azure portal:

For this leg of the exercise, we shift away from using Microsoft Entra's GUI and use powershell within the Azure portal instead. We will create a user named Isabel Garcia and create/assign her to the Junior Admins group.

The first step will be accessing powershell within the Azure portal and mounting or storage account. For this exercise we will be using the default free options.

![cloudps1](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/34719f32-c3b1-45d2-bc23-165ee668c8dc)

After our powershell is assigned to us we will start the process of defining password requirments for our new users with a PasswordProfile. We will make it so upon next login Isabel must change her password from the default we have provided.

![cloudps3](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/1299de23-284f-44d7-b3e5-3d62a437d1f5)
![cloudps4](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/3f8d1a45-1048-4bc9-8fb6-77238a0c43eb)

We will then connect to Microsoft Graph with the defined permissions needed to create users.

![cloudps5](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/c5c661a6-969a-4c23-a9b9-a043e42b6fda)

Then we will define and enable Isabel's account.

![cloudps6](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/1ae335fc-3a3f-4136-957b-f9b5eb9f5432)
![cloudps7](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/78e10643-30a5-44d2-b141-a87729a49a3b)

After we have confirmed that her account has been created we can assign her to her group, "Junior Admins."

![cloudps8](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/d86bc3e2-015e-487f-924a-1d4496a87533)
![cloudps9](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/808a21f9-96cb-4bd4-b15c-dfe8d7346c12)


# Exercise 3 - Creating groups and users using Bash within Azure portal:

We will continue creating users and groups, this time utilizing Bash instead of Powershell. We start by running the following command to identify the name of my Microsoft Entra tenant.

![bash1](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/d9b0a719-b9ad-4a4c-9ffc-4bcf2446c7e6)

Then we will create the username and password for our next employee, Dylan Williams. Then we will confirm he is amongst our other employees.

![bash2](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/75ddaa41-25d3-42b9-9084-1d81cc6e25a9)
![bash3](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/90192c3f-fc1f-488a-a351-d000bb7ebc05)

Then we will create a group for Dylan's department, which will be the "Service Desk." We will then list the users/groups to verify.

![bash4](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/9724f943-051a-4797-8cd0-0636e44dbd5b)
![bash5](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/766f34af-1597-48a1-8ff8-8e7287f524e5)
![bash6](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/231b90ce-326c-4702-acc5-bbab215b1df8)


# Exercise 4 - Assign Dylan Williams the role of Virtual Machine Contributor:

In this final exercise we are going to take our employee Dylan Williams from the previous exercise and grant it the role of Virtual Machine Contributor.

We start by navigating over to the resource groups page within the Azure portal and create a resource group.

![vmc1](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/448efb78-6877-4b2c-bfe0-ea9ae738a978)
![vmc2](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/cdd1068e-3087-47c3-bb39-8eaab13b6b2c)

Then from withing the new resource group, we will add the role. In this case, we are looking for the "Virtual Machine Contributor."

![vmc3](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/d795eaf1-9478-44d1-b079-6d914bc51d2a)

Then we will select Dylan Williams for the members assigned this role.

![vmc4](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/30ca1b64-fc62-4c86-b827-e406dc201e6b)

# Upon Completion:

Upon completing this set of four exercises we will go back into Powershell within the Azure portal and run a command to free up any resources we tied up.

![clean up resources](https://github.com/BaylieSmith/RBAC-Microsoft-Labs/assets/174283518/f0670c25-e560-4a14-b61c-83a1d8bbfe08)

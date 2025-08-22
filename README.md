# AWS IAM Project Documentation

This README documents a hands-on AWS Identity and Access Management (IAM) project.  
The project demonstrates **secure access management** for a developer (**John**) and a data analyst (**Mary**) by setting up IAM users, custom policies, and Multi-Factor Authentication (MFA) — all following the **principle of least privilege**.

---

## Project Overview

In this project, you will:

1. Log in to the AWS root account.
  ![sreenshot](images/rwadash.png)
![sreenshot](images/policy.png)
3. Create custom IAM policies:
     - **EC2 access** for developers
   ![sreenshot](images/creatpol.png)
    ![sreenshot](images/cratp.png)
    ![sreenshot](images/choosec2.png)
    ![sreenshot](images/all.png)
    ![sreenshot](images/allnext.png)
    ![sreenshot](images/developers.png)
    ![sreenshot](images/polcreated.png)
    ![sreenshot](images/developed.png)
  - **S3 access** for analysts
   -  ![sreenshot](images/creatpol.png)
    ![sreenshot](images/cratp.png)
    ![sreenshot](images/s3.png)
    ![sreenshot](images/data.png)
    ![sreenshot](images/specifics.png)
    ![sreenshot](images/analystdet.png)
    ![sreenshot](images/analyscreat.png)
    ![sreenshot](images/analy.png)
    

##Create custom user group: for Development-Team
![sreenshot](images/ug.png)
![sreenshot](images/ugdev.png)
![sreenshot](images/devug.png)

##Create custom user group: for Data-Team
![sreenshot](images/ug.png)
![sreenshot](images/datateam.png)
![sreenshot](images/datacreatt.png)



  
## Create IAM users:
   - John (**Developer**) 
   ![sreenshot](images/iam.png)
   ![sreenshot](images/ami.png)  
    ![sreenshot](images/john.png)
   ![sreenshot](images/johnn.png)  
    ![sreenshot](images/johnn2.png)
   ![sreenshot](images/oer.png) 
    ![sreenshot](images/review.png)
   ![sreenshot](images/viewuse.png)  
 
 
 - Mary (**Analyst**)
 -   ![sreenshot](images/iam.png)
   ![sreenshot](images/ami.png)  
    ![sreenshot](images/mary.png)
   ![sreenshot](images/mare.png)
   ![sreenshot](images/nare.png)
   ![sreenshot](images/passwrd.png)
   ![sreenshot](images/maryt.png)
   ![sreenshot](images/iamlogin.png)
##Assign policies to users.
   ![sreenshot](images/.png)
   ![sreenshot](images/.png)
![sreenshot](images/.png)

8. Validate permissions for each user.
   ##User John
   ![sreenshot](images/johhnsignin.png)
   ![sreenshot](images/changepd.png)
   ![sreenshot](images/changepd.png)
   ![sreenshot](images/psswdchanged.png)
   ![sreenshot](images/johnresult.png)
   ![sreenshot](images/johnec.png)
   ![sreenshot](images/lau.png)
   ![sreenshot](images/johnapp.png)
   ![sreenshot](images/johnkey.png)
   ![sreenshot](images/launjh.png)
   ![sreenshot](images/ps.png)
   ![sreenshot](images/stopw.png)
   ![sreenshot](images/johnstop.png)

   ##For Mary
    ![sreenshot](images/maryprompt.png)
   ![sreenshot](images/marypwd.png)
   ![sreenshot](images/marylimit.png)
   ![sreenshot](images/marys3.png)
   ![sreenshot](images/maryac.png)
   ![sreenshot](images/bucmar.png)
   ![sreenshot](images/sawmary.png)
   ![sreenshot](images/bucname.png)
   ![sreenshot](images/marybucn.png)
   ![sreenshot](images/sedel.png)
   ![sreenshot](images/dels3.png)
   ![sreenshot](images/successfullydel.png)
   
10. Enable MFA for both users.
  ##For John
   ![sreenshot](images/mmfa.png)
      ![sreenshot](images/allowmfa.png)
   ![sreenshot](images/authjohn.png)
   ![sreenshot](images/authsec.png)
    
      ![sreenshot](images/hhhhpng)
   ![sreenshot](images/mfasc.png)
  ##For Mary
    ![sreenshot](images/maryconl.png)
   ![sreenshot](images/mary-mfa.png)
  ![sreenshot](images/marrry.png)
   ![sreenshot](images/marrysucc.png)

---


### Principle of Least Privilege
- **Grant only what is needed.**  
- Reduces risk and improves security.

---

## Scenario Summary

| User   | Role         | Permissions      | MFA Enabled | Group         |
|--------|--------------|------------------|-------------|--------------|
| John   | Developer    | EC2 (custom)     | ✅          | Developers   |
| Mary   | Data Analyst | S3 (custom)      | ✅          | Analysts     |

Both users **only** have the access they need for their job functions.

---

1. Role and Purpose of IAM in AWS:
IAM (Identity and Access Management) in AWS is used to securely control access to AWS resources. It allows you to create users, groups, and policies for managing permissions. IAM helps organizations enforce security by ensuring only authorized users can access specific cloud resources—making cloud management both safe and efficient.

2. Difference Between IAM Users and Groups:

IAM Users: Individual identities (like a developer or analyst) with their own credentials and permissions.
Example: Create a user for John so he can log in and manage EC2 instances.
IAM Groups: Collections of users with shared permissions, making access management easier for teams.
Example: Place all developers in a “Developers” group and attach the EC2 policy—everyone in the group gets the same access.
3. Creating IAM Policies:
To create a custom IAM policy:

Identify the role (e.g., developer needs EC2 access).
Select the necessary permissions (actions on EC2, like “StartInstances”).
Write the policy (usually in JSON format).
Attach the policy to the appropriate user or group.
This ensures each user or group gets only the permissions they need.
4. Principle of Least Privilege:
The principle of least privilege means giving users only the minimum permissions required to perform their tasks. In AWS IAM, it’s vital for security—limiting user access reduces the risk of accidental changes or security breaches.

5. John and Mary Scenario:

John (Developer): Created as an IAM user, added to the “Developers” group, and given a custom EC2 policy—he can only access EC2, not S3 or other services.
Mary (Data Analyst): Created as an IAM user, added to the “Analysts” group, and given a custom S3 policy—she can access S3 but not EC2.
Both users have MFA enabled. These configurations match their job roles and follow least privilege—each has access only to what’s needed for their work.
---

## Need Help?

Open an [issue](https://github.com/Dowlib1/Zappy-e-Bank/issues) or contact the repo owner for questions.

---

**Happy Securing on AWS!** 🚀🔐

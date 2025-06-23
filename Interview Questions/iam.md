# AWS Identity and Access Management (IAM) - Overview & FAQ

AWS IAM enables secure access control to AWS services and resources. It allows you to define who can access what under what conditions, providing fine-grained permissions management for your AWS environment.

---

## 🔐 1. What is AWS IAM?
AWS IAM is a service that lets you manage **users**, **groups**, **roles**, and **permissions** for accessing AWS resources. It centralizes control over authentication and authorization.

---

## 📦 2. Key Components of AWS IAM
- **Users**
- **Groups**
- **Roles**
- **Policies**
- **Permissions**
- **Identity Providers (IdPs)**

---

## ⚙️ 3. How Does AWS IAM Work?
You:
- Create IAM **users** and **groups**
- Attach **policies** that define permissions
- Use **roles** to delegate temporary access to AWS services or other users

---

## ✅ 4. Authentication vs Authorization
- **Authentication**: Verifying who the user or system is
- **Authorization**: Determining what actions they are allowed to perform

---

## 🛡️ 5. How to Secure Your AWS Account Using IAM
- Enforce **least privilege**
- Set **strong password policies**
- Enable **MFA (Multi-Factor Authentication)**
- Regularly audit **IAM permissions and access logs**

---

## 👤 6. IAM Users vs IAM Roles
- **IAM Users**: Permanent credentials, used by individuals or applications
- **IAM Roles**: Temporary credentials, assumed by trusted entities (users, services)

---

## 📄 7. What is an IAM Policy?
A **JSON document** that defines what **actions** are allowed/denied on which **resources** for which **principals** (users, groups, roles).

---

## 🖥️ 8. What is the AWS Management Console?
A **web-based GUI** for managing AWS resources. IAM users with sufficient permissions can use it to perform operations.

---

## 🔑 9. How Does IAM Manage Access Keys?
IAM users can be assigned:
- **Access Key ID**
- **Secret Access Key**
These are used for programmatic access via AWS CLI or SDKs.

---

## 👥 10. Purpose of IAM Groups
IAM groups are used to:
- Organize users
- Assign **common permissions** via policies
This simplifies permission management.

---

## 📜 11. IAM Policy Document Role
Defines what **actions**, **resources**, and **conditions** apply to an identity or service. Written in **JSON format**.

---

## ➕ 12. Granting Permissions to IAM Users
You can:
- Attach policies **directly** to the user
- Add user to a **group** that has policies attached

---

## 🔄 13. Delegating Permissions via IAM Roles
IAM roles allow **EC2 instances, Lambda functions**, or other entities to access resources without long-term credentials.

---

## 🔁 14. What is Cross-Account Access?
It allows one AWS account to grant access to users, roles, or services from another account via **IAM roles and trust policies**.

---

## 🌐 15. What is Identity Federation?
Enables users from external identity systems (e.g., **Active Directory**, **Google**, **SAML**) to access AWS using **temporary credentials**.

---

## 📊 16. IAM Access Advisor
Helps analyze:
- Which **services** a user accessed
- What **permissions** are unused
Supports access auditing and cleanup.

---

## 🛡️ 17. Principle of Least Privilege
IAM encourages giving users and roles **only the permissions they need**—nothing more.

---

## ⚖️ 18. IAM Policies vs Resource-Based Policies
- **IAM Policies**: Attached to users, groups, or roles
- **Resource-Based Policies**: Attached directly to AWS resources (e.g., S3 bucket policy)

---

## 🔐 19. Implementing MFA in IAM
Enable MFA for IAM users via:
- **Virtual MFA devices** (e.g., Google Authenticator)
- **Hardware MFA tokens**
Provides extra security beyond just passwords.

---

## 🧠 20. IAM Policy Evaluation Logic
IAM uses an **explicit deny model**:
- If a policy explicitly **denies** an action, it overrides any **allow**
- If no policy allows an action, it is implicitly denied

---

## 📚 Summary
AWS IAM is foundational for securing access to AWS resources. By combining users, groups, roles, and policies with best practices like MFA and least privilege, you can build a secure and compliant AWS environment.

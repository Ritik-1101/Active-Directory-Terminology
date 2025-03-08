# **Active Directory Terminology**

## **1. Overview of Active Directory**
Active Directory (AD) is Microsoft's centralized directory service for Windows networks. It acts as a backbone for authentication, authorization, and management of users, devices, and resources within an enterprise environment.

## **2. Core Components of Active Directory**

### **a. Domain**
A domain is a logical boundary that organizes users, computers, and resources under a single administrative umbrella. Security policies and authentication mechanisms apply consistently across all objects in a domain.

### **b. Forest**
A forest is the highest level of the Active Directory hierarchy. It consists of one or more domains that share a common schema and global catalog, enabling seamless communication and trust relationships.

### **c. Tree**
A tree is a collection of domains arranged hierarchically. Each domain within a tree shares a contiguous namespace and a trust relationship with other domains in the tree.

### **d. Organizational Unit (OU)**
An OU is a container used to structure objects within a domain for better management and policy enforcement. OUs allow administrators to apply group policies and delegate control efficiently.

### **e. Site**
A site represents a physical location in a network, optimizing authentication and replication traffic to improve performance across geographical locations.

## **3. Active Directory Database and Storage**

### **a. NTDS.DIT**
The heart of Active Directory. The NTDS.DIT file is the database that stores all directory objects, attributes, and security policies.

### **b. Schema**
The schema defines object types and their attributes within Active Directory. It ensures consistency and standardization across the directory.

### **c. Global Catalog**
The Global Catalog (GC) is a distributed database that stores partial replicas of directory objects. It enables efficient searching across an entire forest while reducing query latency.

## **4. Authentication and Authorization**

### **a. Kerberos Authentication**
Active Directory relies on the Kerberos protocol for secure, ticket-based authentication. It eliminates the need for repeated password transmissions, making authentication more secure.

### **b. Lightweight Directory Access Protocol (LDAP)**
LDAP is a protocol used to query, modify, and interact with directory services. It provides a flexible way to access and manage Active Directory data.

### **c. Security Groups**
Security groups help streamline access control by assigning permissions collectively rather than on an individual user basis.

## **5. Domain Controllers and Replication**

### **a. Domain Controller (DC)**
A domain controller is a server that manages authentication, enforces policies, and synchronizes directory data.

### **b. Read-Only Domain Controller (RODC)**
An RODC is a domain controller that provides read-only access to the Active Directory database. It is ideal for branch offices where security risks are higher.

### **c. Flexible Single Master Operations (FSMO) Roles**
FSMO roles are specialized domain controller tasks that ensure consistency across the directory:
- **Schema Master** – Manages the AD schema.
- **Domain Naming Master** – Controls domain additions and removals.
- **RID Master** – Allocates unique security identifiers (SIDs).
- **PDC Emulator** – Handles time synchronization, password changes, and legacy authentication.
- **Infrastructure Master** – Maintains references between domains.

### **d. Replication**
Active Directory replication ensures directory data is synchronized across all domain controllers. Proper replication prevents authentication failures and data inconsistencies.

## **6. Group Policy and Management**

### **a. Group Policy Objects (GPOs)**
GPOs define security and administrative settings that apply to users and computers. They enforce policies such as password complexity, software restrictions, and login scripts.

### **b. Active Directory Users and Computers (ADUC)**
ADUC is a management console used to create, manage, and organize users, groups, and devices in a domain.

## **7. Trusts and Federation**

### **a. Trust Relationships**
Trusts enable authentication between different domains or forests. Common types include:
- **Parent-Child Trust** – Automatically established between parent and child domains.
- **Tree-Root Trust** – Links different domain trees within a forest.
- **External Trust** – Connects AD domains to non-AD environments.
- **Forest Trust** – Establishes trust between separate forests.
- **Shortcut Trust** – Reduces authentication latency between domains.

### **b. Active Directory Federation Services (AD FS)**
AD FS enables Single Sign-On (SSO) across organizations and cloud applications, enhancing security while improving user experience.

## **8. Active Directory Services**

### **a. Active Directory Domain Services (AD DS)**
AD DS is the core directory service, handling authentication, authorization, and object management.

### **b. Active Directory Certificate Services (AD CS)**
AD CS issues and manages digital certificates, supporting encryption, secure authentication, and email security.

### **c. Active Directory Lightweight Directory Services (AD LDS)**
AD LDS provides directory services without requiring full domain integration, making it suitable for applications needing directory capabilities.

### **d. Active Directory Rights Management Services (AD RMS)**
AD RMS helps secure sensitive data through encryption, access control, and policy enforcement.

## **9. Security and Best Practices**

### **a. Role-Based Access Control (RBAC)**
RBAC enforces the principle of least privilege by assigning permissions based on user roles rather than individual assignments.

### **b. Auditing and Monitoring**
Regular auditing and monitoring of Active Directory events help detect anomalies, unauthorized changes, and potential security breaches.

### **c. Backup and Recovery**
Routine backups of Active Directory are essential for disaster recovery. A well-defined recovery plan ensures business continuity in case of corruption or compromise.

## **10. Conclusion**
Active Directory is a fundamental part of enterprise IT infrastructure. It centralizes identity and access management, streamlines operations, and enhances security. A strong understanding of its architecture, security mechanisms, and best practices is crucial for cybersecurity professionals.

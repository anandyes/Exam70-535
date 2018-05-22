## Designing Security and Identity

Key Security areas
* Identity and Access (Identity for users and resources)
* Network security (secure access, isolation and publishing)
* Data Protection (Encryption of data at rest and in transit) 
* Protecting Secrets (Keys, Certificates, credentials)
* System Integrity (Patched, Protected)
* Insight (auditing, system state, Health)

Azure AD(AD) and On-Prem Windows Server Active Directory (WSAD)
Azure AD does not support Windows Authentication, Group Policies as supported by Windows Server AD.

Authentication Options for AAD
* Identity sync with Password hash.
* Identity sync with ADFS
* Identity sync with Pass-through authentication agent

### Azure AD Domain Services:
Azure AD Domain Services provides managed domain services such as domain join, group policy, LDAP, Kerberos/NTLM authentication that are fully compatible with Windows Server Active Directory. 

Azure ADDS Managed domain features:
* The managed domain is stand-alone domain and not an extension of on-premisis domain
* The domain controllers in managed domain does not need to be managed, patched, or monitored
* No need to manage AD replication to managed domain. All User accounts, group memberships and credentials are automatically available with managed domain. The synchronization from on-prem to Azure AD is done using AD Connect.
* The Domain administrator or Enterprise administrator privileges are not avaialble in managed domain.

MFA is available in AD premium, but can also be obtained by pay per use basis

### Azure Key Vault
* On-Prem solution is HSM (Hardware Security Module)
* HSM protected and Software protected
* Azure Key Vault can store Secrets, Keys and Certificates(x509 compliant)
* Authentication is via Azure AD OAuth2 token
* Authorization is via Access Control List (ACL) on the key vault
* Roles include - Key Vault Owner, Key/Secret Owner, App Operator, Auditor

### Network Security
* OS - Patched, Anti-virus, Managed Policy, Managed Firewall
* Virtual Subnet - RBAC, NSG, Virtual Appliance
* Virtual Network - RBAC, NSG, App Gateway, S2S VPN / Express Routes, Forced Tunneling
* Virtual Network is tied to a Region and in turn to a Subscription
* Virtual Appliances- A VM with preconfigured software such as Firewalls, load balancers
* Azure Application Gateway - A layer 7 reverse proxy, SSL termination
* Web Application Firewall - Optional to App Gateway, Implements CRS3.O

### Azure Resource Manager
* Resource, Resource Groups, Subscription
* Reosource Group is not an access boundary.

### Role Based Access Control
* RBAC enables assignment of roles at various levels: Subscription, Resource Group, Individual resource.
* Assigned rights are inherited by chlid objects

Three basic roles:
* **Owner** has full access to all resources including the right to delegate access to others.
* **Contributor** can create and manage all types of Azure resources but can’t grant access to others.
* **Reader** can view existing Azure resources.

[Built-in Roles](https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)

### Azure AD P2 features

* Previliged Identity Management - Just in time privilege elevation
* Identity Protection

Azure Security Center gives overview of overall security

[B2B users access on-prem application](https://docs.microsoft.com/en-us/azure/active-directory/b2b/hybrid-cloud-to-on-premises)
![Authorization via a B2B user object in the on-premises directory](https://docs.microsoft.com/en-us/azure/active-directory/b2b/media/hybrid-cloud-to-on-premises/mimscriptsolution.png)
## Azure Active Directory [^](https://azure.microsoft.com/documentation/articles/active-directory-whatis/)

* Azure AD is a directory service in Azure
* Azure AD Service is not a replacement for Windows Server Active Directory
* **Azure AD Connect** synchronization services used to synch on-prem AD groups and users to Azure AD, which is called **Hybrid Identity**
* AD Connect is successor to DirSync, AzureADSync, Forefront Identity Manager.
* Azure AD can be associated with an on-premises Active Directory to support single sign-on (SSO).
* True SSO using Active Directory Federation Services (AD FS) or shared sign-on, in which Azure AD Connect is used to sync a password hash between Active Directory and Azure AD
* Azure AD is accessible via a modern REST API, Graph REST APIs.

Azure AD serves as key component for identity management in MS cloud and has the following capabilities:
* Multi-Factor Authentication,
* Device registration,
* Role Based Access Control (RBAC),
* Application usage monitoring,
* Security Monitoring and Alerting,
* Self-serivce password management

Important Azure AD features:
* Azure AD B2C (business to consumer)[^](https://azure.microsoft.com/documentation/articles/active-directory-b2c-overview/)

    - Leverages existing social accounts(Facebook, MS, Google, Amazon, LinkedIn) or custom accounts
    - It is the evolution of Azure AD Access Control Sevice - classic service (ACS) 

* Azure AD B2B (business to business)[^](https://azure.microsoft.com/documentation/articles/active-directory-b2b-collaboration-overview/)

    - enable access to your organization’s applications from external business partner identities
    - allows your business partners to use their own authentication credentials
* Azure AD Application Proxy[^](https://azure.microsoft.com/documentation/articles/active-directory-application-proxy-get-started/)
    - enables users to leverage SSO to securely access on-premises web applications such as SharePoint sites and Outlook Web Access—without the need for a VPN.
    - Application Proxy is available for the Basic and Premium editions of Azure AD

* Azure AD Directory Join [^](https://azure.microsoft.com/documentation/articles/active-directory-azureadjoin-windows10-devices-overview/)

    - Directory Join enables Windows 10 devices to connect with Azure AD.
    - Allows users to sign-in to Windows using Azure AD accounts, will enable SSO to Azure resources, Windows Store, device access restriction using group policy.
    - Suitable for devices that cannot domain join

* Azure AD Domain Services [^](https://azure.microsoft.com/documentation/articles/active-directory-ds-overview/)
    - Domain Services provide fully managed domain services such as domain join, group policy, LDAP, Kerberos/NTLM, and so on that are compatible with Windows Server Active Directory.

* Azure AD Device Registration [^](https://azure.microsoft.com/documentation/articles/active-directory-conditional-access-device-registration-overview/)
    - enables mobile devices (such as iOS, Android, and Windows devices) to be registered in Azure AD
   - enable conditional access to on-premises or Office 365 applications

* Azure AD Cloud App Discovery[^](https://azure.microsoft.com/documentation/articles/active-directory-cloudappdiscovery-whatis/)

    - finds the applications being used (usage metrics), identifies users, and enables offline data analysis.
    - enables IT departments to discover cloud applications used in their organization
    - allows the applications to be brought under IT control to help mitigate risk of potential data leakage or other security threats

* Azure AD Connect
	- Manages user sign-in options
	- Sign-on methods: Password Synchronization, Pass-through authentication, and Federation with AD FS.
	- Write-back for password, devices and groups
	- Tools to support AD FS	
	
* Azure AD Connect Health [^](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect-health/)

    - enables you to monitor and gain insights into the overall health of the integration between your on-premises Windows Server Active Directory/Active Directory Federation Service and Azure AD (or Office 365).
	- Agents installed on identity infrastructure components, Monitoring and alerts, email notifications and critical alerts, trends, usage report.
	- Requires a P1 license

* Azure AD Identity Protection [^](https://azure.microsoft.com/documentation/articles/active-directory-identityprotection/) 

    - is a security service that enables you to gain insights into potential security vulnerabilities affecting users in your organization (more specifically, their identities)

* Azure AD Pass-through Authentication[^](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication)
	- Allows your users to sign in to both on-premises and cloud-based applications using the same passwords.
	- This feature is an alternative to Azure AD Password Hash Synchronization, which provides the same benefit of cloud authentication to organizations
	- ![Azure AD PTA](https://docs.microsoft.com/en-us/azure/active-directory/connect/media/active-directory-aadconnect-pass-through-authentication/pta1.png)


### Active Directory editions [^](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis#choose-an-edition) [^](https://azure.microsoft.com/en-us/pricing/details/active-directory/)

* **Free** - manage users, synchronize with on-premises Active Directory, establish SSO across Azure and Office 365, and access SaaS applications in the Azure AD application gallery

* **Basic** - Free tier, plus self-service password resets, group-based application access, customizable branding, Azure AD Application Proxy, and a 99.9 percent availability service level agreement (SLA)

* **Premium (P1, P2)** - Free and Basic tiers, plus self-service group management, advanced security reports and alerts, Multi-Factor Authentication, and licenses for Microsoft Identity Manager. P2: provides Identity Protection and Privileged Identity Management.

| **Basic** | **Premium (P1 & P2)**|
|---:|:---|
|99.9% uptime SLA | Includes Microsoft Identity Manager (MIM) 2016 (an on-premises identity and access management suite)|
| Self-service password reset |  Self-service password reset with write-back |
| Azure AD Join for Windows 10 | Multi-facator authentication (MFA) |
| SSO for 10 apps / user |  No SSO app limit |
| Azure AD Application Proxy | MDM auto-enrollment|
| | P2: Identity Protection and Privileged Identity Management|

Azure AD DS

Using Shared Access Signatures (SAS)[^](https://docs.microsoft.com/en-in/azure/storage/common/storage-dotnet-shared-access-signature-part-1)
* Service SAS
* Account SAS

* Ad hoc SAS
* SAS with stored access policy

[Integrating applications with Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-integrating-applications)
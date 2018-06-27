#

## Azure Security Center[^](https://docs.microsoft.com/en-us/azure/security-center/security-center-intro)

Azure Security Center helps you prevent, detect, and respond to threats with increased visibility into and control over the security of your Azure resources. It provides integrated security monitoring and policy management across your subscriptions, helps detect threats that might otherwise go unnoticed, and works with a broad ecosystem of security solutions.

Why use Security Center?

* Centralized policy management
  -A security policy defines the desired configuration of the workloads
* Continuous security assessment
  -Security Center analyzes the security state of compute resources, virtual networks, storage and data services, and applications.
* Actionable recommendations
* Advanced cloud defenses
* Prioritized alerts and incidents
* Integrated security solutions

Security Center Pricing Tiers[^](https://docs.microsoft.com/en-us/azure/security-center/security-center-pricing):

* Free tier - provides security policy, continuous security assessment, and actionable security recommendations.
* Standard tier - Hybrid security (on prem and Cloud), Advanced threat detection, Access and application controls, OS security configuration customization.

Note: To customize OS security configurations, you must be assigned the role of Subscription Owner, Subscription Contributor, or Security Administrator

The Azure Security Center dashboard has the following sections:

* Overview - lists all the Recommendations, Security Solutions, Alerts and Incidents, Events
* Prevention - Shows resources in Compute, Networking, Storage & Data, Applications
* Detection (Advanced Threat Detection feature)- Security Alerts, Most Attacked resources

### Data collection in Azure Security Center

* Security Center collects data from your Azure virtual machines (VMs) and non-Azure computers to monitor for security vulnerabilities and threats
* Data is collected using the **Microsoft Monitoring Agent**, which reads various security-related configurations and event logs from the machine and copies the data to your workspace for analysis
* Automatic provisioning enables the installation of the Microsoft Monitoring Agent on all the VMs in the subscription
* Data collected by Security Center is stored in Log Analytics workspace(s)
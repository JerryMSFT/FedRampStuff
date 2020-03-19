# FedRampStuff
Azure BlurePrint examples can be found @ https://docs.microsoft.com/en-us/azure/governance/blueprints/samples/

Deployment Instructions can be found here @ https://docs.microsoft.com/en-us/previous-versions/azure/security/blueprints/fedramp-iaaswa-overview

This solution uses the following Azure services. Details of the deployment architecture are located in the deployment architecture section. This will deploy to AzureGov

Azure Virtual Machines
(1) bastion host (Windows Server 2016 Datacenter)
(2) Active Directory domain controller (Windows Server 2016 Datacenter)
(2) SQL Server cluster node (SQL Server 2017 on Windows Server 2016)
(2) Web/IIS (Windows Server 2016 Datacenter)

Availability Sets
(1) Active Directory domain controllers
(1) SQL cluster nodes
(1) Web/IIS
Azure Virtual Network
(1) /16 virtual networks
(5) /24 subnets

DNS settings are set to both domain controllers
Azure Load Balancer
Azure Application Gateway
(1) WAF Application Gateway enabled

firewall mode: prevention
rule set: OWASP 3.0
listener: port 443

Azure Storage
(7) Geo-redundant storage accounts
Azure Cloud Witness

Recovery Services vault
Azure Key Vault
Azure Active Directory (Azure AD)
Azure Resource Manager
Azure Monitor (logs)

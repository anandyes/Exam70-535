## Networking[^](https://docs.microsoft.com/en-us/azure/networking/networking-overview)


### Virtual Networks[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-vnet-plan-design-arm)
* Azure Virtual Network enables many types of Azure resources, such as Azure Virtual Machines (VM), to securely communicate with each other, the internet, and on-premises networks.
* All resources in a virtual network can communicate outbound to the internet, by default.
* Communicate between Azure resources:
    * Through a virtual network
    * Through a virtual network service endpoint: Virtual Network (VNet) service endpoints extend your virtual network private address space and the identity of your VNet to the Azure services(Storage, SQL DB, SQL DW), over a direct connection.[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview)
* Communicate with on-premises resources:
    * Point-to-site virtual private network (VPN) - communication between a single computer in your network and a virtual network
    * Site-to-site VPN - communication between your on-premises VPN device and an Azure VPN gateway
    * Azure ExpressRoute - private connection between your network and Azure, through an ExpressRoute partner
* Filter network traffic between subnets using
    * Network security groups
    * Network virtual appliances - a VM that performs a network function, such as a firewall, WAN optimization.
* Routes traffic between subnets, connected VNets, on-prem networks and Internet[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview)
    * Route tables: control where traffic is routed to for each subnet
    * Border gateway protocol (BGP) routes: you can propagate your on-premises BGP routes to your virtual networks
* Connect virtual networks using Virtual network peering (local or global)[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)


### Load Balancer[^](https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview)
* With Azure Load Balancer you can scale your applications and create high availability for your services.
* You can use Azure Load Balancer to:
    * Load-balance incoming internet traffic to your VMs (Public load balancer
)
    * Load-balance traffic across VMs inside a virtual network (Internal load balancer)
    * Port forward traffic to a specific port on specific VMs with inbound network address translation (NAT) rules.
    * Provide outbound connectivity for VMs inside your virtual network by using a public load balancer.
* Use Application Gateway for Transport Layer Security (TLS) protocol termination ("SSL offload") or per-HTTP/HTTPS request, application-layer processing.
* Use Traffic Manager for global DNS load balancing.
* Load Balancer features:
    * Load balancing - can create a load-balancing rule to distribute traffic that arrives at front-end to back-end pool instances.Load Balancer uses a hash-based algorithm (5 tuple hash by default)
    ![Hash Based Load Balancing](https://docs.microsoft.com/en-us/azure/load-balancer/media/load-balancer-overview/load-balancer-distribution.png)
    * Port forwarding - create an inbound NAT rule to port forward traffic from a specific port of a specific front-end IP address to a specific port of a specific back-end instance inside the virtual network. Remote Desktop Protocol (RDP) or Secure Shell (SSH) sessions.
    * Application agnostic and transparent - does not directly interact with TCP or UDP or the application layer
    * Automatic reconfiguration - reconfigures itself when you scale instances up or down
    * Health probes - stops sending new connections to the unhealthy instances. (HTTP custom probe, TCP custom probe, Guest agent probe)
    * Outbound connections (source NAT / SNAT)
* Supports both Basic and Standard SKUs.

![Public Load Balancer](https://docs.microsoft.com/en-us/azure/load-balancer/media/load-balancer-overview/IC727496.png)
![Internal load balancer](https://docs.microsoft.com/en-us/azure/load-balancer/media/load-balancer-overview/IC744147.png)

### Application Gateway[^](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-introduction)
* Azure Application Gateway is a web traffic load balancer that enables you to manage traffic to your web applications. 
* application layer (OSI layer 7) load balancing - can route traffic based on the incoming URL (/images, /video).
* URL-based routing - route traffic to back-end server pools based on URL Paths of the request
* Redirection - automatic HTTP to HTTPS redirection to ensure all communication between an application and its users occurs over an encrypted path. (Global redirection from one port to another port, Path-based redirection, Redirect to an external site)
* Multiple-site hosting -  configure more than one web site on the same application gateway instance
* Session affinity - cookie-based session affinity keeps a user session on the same server
* Secure Sockets Layer (SSL) termination - saves web servers from costly encryption and decryption overhead. Also supports end to end SSL encryption.
* Web application firewall (WAF) - provides centralized protection of your web applications from common exploits and vulnerabilities ( SQL injection attacks, cross site scripting attacks)
* Websocket and HTTP/2 traffic - enable full duplex communication between a server and a client over a long running TCP connection. 

### Traffic Manager[^](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview)
* Azure Traffic Manager allows you to control the distribution of user traffic for service endpoints in different datacenters.
* Traffic Manager uses the Domain Name System (DNS) to direct client requests to the most appropriate endpoint based on a traffic-routing method and the health of the endpoints.
* Traffic Manager benefits:
    * Improve availability of critical applications - automatic failover 
    * Improve responsiveness for high-performance applications - by directing traffic to the endpoint with the lowest network latency
    * Perform service maintenance without downtime - directs traffic to alternative endpoints while the maintenance is in progress
    * Combine on-premises and Cloud-based applications - supports external, non-Azure endpoints
    * Distribute traffic for large, complex deployments - use nested Traffic Manager profiles
* Traffic Manager routing methods - Priority, Weighted, Performance, Geographic
    * **[Priority](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-routing-methods#priority):** Select **Priority** when you want to use a primary service endpoint for all traffic, and provide backups in case the primary or the backup endpoints are unavailable.
    * **[Weighted](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-routing-methods#weighted):** Select **Weighted** when you want to distribute traffic across a set of endpoints, either evenly or according to weights, which you define.
    * **[Performance](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-routing-methods#performance):** Select **Performance** when you have endpoints in different geographic locations and you want end users to use the "closest" endpoint in terms of the lowest network latency.
    * **[Geographic](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-routing-methods#geographic):** Select **Geographic** so that users are directed to specific endpoints (Azure, External, or Nested) based on which geographic location their DNS query originates from. This empowers Traffic Manager customers to enable scenarios where knowing a user’s geographic region and routing them based on that is important. Examples include complying with data sovereignty mandates, localization of content & user experience and measuring traffic from different regions.

### Azure DNS[^](https://docs.microsoft.com/en-us/azure/dns/dns-overview)
* The Domain Name System, or DNS, is responsible for translating (or resolving) a website or service name to its IP address. 
* Reliability and performance - uses Anycast networking so that each DNS query is answered by the closest available DNS server.
* Seamless integration - to manage DNS records for Azure services and external resources as well
* Securtiy - ARM provides role-based access control, audit logs, and resource locking
* Azure DNS does not currently support purchasing of domain names

### NSG[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-nsg)
* A network security group (NSG) contains a list of security rules that allow or deny network traffic to resources connected to Azure Virtual Networks (VNet)
* NSGs can be associated to subnets, individual VMs (classic), or individual network interfaces (NIC) attached to VMs (Resource Manager)
* Endpoint-based access control lists (ACL) and NSGs are not supported on the same VM instance

### User Defined Routes (UDRs)[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview)[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-scenario-udr-gw-nva)
* You can create custom, or user-defined, routes in Azure to override Azure's default system routes, or to add additional routes to a subnet's route table.
* Each subnet in Azure can be linked to a UDR table used to define how traffic initiated in that subnet is routed. If no UDRs are defined, Azure uses default routes to allow traffic to flow from one subnet to another
* The following next hop types can be specified when creating a user-defined route:
    * Virtual appliance - next hop IP address (private IP of NIC, private IP of internal load balancer)
    * Virtual network gateway - traffic destined for specific address prefixes routed to a virtual network gateway
    * None - Specify when you want to drop traffic to an address prefix
    * Virtual network
    * Internet
* A route with the 0.0.0.0/0 address prefix instructs Azure how to route traffic destined for an IP address that is not within the address prefix of any other route in a subnet's route table.
* Azure creates a default route to the 0.0.0.0/0 address prefix, with the Internet next hop type.
* You cannot specify VNet peering or VirtualNetworkServiceEndpoint as the next hop type in user-defined routes. 

### VNet Peering[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)
* Virtual network peering enables you to seamlessly connect two Azure virtual networks.
* VNet peering - connecting VNets within the same Azure region
* Global VNet peering - connecting VNets across Azure regions
* Service chaining enables you to direct traffic from one virtual network to a virtual appliance, or virtual network gateway, in a peered virtual network, through user-defined routes.
*  A virtual network can have only one gateway.
* You can deploy hub-and-spoke networks, where the hub virtual network can host infrastructure components such as a network virtual appliance or VPN gateway.[^](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke)
* Each virtual network can have its own gateway and use it to connect to an on-premises network

### VNet Service Endpoints[^](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview)
* Virtual Network (VNet) service endpoints extend your virtual network private address space and the identity of your VNet to the Azure services, over a direct connection.
* Traffic from your VNet to the Azure service always remains on the Microsoft Azure backbone network.
* Azure services available:
    * Azure Storage
    * Azure SQL Database
    * Azure SQL Data Warehouse
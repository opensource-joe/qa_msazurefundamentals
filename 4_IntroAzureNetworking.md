# Intro to Azure Networking

- Azure Virtual Network (VNet) - VMs, firewalls, and Kubernetes clusters.
- VNet - specify IP address and any subnets. It needs a name, subscription, and regional location.
- Use Subnets for allocation of resources. Default Route for connecting resources and the Internet.
- Public IP Addresses - needed for accessing VNet resources.

- Need a name resolution service to translate between names and IP addresses.
    - Azure provided name resolution - if you only need the resources in a VNet to communicate with each other using names.
    - Azure DNS Private Zones - if your resources need to resolve names of systems in another virtual network.
    - Own DNS Server or Azure DNS - if the resources in your virtual network need to resolve the names of systems in an on-premises environment.

- Connecting to other networks.
    - VNet Peering - connecting resources directly.
    - Global VNet Peering - connecting VNets in different regions.
    - Peering connections go over MS Backbone Network making the connection faster and more secure.
    - Connect VNet to on-prem network using Azure VPN or Azure ExpressRoute.
    - Site to Site - Azure VPN - need to establish Gateway on Azure and with on-prem or outside VNet connection.
    - Point to Site - connecting mobile devices to VNet. Need certificate to pass through Azure VPN Gateway.
    
    - Routing
        1) Policy-based - does not support point-to-sight connections to VPN Gateway.
        2) Route-based - more robust and only supported option for point-to-site connections.
    
    - Azure ExpressRoute - for direct connections between VNet and on-prem env. Does not go over the internet. Much more expensive solution.

    - Four ways Azure uses an ExpressRoute and comes down to where IT infrastructure is located.
        1) Co-Location Facility - MS facility allowing for Direct Model connection with ExpressRoute. Supports connections of 10GB to 100GB through an enterprise edge device.
        2) Cloud Exchange Location - 50MB and 10GB per second. Uses service provider model.
        3) Any-to-Any (IPVPN) Connection
        4) Point-to-Point Ethernet Provider - rent a lease line.

    - Use ExpressRoute to connect to Office 365.
    - ExpressRoute Global Reach - connect to branch offices around the world through the MS network than the internet. Have to pay extra for this service.

- Private Endpoints - indirect way to connect external VNet services (storage) to VNet. It's a private IP outside the resource. Resource needs to be connected through a Private Link.
- Public Endpoints - connecting to resources outside VNet. These are exposed to the internet which is a security risk.
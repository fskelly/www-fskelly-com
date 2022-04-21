---
title: "Using Azure Virtual WAN to connect to Azure VMware Solution"
date: 2022-03-28T07:27:16+01:00
author: "Fletcher Kelly"
Description: ""
Tags: [
    AVS,Networking
]
Categories: [
    Azure VMware Solution, Azure
]
DisableComments: false
draft: false
authors: ["Fletcher Kelly"]

---
## How do I connect my on-premises environment to AVS in a quick and simple way?

There are a few patterns available for connecting [Azure VMware Solution][Azure VMware Solution] to your on-premises network. There is specific guidance for PRODUCTION deployments here [here](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/azure-vmware/eslz-network-topology-connectivity). The option we are talking about here is for a different use case.

**Specific use case:** A _**PoC (Proof of Concept)**_ type environment or smaller environments for testing with a plan to grow after the fact.  

Azure Virtual WAN is one of the easy ways to get this accomplished. Below, we are going to work through an example.

## What are we going to deploy?

{{< figure src="/images/blogImages/2022/vwan-avs-poc/topology.jpg" alt="deployed vwan topology" height="300" width="900" >}}

We are going to use [Azure Virtual WAN][Azure Virtual WAN] to allow for a connection from on-premises to [Azure VMware Solution][Azure VMware Solution].

I have this as modular as possible with [booleans](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/bicep-functions-logical#bool) in [Bicep](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep) to make this is as customizable as possible for you.

> **A VPN Gateway will be deployed.**

```bicep
@description('Specifies whether or not to deploy the site to site connection.')
param deployS2SConnection bool = true
```

> **An ExpressRoute Gateway will be deployed.**

```bicep
@description('Specifies whether or not to deploy ExR connection.')
param deployExRConnection bool = true
```

💪 Bicep code can be found [here](https://github.com/fskelly/flkelly-AzureCode-bicep/tree/main/examples/virtualWan/AVS/module-example).

What to expect when deploying?

1. You will get an ExpressRoute gateway. I set this as a "true" boolean value to cater for this.
1. The deployment will happen over 2 resource groups - if deploying the "vnetconnection" option.  {{< figure src="/images/blogImages/2022/vwan-avs-poc/2resourcegoups.jpg" alt="deployment screenshot showing the 2 deployed resource groups" >}}
1. It will look like nothing is happening in the Virtual WAN resource group. Show hidden items here.  {{< figure src="/images/blogImages/2022/vwan-avs-poc/showHiddenTypes.jpg" alt="deployment screenshot showing hidden items checked" >}}
1. The deployment, if choosing anything Gateway related (VPN Gateway or ExpressRoute gateway) will take some time - up to 35 minutes.  {{< figure src="/images/blogImages/2022/vwan-avs-poc/vHubDeploy.jpg" alt="deployment screenshot showing times" >}}
1. The deployment will deploy a VPN Gateway (on-premises to Azure)
1. The deployment will deploy a ExR Gateway (Azure to AVS)

This deployment is based upon this [Configure a site-to-site VPN in vWAN for Azure VMware Solution](https://docs.microsoft.com/en-us/azure/azure-vmware/configure-site-to-site-vpn-gateway). Whilst I like this article, it is not 100% complete. For the [Azure VMware Solution][Azure VMware Solution] (AVS) to work fully, an [ExpressRoute Gateway for Azure Virtual WAN](https://docs.microsoft.com/en-us/azure/virtual-wan/virtual-wan-expressroute-portal) is needed. I prefer an IaC approach as the [Azure Portal](https://portal.azure.com) UI can change and I like repeatable processes.

{{< figure src="/images/blogImages/2022/vwan-avs-poc/topology.jpg" alt="deployed vwan topology" height="300" width="900" >}}

This solution then allow you connect your on-premises environment to connect to [Azure VMware Solution][Azure VMware Solution]. This is probably one of the easiest ways to connect to [Azure VMware Solution][Azure VMware Solution]

[Azure Virtual WAN][Azure Virtual WAN] can be further extended to ALSO include Point-to-Site connections - [This](https://mecdata.it/en/2020/06/configure-a-point-to-site-vpn-connection-via-openvpn/) is a good starting point for building the certificates (self-signed) for the Point-To-Site connections, if you choose to deploy this.

***DISCLAIMER:***
**These files are NOT production ready, they used to explain concepts and better prepare you for production.**

[Azure VMware Solution]: https://docs.microsoft.com/en-us/azure/azure-vmware/introduction
[Azure Virtual WAN]: https://docs.microsoft.com/en-us/azure/virtual-wan/virtual-wan-about

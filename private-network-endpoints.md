---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-21"

keywords: set up private endpoints, private endpoint, connect service over private network, 

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Setting up service endpoints
{: #private-network-endpoints}

To connect to {{site.data.keyword.cloud}} services over a private network, you must have access to classic infrastructure and enable virtual routing and forwarding (VRF) and connectivity to service endpoints for your account. Then, you can start creating services that support service endpoints for a private network connection.
{: shortdesc}

Complete the following steps to ensure that your account is set up to create and use services that support service endpoints:

1. Check that you have access to {{site.data.keyword.cloud_notm}} infrastructure in your account. Go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Classic Infrastructure** to verify that you have access.
2. Enable your account for VRF. For more information, see [Enabling virtual routing and forwarding](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Enable your account for connectivity to service endpoints. For more information, see [Enabling service endpoints](/docs/account?topic=account-vrf-service-endpoint#service-endpoint).

After you enable the VRF and service endpoint account settings, you can create resources from the catalog that support service endpoints. The following table lists the services that support using service endpoints. 

Refer to the documentation for the specific service for more information about using service endpoints.
{: tip}

## Services that support service endpoints
{: #services-support-service-endpoints}

| Service | Documentation |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} service endpoints integration](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} service endpoints integration](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} service endpoints integration](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} service endpoints integration](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} service endpoints integration](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Connectivity options](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Connecting to a private endpoint](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Adding a private endpoint](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Available for all dedicated hardware plans deployed after 1 January 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} documentation](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Managing service endpoints for {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Connecting to {{site.data.keyword.keymanagementserviceshort}} on the {{site.data.keyword.cloud_notm}} private network](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} documentation](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Public and private service endpoints for {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-plan_clusters#workeruser-master) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) utilizes {{site.data.keyword.keymanagementserviceshort}}'s service endpoint for its BYOK integration|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} service endpoints integration](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Table 1. Services that support using service endpoints" caption-side="top"}








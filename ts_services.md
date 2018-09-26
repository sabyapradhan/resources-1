---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Troubleshooting for services and resources
{: #services}

{{site.data.keyword.Bluemix}} service problems might include issues with deleting service instances. You can recover from these problems by following a few easy steps.
{:shortdesc}

## Why can't I delete my service instance?
{: #ts_service_broker}

You might receive an error message if you try to delete a service instance that is already deleted from the cloud controller.
{:shortdesc}

When you try to delete a service instance, the following error message is displayed:
{: tsSymptoms}

`Gateway timeout`

This problem happens if the service instance is already deleted from the cloud controller.
{: tsCauses}

Create a service instance with the same service name, and bind it to your applications. Then, you can delete the service instance and the applications that use the service.   
{: tsResolve}

---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-19"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Troubleshooting for services
{: #services}

{{site.data.keyword.Bluemix}} service problems might include a gateway timeout error that occurs if you delete a service instance. You can recover from these problems by following a few easy steps.
{:shortdesc}

Services have different types and levels of maturity in {{site.data.keyword.Bluemix_notm}}. For example, there are IBM services and third-party services and levels of those services such as GA, beta, and experimental. Based on the type of service and level of maturity, different levels of support might be offered. For more information, see [How do I get support for services?](/docs/get-support/servicessupport.html#support-different-services)

## Service broker error occurs when you delete a service instance
{: #ts_service_broker}

You might receive an error message if you try to delete a service instance that is already deleted from the cloud controller.
{:shortdesc}

When you try to delete a service instance, you see the following service broker error message:
{: tsSymptoms}
`Gateway timeout`

This problem happens if the service instance is already deleted from the cloud controller.
{: tsCauses}

Create a service instance with the same service name, then bind it to your applications. Then, you can delete the service instance and the applications that use the service.   
{: tsResolve}

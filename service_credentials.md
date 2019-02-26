---

copyright:

  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service key, api key, bind, credential

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}


# Adding a credential
{: #service_credentials}

You can generate a new set of credentials for cases where you want to manually connect an external consumer to an {{site.data.keyword.Bluemix}} service. For example, if you're trying to bind an AWS app to a Watson service, you need to generate a new credential that can be used to bind them together.

## Adding a credential when binding an IAM-enabled service
{: #IAM}

Services that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a user name, password, host name, port, and a URL.

However, while the contents of each credential is unique to the service that generates it, all services managed by IAM require that new credentials include an IAM Service access role. Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

Complete the following steps to add a credential to a service that is managed by IAM:

1. From the resource list, select the name of the service to open the service details page. Then, select the Credentials tab, and click **New Credential +**.
2. From the Add New Credential dialog, provide a **Name**.
3. Specify the role. This value sets the IAM service access role. For more information, see: [IAM Access](/docs/iam?topic=iam-userroles)
4. Optionally, you can provide a Service ID by either allowing IAM to generate a unique value for you, or by providing an existing Service ID. For more information, see: [Creating and working with service IDs](/docs/iam?topic=iam-serviceids)
5. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

  Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
  {: note}
6. Click **Add** to generate the new service credential.

## Adding a credential when binding a Cloud Foundry service
{: #cf_credential}

Cloud Foundry services can generate a service key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A service credential might contain a user name, password, host name, port, and a URL.

However, the contents of each credential is unique to the service that generates it. Some services might generate extra data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the service key that is generated.

Complete the following steps to add a Cloud Foundry credential:

1. From the service details page, select the Credentials tab, and click **New Credential +**.
2. From the Add New Credential dialog, provide a **Name**.
3. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

  Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
  {: note}
4. Click **Add** to generate the new service credential.

---

copyright:
  years: 2015, 2018
lastupdated: "2018-06-14"

---

{:shortdesc: .shortdesc}

# Using services in another region
{: #cross_region_service}

If you have a service instance that is created and bound to apps in one region, you can use this service instance in another region by one of the following methods:
{: shortdesc}

  * Use the service credentials to configure your app instance directly. See [Enabling external apps to use {{site.data.keyword.Bluemix_notm}} service](/docs/apps/reqnsi.html#accser_external){: new_window} for details.
  * Create a user-provided service as a bridge.

	To use a service instance that exists in another region, complete the following steps:

      1. Switch to the region where the service instance exists. From {{site.data.keyword.Bluemix_notm}} console dashboard, expand the **LOCATION** menu, and select the region where the service instance exists.

      2. Retrieve the credentials and the connection parameters from the VCAP_SERVICES environment variable of the service instance in the region where the service exists. Complete the following steps:

	       1. In the {{site.data.keyword.Bluemix_notm}} Dashboard, click your application tile. The Overview page is displayed.
	       2. In the navigation pane, click **Credentials**. The *VCAP_SERVICES* environment variable details are displayed. Record the JSON content for the service instance.

      3. Switch to the region where you want to use the service instance. From {{site.data.keyword.Bluemix_notm}} console dashboard, expand the **LOCATION** menu, and select the region where you want to use the service instance.

      4. Create a user-provided service instance by using the credentials and connection parameters that you recorded from the *VCAP_SERVICES* environment variable. For information, see [Creating a user-provided service instance](/docs/apps/reqnsi.html#user_provide_services).

      5. Bind the user-provided service instance to your app by using the following command:

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```

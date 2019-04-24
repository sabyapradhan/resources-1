---

copyright:

  years: 2017, 2019

lastupdated: "2019-02-19"

keywords: migrate, migrating to a resource group, migrate Cloud Foundry

subcollection: resources

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Cloud Foundry 서비스 인스턴스 및 앱을 리소스 그룹으로 마이그레이션
{: #migrate}

더 간단하고 유연하게 {{site.data.keyword.Bluemix}}를 사용할 수 있도록 Cloud Foundry 영역과 유사한 개념의 [리소스 그룹](/docs/resources?topic=resources-rgs)이 도입되었습니다. 그러나 리소스 그룹에는 IBM Cloud Identity and Access Management(IAM)를 사용하는 정교한 액세스 제어, 서비스 인스턴스를 여러 지역의 앱 및 서비스에 연결하는 기능 및 그룹당 사용량을 볼 수 있는 쉬운 방법과 같은 몇 가지 추가 이점이 있습니다.
{:shortdesc}

당사에서는 리소스 그룹의 이점을 활용하기 위해 Cloud Foundry에서 서비스를 이동하기 시작했습니다. 즉, 리소스 그룹에서 서비스 중 하나의 옆에 ![이 서비스 인스턴스를 리소스 그룹으로 마이그레이션](images/migrate.svg "이 서비스 인스턴스를 리소스 그룹으로 마이그레이션") 아이콘이 표시되면 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://cloud.ibm.com/developer/appservice/dashboard)을 통해 작성된 서비스 인스턴스 또는 앱에 대한 마이그레이션 플랜을 시작하여 현재 Cloud Foundry 조직 및 영역에서 리소스 그룹으로 이동해야 합니다. {{site.data.keyword.Bluemix_notm}} 서비스가 Cloud Foundry 조직, 영역 및 역할 사용에서 IAM 및 리소스 그룹 사용으로 이동할 때까지 기존 Cloud Foundry 서비스 인스턴스를 리소스 그룹으로 마이그레이션할 수 없습니다.

기존 Cloud Foundry 서비스 인스턴스 또는 {{site.data.keyword.dev_console}} 앱을 리소스 그룹으로 마이그레이션하는 경우 마이그레이션이 완료된 후에는 사용자가 선택한 그룹을 변경할 수 없습니다. 따라서 마이그레이션하기 전에 계정에서 리소스를 구성할 방법을 먼저 계획해야 합니다. 이는 청구 가능한 계정이 있는 경우 마이그레이션 전에 하나 이상의 리소스 그룹을 작성해야 한다는 것을 의미할 수 있습니다.

Cloud Foundry 영역에서 리소스를 구성한 방법과 동일한 방법으로 사용자 리소스를 리소스 그룹으로 구성할 수 있습니다. 리소스 그룹 사용에 대한 자세한 정보는 [리소스 그룹의 리소스 구성 우수 사례](/docs/resources?topic=resources-bp_resourcegroups)를 참조하십시오.
{: tip}


## 마이그레이션하는 이유는 무엇입니까?
{: #why_migrate}

### Cloud Foundry 서비스 인스턴스
{: #cf_instances}

리소스 그룹 내에서 Cloud IAM 액세스 제어 및 조직을 지원하는 서비스에는 여러 가지 이점이 있습니다.

* 세분화된 액세스 제어를 사용하여 개별 서비스 인스턴스 또는 리소스 그룹으로 구성된 일련의 리소스에 대한 액세스를 설정할 수 있습니다.
* 액세스 그룹 및 리소스 그룹을 사용하여 사용자 및 리소스를 구성함으로써 최소 수의 액세스 정책만 설정하면 됩니다. 예를 들어, 개발 환경의 리소스에 대한 액세스 권한이 필요한 개발자 집단이 있는 경우, 모든 해당 사용자를 개발자 액세스 그룹으로 구성한 다음 액세스가 필요한 모든 리소스를 단일 리소스 그룹에 추가할 수 있습니다. 그런 다음 리소스 그룹 내의 모든 리소스에 대한 액세스 권한을 갖도록 액세스 그룹에 대한 단일 정책을 설정할 수 있습니다.
* Cloud Foundry 조직별로 사용량을 보는 방법과 유사하게 리소스 그룹별로 사용량을 볼 수 있습니다.
* 모든 Cloud Foundry 영역의 앱과 서비스에 연결할 수 있으며 이를 통해 서로 다른 지역의 앱과 서비스를 연결할 수 있습니다. 마이그레이션하는 경우 원래 Cloud Foundry 서비스 인스턴스를 별명으로 변경하고 연결된 인스턴스를 선택한 리소스 그룹에 작성하면 연결이 자동으로 설정됩니다. 다음은 별명을 사용하여 연결하는 방법을 보여주는 그래픽입니다.

![별명을 작성하기 위해 서비스 인스턴스를 Cloud Foundry 영역에 바인딩](images/alias.svg "별명을 작성하기 위해 서비스 인스턴스를 Cloud Foundry 영역에 바인딩")

### {{site.data.keyword.dev_console}}apps

{: #app_services}

이전에는 {{site.data.keyword.dev_console}} 앱이 Cloud Foundry 서비스 인스턴스와만 연관될 수 있었습니다. 이제 앱을 리소스 그룹으로 마이그레이션하는 경우 리소스 그룹에 속하고 Cloud IAM 액세스 제어를 지원하는 서비스 인스턴스와 앱을 연관시킬 수 있습니다.

## 누가 마이그레이션할 수 있습니까?
{: #whocanmigrate}

### 서비스 인스턴스에 필요한 액세스 권한
{: #required_access_instances}

Cloud Foundry 서비스 인스턴스를 리소스 그룹에 마이그레이션하려면 사용자에게 특정 액세스 권한이 있어야 합니다.

* 사용자는 Cloud Foundry 영역의 개발자 역할 또는 인스턴스가 속한 조직의 조직 관리자 Cloud Foundry 역할이 있어야 합니다.
* 사용자는 인스턴스가 마이그레이션될 리소스 그룹을 관리하려면 뷰어 이상의 IAM 역할이 있어야 합니다.
* 사용자는 서비스의 편집자 이상의 IAM 역할이 있어야 합니다.

올바른 액세스 지정에 대한 자세한 정보는 [Cloud Foundry 액세스](/docs/iam?topic=iam-cfaccess) 및 [IAM 액세스](/docs/iam?topic=iam-userroles#platformrolestable1)를 참조하십시오.

사용자에게 있는 액세스 권한을 확인하려면 콘솔 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭한 후 **사용자**를 클릭하십시오. 이름을 클릭하여 지정된 IAM 역할 및 **Cloud Foundry 액세스**에 대한 **액세스 정책**을 검토하여 액세스 권한이 있는 조직 및 지정된 Cloud Foundry 역할을 확인하십시오.
{: tip}

### {{site.data.keyword.dev_console}} 앱에 필요한 액세스 권한
{: #required_access_apps}

{{site.data.keyword.dev_console}} 앱에 액세스할 수 있는 모든 사용자가 해당 앱을 마이그레이션할 수 있습니다. 그러나 앱을 마이그레이션해도 해당 앱과 연관된 서비스는 마이그레이션되지 않습니다. 서비스 인스턴스를 별도로 마이그레이션해야 합니다.

## 마이그레이션은 어떻게 작동합니까?
{: #how}

### 서비스 인스턴스 마이그레이션
{: #migrate_instances}

Cloud Foundry 조직 및 영역에서 리소스 그룹으로 서비스 인스턴스를 마이그레이션하는 경우 연결된 새 서비스 인스턴스가 리소스 그룹에 작성됩니다. Cloud Foundry 조직 및 영역의 원래 인스턴스는 [별명](/docs/resources?topic=resources-connect_app#what_is_alias)이 됩니다. 별명이 조직의 할당량에 포함되지만 리소스 그룹에서 서비스 인스턴스의 사용에 대해 비용이 청구됩니다.

![리소스 그룹으로 Cloud Foundry 서비스 인스턴스 마이그레이션](images/migration.gif){: gif}

Cloud Foundry 서비스 인스턴스와 연관된 ![이 서비스 인스턴스를 리소스 그룹으로 마이그레이션](images/migrate.svg "이 서비스 인스턴스를 리소스 그룹으로 마이그레이션") 아이콘을 통해 리소스 목록에서 알림을 받은 경우 서비스 인스턴스가 한 번에 하나씩 마이그레이션됩니다.

마이그레이션 프로세스를 시작하기 전에 서비스 문서를 검토하여 서비스 인스턴스를 리소스 그룹으로 마이그레이션할 때 수행해야 하는 추가적인 서비스별 변경사항이 있는지 확인하십시오. 예를 들어, Cloud Foundry 별명을 삭제하는 경우 데이터를 이전 인스턴스에서 새 인스턴스로 마이그레이션하거나 앱에 사용된 인증 정보를 업데이트해야 할 수 있습니다. 마이그레이션된 서비스의 API에 대한 직접 호출을 작성하는 애플리케이션은 IAM API 키 또는 액세스 토큰을 사용하도록 API 호출을 업데이트해야 합니다.
{: tip}

1. **추가 조치** 메뉴를 여십시오.
2. 시작할 **리소스 그룹으로 마이그레이션**을 선택하십시오.
3. 리소스 그룹을 선택하십시오.
4. **마이그레이션**을 클릭하면 인스턴스가 마이그레이션됩니다.
5. 한 번에 하나의 인스턴스만 마이그레이션할 수 있으므로 첫 번째 인스턴스를 마이그레이션한 후에 적격한 인스턴스를 계속 마이그레이션할 수 있습니다.

인스턴스를 마이그레이션하고 나면 리소스 목록의 서비스 섹션에 표시됩니다. 별명은 리소스 목록의 Cloud Foundry 섹션에 남아 있습니다. 리소스 목록의 Cloud Foundry 섹션에 있는 ![링크 아이콘](images/link.svg "별명을 표시하는 링크 아이콘")을 사용하여 별명을 식별할 수 있습니다.

### {{site.data.keyword.dev_console}} 앱 마이그레이션
{: #migrate_apps}

앱 목록 보기에서 각 항목과 연관된 ![이 서비스 인스턴스를 리소스 그룹으로 마이그레이션](images/migrate.svg "이 서비스 인스턴스를 리소스 그룹으로 마이그레이션") 아이콘을 클릭하면 앱이 한 번에 하나씩 마이그레이션됩니다.

1. **메뉴** 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg)을 클릭한 후 Watson, 모바일 또는 웹 앱과 같은 관심 있는 개발자 포털을 선택하십시오.
2. **앱(조치가 필요함)** 및 **앱(마이그레이션됨)** 목록을 표시하는 **앱**을 선택하십시오.
3. **앱(조치가 필요함)** 목록의 각 항목에 대해 **마이그레이션** 아이콘 ![이 서비스 인스턴스를 리소스 그룹으로 마이그레이션](images/migrate.svg "이 서비스 인스턴스를 리소스 그룹으로 마이그레이션")을 클릭하십시오.
4. 새 리소스 그룹을 선택하거나 작성하십시오.
5. **마이그레이션**을 클릭하면 앱이 마이그레이션됩니다.
6. 이제 앱이 **앱(마이그레이션됨)** 목록에 표시되는지 확인하십시오.
7. 한 번에 하나의 앱만 마이그레이션할 수 있으므로 첫 번째 앱을 마이그레이션한 후에 적격한 앱을 계속 마이그레이션할 수 있습니다.


## 다음 단계
{: #migrate_next_steps}

Cloud Foundry 서비스 인스턴스를 리소스 그룹으로 마이그레이션한 다음 계정 내의 사용자가 계정 리소스 그룹 내의 리소스에 대한 필수 레벨의 액세스 권한을 보유하고 있는지 확인해야 합니다. 또한 리소스 그룹을 관리하기 위한 액세스 권한을 제공하고자 하는 경우가 있으므로 사용자가 계정 리소스 그룹 내에 새 서비스 인스턴스를 작성할 수 있습니다.

리소스 그룹 내의 리소스에 대한 액세스를 지정하는 방법에 대한 자세한 정보는 [리소스 그룹 및 그룹 내의 리소스에 대한 액세스 지정](/docs/resources?topic=resources-bp_resourcegroups#assigning_access_rgs)을 참조하십시오.

또한 서비스에 대한 문서를 검토하여 마이그레이션이 완료된 후에 기존 앱에 대해 업데이트를 수행해야 하는지 확인하십시오.


## 문제점 해결
{: #ts_migration}

Cloud Foundry 서비스 인스턴스 마이그레이션과 관련된 문제가 발생하는 경우 [서비스 인스턴스 문제점 해결](/docs/resources?topic=resources-services)을 확인하십시오.

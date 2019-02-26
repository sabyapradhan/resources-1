---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# 리소스의 개념
{: #resource}

리소스란 [리소스 그룹](/docs/resources?topic=resources-rgs) 내에서 작성, 관리 및 포함될 수 있는 모든 것입니다. 일부 예제에는 앱, 서비스 인스턴스, 컨테이너 클러스터, 스토리지 볼륨 및 가상 서버가 포함됩니다. 카탈로그에서 작성될 때 리소스 그룹에 추가될 수 있는 모든 서비스 인스턴스를 리소스라고 하며 IAM 액세스 제어를 사용하여 관리됩니다. [액세스에 대한 IAM 역할](/docs/iam?topic=iam-userroles#iamusermanrol)의 사용 및 리소스 그룹 내의 조직을 지원하는 서비스가 IAM 사용 서비스입니다.

현재 모든 서비스가 리소스 그룹 및 IAM의 사용을 지원하지는 않습니다. 카탈로그에서 작성될 때 Cloud Foundry 조직 및 영역에 추가되는 모든 서비스 인스턴스는 IAM 사용 서비스와 명백하게 다릅니다. Cloud Foundry 서비스는 리소스 그룹에 연결되지 않으며 [액세스 관리에 대한 Cloud Foundry 역할](/docs/iam?topic=iam-cfaccess#cfroles)을 사용합니다. 이러한 서비스를 Cloud Foundry 서비스라고 합니다. 서비스에서 IAM 및 리소스 그룹에 대한 지원을 사용으로 설정하면 사용자가 [기존 Cloud Foundry 인스턴스를 리소스 그룹에 마이그레이션](/docs/resources?topic=resources-migrate)하는 기능에 대한 알림을 받습니다.



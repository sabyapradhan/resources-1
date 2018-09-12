---

copyright:

  years: 2015, 2018
  
lastupdated: "2018-08-29"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# FAQ
{: #resources-faq}

## 리소스 그룹의 개념
{: #resource-group}

리소스 그룹은 사용자 정의할 수 있는 그룹화에서 계정 리소스를 구성하기 위한 방법입니다. {{site.data.keyword.Bluemix}} Identity and Access Management(IAM) 액세스 제어를 사용하여 관리되는 계정 리소스는 계정 내의 리소스 그룹에 속합니다. 카탈로그에서 리소스를 작성할 때 리소스 그룹에 지정합니다. 그런 다음 계정의 리소스 그룹당 사용량을 보고 리소스 그룹의 모든 리소스 또는 리소스 그룹의 단일 리소스에 대한 사용자 액세스를 쉽게 지정할 수 있습니다.

리소스 그룹 작성 및 작업에 대한 자세한 정보는 [리소스 그룹 관리](/docs/resources/resourcegroups.html#rgs)를 참조하십시오.  

## 내 Cloud Foundry 서비스 인스턴스를 리소스 그룹으로 마이그레이션하는 이유는 무엇입니까?
{: #instance-migrated}

Cloud Foundry 서비스를 리소스 그룹으로 마이그레이션하면 사용 중인 서비스를 IAM 액세스 제어 및 리소스 그룹에서 사용할 수 있습니다. IAM 역할을 사용하여 세분화된 액세스 제어를 활용할 수 있습니다. 또한 계정에서 리소스 그룹당 사용량을 볼 수 있습니다. 

리소스 그룹으로 마이그레이션할 수 있는 Cloud Foundry 서비스가 있는 경우 대시보드에서 알림을 받습니다. 마이그레이션 프로세스에 대한 자세한 정보는 [Cloud Foundry 서비스 인스턴스 및 앱을 리소스 그룹으로 마이그레이션](/docs/resources/instance_migration.html#migrate)을 참조하십시오.

## 왜 리소스를 작성하여 리소스 그룹에 추가할 수 없습니까?
{: #create-add-resource}

아마도 액세스 문제가 있는 것 같습니다. 리소스 그룹 자체에서 최소한 뷰어 역할을 갖고 있어야 하고 계정의 서비스에서는 최소한 편집자 역할을 갖고 있어야 합니다. 계정 관리자에게 문의하여 계정에서 지정된 액세스 권한을 검증할 수 있습니다. 

## 누가 리소스 그룹을 작성할 수 있습니까?
{: #create-resource}

계정의 모든 {{site.data.keyword.Bluemix_notm}} IAM 사용 서비스에서 관리자 역할을 지정받은 경우에만 리소스 그룹을 작성할 수 있습니다.

## 리소스 그룹을 삭제할 수 있습니까?
{: #delete-resource-group}

작성된 후에는 리소스 그룹을 삭제할 수 없습니다.

## 리소스 그룹 간에 서비스 인스턴스를 이동할 수 있습니까?
{: #instances-between-rgs}

리소스 그룹 간에 서비스 인스턴스를 이동할 수 없습니다. 서비스 인스턴스를 올바르지 않게 지정한 경우, 인스턴스를 삭제하고 다시 작성하여 올바른 리소스 그룹에 지정해야 합니다.  

## 리소스 그룹당 사용량을 볼 수 있습니까?
{: #view-usage}

예, 볼 수 있습니다. 사용량 대시보드 페이지를 열려면 **관리 > 청구 및 사용량 > 사용량**을 클릭하십시오. 계정의 리소스 그룹별 사용량에 대한 요약을 볼 수 있습니다. 

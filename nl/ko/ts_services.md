---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# 서비스 및 리소스 문제점 해결
{: #services}

서비스 및 리소스에 대한 일반 문제점에는 서비스 인스턴스 삭제와 관련된 문제 또는 서비스 마이그레이션에 대한 문제가 포함될 수 있습니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

## 서비스 인스턴스를 삭제할 수 없는 이유는 무엇입니까?
{: #ts_service_broker}
{: troubleshoot}

클라우드 제어기에서 이미 삭제된 서비스 인스턴스를 삭제하려고 하는 경우 오류 메시지가 표시될 수 있습니다.
{:shortdesc}

서비스 인스턴스 삭제를 시도하는 경우 다음 오류 메시지가 표시됩니다.
{: tsSymptoms}

`Gateway timeout`

이 문제점은 서비스 인스턴스가 클라우드 제어기에서 이미 삭제된 경우에 발생합니다.
{: tsCauses}

동일한 서비스 이름으로 서비스 인스턴스를 작성한 후에 이를 애플리케이션에 바인드하십시오. 그런 다음 서비스 인스턴스 및 서비스를 사용하는 애플리케이션을 삭제할 수 있습니다.   
{: tsResolve}

## 서비스 인스턴스가 잘못된 리소스 그룹으로 마이그레이션된 이유는 무엇입니까? 
{: #ts_service_instance}
{: troubleshoot}

서비스 인스턴스가 잘못된 리소스 그룹으로 마이그레이션되었고 재지정될 수 없습니다.
{:shortdesc}

리소스가 지정된 후에는 리소스 그룹 간에 해당 리소스를 이동할 수 없습니다.
{: tsSymptoms}

인스턴스를 잘못된 리소스 그룹에 지정했습니다.  
{: tsCauses}

이 문제를 정정하기 위해 인스턴스를 삭제하고 카탈로그에서 새 인스턴스를 작성하려고 시도할 수 있습니다. 새 인스턴스를 작성할 때 올바른 리소스 그룹에 지정할 수 있습니다.
{: tsResolve}

## 적합한 인스턴스를 마이그레이션할 수 없는 이유는 무엇입니까?
{: #ts_migrate_instance}
{: troubleshoot}

계정의 사용자가 적합한 인스턴스를 마이그레이션할 때 문제가 발생합니다.
{:shortdesc}

적합한 인스턴스를 마이그레이션할 수 없습니다.
{: tsSymptoms}

적합한 인스턴스를 마이그레이션할 수 없는 경우 올바른 액세스 권한이 없을 수도 있습니다.
{: tsCauses}

인스턴스를 마이그레이션하려면 사용자에게 특정 액세스 권한이 있어야 합니다. 사용자에게 있는 액세스 권한을 확인하려면 콘솔 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭한 후 **사용자**를 클릭하십시오. 이름을 클릭하고 지정된 IAM 역할 및 Cloud Foundry 액세스에 대한 액세스 정책을 검토하여 액세스 권한이 있는 조직 및 지정된 Cloud Foundry 역할을 확인하십시오.
{: tsResolve}

## 내 서비스를 모두 마이그레이션할 수 없는 이유는 무엇입니까?
{: #ts_service_migration}
{: troubleshoot}

모든 서비스가 마이그레이션에 적합한 것은 아닙니다.
{:shortdesc}

특정 서비스를 마이그레이션할 수 없습니다.
{: tsSymptoms}

리소스 그룹에 추가될 수 없고 Identity and Access Management(IAM)를 사용하여 관리되지 않는 서비스를 마이그레이션 중입니다. 서비스가 적합하지 않은 경우 마이그레이션을 위한 옵션이 없습니다.
{: tsCauses}

서비스를 검사하여 마이그레이션에 적합한지 확인하십시오. 알림이 수신되고 서비스가 마이그레이션에 적합한지 여부를 알리는 `support_rc_migration` 플래그가 표시됩니다.
{: tsResolve}

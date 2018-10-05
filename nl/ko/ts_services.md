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


# 서비스 및 리소스 문제점 해결
{: #services}

{{site.data.keyword.Bluemix}} 서비스 문제점에는 서비스 인스턴스 삭제와 관련된 문제가 포함될 수 있습니다. 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

## 서비스 인스턴스를 삭제할 수 없는 이유는 무엇입니까?
{: #ts_service_broker}

클라우드 제어기에서 이미 삭제된 서비스 인스턴스를 삭제하려고 하는 경우 오류 메시지가 표시될 수 있습니다.
{:shortdesc}

서비스 인스턴스 삭제를 시도하는 경우 다음 오류 메시지가 표시됩니다.
{: tsSymptoms}

`Gateway timeout`

이 문제점은 서비스 인스턴스가 클라우드 제어기에서 이미 삭제된 경우에 발생합니다.
{: tsCauses}

동일한 서비스 이름으로 서비스 인스턴스를 작성한 후에 이를 애플리케이션에 바인드하십시오. 그런 다음 서비스 인스턴스 및 서비스를 사용하는 애플리케이션을 삭제할 수 있습니다.   
{: tsResolve}

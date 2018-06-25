---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-02"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 서비스 문제점 해결
{: #services}

{{site.data.keyword.Bluemix}} 서비스 문제점에는 서비스 인스턴스를 삭제할 때 발생하는 게이트웨이 제한시간 오류가 포함될 수 있습니다. 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

{{site.data.keyword.Bluemix_notm}}의 서비스에는 서로 다른 유형 및 레벨의 완성도가 존재합니다. 예를 들어, IBM 서비스 및 써드파티 서비스가 있으며 GA, 베타 및 시범 레벨의 서비스가 있습니다. 서비스의 유형 및 완성도 레벨에 따라 다른 레벨의 지원이 제공될 수 있습니다. 자세한 정보는 [서비스에 대한 지원은 어떻게 받습니까?](/docs/get-support/servicessupport.html#support-different-services)를 참조하십시오.

## 서비스 인스턴스를 삭제할 때 서비스 브로커 오류 발생
{: #ts_service_broker}

클라우드 제어기에서 이미 삭제된 서비스 인스턴스를 삭제하려고 할 경우 오류 메시지가 표시될 수 있습니다.
{:shortdesc}

서비스 인스턴스를 삭제하려는 경우 다음 서비스 브로커 오류 메시지가 표시됩니다.
{: tsSymptoms}
`Gateway timeout`

이 문제점은 서비스 인스턴스가 클라우드 제어기에서 이미 삭제된 경우에 발생합니다.
{: tsCauses}

동일한 서비스 이름으로 서비스 인스턴스를 작성한 후 애플리케이션에 바인드하십시오. 그런 다음 서비스 인스턴스 및 서비스를 사용하는 애플리케이션을 삭제할 수 있습니다.   
{: tsResolve}

---

copyright:

  years: 2015, 2019
lastupdated: "2019-02-18"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# 리소스 검색
{: #searching-for-resources}

{{site.data.keyword.cloud}} 콘솔의 어느 위치에서나 카탈로그의 리소스 목록 및 오퍼링에서 찾으려는 프로비저닝된 리소스를 검색할 수 있습니다. 콘솔 메뉴 표시줄의 검색 필드에 리소스 또는 태그를 입력하십시오. {{site.data.keyword.Bluemix_notm}} 명령행 인터페이스(CLI)를 사용하여 리소스에서 검색할 수도 있습니다. CLI는 위치와 데이터 센터 전체에서 분산 애플리케이션 및 서비스 인스턴스를 검색합니다.
{:shortdesc}

## 검색 결과 세분화
{: #results}

<dl>
<dt>모든 리소스 결과 보기</dt>
<dd>리소스 목록 내의 이름 필드를 자동으로 채워 가장 관련성이 높은 결과를 제공하는 필터링된 리소스 목록을 보려면 이 옵션을 사용하십시오. 리턴된 검색에는 처음 10개의 검색 결과가 표시됩니다. 더 많은 결과가 있음을 알고 있는 경우 리소스 목록에서 모든 결과를 볼 수 있습니다. 이 옵션은 리소스 결과 또는 태그 검색과 일치하는 경우에 표시됩니다. 리소스 결과 이름 또는 태그와 일치하지 않으면 표시되지 않습니다.</dd>
<dt>모든 카탈로그 결과 보기</dt>
<dd>필터링된 카탈로그 검색을 보려면 이 옵션을 사용하십시오. 처음 5개의 결과가 이름별로 표시됩니다. 카탈로그 항목에 대한 세부적인 검색 기준을 원하는 경우(예: 설명 검색) 이 링크를 클릭하여 필터링된 카탈로그 결과 보기를 가져올 수 있습니다. 이 옵션은 작성할 오퍼링을 빠르게 찾는 데 도움이 됩니다. 이 옵션은 카탈로그 결과와 일치하는 경우에 표시됩니다. 검색 조회가 `tag:`로 시작하는 경우에는 이 필드가 표시되지 않습니다.</dd>
<dt>검색 지원 케이스</dt>
<dd>인프라 리소스를 포함하여 플랫폼 전체에서 열린 지원 케이스를 기준으로 필터링하려면 이 옵션을 사용하십시오. `tag:`로 검색하는 경우를 포함하여 임의의 항목을 검색하는 경우 검색의 끝에 이 옵션이 표시됩니다.</dd>
<dt>문서에서 검색</dt>
<dd>필터링된 문서를 가져오려면 이 옵션을 사용하십시오. `tag:`로 검색하는 경우를 포함하여 임의의 항목을 검색하는 경우 검색의 끝에 이 옵션이 표시됩니다.</dd>
</dl>

커서를 검색 필드로 이동하려면 슬래시 키(/)를 누르십시오.
{: tip}


## CLI를 사용하여 검색
{: #searching-cl}

버전 0.6.7부터 {{site.data.keyword.Bluemix_notm}} CLI를 사용하여 하나의 명령으로 Lucene 조회 구문을 통해 모든 리소스에서 검색할 수도 있습니다.

  현재 CLI는 클래식 인프라 인스턴스에서 실행 중인 리소스를 검색하지 않습니다.
  {: note}

다음 속성을 검색할 수 있습니다.

<dl>
<dt>`name`</dt>
<dd> 리소스의 사용자 정의 이름입니다.</dd>
<dt>`region`</dt>
<dd>리소스가 프로비저닝된 지리적 위치입니다. 허용되는 값은 `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` 및 `jp-tok`입니다.</dd>
<dt>`service_name`</dt>
<dd>'ibmcloud catalog service-marketplace' 출력의 이름 열에 표시되는 서비스의 이름입니다.</dd>
<dt>`family`</dt>
<dd>리소스가 속한 클라우드 컴포넌트입니다. 허용되는 값은 `cloud_foundry`, `containers` 또는 `resource_controller`입니다.</dd>
<dt>`organization_id`</dt>
<dd>Cloud Foundry 조직 GUID입니다.</dd>
<dt>`doc.space_id`</dt>
<dd>Cloud Foundry 영역 GUID입니다.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>리소스 그룹의 ID입니다.</dd>
<dt>`type`</dt>
<dd>리소스 유형입니다. 허용되는 값은 `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding` 및 `resource-group`입니다.</dd>
<dt>`creation_date`</dt>
<dd>리소스가 작성된 날짜입니다.</dd>
<dt>`modification_date`</dt>
<dd> 마지막으로 리소스가 수정된 날짜입니다.</dd>
</dl>

### 검색 예제
{: #resource-name}

다음 예제는 계정 리소스를 검색하는 데 도움이 될 수 있습니다.

* `ABC`라는 모든 리소스를 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search ‘name:ABC’`

* `MyResource`라는 모든 Cloud Foundry 애플리케이션을 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* Message Hub의 모든 서비스 인스턴스를 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search 'service_name:messagehub'`

* `us-south` 지역에 있는 `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry 조직 또는 `c900d9671b235c00461c5e311a8aeced` 리소스 그룹에서 모든 리소스를 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* 2018년 5월 16일에서 2018년 5월 20일 사이에 작성된 모든 리소스를 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`

* 이름이 "my"로 시작하는 모든 리소스를 검색하려면 다음 명령을 입력하십시오.

    `ibmcloud resource search 'name:my*' -s type`

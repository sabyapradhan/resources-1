---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-26"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# 다른 지역에서 서비스 사용
{: #cross_region_service}

한 지역에서 작성되어 앱에 바인딩된 서비스 인스턴스가 있는 경우, 다음 방법 중 하나를 사용하여 다른 지역에서 이 서비스 인스턴스를 사용할 수 있습니다.
{: shortdesc}

  * 서비스 인증 정보를 사용하여 직접 앱 인스턴스를 구성하십시오. 세부사항은 [외부 앱에 서비스 연결](/docs/resources?topic=resources-externalapp#externalapp)을 참조하십시오.
  * 사용자 제공 서비스를 브릿지로 작성하십시오.

	다른 지역에 있는 서비스 인스턴스를 사용하려면 다음 단계를 수행하십시오.

      1. 서비스 인스턴스가 있는 지역으로 전환하려면 **메뉴 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg)** > **리소스 목록**을 클릭하십시오. 그런 다음 **위치** 메뉴를 펼친 후 지역을 선택하십시오.

      2. 서비스가 있는 지역 내 서비스 인스턴스의 VCAP_SERVICES 환경 변수에서 인증 정보와 연결 매개변수를 검색하십시오. 다음 단계를 수행하십시오.

	       1. {{site.data.keyword.Bluemix_notm}} 대시보드의 앱 타일에서 **모두 보기**를 클릭하십시오. 개요 페이지가 표시됩니다.
	       2. 탐색 분할창에서 **인증 정보**를 클릭하십시오. *VCAP_SERVICES* 환경 변수 세부사항이 표시됩니다. 서비스 인스턴스의 JSON 컨텐츠를 기록하십시오.

      3. 서비스 인스턴스를 사용하려는 지역으로 전환하십시오. **메뉴 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg)** > **리소스 목록**을 클릭하십시오. 그런 다음 **위치** 메뉴를 펼친 후 서비스 인스턴스를 사용할 지역을 선택하십시오.

      4. *VCAP_SERVICES* 환경 변수에서 기록한 인증 정보와 연결 매개변수를 사용하여 사용자 제공 서비스 인스턴스를 작성하십시오. 자세한 정보는 [사용자 제공 서비스 인스턴스 작성](/docs/apps/tutorials?topic=creating-apps-add-resource#user_provide_services)을 참조하십시오. 

      5. 다음 명령을 사용하여 사용자 제공 서비스 인스턴스를 앱에 바인딩하십시오.

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```

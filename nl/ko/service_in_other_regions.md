---

copyright:
  years: 2015, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}

# 다른 지역에서 서비스 사용
{: #cross_region_service}

한 지역에서 작성되어 앱에 바인딩된 서비스 인스턴스가 있는 경우, 다음 방법 중 하나를 사용하여 다른 지역에서 이 서비스 인스턴스를 사용할 수 있습니다.
{: shortdesc}

  * 서비스 신임 정보를 사용하여 직접 앱 인스턴스를 구성하십시오. 세부사항은 [외부 앱이 {{site.data.keyword.Bluemix_notm}} 서비스를 사용하도록 설정](/docs/apps/reqnsi.html#accser_external){: new_window}을 참조하십시오.
  * 사용자 제공 서비스를 브릿지로 작성하십시오.

	다른 지역에 있는 서비스 인스턴스를 사용하려면 다음 단계를 수행하십시오.

      1. 서비스 인스턴스가 있는 지역으로 전환하십시오. {{site.data.keyword.Bluemix_notm}} 메뉴 표시줄에서 **지역** 메뉴를 펼친 후 서비스 인스턴스가 있는 지역을 선택하십시오.

      2. 서비스가 있는 지역 내 서비스 인스턴스의 VCAP_SERVICES 환경 변수에서 신임 정보와 연결 매개변수를 검색하십시오. 다음 단계를 수행하십시오.

	       1. {{site.data.keyword.Bluemix_notm}} 대시보드에서 애플리케이션 타일을 클릭하십시오. 개요 페이지가 표시됩니다.
	       2. 탐색 분할창에서 **신임 정보**를 클릭하십시오. *VCAP_SERVICES* 환경 변수 세부사항이 표시됩니다. 서비스 인스턴스의 JSON 컨텐츠를 기록하십시오.

      3. 서비스 인스턴스를 사용하려는 지역으로 전환하십시오. {{site.data.keyword.Bluemix_notm}} 메뉴 표시줄에서 **지역** 메뉴를 펼친 후 서비스 인스턴스를 사용할 지역을 선택하십시오.

      4. *VCAP_SERVICES* 환경 변수에서 기록한 신임 정보와 연결 매개변수를 사용하여 사용자 제공 서비스 인스턴스를 작성하십시오. 사용자 제공 서비스 인스턴스를 작성하는 방법에 대한 정보는 [사용자 제공 서비스 인스턴스 작성](/docs/apps/reqnsi.html#user_provide_services)의 내용을 참조하십시오.

      5. 다음 명령을 사용하여 사용자 제공 서비스 인스턴스를 앱에 바인딩하십시오.

	     ```
	     bluemix service bind myapp user-provided_service_instance
	     ```

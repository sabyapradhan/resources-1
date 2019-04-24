---

copyright:

  years: 2015, 2019
lastupdated: "2019-04-10"

keywords: location, regions, data centers, service location, service availability

subcollection: resources

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# サービス可用性
{: #services_region}

{{site.data.keyword.Bluemix}} によって、サービスとアプリの実装、ホスト、および拡大を簡単に行うことができます。 それにより、
アプリケーション・ロジックとアプリケーション設計に集中することができます。
{:shortdesc}

各 {{site.data.keyword.Bluemix_notm}} ロケーションですべてのサービスが購入できるわけではありません。 また、当該ロケーションでサービスが購入可能な場合でも、サービスは別の場所でホストされていることがあります。 以下の表は、IBM が提供するサービスを示しています。 使用可能なリソースの全リストは、{{site.data.keyword.Bluemix_notm}} コンソール内の[カタログ](https://cloud.ibm.com/catalog){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") を参照してください。

グローバルにホストされるサービスが作成するリソースは複数のロケーションで作動します。 例えば、{{site.data.keyword.cos_full_notm}} を使用すると、アプリケーションが REST API 要求を送信する[エンドポイントの選択](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-service-availability#service-availability)によって、1 つの[データ・センター](/docs/overview?topic=overview-zero-downtime#data_center)に、または、複数のロケーションの組み合わせにでも、データを分散させることを選択できます。

<!-- Do not manually change the table or add content after the table. -->
<!-- Everything after the second line of the table will be deleted. -->
<!-- Also, do not change the number of dashes in the second line. -->
<!-- Ping @natimpe for details. -->

| サービス | ダラス | ロンドン | フランクフルト | シドニー | ワシントン DC | 東京 |
|-----|-----|-----|-----|-----|-----|
| API Connect | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Activity Tracker | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Alert Notification | ダラスでホスト | ロンドンでホスト | 使用不可 | シドニーでホスト | 使用不可 | 使用不可 | 
| Analytics Engine | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 東京でホスト | 
| Apache Spark | ダラスでホスト | ロンドンでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| App Connect | ダラスでホスト | ロンドンでホスト | 使用不可 | ダラスからシンジケート | 使用不可 | 使用不可 | 
| App ID | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 東京でホスト | 
| App Launch | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Auto-Scaling | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Automated Accessibility Tester | ダラスでホスト | ロンドンでホスト | 使用不可 | ロンドンからシンジケート | 使用不可 | 使用不可 | 
| Availability Monitoring | ダラスでホスト | ロンドンでホスト | 使用不可 | シドニーでホスト | 使用不可 | 使用不可 | 
| BigInsights for Apache Hadoop (サブスクリプション) | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Blockchain | ダラスでホスト | ダラスからシンジケート | ダラスからシンジケート | ダラスからシンジケート | 使用不可 | 使用不可 | 
| Blockchain Platform 2.0 | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Certificate Manager | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 東京でホスト | 
| Cloud Foundry エンタープライズ環境 | 使用不可 | 使用不可 | フランクフルトでホスト | 使用不可 | 使用不可 | 使用不可 | 
| Cloud Object Storage | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 
| Cloudant | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Compare and Comply | ダラスでホスト | 使用不可 | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| Compose Enterprise | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for Elasticsearch | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for JanusGraph | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for MongoDB | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for MySQL | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for PostgreSQL | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for RabbitMQ | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for Redis | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for RethinkDB | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for ScyllaDB | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Compose for etcd | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Consult with IBM Cloud Garage | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 
| Continuous Delivery | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 東京でホスト | 
| Cost and Asset Management | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Data Store for Memcache | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Databases for Elasticsearch | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Databases for MongoDB | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Databases for PostgreSQL | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Databases for Redis | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Databases for etcd | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Db2 Hosted | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Db2 Warehouse | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Db2 on Cloud | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Decision Optimization | ダラスでホスト | ロンドンでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| DevOps Insights | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 使用不可 | 
| Digital Content Checker | ダラスでホスト | ロンドンでホスト | 使用不可 | ロンドンからシンジケート | 使用不可 | 使用不可 | 
| Discovery | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Event Management | ダラスでホスト | ロンドンでホスト | 使用不可 | シドニーでホスト | 使用不可 | 使用不可 | 
| Event Streams | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Functions | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 東京でホスト | 
| Geospatial Analytics | ダラスでホスト | ロンドンでホスト | 使用不可 | ロンドンからシンジケート | 使用不可 | 使用不可 | 
| Globalization Pipeline | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| HPC Cluster | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 
| Historical Instrument Analytics | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Hyper Protect Crypto Services | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Hyper Protect DBaaS | 使用不可 | 使用不可 | 使用不可 | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| IBM Cognos Dashboard Embedded | ダラスでホスト | ロンドンでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| IBM Identity Mixer | 使用不可 | ロンドンでホスト | 使用不可 | シドニーでホスト | 使用不可 | 使用不可 | 
| Information Server | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Informix | ダラスでホスト | ダラスからシンジケート | 使用不可 | ダラスからシンジケート | 使用不可 | 使用不可 | 
| Instrument Analytics | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| インターネット・サービス | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 
| Internet of Things Platform | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 使用不可 | 
| Investment Portfolio | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Key Protect | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Knowledge Catalog | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 東京でホスト | 
| Knowledge Studio | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Language Translator | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Lift CLI | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Log Analysis | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| MQ | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Machine Learning | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 東京でホスト | 
| Managed Financial Data API | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| Master Data Management | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Messages for RabbitMQ | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Mobile Foundation | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Monitoring | ダラスでホスト | ロンドンでホスト | ダラスからシンジケート | シドニーでホスト | 使用不可 | 使用不可 | 
| Natural Language Classifier | ダラスでホスト | 使用不可 | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 東京でホスト | 
| Natural Language Understanding | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Object Storage OpenStack Swift | ダラスでホスト | ロンドンでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Personality Insights | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Portfolio Optimization | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Predictive Market Scenarios | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Push Notifications | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 使用不可 | 
| Real-Time Payments | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| SQL Query | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Secure Gateway | ダラスでホスト | ロンドンでホスト | ダラスからシンジケート | ダラスからシンジケート | ワシントン DC でホスト | 使用不可 | 
| セキュリティー・アドバイザー | ダラスでホスト | ロンドンでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Simulated Historical Instrument Analytics | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Simulated Instrument Analytics | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Simulated Instruments Analytics API | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| Speech to Text | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Streaming Analytics | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| Text to Speech | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Tone Analyzer | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| ツールチェーン | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | ワシントン DC でホスト | 東京でホスト | 
| VMware ソリューション | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 　グローバルにホスト | 
| Visual Recognition | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Voice Agent with Watson | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | ワシントン DC でホスト | 使用不可 | 
| Watson Assistant | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | ワシントン DC でホスト | 東京でホスト | 
| Watson OpenScale | ダラスでホスト | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 使用不可 | 
| Watson Studio | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | 使用不可 | 使用不可 | 東京でホスト | 
| Weather Company Data | ダラスでホスト | ロンドンでホスト | 使用不可 | シドニーでホスト | 使用不可 | 使用不可 | 
| WebSphere Application Server | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
| Workload Scheduler | ダラスでホスト | ロンドンでホスト | フランクフルトでホスト | シドニーでホスト | 使用不可 | 使用不可 | 
{: caption="表 1. サービスの利用可能性" caption-side="top"}

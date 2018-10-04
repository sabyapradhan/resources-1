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


# Resolução de problemas para serviços e recursos
{: #services}

Problemas de serviço do {{site.data.keyword.Bluemix}} podem incluir problemas na exclusão de instâncias de serviço. É possível recuperar desses problemas seguindo algumas etapas fáceis.
{:shortdesc}

## Por que não é possível excluir minha instância de serviço?
{: #ts_service_broker}

Talvez você receba uma mensagem de erro se tentar excluir uma instância de serviço que já tenha sido excluída do controlador de nuvem.
{:shortdesc}

Ao tentar excluir uma instância de serviço, a mensagem de erro a seguir será exibida:
{: tsSymptoms}

`Tempo limite do gateway`

Esse problema ocorrerá se a instância de serviço já tiver sido excluída do controlador de nuvem.
{: tsCauses}

Crie uma instância de serviço com o mesmo nome de serviço e ligue-a a seus aplicativos. Em seguida, será possível excluir a instância de serviço e os aplicativos que usam o serviço.   
{: tsResolve}

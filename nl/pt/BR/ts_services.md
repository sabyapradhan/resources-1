---

copyright:

  years: 2015, 2019

lastupdated: "2019-01-28"

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


# Resolução de problemas para serviços e recursos
{: #services}

Problemas gerais com serviços e recursos podem incluir problemas com a exclusão de instâncias de serviço ou problemas com a migração de serviço. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}

## Por que não é possível excluir minha instância de serviço?
{: #ts_service_broker}
{: troubleshoot}

Talvez você receba uma mensagem de erro se tentar excluir uma instância de serviço que já tenha sido excluída do controlador de nuvem.
{:shortdesc}

Ao tentar excluir uma instância de serviço, a mensagem de erro a seguir será exibida:
{: tsSymptoms}

`Tempo limite do gateway`

Esse problema ocorrerá se a instância de serviço já tiver sido excluída do controlador de nuvem.
{: tsCauses}

Crie uma instância de serviço com o mesmo nome de serviço e ligue-a a seus aplicativos. Em seguida, será possível excluir a instância de serviço e os aplicativos que usam o serviço.   
{: tsResolve}

## Por que uma instância de serviço foi migrada para o grupo de recursos incorreto? 
{: #ts_service_instance}
{: troubleshoot}

Você pode observar que uma instância de serviço foi migrada para o grupo de recursos incorreto e não pode ser redesignada. 
{:shortdesc}

Não é possível mover recursos entre os grupos de recursos após eles serem designados.
{: tsSymptoms}

Você designou a instância ao grupo de recursos incorreto.  
{: tsCauses}

Para corrigir esse problema, é possível tentar excluir a instância e criar uma nova por meio do catálogo. É possível designá-la ao grupo de recursos correto ao criar a nova instância.
{: tsResolve}

## Por que não posso migrar uma instância elegível?
{: #ts_migrate_instance}
{: troubleshoot}

Como um usuário na conta, você está tendo problemas ao migrar uma instância elegível. 
{:shortdesc}

Não é possível migrar uma instância elegível. 
{: tsSymptoms}

Se não for possível migrar uma instância elegível, talvez você não tenha o acesso correto. 
{: tsCauses}

Os usuários devem ter acesso específico para migrar uma instância. Para conferir o acesso que você tem, clique em **Gerenciar** &gt; **Acessar (IAM)** na barra de menus do console e, em seguida, clique em **Usuários**. Clique em seu nome e revise suas políticas de acesso para as funções designadas do IAM e acesso do Cloud Foundry para ver a quais organizações você tem acesso e suas funções designadas do Cloud Foundry. 
{: tsResolve}

## Por que não posso migrar todos os meus serviços?
{: #ts_service_migration}
{: troubleshoot}

Nem todos os serviços são elegíveis para migração. 
{:shortdesc}

Não é possível migrar determinados serviços. 
{: tsSymptoms}

Você está migrando serviços que não estão disponíveis para serem incluídos em grupos de recursos e que não são gerenciados usando o Identity and Access Management (IAM). Se um serviço não for elegível, não haverá uma opção para migração. 
{: tsCauses}

Verifique os serviços para confirmar que eles são elegíveis para migração. Você recebe uma notificação e vê um sinalizador `support_rc_migration` para informar se um serviço é elegível para migração.
{: tsResolve}

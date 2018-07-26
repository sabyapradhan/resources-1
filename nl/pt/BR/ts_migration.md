---

copyright:

  years: 2018

lastupdated: "2018-07-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Resolução de problemas para migração de instâncias de serviço

Se você tiver problemas ao migrar uma instância de serviço do Cloud Foundry para um grupo de recursos, revise os problemas comuns a seguir para ajudá-lo a avançar.

## Uma instância de serviço foi migrada para o grupo de recursos errado

Não é possível mover recursos entre os grupos de recursos após serem designados. Portanto, se você designou uma instância ao grupo de recursos errado, será possível tentar excluir a instância e criar uma nova por meio do catálogo. É possível designá-lo ao grupo de recursos correto ao criar a instância.

## Um usuário na conta não pode migrar uma instância elegível

Talvez o acesso correto não esteja designado a você para migrar uma instância de serviço. Para obter mais informações, consulte [Quem pode migrar instâncias de serviço](/docs/resources/instance_migration.html#whocanmigrate).

## Nenhum serviço é elegível para migração

Nem todos os serviços estão disponíveis para serem incluídos em grupos de recursos e gerenciados usando o Identity and Access Management. Você é notificado quando os serviços são elegíveis, caso você tenha acesso para concluir a tarefa de migração.

---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Resolução de problemas de migração de instâncias de serviço

Se você encontrar problemas ao migrar uma instância de serviço do Cloud Foundry para um grupo de recursos, revise os problemas comuns a seguir para ajudá-lo a avançar com sua migração.

## E se eu migrei minha instância de serviço para o grupo de recursos errado?

No momento, não é possível mover recursos entre grupos de recursos depois que eles são designados. Então, se você migrou uma instância para o grupo de recursos errado, é possível tentar excluir a instância e criar uma nova por meio do catálogo. É possível designá-la ao grupo de recursos correto quando você está criando a instância.

## Por que não posso migrar?

Você pode não ter o acesso correto designado para migrar uma instância de serviço. Veja [Quem pode migrar instâncias de serviço](/docs/account/instance_migration.html#whocanmigrate) para obter mais informações.

## Por que nem todos os meus serviços são elegíveis para migração?

Nem todos os serviços estão disponíveis para serem gerenciados usando o controle de acesso IAM e os grupos de recursos neste momento. Você será notificado quando os serviços ativarem o uso do IAM caso tenha acesso para concluir a tarefa de migração.

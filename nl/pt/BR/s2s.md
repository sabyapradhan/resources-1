---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-06"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Conectando serviços a um app Cloud Foundry
{: #s2s_binding}

Para usar um serviço em um app Cloud Foundry, deve-se criar uma conexão ou ligar esse serviço ao app.
{: shortdesc}

Para conectar um serviço ao seu app iniciando na página de detalhes para um serviço específico, conclua as etapas a seguir:

Também é possível criar conexões do seu app com o serviço. Selecione seu app na lista de recursos, acesse o menu **Conexões** e selecione o serviço.
{: note}

1. Na lista de recursos, clique em **Serviços** e selecione o serviço que você deseja acessar. A página de detalhes do serviço é exibida.
2. Clique em **Conexões** na navegação.
3. Clique em **Criar conexão**.
4. Clique em **Conectar** para a linha do app para o qual você deseja criar a conexão.
5. Selecione uma função de acesso para designar à conexão. Essa função define as ações permitidas que podem ser executadas pelo app acessando o serviço.
6. Opcional: selecione, crie ou gere automaticamente um ID de serviço para o app a ser usado para acessar o serviço. Esse ID de serviço é designado à função de acesso que você selecionou na etapa anterior e, se não selecionar uma opção, uma será gerada.
7. Opcional: inclua parâmetros de configuração no formato JSON.
8. Clique em **Conectar e remontar app**.


Se você desejar restringir o acesso de um app à instância de serviço, clique em **Conexões** na área de janela de navegação e, em seguida, clique em **Desvincular** no menu para o aplicativo conectado para remover a ligação de serviço.
{: tip}

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

# 将服务连接到 Cloud Foundry 应用程序
{: #s2s_binding}

要在 Cloud Foundry 应用程序中使用某个服务，您必须创建与该应用程序的连接或将该服务绑定到该应用程序。
{: shortdesc}

要首先在特定服务的详细信息页面中将服务连接到应用程序，请完成以下步骤：

您还可以创建从应用程序到服务的连接。从资源列表中选择应用程序，转至**连接**菜单，然后选择服务。
{: note}

1. 在资源列表上，单击**服务**，然后选择要访问的服务。这将显示服务详细信息页面。
2. 在导航中单击**连接**。
3. 单击**创建连接**。
4. 对于要为其创建连接的应用程序所在行，单击**连接**。
5. 选择要分配的对连接的访问角色。此角色定义访问服务的应用程序可以执行的允许操作。
6. 可选：选择、创建或自动生成应用程序用于访问服务的服务标识。将为此服务标识分配在上一步中选择的访问角色，如果未选择选项，将生成访问角色。
7. 可选：以 JSON 格式添加配置参数。
8. 单击**连接并重新编译打包应用程序**。


如果要限制应用程序对服务实例的访问权，请单击导航窗格中的**连接**，然后在已连接的应用程序的菜单中单击**取消绑定**来除去服务绑定。
{: tip}

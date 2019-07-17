---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-28"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Terminais em serviço para conexões de rede privada
{: #service-endpoints}

Um foco maior na segurança é necessário para clientes que usam serviços baseados em
nuvem para cargas de trabalho de produção. Para muitos clientes, o acesso aos serviços de
uma maneira segura não é apenas uma política corporativa sensata, mas em alguns casos
exigido por regulamentações de conformidade. O {{site.data.keyword.IBM_notm}}
aprimorou as opções de conectividade para clientes que requerem opções de conectividade
isoladas para suas cargas de trabalho. 

Com os terminais em serviço do {{site.data.keyword.cloud}}, é possível se
conectar aos serviços {{site.data.keyword.cloud_notm}} por meio da rede privada
do {{site.data.keyword.cloud_notm}}. Mover estas cargas de trabalho da rede
pública oferece duas vantagens:

* Os serviços não são mais entregues em um endereço IP da Internet roteável. Ele
está se tornando cada vez mais comum para os consumidores de nuvem que desejam acesso
limitado ou nenhum acesso à Internet pública de qualquer um de seus serviços. Agora, com
o recurso de terminal em serviço, as equipes de serviço podem criar uma interface sobre a
rede privada para seu serviço que os clientes podem usar para se conectar. O acesso à
Internet não é mais um requisito para que você se conecte aos serviços do
{{site.data.keyword.cloud_notm}}.
* Não há encargos de largura de banda faturáveis ou medidos na rede privada. No
passado, você era cobrado por largura da banda egressa ao falar com um serviço
{{site.data.keyword.cloud_notm}} . 

A figura a seguir mostra como o tráfego é roteado por meio da rede privada do
{{site.data.keyword.cloud_notm}} ao acessar serviços de nuvem por meio de
terminais em serviço:

![Terminal em serviço do IBM Cloud](images/CSE.png "Tráfego sendo roteado por meio de um terminalem serviço")


Para usar os terminais em serviço do {{site.data.keyword.cloud_notm}},
deve-se ativar o roteamento virtual e o encaminhamento (VRF) em sua conta. Em seguida, é
possível ativar o uso de terminais em serviço. Após ambas as opções serem ativadas, é
possível iniciar a criação de serviços que suportam o uso de VRF e de terminais em
serviço a partir do catálogo. Para obter mais informações, consulte
[Ativando o VRF e os
terminais em serviço](/docs/account?topic=account-vrf-service-endpoint).

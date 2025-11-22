# Passo-a-passo para criar um Agent

## Pré-requisitos
✔️ Conta ativa no **Azure** free: https://portal.azure.com/<br>
✔️ Conta ativa no **Azure AI Foundry**: https://ai.azure.com/<br>
✔️ Criar um **Resource Group**

## Criando um Resoure Group
1. Entre no https://portal.azure.com/ e faça o login.
2. Selecione **Resources Groups (Resource Manage)** no menu Show portal menu lateral à esquerda.
3. Clicar em **+ Create** no menu central da página.
4. Preencher:<br>
   •	**Subscription:** selecione sua assinatura<br>
   •	**Resource group name:** `rg-challenge-afg`<br>
   •	**Region:** `(Europe) Sweden Central`<br>
5. Clicar no botão **Review + create -> Create** no menu inferior da página. 

## Criando um Projeto
1.	Clicar no **resource group:** rg-challenge-afg
2.	Clicar em **+ Create** no menu central da página.
3.	Na barra de pesquisa digitar: **AI Foundry**.
4.	No **AI Foundry** clicar no botão **Create -> Microsoft Foundry**.
5.	Preencher:<br>
  • **Subscription:** selecione sua assinatura<br>
  • **Resource group name:** `rg-challenge-afg`<br>
  • **Name:** `rg-challenge-afg`<br>
  • **Region:** `(Europe) Sweden Central`<br>
  • **Default project name:** `proj-challenge-afg`<br>
6.	Clicar no botão **Next** no menu inferior da página. 
7.	Selecionar: **All networks, including the internet, can access this resource -> Next** no menu inferior da página. 
8.	Clicar no botão **Next** no menu inferior da página.
9.	Clicar no botão **Next** no menu inferior da página.
10.	Clicar no botão **Next** no menu inferior da página.
11.	Clicar no botão **Create** no menu inferior da página

## Criando Models + endpoints
1. Entre no https://ai.azure.com/ e faça o login.
2. Clicar em **Models + endpoints** no menu lateral esquerdo da página
3. Clicar em **+ Deploy model -> Deploy bade model** no menu central da página.
4. Na barra de pesquisa digitar: **`gpt-4.1-mini`**.<br>
5. Selecionar **gpt-4.1-mini -> confirm**

## Criando um Agente
1. Entre no https://ai.azure.com/ e faça o login.
2. Clicar em **Go to Azure AI Foundry** portal no menu central da página
 <p align="center">
<img src="prints/Create Agent/createAgent_1.jpg" width="700">
</p>

3. Selecione **Agents** no menu lateral à esquerda. 
<p align="center">
<img src="prints/Create Agent/createAgent_2.jpg" width="700">
</p>

4. Clicar em **+ New agent** no menu central de configuração **Create and debug your agents**.
 <p align="center">
<img src="prints/Create Agent/createAgent_3.jpg" width="700">
</p>

5. Preencher os campos na tela de configuração do **model em Setup** na lateral direita:<br>
   •	**Agent name:** `TravelSuggestions`<br> 
   •	**Deployment:** `gpt-4.1-mini (version:2025-04-14)`<br>
   •	**Instructions:**
       Você é um agente especializado em viagens nacionais e internacionais.
       Sua função é recomendar uma lista das melhores cidades e países para viajar considerando:<br>
           • Clima ideal<br>
           • Preferências opcionais do usuário (praia, frio, barato, cultura)<br>
           • Eventos culturais e festivais no destino<br>
           • Temporada de preços (alta, média, baixa)<br>
           • Segurança e facilidade de viagem<br>
           • Melhor mês<br>
Para obter informações, utilize as ferramentas configuradas (clima, eventos, pesquisas, preços).<br>
Regras:
    1. Se o usuário informar um MÊS → sugira 5–10 destinos adequados naquele mês.
    2. Se o usuário informar um LUGAR → sugira destinos semelhantes ou complementares ao perfil do lugar.
    3. Se o usuário informar um Clima → sugira destinos semelhantes ou complementares ao perfil do clima/temperatura.
    4. Se o usuário informar ambos → filtre destinos que combinem com o mês, com o estilo do lugar e o clima/ temperatura.
    5. Sempre explique por que está sugerindo cada destino.
    6. Alternativas econômicas
    7. Aviso (chuva, época de tornados, furacões, monções, frio extremo etc.)
    8. Responda sempre de forma clara, organizada e objetiva.
    9. Você não responde perguntas sobre qualquer outro assunto. Você só retorna a pesquisa somente se for sobre viagem
**Agent Description:**
O agente faz uma pesquisa de melhores meses ou locai para viajar de acordo com os dados inseridos pelo usuário, retornando as informações dos melhores meses ou locais para viajar.
 <p align="center">
<img src="prints/Create Agent/createAgent_4.jpg" width="700">
</p>

6.	Preencher o campo na tela de configuração do **model em Setup** na lateral direita:<br>
	• **Model Settings ->** Temperature: 0.3
 <p align="center">
<img src="prints/Create Agent/createAgent_5.jpg" width="700">
</p>

## Adicionando Actions:
1.	Clicar em **Action -> + Add** na tela de **configuração do model em Setup** na lateral direita.
<p align="center">
<img src="prints/Add actions/actionsAddt_1.jpg" width="700">
</p>
 
2.	Clicar em **Azure Logic Apps** na tela de **Add action** na lateral direita.  
<p align="center">
<img src="prints/Add actions/actionsAddt_2.jpg" width="700">
</p>

3.	Clicar em **Call external HTTP or HTTPS endpoints** na tela de **Add Logic Add action** na lateral esquerda.
 <p align="center">
<img src="prints/Add actions/actionsAddt_3.jpg" width="700">
</p>

4.	Preencher os campos **Your action name -> Your action description ->** Clicar no botão **Next** na tela de **Add Logic Add action** na lateral esquerda.
 <p align="center">
<img src="prints/Add actions/actionsAddt_4.jpg" width="700">
</p>

5.	Selecionar no campo **Value: GET ->** Clicar no botão **Next** na tela de **Add Logic Add action** na lateral esquerda.
 <p align="center">
<img src="prints/Add actions/actionsAddt_5.jpg" width="700">
</p>

6.	Selecionar checklist **I acknowledge that connecting to an Azure Logic Apps service will incur additional costs to my account ->** Clicar no botão **Next** na tela de **Add Logic Add action** na lateral esquerda.
<p align="center">
<img src="prints/Add actions/actionsAddt_6.jpg" width="700">
</p>
 
7.	Clicar no botão **Create** na tela de **Add Logic Add action** na lateral direita.
 <p align="center">
<img src="prints/Add actions/actionsAddt_7.jpg" width="700">
</p>

**⬅️ [Voltar ao README principal](../README.md)**


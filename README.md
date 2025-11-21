# :airplane: TravelSuggestions 
O Agente de Pesquisa de Destinos de Viagem é uma solução inteligente desenvolvida utilizando o Azure AI Foundry, com o objetivo de oferecer recomendações personalizadas de destinos turísticos com base em informações fornecidas pelo usuário, como mês da viagem, local de referência, orçamento ou preferências específicas.

## 🎯 Objetivos do Projeto
Criar um agente inteligente capaz de recomendar destinos de viagem com precisão e contexto, usando IA generativa e dados externos.<br>
- [x] Feito Analisar informações fornecidas pelo usuário (mês, destino, preferências).<br>
- [x] Feito	Recomendar destinos adequados com base em clima, temporada e atividades.<br>
- [x] Feito	Integrar-se a APIs externas de:<br>
  *	clima em tempo real,<br>
  *	preços,<br>
  *	eventos e atividades.<br>
- [x] Feito	Oferecer explicações claras e orientações de planejamento.<br>

## ❗ Problema que o Projeto Resolve
Viajar exige planejamento cuidadoso. Muitos viajantes acabam escolhendo um destino para viajar com base somente nos preços. Pois muitas vezes os preços são muito atraentes em determinados meses para alguns países, mas são época de tornados, furacões, tsunâmis, chuvas, etc.<br>
Muitos não sabem:
*	quais destinos são melhores em cada mês;
*	quais locais têm melhor clima na época desejada;
* onde há eventos ou festivais interessantes;
* qual é o custo médio da viagem;
* alternativas semelhantes ao destino desejado.

## Solução
O projeto resolve esse problema ao oferecer um agente conversacional inteligente, capaz de entregar recomendações contextualizadas e atualizadas.

## 🧩 Recursos do Agente
✔️ Recomendação de destinos com base no perfil do usuário
✔️ Sugestão de roteiros personalizados
✔️ Estimativa de custos de viagem
✔️ Informações sobre clima, atrações e transporte
✔️ Suporte a múltiplos idiomas
✔️ Extensível com ferramentas (APIs externas, bancos de dados etc.)

## 🧠 Tecnologias Utilizadas
✔️ Azure AI Foundry<br>
✔️ Azure OpenAI Service<br>
✔️ Modelos GPT e Chat Completions<br>
✔️ Azure Functions / Logic Apps (opcional)
✔️ Python / JavaScript (dependendo da implementação)<br>
✔️ APIs externas (ex.: clima, preços de passagens)<br>

## 🏗️: Arquitetura
Usuário → Agente de Viagens (Azure AI Foundry)
             ↓
        Ferramentas/Plugins
   - API de clima
   - API de destinos
   - Banco de dados de viagens
             ↓
        Resposta personalizada

## Como Executar o Projeto
1️⃣ Pré-requisitos<br>
✅ Conta no Azure<br>
✅ Acesso ao Azure AI Foundry<br>
✅ Node.js ou Python instalado (dependendo do código)<br>
✅ Chave e endpoint do Azure AI<br>

## Criando um Agent

<p align="center">
  <img src="docs/prints/Add actions/actionsAdd_1.jpg" width="400">
</p>



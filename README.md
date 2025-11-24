# 🤖 AI-WA: Agente Inteligente WhatsApp com Gemini (Solução Proprietária)

## ✨ Visão Geral da Plataforma

**AI-WA** (Agente Inteligente WhatsApp) é uma solução *custom-built* de automação de atendimento ao cliente, projetada para ser uma alternativa robusta e de **custo otimizado** aos Provedores de Solução de Negócios (BSPs) tradicionais.

Utilizando a **Meta Cloud API** (conexão oficial) e a **Gemini API** (Google), a plataforma garante máxima escalabilidade e controle total sobre o fluxo de dados e lógica de negócios.

### Foco Estratégico:

* **Economia Operacional:** Redução drástica dos custos por token e por conversa.
* **Controle Total:** Ausência de dependência de plataformas intermediárias.
* **Inteligência de Ponta:** Utilização da IA Generativa do Gemini para respostas contextuais e personalizadas.

---

## 🚀 Funcionalidades e Design

O projeto foi arquitetado com uma lógica de **Middleware em Python** que atua como o motor de decisão, garantindo que o Agente de IA seja acionado apenas em cenários de alta complexidade.

| Recurso | Descrição | Valor Agregado |
| :--- | :--- | :--- |
| **IA Principal** | **Gemini API** (`gemini-2.5-flash`) | Raciocínio rápido e natural para atendimento de cauda longa e intenções ambíguas. |
| **Memória de Sessão** | Google Cloud Firestore / Redis | Armazenamento persistente do histórico de conversas para manter o contexto. |
| **Handoff Inteligente** | Lógica de Transbordo Humano | O middleware identifica falhas do bot ou pedidos de intervenção humana e realiza o escalonamento. |
| **Tool Use (Function Calling)** | Estrutura Proprietária de Chamadas | Capacidade do Agente de interagir com APIs externas (ex: CRM, ERP do cliente) para executar ações em tempo real. |
| **Filtro de Custo** | Middleware em Python | Filtro inicial que identifica mensagens simples ("Oi", "Obrigado") e responde de forma estática, **evitando o consumo de tokens** para interações básicas. |

---

## 🏗️ Arquitetura do Sistema (Serverless)

A arquitetura se baseia em um fluxo de **Webhook** acionado pela Meta, garantindo que o sistema pague apenas pelo uso (serverless), sem custos fixos de servidor.



**Componentes Chave da Stack:**

* **Linguagem de Desenvolvimento:** Python (Flask/FastAPI).
* **Hospedagem:** Google Cloud Run / Cloud Functions (Serverless).
* **Mensageria:** Meta Cloud API.
* **Inteligência:** Gemini API.
* **Persistência:** Google Cloud Firestore / Redis.

---

## 💡 Estratégia de Otimização de Custos

O projeto foi concebido sob três pilares de economia:

1.  **API Direta:** Uso da Meta Cloud API para eliminar margens de lucro de BSPs.
2.  **Token Minimalista:** Utilização estratégica do modelo `gemini-2.5-flash` e limitação rigorosa da janela de contexto (histórico) para reduzir o consumo de tokens.
3.  **Serverless:** Hospedagem em serviços *pay-per-use*, garantindo que os custos de infraestrutura sejam mínimos e variáveis de acordo com a demanda.

---

## 🔑 Credenciais e Ambiente

A solução requer integração de APIs robustas. O código é configurado via variáveis de ambiente para acesso seguro e dinâmico às seguintes plataformas:

* **Meta Cloud API** (Token de Acesso e IDs de Telefone).
* **Gemini API** (Chave de Acesso Principal).
* **GCP/Firebase** (Credenciais de Serviço para Firestore/Redis).

---

## 📄 Conclusão

O **AI-WA** representa a próxima geração de atendimento ao cliente no WhatsApp: altamente inteligente, escalável e construído com um foco inigualável na eficiência de custos.
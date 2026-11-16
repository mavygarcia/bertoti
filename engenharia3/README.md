# Engenharia 3, Contribuições:


Este documento apresenta minhas principais contribuições nos projetos desenvolvidos na disciplina de Engenharia 3, contemplando o projeto de Design Patterns e o desenvolvimento da API.

---

## 1. Projeto de Design Patterns

Fiquei responsável pela criação de clientes e pedidos fictícios para utilização nos testes do projeto. Também desenvolvi consultas ao CRM simulado, permitindo que o agente de IA recuperasse informações sobre os clientes e seus pedidos.

Além disso, trabalhei na criação de uma base de conhecimento contendo perguntas frequentes e políticas de reembolso, na implementação do histórico de conversas por cliente e na integração das informações recuperadas ao contexto enviado ao modelo de IA.

**Principais classes relacionadas às minhas contribuições:**

- `Customer`
- `Order`
- `CrmService`
- `KnowledgeBaseService`
- `ConversationMemoryService`

**Resultado:** Com essas implementações, o agente consegue consultar dados simulados e utilizar o histórico de cada cliente para fornecer respostas mais contextualizadas.

---

## 2. Desenvolvimento da API

Fiquei responsável pela criação e estruturação do banco de dados da aplicação, utilizando **PostgreSQL** e a extensão **pgvector**. Desenvolvi a estrutura das entidades e seus relacionamentos, incluindo usuários, projetos e documentos, preparando a base para atender às funcionalidades da API.

Também trabalhei na implementação de rotas para cadastro e listagem de projetos, incluindo validações, e na exposição do estado de login (ativo ou desativado) nas rotas de gestão.

Além do desenvolvimento, realizei testes dos fluxos de análise de rascunhos no chat e dos alertas de similaridade, contribuindo para validar o funcionamento dessas funcionalidades.

**Principais atividades realizadas:**

- Criação e estruturação do banco de dados utilizando PostgreSQL e pgvector.
- Modelagem da entidade de usuário.
- Modelagem da entidade de projeto e implementação das rotas de cadastro e listagem com validações.
- Modelagem da entidade de documento.
- Exposição do estado de login (ativo/desativado) nas rotas de gestão.
- Testes do fluxo de análise de rascunhos no chat.
- Testes do fluxo de alertas de similaridade.

**Resultado:** Minhas contribuições envolveram desde a criação da estrutura do banco de dados até a implementação e validação de funcionalidades da API.

---

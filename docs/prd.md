### 📄 3. `docs/prd.md`

```markdown
# 📄 Product Requirements Document (PRD) - Ultra Legacy

## 1. Visão Geral e Objetivo

O **Ultra Legacy** é uma aplicação web didática que simula as operações básicas de agendamento de serviços de estética automotiva (abertura de conta, seleção de serviços, aplicação de descontos e histórico de serviços).

**O grande diferencial (Regra de Negócio Principal):** A Ultra Legacy oferece um **Desconto Fidelidade automático de 10%** para qualquer serviço automotivo agendado no sistema, garantindo um benefício direto ao cliente em todas as operações efetuadas.

## 2. Atores do Sistema

- **Visitante:** Usuário não autenticado que acessa a página inicial e deseja se cadastrar.
- **Cliente:** Usuário autenticado que deseja agendar um serviço automotivo ou consultar seus agendamentos anteriores.
- **A Oficina (Sistema):** Ator invisível que aplica as regras de negócio e calcula o desconto fidelidade automaticamente a cada agendamento.

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (Minimum Viable Product), escritas sob a perspectiva do usuário final.

### 👤 Épico 1: Autenticação e Cadastro

- **US01 - Cadastro de Cliente:** Como um Visitante, quero preencher um formulário com meus dados pessoais (Nome, CPF, Telefone, Senha) para criar uma nova conta na Ultra Legacy.
  - _Critérios de Aceitação:_ O CPF e Telefone devem ser validados; todos os campos são obrigatórios.
- **US02 - Acesso ao Sistema (Login):** Como um Cliente, quero inserir meu CPF e Senha para acessar meu painel de agendamentos.

### 🚗 Épico 2: Agendamento de Serviços

- **US03 - Visualização de Serviços:** Como um Cliente logado, quero ver o catálogo de serviços disponíveis e seus respectivos preços de tabela.
- **US04 - Realizar Agendamento:** Como um Cliente, quero selecionar um serviço e uma data para agendar o atendimento do meu veículo.
  - _Critérios de Aceitação:_ O sistema deve aplicar automaticamente o **"Desconto Fidelidade" de 10%** sobre o valor original do serviço e exibir o valor líquido final a ser pago.

### 📊 Épico 3: Histórico e Acompanhamento

- **US05 - Visualizar Meus Agendamentos:** Como um Cliente, quero visualizar uma lista (tabela ou cards) com o histórico de todos os meus agendamentos.
  - _Critérios de Aceitação:_ A lista deve mostrar a data, o serviço agendado, o valor bruto, **o valor do desconto aplicado** e o valor total cobrado.

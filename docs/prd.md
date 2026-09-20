# 📄 Product Requirements Document (PRD) - Ultra Legacy

## 1. Visão Geral e Objetivo

A **Ultra Legacy** é uma aplicação web desenvolvida para uma estética automotiva que oferece serviços como lavagem, polimento, higienização e proteção de pintura.

O sistema tem como objetivo organizar o relacionamento com os clientes, permitindo o cadastro de clientes e veículos, gerenciamento de serviços e agendamentos, além da consulta de informações e valores de referência de veículos por meio da **FIPE API**.

A aplicação busca substituir controles manuais realizados por papel ou planilhas, facilitando o acesso às informações dos clientes, veículos, serviços e histórico de atendimentos.

**Objetivo principal:** centralizar o gerenciamento de clientes, veículos, serviços e agendamentos em uma única aplicação web.

---

## 2. Atores do Sistema

* **Visitante:** Usuário não autenticado que acessa o site institucional para conhecer a Ultra Legacy, visualizar serviços, preços e entrar em contato ou realizar seu cadastro.

* **Cliente Autenticado:** Usuário cadastrado e autenticado que pode gerenciar seus veículos, visualizar serviços, solicitar agendamentos e consultar seu histórico de serviços.

* **Administrador/Funcionário:** Responsável pelo gerenciamento dos clientes, veículos, serviços e agendamentos da estética automotiva, além de realizar consultas de veículos e acompanhar as informações da operação.

---

## 3. Histórias de Usuário e Escopo

Abaixo estão as principais funcionalidades do sistema, organizadas de acordo com as necessidades dos usuários da aplicação.

### 👤 Épico 1: Autenticação e Conta

* **US01 - Cadastro de Cliente:** Como um Visitante, quero preencher um formulário com meus dados pessoais, como nome, e-mail e senha, para criar uma conta na Ultra Legacy.

  * *Critérios de Aceitação:* Os campos obrigatórios devem ser preenchidos corretamente e o e-mail deve possuir formato válido.

* **US02 - Acesso ao Sistema:** Como um Cliente, quero informar meu e-mail e senha para acessar minha área restrita.

* **US03 - Encerramento da Sessão:** Como um Cliente autenticado, quero realizar logout para encerrar meu acesso à área restrita.

* **US04 - Atualização dos Dados:** Como um Cliente autenticado, quero editar meus dados pessoais, como telefone e e-mail, para manter meu cadastro atualizado.

---

### 🚗 Épico 2: Cadastro e Gerenciamento de Veículos

* **US05 - Cadastro de Veículo:** Como um Cliente autenticado, quero cadastrar um veículo informando seus dados, para vinculá-lo à minha conta.

* **US06 - Consulta de Veículo:** Como um Cliente autenticado, quero consultar informações de um veículo utilizando tipo, marca, modelo e ano, para visualizar seus dados e seu valor de referência na Tabela FIPE.

* **US07 - Edição de Veículo:** Como um Cliente autenticado, quero editar os dados de um veículo já cadastrado, para corrigir ou atualizar suas informações.

* **US08 - Exclusão de Veículo:** Como um Cliente autenticado, quero excluir um veículo do meu cadastro, para remover veículos que não utilizo mais.

* **US09 - Lista de Veículos:** Como um Cliente autenticado, quero visualizar todos os meus veículos cadastrados, para ter uma visão geral dos veículos associados à minha conta.

* **US10 - Consulta de Veículo pelo Administrador:** Como um Administrador, quero consultar informações de veículos pela FIPE API, para obter dados de referência durante o atendimento.

---

### 🧽 Épico 3: Serviços e Agendamentos

* **US11 - Visualização de Serviços:** Como um Cliente autenticado, quero visualizar os serviços oferecidos pela Ultra Legacy, com suas respectivas descrições e preços, para escolher o serviço que desejo contratar.

* **US12 - Solicitação de Agendamento:** Como um Cliente autenticado, quero solicitar um agendamento para um dos meus veículos, informando data e horário desejados, para reservar um atendimento.

* **US13 - Histórico de Serviços:** Como um Cliente autenticado, quero visualizar o histórico de serviços realizados em cada veículo, para acompanhar os atendimentos realizados.

* **US14 - Visualização de Agendamentos:** Como um Administrador, quero visualizar os agendamentos pendentes, para organizar a agenda da estética.

* **US15 - Gerenciamento de Agendamentos:** Como um Administrador, quero confirmar, remarcar ou cancelar um agendamento, para administrar os atendimentos da empresa.

* **US16 - Conclusão de Serviço:** Como um Administrador, quero registrar a conclusão de um serviço realizado em um veículo, para manter o histórico de atendimento atualizado.

---

### 👥 Épico 4: Gestão de Clientes e Veículos

* **US17 - Lista de Clientes:** Como um Administrador, quero visualizar todos os clientes cadastrados, para ter controle da base de clientes.

* **US18 - Pesquisa de Cliente:** Como um Administrador, quero pesquisar um cliente pelo nome ou pelas informações do veículo, para localizá-lo rapidamente durante o atendimento.

* **US19 - Cadastro de Veículo pelo Administrador:** Como um Administrador, quero cadastrar um veículo em nome de um cliente diretamente no atendimento, para atender clientes que chegam sem agendamento prévio.

* **US20 - Consulta FIPE:** Como um Administrador, quero consultar informações de um veículo utilizando a FIPE API, para obter informações como marca, modelo, ano e valor de referência.

---

### 🌐 Épico 5: Site Institucional

* **US21 - Página Inicial:** Como um Visitante, quero visualizar a página inicial com a apresentação da Ultra Legacy, para conhecer a empresa e seus serviços.

* **US22 - Página de Serviços:** Como um Visitante, quero visualizar os serviços oferecidos pela Ultra Legacy, com descrições e preços, para conhecer as opções disponíveis.

* **US23 - Formulário de Contato:** Como um Visitante, quero preencher um formulário de contato, para tirar dúvidas ou solicitar informações sobre os serviços.

* **US24 - Gerenciamento de Mensagens:** Como um Administrador, quero visualizar as mensagens enviadas pelo formulário de contato, para responder aos interessados.

---

### 📊 Épico 6: Recursos Complementares

* **US25 - Confirmação de Ações:** Como um Cliente autenticado, quero receber uma mensagem visual de sucesso ao cadastrar um veículo ou solicitar um agendamento, para saber que a ação foi concluída.

* **US26 - Dashboard Administrativo:** Como um Administrador, quero visualizar um painel com informações gerais, como quantidade de clientes, veículos e agendamentos do dia, para acompanhar rapidamente a situação da estética.

---

## 4. Mapeamento com os Indicadores de Desempenho (ID)

As funcionalidades da Ultra Legacy serão utilizadas para atender aos 24 Indicadores de Desempenho exigidos pela disciplina.

| ID    | Como será atendido no projeto                                                                                                                                             |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ID 01 | Prototipar no Stitch as telas mobile e desktop da Home, Serviços, Cadastro de Veículo e Área do Cliente.                                                                  |
| ID 02 | Utilizar Bootstrap, com Grid e Flexbox do framework, para construir o layout responsivo.                                                                                  |
| ID 03 | Utilizar Flexbox ou Grid CSS puro em componentes específicos da aplicação.                                                                                                |
| ID 04 | Utilizar componentes Bootstrap como cards, buttons, modal e carousel.                                                                                                     |
| ID 05 | Utilizar `%`, `rem`, `vw` e `vh` para desenvolver um layout fluido.                                                                                                       |
| ID 06 | Utilizar um Design System com paleta de cores, tipografia e padrões visuais consistentes.                                                                                 |
| ID 07 | Utilizar Sass (SCSS), com variáveis e mixins para organização dos estilos.                                                                                                |
| ID 08 | Aplicar tipografia responsiva utilizando media queries ou `clamp()`.                                                                                                      |
| ID 09 | Utilizar `object-fit` e containers responsivos para imagens de veículos e serviços.                                                                                       |
| ID 10 | Utilizar imagens em formatos modernos, como WebP, e técnicas como `srcset` ou `picture`.                                                                                  |
| ID 11 | Utilizar validação HTML nativa nos formulários de cliente, veículo, contato e agendamento.                                                                                |
| ID 12 | Utilizar REGEX para validação de e-mail, telefone e placa de veículo.                                                                                                     |
| ID 13 | Utilizar `select`, `radio` e `checkbox` para coleta de informações nos formulários.                                                                                       |
| ID 14 | Utilizar `localStorage` para armazenar informações como última consulta de veículo e rascunhos de formulários.                                                            |
| ID 15 | Configurar Node.js e NPM para gerenciamento das dependências do projeto.                                                                                                  |
| ID 16 | Utilizar Git/GitHub, branches e `.gitignore` para controle de versão.                                                                                                     |
| ID 17 | Manter o `README.md` padronizado com o checklist dos 24 IDs.                                                                                                              |
| ID 18 | Organizar o projeto de forma modular, utilizando pastas como `docs/`, `src/pages/`, `src/styles/`, `src/scripts/` e `src/assets/`.                                        |
| ID 19 | Configurar ESLint e Prettier para padronização e qualidade do código.                                                                                                     |
| ID 20 | Utilizar jQuery para manipulação do DOM e interações da aplicação.                                                                                                        |
| ID 21 | Utilizar um plugin jQuery relevante, como jQuery Mask, para auxiliar na formatação de campos.                                                                             |
| ID 22 | Utilizar JSON Server como API Fake para persistir dados de clientes, veículos e agendamentos.                                                                             |
| ID 23 | Utilizar JSON Server para consultar e exibir dados de serviços e agendamentos.                                                                                            |
| ID 24 | Utilizar uma API pública real, a FIPE API, para consultar informações e valores de referência de veículos, realizando requisições assíncronas e tratando possíveis erros. |

---

## 5. Escopo do MVP

A primeira versão funcional do sistema deverá contemplar:

* Cadastro e autenticação de clientes;
* Cadastro e gerenciamento de veículos;
* Consulta de veículos utilizando a FIPE API;
* Cadastro e visualização de serviços;
* Solicitação de agendamentos;
* Gerenciamento de agendamentos;
* Histórico de serviços;
* Área administrativa;
* Site institucional;
* Formulário de contato;
* Persistência de dados utilizando JSON Server;
* Armazenamento auxiliar utilizando `localStorage`;
* Interface responsiva para dispositivos móveis e desktop.

# 📄 PRD — Ultra Legacy

## 1. Visão Geral

O **Ultra Legacy** é um sistema web para gerenciamento de uma empresa de estética automotiva.

O sistema permitirá controlar clientes, veículos, serviços e agendamentos, além de consultar informações de veículos através da FIPE API.

## 2. Atores

### Visitante

* Visualizar empresa e serviços;
* Acessar contato;
* Realizar cadastro.

### Cliente

* Gerenciar seus dados;
* Cadastrar e gerenciar veículos;
* Consultar veículos;
* Visualizar serviços;
* Solicitar agendamentos;
* Consultar histórico.

### Administrador/Funcionário

* Gerenciar clientes;
* Gerenciar veículos;
* Gerenciar serviços;
* Gerenciar agendamentos;
* Consultar veículos;
* Visualizar mensagens e informações do sistema.

## 3. Principais Funcionalidades

### Clientes

* Cadastro;
* Login e logout;
* Edição de dados.

### Veículos

* Cadastro;
* Listagem;
* Edição;
* Exclusão;
* Consulta de informações pela FIPE API.

### Serviços

* Listagem de serviços;
* Preços e informações.

### Agendamentos

* Solicitação;
* Confirmação;
* Reagendamento;
* Cancelamento;
* Conclusão;
* Histórico.

### Administração

* Clientes;
* Veículos;
* Agendamentos;
* Mensagens de contato;
* Dashboard.

## 4. FIPE API

A consulta seguirá:

```text
Tipo → Marca → Modelo → Ano → Dados do veículo
```

A placa será utilizada como identificação do veículo no sistema, mas não será consultada diretamente na FIPE API.

## 5. Interface

O sistema deverá ser responsivo para:

* Celulares;
* Tablets;
* Computadores.

O **Bootstrap 5.3.3** será utilizado para Grid, Flexbox e componentes da interface.

## 6. MVP

A primeira versão deverá possuir:

* Cadastro de clientes;
* Cadastro de veículos;
* Consulta FIPE;
* Serviços;
* Agendamentos;
* Histórico;
* Área administrativa;
* Formulário de contato;
* Interface responsiva.

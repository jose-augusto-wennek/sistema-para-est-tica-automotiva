# PRD - Product Requirements Document

## 1. Identificação

- **Nome do aluno:** [Jose Augusto Wennek Fiuza]
- **Nome do projeto:** Ultra Legacy

## 2. Descrição

A **Ultra Legacy** é uma estética automotiva (lavagem, polimento, higienização, proteção de pintura, etc.) que precisa de um sistema web para organizar o relacionamento com seus clientes. Atualmente o controle de veículos e serviços é feito de forma manual (papel/planilha), o que causa perda de histórico, dificuldade em identificar rapidamente o veículo de um cliente e retrabalho no atendimento.

O sistema resolve esse problema permitindo que a estética **cadastre clientes e seus veículos**, **consulte automaticamente dados do veículo a partir da placa** (via API de consulta veicular), e **gerencie os serviços/agendamentos** prestados a cada carro, mantendo um histórico completo por cliente.

## 3. Atores do Sistema

| Ator | Descrição |
|---|---|
| **Visitante** | Usuário não autenticado que navega pelo site institucional (serviços, preços, contato) e pode se cadastrar. |
| **Cliente Autenticado** | Usuário logado que cadastra seus próprios veículos, acompanha o histórico de serviços e solicita agendamentos. |
| **Administrador/Funcionário** | Responsável por gerenciar clientes, veículos, serviços, agendamentos e consultar dados via API de placas. |

## 4. Histórias de Usuário (Escopo)

### Autenticação e Conta
1. Como Visitante, quero me cadastrar informando nome, e-mail e senha, para me tornar Cliente Autenticado.
2. Como Cliente Autenticado, quero fazer login e logout, para acessar minha área restrita com segurança.
3. Como Cliente Autenticado, quero editar meus dados pessoais (telefone, e-mail), para manter meu cadastro atualizado.

### Cadastro de Veículos
4. Como Cliente Autenticado, quero cadastrar um veículo informando a placa, para vincular meu carro à minha conta.
5. Como Cliente Autenticado, quero que o sistema busque automaticamente marca, modelo, ano e cor do veículo a partir da placa (via API de placas), para não precisar digitar tudo manualmente.
6. Como Cliente Autenticado, quero editar os dados de um veículo já cadastrado, para corrigir informações incorretas.
7. Como Cliente Autenticado, quero excluir um veículo do meu cadastro, para remover carros que não uso mais.
8. Como Cliente Autenticado, quero listar todos os meus veículos cadastrados, para ter uma visão geral da minha garagem.

### Serviços e Agendamentos
9. Como Cliente Autenticado, quero visualizar a lista de serviços oferecidos (ex: lavagem simples, polimento, vitrificação), com descrição e preço, para escolher o que contratar.
10. Como Cliente Autenticado, quero solicitar um agendamento de serviço para um dos meus veículos, informando data e horário desejado, para reservar um atendimento.
11. Como Cliente Autenticado, quero visualizar o histórico de serviços já realizados em cada veículo, para acompanhar a manutenção estética do carro.
12. Como Administrador, quero visualizar todos os agendamentos pendentes, para organizar a agenda da estética.
13. Como Administrador, quero confirmar, remarcar ou cancelar um agendamento, para gerenciar a operação do dia a dia.
14. Como Administrador, quero registrar a conclusão de um serviço em um veículo, para manter o histórico atualizado.

### Gestão de Clientes e Veículos (Administrador)
15. Como Administrador, quero listar todos os clientes cadastrados, para ter controle da base de clientes.
16. Como Administrador, quero pesquisar um cliente pelo nome ou pela placa do veículo, para localizá-lo rapidamente no atendimento.
17. Como Administrador, quero cadastrar um veículo em nome de um cliente diretamente no balcão, para atender clientes que chegam sem agendamento prévio.
18. Como Administrador, quero consultar os dados de uma placa a qualquer momento (mesmo sem vínculo com cadastro), para conferir informações de um veículo na hora do atendimento.

### Site Institucional
19. Como Visitante, quero ver a página inicial com a apresentação da Ultra Legacy, para conhecer a empresa.
20. Como Visitante, quero ver a página de serviços com descrição e preços, para decidir se quero contratar.
21. Como Visitante, quero preencher um formulário de contato, para tirar dúvidas ou solicitar um orçamento.
22. Como Administrador, quero visualizar as mensagens enviadas pelo formulário de contato, para responder aos interessados.

### Extras
23. Como Cliente Autenticado, quero receber uma confirmação visual (mensagem de sucesso) ao cadastrar um veículo ou agendamento, para saber que a ação foi concluída.
24. Como Administrador, quero ver um painel (dashboard) simples com números gerais (total de clientes, veículos e agendamentos do dia), para ter uma visão rápida do negócio.

## 5. Mapeamento com os Indicadores de Desempenho (ID)

Esta tabela liga funcionalidades da Ultra Legacy aos 24 IDs exigidos pela disciplina, servindo de guia de implementação (o checklist completo, com status marcado, fica no `README.md`).

| ID | Como será atendido no projeto |
|---|---|
| ID 01 | Prototipar (Figma/Stitch) as telas mobile e desktop de: Home, Serviços, Cadastro de Veículo e Área do Cliente. |
| ID 02 | Usar Bootstrap (Grid/Flex do framework) para o layout geral do site. |
| ID 03 | Usar Flexbox/Grid puro em componentes específicos (ex.: cards de veículo). |
| ID 04 | Usar componentes prontos do Bootstrap: card (serviço/veículo), button, modal (confirmação de agendamento), carousel (fotos de antes/depois). |
| ID 05 | Layout fluido com `%`, `rem`, `vw/vh` nos containers e espaçamentos principais. |
| ID 06 | Definir um Design System simples: paleta de cores da marca, tipografia e padrão de botões/cards aplicado em todas as páginas. |
| ID 07 | Usar Sass (SCSS) com variáveis (cores, espaçamentos) e mixins (ex.: mixin de card). |
| ID 08 | Tipografia responsiva com media queries mobile-first (ou `clamp()`) nos títulos e textos. |
| ID 09 | `object-fit: cover` nas fotos de veículos/serviços dentro de containers com `%`. |
| ID 10 | Servir imagens em WebP e usar `srcset`/`picture` para diferentes tamanhos de tela. |
| ID 11 | Validação HTML nativa nos formulários de cadastro de cliente, veículo, contato e agendamento (campos obrigatórios, `type=email`, `maxlength`). |
| ID 12 | REGEX para validar formato de placa (padrão antigo `AAA-0000` e Mercosul `AAA0A00`), e-mail e telefone. |
| ID 13 | `select` para escolher o serviço no agendamento, `radio`/`checkbox` para forma de pagamento ou aceite de termos. |
| ID 14 | `localStorage` para salvar a última placa pesquisada e rascunho do formulário de agendamento (ver `architecture.md`). |
| ID 15 | Projeto configurado com Node.js/NPM (`package.json`) para gerenciar dependências (Bootstrap, Sass, JSON Server, etc.). |
| ID 16 | Uso de branches (ex.: `main` + branches de feature) e `.gitignore` (excluindo `node_modules/`). |
| ID 17 | `README.md` padronizado com o checklist dos 24 IDs preenchido conforme o progresso. |
| ID 18 | Organização de pastas modular (ex.: `docs/`, `src/pages/`, `src/styles/`, `src/scripts/`, `src/assets/`). |
| ID 19 | Configuração de ESLint e Prettier no projeto. |
| ID 20 | jQuery para interações como abrir/fechar menu mobile, animações simples ao cadastrar um veículo. |
| ID 21 | Plugin jQuery Mask no campo de placa e telefone (ou outra lib equivalente). |
| ID 22 | JSON Server (fake API) para persistir o cadastro de cliente/veículo/agendamento enviado pelo formulário. |
| ID 23 | JSON Server (fake API) para exibir a lista de serviços e o histórico de agendamentos na página. |
| ID 24 | API pública real de consulta de placas veiculares para buscar marca/modelo/ano/cor do veículo, tratando erro quando a placa não é encontrada. |


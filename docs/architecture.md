🛠️ Especificação Técnica (Tech Spec) - Ultra Legacy
Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do sistema da estética automotiva Ultra Legacy.

1. Modelo de Dados (Diagrama ER)
Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do nosso "banco de dados" (db.json) e como as informações se conectam.

Snippet de código
erDiagram
CLIENTE ||--o{ AGENDAMENTO : "realiza (e ganha desconto)"
CLIENTE {
string id PK "Gerado automaticamente"
string nome
string cpf "Usado para o login"
string telefone
string senha
}
AGENDAMENTO {
string id PK
string clienteId FK "Vínculo com o Cliente"
string servico "Ex: 'Polimento Técnico' ou 'Lavagem Detalhada'"
float valorBruto
float desconto "Calculado automaticamente (10%)"
float valorFinal
string data "Formato ISO (YYYY-MM-DD)"
}
2. Dicionário de Dados
Breve explicação das tabelas principais:

Clientes: Responsável por armazenar os dados de autenticação e contato do usuário.

id: Identificador único gerado pelo JSON Server (String ou Hash).

cpf: Chave de acesso do usuário. Em um cenário real seria único, mas para o MVP não há trava estrita no banco, apenas validação no front-end.

telefone: Telefone do cliente para confirmação do serviço.

Agendamentos: Registra o histórico de serviços contratados. Regra de Negócio Crítica: Todo agendamento feito pelo cliente deve calcular, via JavaScript, um valor secundário automático do tipo DESCONTO, reduzindo o valor final cobrado.

clienteId: Chave estrangeira que vincula o agendamento ao cliente (padrão de nomenclatura exigido pelo JSON Server para rotas aninhadas).

servico: Nome do serviço automotivo selecionado.

valorBruto: Valor original do serviço.

desconto: Valor deduzido referente ao desconto fidelidade.

valorFinal: Valor líquido que o cliente irá pagar no final.

3. Rotas da API (JSON Server)
A aplicação consome a API local simulada pelo JSON Server. Abaixo os principais endpoints:

GET /clientes - Retorna a lista de clientes.

POST /clientes - Cadastra um novo cliente.

GET /agendamentos?clienteId=1 - Retorna os agendamentos de um cliente específico.

POST /agendamentos - Cadastra um novo agendamento de serviço.

4. Estrutura do Banco de Dados (db.json)
Esta é a representação em formato JSON do banco de dados simulado. Esta estrutura serve de contexto para ferramentas de IA e para o JSON Server inicializar a API Fake.

JSON
{
  "clientes": [
    {
      "id": "1",
      "nome": "João da Silva",
      "cpf": "12345678900",
      "telefone": "41999998888",
      "senha": "senha_super_segura"
    }
  ],
  "agendamentos": [
    {
      "id": "1",
      "clienteId": "1",
      "servico": "Polimento Técnico",
      "valorBruto": 350.00,
      "desconto": 35.00,
      "valorFinal": 315.00,
      "data": "2026-03-16"
    },
    {
      "id": "2",
      "clienteId": "1",
      "servico": "Higienização Interna",
      "valorBruto": 200.00,
      "desconto": 20.00,
      "valorFinal": 180.00,
      "data": "2026-03-17"
    }
  ]
}

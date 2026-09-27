# 🛠️ Especificação Técnica (Tech Spec) - Ultra Legacy

Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do sistema da estética automotiva Ultra Legacy.

## 1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do nosso "banco de dados" (`db.json`) e como as informações se conectam.

```mermaid
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

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

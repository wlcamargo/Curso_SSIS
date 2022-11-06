# Documentação do Projeto - Curso SSIS

Desenvolvedor: Wallace Camargo

Cliente: Curso de Integration Services para a Escola da Análise de Dados

Data do Deploy: Novembro de 2022

# Objetivos
Simular a construção de um banco transacional e construção de fluxo para o Data Warehouse, passando pela camada de Staging.
O projeto em questão é para a área do Marketing da empresa.

Fonte de dados: Planilha de Excel e Banco de Dados

Arquitetura do Projeto --> Pasta Imagens

Schema do Projeto --> Pasta Imagens

# Etapas do Projeto
- Importar dados da planilha de Excel para simular o banco de produção
- Criar banco de dados de staging e realizar a migração 
- Criar consultas desnormalizando (juntando) as tabelas que serão dimensões e fato
- Construção de chaves substitutas (SK)
- Testar Versionamento dos atributos históricos nas dimensões
- Criar orquestrador para sequenciar tarefas
- Deploy do projeto no SQL Server
- Agendamento do processo no SQL Server Agent
- Configuração de feedback por e-mail do job realizado
- Criar loop para importar todos os arquivos de meta para o banco de dados
- Movimentar arquivos de meta para pasta “metas processadas”

# Especificações 

Modelo do projeto: Star Schema (modelo estrela)

Dimensões: dCalendario, dCliente e dProduto

Fatos: fMetas e fVendas

# Dados históricos das dimensões

dProduto: Preço

dCliente: Salário, Score e Tipo Profissional

# Restrições do Projeto

fMetas não está relacionada com a dCalendario

dProdutos no plural, fora do padrão dos nomes das dimensões


------------------------------------------------------------------------------------------------
Observação sobre as aulas: foram mais de 50 aulas, mas mantivemos aqui apenas os tópicos principais.

Aula 1 - Introdução ao Git e Github

Aula 2 - Renomeando Pacotes

Aula 3 - Criando Conectores planilha e SQL Server

Aula 4 - Criando tabela no SQL Server e importando dados da planilha 

Aula 5 - Loop de Truncate Table

Aula 6 - Dividindo Fluxo de ETL

Aula 7 - Importando Dados dos Clientes

Aula 8 - Importando Dados de Vendas

Aula 9 - Inclusao Pacote Principal (main)

Aula 10 - Migração Produção para Staging

Aula 11 - Criação da dProduto no DW (com SCD tipo 2) Histórico na dimensão

Aula 12 - Criação da dCliente no DW (com SCD tipo 2) Histórico na dimensão

Aula 13 - Criação da dimensão calendário

Aula 14 - Criação da tabela fato

Aula 15 - Criando orquestrador de MKT

Aula 16 - Criar um pacote de loop

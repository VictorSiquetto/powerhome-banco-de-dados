# ⚡ Projeto Banco de Dados: PowerHome

**Sistema de Monitoramento de Energia**

## Sobre o Projeto

O PowerHome é um conceito de solução IoT para o monitoramento e gestão do consumo energético residencial. 

**Nota:** Este repositório foca exclusivamente na estrutura de Banco de Dados do projeto, atuando como um protótipo acadêmico para demonstrar a modelagem de dados e a implementação rigorosa de regras de negócio utilizando puramente SQL.

## Modelagem de Dados

A arquitetura do banco foi mapeada antes do desenvolvimento dos scripts e está dividida em duas etapas no repositório:

* **`der-conceitual/`**: Contém o Diagrama de Entidade-Relacionamento (DER) de alto nível, definindo as entidades principais (como Usuários, Cômodos e Dispositivos) e as regras de negócio.
* **`der-logico/`**: Contém o esquema lógico, detalhando os tipos de dados, chaves estrangeiras, multiplicidades e o modelo relacional pronto para o banco.

## Implementação em SQL (`codigo-mysql/`)

O diretório `codigo-mysql/` concentra todo o desenvolvimento do banco relacional. O código foi estruturado para ir além do básico, utilizando os seguintes recursos:

* **Modelagem Estrutural (DDL):** Criação das tabelas contemplando relacionamentos complexos, chaves primárias e estrangeiras (com ações como `ON DELETE CASCADE`) e restrições de integridade (`CHECK`).
* **Povoamento de Dados (DML):** Scripts completos de inserção de dados fictícios para simular um ambiente residencial real e testar as consultas de forma prática.
* **Stored Procedures:** Criação de rotinas armazenadas para automatizar e padronizar as operações de CRUD (Inclusão, Atualização e Exclusão Lógica) em todas as entidades do sistema.
* **Views (Visualizações):** Consultas pré-definidas para alimentar relatórios gerenciais e dashboards, como "Dispositivos em Alerta", "Automações Programadas" e "Resumo de Status da Rede".
* **Otimização e Segurança:** Implementação de Índices (`INDEX`) para acelerar pesquisas críticas (como endereços MAC e e-mails) e o uso de Transações de dados (`START TRANSACTION` / `COMMIT`) para garantir a consistência de operações múltiplas.

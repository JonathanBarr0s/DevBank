# DevBank - API de Banco Digital

## Descrição

O DevBank é um projeto piloto de criação de uma API para um Banco Digital. Este projeto visa oferecer funcionalidades essenciais de um banco, com a perspectiva de expansão para incluir recursos adicionais no futuro. A API é desenvolvida com base em princípios RESTful e todas as informações são armazenadas em memória, utilizando o objeto existente no arquivo **`bancodedados.js`**. É importante destacar que os dados fundamentais do banco, como nome e agência, permanecem imutáveis durante a execução deste projeto.

O DevBank é um Banco Digital que oferece uma API RESTful com os seguintes recursos:

- **Listar Contas Bancárias:** Este recurso permite listar todas as contas bancárias existentes, após verificar a senha do banco;
- **Criar Conta Bancária:** Permite a criação de novas contas bancárias, gerando números únicos de conta e aplicando várias validações para garantir a integridade dos dados;
- **Atualizar Dados do Usuário da Conta Bancária:** Este recurso permite a atualização de informações do usuário de uma conta bancária específica, garantindo que todos os campos sejam preenchidos corretamente e que não haja duplicação de CPF ou e-mail;
- **Excluir Conta Bancária:** Permite a exclusão de contas bancárias existentes, desde que o saldo seja igual a zero, garantindo a integridade das operações;
- **Depositar:** Permite aos clientes depositar dinheiro em suas contas bancárias, com validações para evitar depósitos negativos ou zerados;
- **Sacar:** Oferece a funcionalidade de saque de contas bancárias, sujeita a verificações de segurança, incluindo a validação da senha e a disponibilidade de saldo;
- **Transferir:** Permite transferências seguras entre contas bancárias, verificando a validade das contas envolvidas, a senha e a disponibilidade de saldo;
- **Saldo:** Fornece informações sobre o saldo de uma conta bancária específica, após verificar a validade da senha;
- **Extrato:** Oferece um relatório detalhado das transações realizadas em uma conta bancária específica, após verificar a validade da senha.

**Status do Projeto:** Concluído e funcionando perfeitamente.

## Objetivo

Para alcançar os objetivos do projeto, foram utilizadas tecnologias e práticas de desenvolvimento de APIs RESTful. Algumas das tecnologias e conceitos empregados incluem:

1. **Node.js**: A API foi desenvolvida em Node.js, uma plataforma de código aberto para execução de JavaScript no servidor;
2. **Express.js**: O framework Express.js foi utilizado para simplificar a criação das rotas da API, gerenciar middlewares e facilitar o tratamento das requisições HTTP;
3. **JSON**: O formato JSON (JavaScript Object Notation) é amplamente utilizado para a troca de dados entre a API e os clientes, devido à sua simplicidade e facilidade de leitura;
4. **REST (Representational State Transfer)**: A API segue o padrão REST, que define um conjunto de princípios para a criação de serviços web escaláveis e flexíveis. Isso inclui o uso adequado de verbos HTTP (GET, POST, PUT, DELETE) e a organização dos recursos em endpoints.

### **Códigos de Requisição HTTP**

Para garantir uma comunicação eficaz entre a API e os clientes, foram utilizados os seguintes códigos de requisição HTTP:

- **GET**: Utilizado para recuperar informações de contas bancárias, saldos, extratos e listar contas existentes;
- **POST**: Usado para criar novas contas bancárias, realizar depósitos, saques e transferências, bem como atualizar os dados do usuário da conta;
- **PUT**: Empregado para atualizar os dados do usuário da conta bancária;
- **DELETE**: Utilizado para excluir uma conta bancária existente.

### **Padrão REST**

O projeto DevBank segue os princípios do padrão REST, que inclui a utilização de endpoints claramente definidos para cada recurso, ações consistentes baseadas em verbos HTTP e o uso de códigos de status adequados para indicar o resultado das operações. Isso torna a API fácil de entender, manter e expandir.

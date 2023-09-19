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

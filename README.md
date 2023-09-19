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

## Instalação

1. **Instale o Visual Studio Code (VS Code)**:
    
    Se você ainda não tem o Visual Studio Code instalado, você pode baixá-lo gratuitamente no site oficial: **https://code.visualstudio.com/**.    
    O VS Code é um ambiente de desenvolvimento integrado (IDE) muito popular que é altamente recomendado para desenvolvimento em Node.js.
    
2. **Instale o Insomnia**:
    
    O Insomnia é uma ferramenta para testar APIs RESTful. Você pode baixá-lo gratuitamente no site oficial: **https://insomnia.rest/download**.    
    O Insomnia permite que você faça requisições à API e visualize as respostas, o que será útil para testar as funcionalidades da API DevBank.

3. **Instale o Node.js**:

    Certifique-se de ter o Node.js instalado no seu sistema. Você pode baixá-lo em **https://nodejs.org/en/download**. Verifique a instalação executando os comandos no terminal:

     ```bash
    node -v
    npm -v
     ```
    Isso deve exibir as versões do Node.js e do npm instaladas no seu sistema.

   
4. **Clone o Repositório**:
    
    Primeiro, você precisa clonar o repositório DevBank para o seu computador. Abra o terminal do VS Code e execute o seguinte comando:
    
    ```bash
    git clone https://github.com/JonathanBarr0s/DevBank.git
    ```
    
    Isso irá criar uma cópia do repositório na sua máquina.
    
5. **Instale as Dependências**:
    
    Navegue até o diretório do projeto DevBank que você acabou de clonar:
    
    ```bash
    cd devbank
    ```
    
    Em seguida, instale todas as dependências do projeto usando o npm (Node Package Manager). Execute o seguinte comando:
    
    ```bash
    npm install    
    ```
    
    Isso instalará todas as bibliotecas e pacotes necessários para executar a aplicação.
    
    

Após seguir esses passos, você estará pronto para iniciar o desenvolvimento e testar a API DevBank no ambiente configurado. Certifique-se de estar no diretório do projeto DevBank no VS Code ao iniciar o desenvolvimento.






## Contribuição
Contribuições são bem-vindas! Se você quiser contribuir para este projeto, siga as etapas abaixo:
1. Faça um fork do repositório
2. Crie uma nova branch: `git checkout -b minha-branch`
3. Faça suas alterações e faça commit: `git commit -m "Minhas alterações"`
4. Faça push para o repositório remoto: `git push origin minha-branch`
5. Envie um Pull Request

## Licença
Este projeto está licenciado sob a licença nenhuma

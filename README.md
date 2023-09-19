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

Aqui estão os passos para configurar o ambiente e executar o projeto DevBank:

1. **Instale o Visual Studio Code:**
    
    O Visual Studio Code (VS Code) é um ambiente de desenvolvimento recomendado para trabalhar com o código-fonte do projeto DevBank. Você pode baixá-lo em **[code.visualstudio.com](https://code.visualstudio.com/)**.
    
2. **Instale o Insomnia:**
    
    O Insomnia é uma ferramenta útil para testar APIs REST. Você pode baixá-lo em **[insomnia.rest/download](https://insomnia.rest/download/)**.
    
    Após a instalação, você pode importar as configurações de ambiente e as requisições do projeto DevBank para o Insomnia.
    
    - Abra o Insomnia.
    - No menu superior, vá em "File" -> "Import/Export" -> "Import Data" -> "From File".
    - Navegue até o diretório do projeto DevBank e selecione o arquivo **`insomnia_export.json`**.
    - As configurações e requisições do projeto serão importadas.
3. **Clone o Repositório:**
    
    Para obter o código-fonte do projeto DevBank no seu computador, siga estas etapas:
    
    ```bash
    git clone https://github.com/JonathanBarr0s/DevBank.git
    ```
    
4. **Instale o Node.js:**
    
    Certifique-se de ter o Node.js instalado no seu sistema. Você pode baixá-lo em **[nodejs.org](https://nodejs.org/)**. Verifique a instalação executando os comandos no terminal:
    
    ```
    node -v
    npm -v
    ```
    
    Isso deve exibir as versões do Node.js e do npm instaladas no seu sistema.
    
5. **Instale as Dependências do Projeto:**
    
    Navegue até o diretório do projeto DevBank que você clonou no passo 3 e execute o seguinte comando para instalar as dependências do projeto:
    
    ```
    npm install
    ```
    
6. **Instale o Nodemon (Development Dependency):**
    
    O Nodemon é uma ferramenta que ajuda a desenvolver aplicativos baseados em Node.js reiniciando automaticamente o servidor quando ocorrem alterações no código. Instale-o como uma dependência de desenvolvimento com o seguinte comando:
    
    ```mathematica
    npm install -D nodemon
    ```
    
7. **Instale a Biblioteca date-fns (Dependency):**
    
    A biblioteca date-fns é utilizada para manipulação de datas no projeto DevBank. Instale-a como uma dependência com o seguinte comando:
    
    ```lua
    npm install date-fns --save
    ```
    
8. **Execute o Projeto:**
    
    Agora, você está pronto para executar o projeto DevBank. Utilize o seguinte comando para iniciar o servidor:
    
    ```arduino
    npm run dev
    ```
    
    O Nodemon será responsável por reiniciar automaticamente o servidor sempre que você fizer alterações no código, facilitando o processo de desenvolvimento.
    

Agora você tem o ambiente configurado e está pronto para executar e testar o projeto DevBank usando o VS Code e o Insomnia. Certifique-se de estar no diretório do projeto DevBank no terminal para executar os comandos relacionados à API.






## Contribuição
Contribuições são bem-vindas! Se você quiser contribuir para este projeto, siga as etapas abaixo:
1. Faça um fork do repositório;
2. Crie uma nova branch: `git checkout -b minha-branch`;
3. Faça suas alterações e faça commit: `git commit -m "Minhas alterações"`;
4. Faça push para o repositório remoto: `git push origin minha-branch`;
5. Envie um Pull Request.

## Licença
Este projeto está licenciado sob a licença nenhuma.

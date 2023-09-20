# DevBank - API de Banco Digital

## 1. Descrição

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

## 2. Objetivo

Para alcançar os objetivos do projeto, foram utilizadas tecnologias e práticas de desenvolvimento de APIs RESTful. Algumas das tecnologias e conceitos empregados incluem:

1. **Node.js**: A API foi desenvolvida em Node.js, uma plataforma de código aberto para execução de JavaScript no servidor;
2. **Express.js**: O framework Express.js foi utilizado para simplificar a criação das rotas da API, gerenciar middlewares e facilitar o tratamento das requisições HTTP;
3. **JSON**: O formato JSON (JavaScript Object Notation) é amplamente utilizado para a troca de dados entre a API e os clientes, devido à sua simplicidade e facilidade de leitura;
4. **REST (Representational State Transfer)**: A API segue o padrão REST, que define um conjunto de princípios para a criação de serviços web escaláveis e flexíveis. Isso inclui o uso adequado de verbos HTTP (GET, POST, PUT, DELETE) e a organização dos recursos em endpoints.

### 2.1 **Códigos de Requisição HTTP**

Para garantir uma comunicação eficaz entre a API e os clientes, foram utilizados os seguintes códigos de requisição HTTP:

- **GET**: Utilizado para recuperar informações de contas bancárias, saldos, extratos e listar contas existentes;
- **POST**: Usado para criar novas contas bancárias, realizar depósitos, saques e transferências, bem como atualizar os dados do usuário da conta;
- **PUT**: Empregado para atualizar os dados do usuário da conta bancária;
- **DELETE**: Utilizado para excluir uma conta bancária existente.

### 2.2 **Padrão REST**

O projeto DevBank segue os princípios do padrão REST, que inclui a utilização de endpoints claramente definidos para cada recurso, ações consistentes baseadas em verbos HTTP e o uso de códigos de status adequados para indicar o resultado das operações. Isso torna a API fácil de entender, manter e expandir.

## 3. Instalação

Aqui estão os passos para configurar o ambiente e executar o projeto DevBank:

1. **Instale o Visual Studio Code:**
    
    O Visual Studio Code (VS Code) é um ambiente de desenvolvimento recomendado para trabalhar com o código-fonte do projeto DevBank. Você pode baixá-lo em **[code.visualstudio.com](https://code.visualstudio.com/)**.
    
2. **Instale o Insomnia:**
    
    O Insomnia é uma ferramenta útil para testar APIs REST. Você pode baixá-lo em **[insomnia.rest/download](https://insomnia.rest/download/)**.
    
    Após a instalação, você pode importar as configurações de ambiente e as requisições do projeto DevBank para o Insomnia.
    
    - Abra o Insomnia.
    - No menu superior direito, clique no +, vá em "Import".
    - Navegue até o diretório do projeto DevBank e selecione o arquivo **`insomnia_export.json`**.
    - As configurações e requisições do projeto serão importadas.
3. **Clone o Repositório:**
    
    Para obter o código-fonte do projeto DevBank no seu computador, execute o comando abaixo no terminal do VS Code:
    
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

## 4. Uso da API DevBank

### 4.1 **Listar contas bancárias**

**Endpoint:** **`GET /contas?senha_banco=Dev123Bank`**

Este endpoint permite listar todas as contas bancárias existentes.

- **Requisição:**
    - Método: GET
    - URL: `**http://localhost:3000/contas?senha_banco=Dev123Bank**`
    - Query Params:
        - **`senha_banco`**: Senha do banco (obrigatório)
- **Resposta:**
    - Status Code: 200 OK
    - Corpo da Resposta: Lista de todas as contas bancárias existentes

### 4.2 **Criar conta bancária**

**Endpoint:** **`POST /contas`**

Este endpoint permite criar uma nova conta bancária.

- **Requisição:**
    - Método: POST
    - URL: **`http://localhost:3000/contas`**
    - Corpo da Requisição (JSON):
        
        ```json
        {
          "nome": "Nome do Titular",
          "cpf": "12345678900",
          "data_nascimento": "1990-01-01",
          "telefone": "11987654321",
          "email": "titular@exemplo.com",
          "senha": "senha123"
        }
        
        // todos os campos são obrigatórios.
        ```
        
- **Resposta:**
    - Status Code:
        - 201 Created (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.3 **Atualizar usuário da conta bancária**

**Endpoint:** **`PUT /contas/:numeroConta/usuario`**

Este endpoint permite atualizar os dados do usuário de uma conta bancária.

- **Requisição:**
    - Método: PUT
    - URL: **`http://localhost:3000/contas/123/usuario`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor e **`123`** pelo número da conta que deseja atualizar.
    - Corpo da Requisição (JSON):
        
        ```json
        {
          "nome": "Novo Nome do Titular",
          "cpf": "987.654.321-00",
          "data_nascimento": "1995-02-15",
          "telefone": "(11) 98765-5432",
          "email": "novo@exemplo.com",
          "senha": "novasenha456"
        }
        
        // todos os campos são obrigatórios.
        ```
        
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.4 **Excluir Conta**

**Endpoint:** **`DELETE /contas/:numeroConta`**

Este endpoint permite excluir uma conta bancária existente.

- **Requisição:**
    - Método: DELETE
    - URL: **`http://localhost:3000/contas/123`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor e **`123`** pelo número da conta que deseja excluir.
- **Resposta:**
    - Status Code:
        - 204 No Content (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.5 **Depositar**

**Endpoint:** **`POST /transacoes/depositar`**

Este endpoint permite realizar um depósito em uma conta bancária.

- **Requisição:**
    - Método: POST
    - URL: **`http://localhost:3000/transacoes/depositar`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor.
    - Corpo da Requisição (JSON): Certifique-se de fornecer o número da conta e um valor válido (não negativo e não zerado).
        
        ```json
        {
          "numero_conta": "123",
          "valor": 100
        }
        
        // todos os campos são obrigatórios.
        ```
        
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.6 **Sacar**

**Endpoint:** **`POST /transacoes/sacar`**

Este endpoint permite realizar um saque em uma conta bancária.

- **Requisição:**
    - Método: POST
    - URL: **`http://localhost:3000/transacoes/sacar`**
    - Corpo da Requisição (JSON): Certifique-se de fornecer o número da conta, um valor válido (não negativo e não zerado) e a senha da conta.
        
        ```json
        {
          "numero_conta": "123",
          "valor": 50.00,
          "senha": "senha123"
        }
        
        // todos os campos são obrigatórios.
        ```
        
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.7 **Transferir**

**Endpoint:** **`POST /transacoes/transferir`**

Este endpoint permite realizar uma transferência entre duas contas bancárias.

- **Requisição:**
    - Método: POST
    - URL: **`http://localhost:3000/transacoes/transferir`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor.
    - Corpo da Requisição (JSON):Certifique-se de fornecer o número da conta de origem, o número da conta de destino, um valor válido (não negativo e não zerado) e a senha da conta de origem.
        
        ```json
        {
          "numero_conta_origem": "123",
          "numero_conta_destino": "456",
          "valor": 75.00,
          "senha": "senha123"
        }
        ```
        
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de falha na validação):
        
        ```json
        {
          "mensagem": "Motivo da falha na validação"
        }
        ```
        

### 4.8 **Saldo**

**Endpoint:** **`GET /contas/saldo?numero_conta=123&senha=senha123`**

Este endpoint permite consultar o saldo de uma conta bancária.

- **Requisição:**
    - Método: GET
    - URL: **`http://localhost:3000/contas/saldo?numero_conta=123&senha=senha123`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor.
    - Query Params:
        - **`numero_conta`**: Número da conta (obrigatório)
        - **`senha`**: Senha da conta (obrigatório)
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de sucesso):O saldo da conta será retornado.
        
        ```json
        {
          "saldo": 500.00
        }
        ```
        

### 4.9 **Extrato**

**Endpoint:** **`GET /contas/extrato?numero_conta=123&senha=senha123`**

Este endpoint permite listar as transações realizadas em uma conta bancária.

- **Requisição:**
    - Método: GET
    - URL: **`http://localhost:3000/contas/extrato?numero_conta=123&senha=senha123`**
        - Certifique-se de substituir **`http://localhost:3000`** pela URL real do servidor.
    - Query Params:
        - **`numero_conta`**: Número da conta (obrigatório)
        - **`senha`**: Senha da conta (obrigatório)
- **Resposta:**
    - Status Code:
        - 200 OK (em caso de sucesso)
        - 400 Bad Request (em caso de falha na validação)
    - Corpo da Resposta (em caso de sucesso):Um relatório com as transações da conta será retornado, incluindo depósitos, saques e transferências.
        
        ```json
        {
        	"depositos": [
        		{
        			"data": "2023-09-19 21:04:57",
        			"numero_conta": "1",
        			"valor": 500
        		},
        		{
        			"data": "2023-09-19 21:04:57",
        			"numero_conta": "1",
        			"valor": 500
        		}
        	],
        	"saques": [
        		{
        			"data": "2023-09-19 21:05:01",
        			"numero_conta": "1",
        			"valor": 500
        		}
        	],
        	"transferenciasEnviadas": [
        		{
        			"data": "2023-09-19 21:05:12",
        			"numero_conta_origem": "1",
        			"numero_conta_destino": "2",
        			"valor": 20
        		}
        	],
        	"transferenciasRecebidas": []
        }
        ```
        

Lembre-se de substituir as URLs e valores de exemplo pelos valores reais ao usar a API DevBank em seu ambiente. Certifique-se de seguir as validações e requisitos especificados em cada endpoint para garantir o funcionamento adequado da API.

## 5. Rotas

Aqui está uma lista das rotas da API:

<div align="center">

| Método | Rota                                   | Descrição                                        |
| ------ | -------------------------------------- | ------------------------------------------------ |
| GET    | `/contas?senha_banco=Dev123Bank`      | Listar Contas Bancárias                         |
| POST   | `/contas`                              | Criar Conta Bancária                            |
| PUT    | `/contas/:numeroConta/usuario`         | Atualizar Usuário da Conta Bancária             |
| DELETE | `/contas/:numeroConta`                 | Excluir Conta                                   |
| POST   | `/transacoes/depositar`               | Depositar                                       |
| POST   | `/transacoes/sacar`                   | Sacar                                           |
| POST   | `/transacoes/transferir`              | Transferir                                      |
| GET    | `/contas/saldo?numero_conta=123&senha=123` | Consultar Saldo                             |
| GET    | `/contas/extrato?numero_conta=123&senha=123` | Emitir Extrato Bancário                   |

<div align="left">



## 6. Contribuição
Contribuições são bem-vindas! Se você quiser contribuir para este projeto, siga as etapas abaixo:
1. Faça um fork do repositório;
2. Crie uma nova branch: `git checkout -b minha-branch`;
3. Faça suas alterações e faça commit: `git commit -m "Minhas alterações"`;
4. Faça push para o repositório remoto: `git push origin minha-branch`;
5. Envie um Pull Request.

## Licença
Este projeto está licenciado sob a licença nenhuma.

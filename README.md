```markdown
# Projeto de Aplicação de Operações Matemáticas

Este projeto é uma aplicação web que fornece uma API para realizar várias operações matemáticas, desenvolvida com **Spring Boot** no backend, e uma interface de usuário utilizando **HTML**, **CSS** e **JavaScript** no frontend. A aplicação permite que os usuários realizem operações como contagem de alunos aprovados, cálculo de MDC (Máximo Divisor Comum), Fibonacci, verificação de número primo, ordenação de um vetor e somador.

## Tecnologias Utilizadas

- **Java 17** ou superior
- **Spring Boot 2.7.x** (ou a versão mais recente)
- **Maven** para gerenciamento de dependências
- **HTML**, **CSS** e **JavaScript** para o frontend

## Estrutura do Projeto

```
meu-projeto
│
├── backend                 // Código do backend (Spring Boot)
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── seu_pacote
│   │   │   │           ├── controller         // Controllers para manipular requisições
│   │   │   │           │   └── MathController.java  // Controller para operações matemáticas
│   │   │   │           ├── service            // Classes de serviço (lógica de negócio)
│   │   │   │           │   └── MathService.java    // Serviço para operações matemáticas
│   │   │   │           ├── model              // Classes de modelo (entidades)
│   │   │   │           │   └── Operacao.java        // Modelo para operações
│   │   │   │           └── MeuProjetoSpringApplication.java // Classe principal
│   │   │   └── resources
│   │   │       └── application.properties    // Configurações da aplicação
│   │   └── test
│   │       └── java
│   │           └── com
│   │               └── seu_pacote
│   │                   └── MathServiceTests.java // Testes para o serviço de operações matemáticas
│   └── pom.xml // Arquivo de configuração do Maven
│
├── frontend                // Código do frontend (HTML, CSS, JavaScript)
│   ├── index.html         // Página principal com botões para operações
│   ├── style.css          // Estilização da aplicação
│   └── script.js          // Lógica do JavaScript para operações
└── README.md               // Documentação do projeto
```

## Backend - Spring Boot

### Instalação

#### Pré-requisitos

- Java JDK 17 ou superior
- Maven

#### Passos para Executar

1. **Clone o Repositório**

   ```bash
   git clone https://github.com/seu_usuario/meu-projeto.git
   cd meu-projeto/backend
   ```

2. **Instale as Dependências**

   Execute o seguinte comando para baixar as dependências do projeto:

   ```bash
   mvn clean install
   ```

3. **Execute a Aplicação**

   Você pode executar a aplicação usando o seguinte comando:

   ```bash
   mvn spring-boot:run
   ```

   A aplicação será iniciada em `http://localhost:8080`.

### Endpoints da API

A aplicação fornece os seguintes endpoints:

1. **Contagem de Alunos Aprovados**
   - **URL:** `/api/math/contagem-aprovados`
   - **Método:** `GET`
   - **Parâmetros:**
     - `quantidade`: Número total de alunos.

2. **Cálculo de Fibonacci**
   - **URL:** `/api/math/fibonacci`
   - **Método:** `GET`
   - **Parâmetros:**
     - `termos`: Número de termos a serem gerados.

3. **Máximo Divisor Comum (MDC)**
   - **URL:** `/api/math/mdc`
   - **Método:** `GET`
   - **Parâmetros:**
     - `a`: Primeiro número.
     - `b`: Segundo número.

4. **Verificação de Número Primo**
   - **URL:** `/api/math/numero-primo`
   - **Método:** `GET`
   - **Parâmetros:**
     - `numero`: O número a ser verificado.

5. **Ordenação de Vetor**
   - **URL:** `/api/math/ordenacao`
   - **Método:** `GET`
   - **Parâmetros:**
     - `numeros`: Lista de números separados por vírgula.

6. **Somador**
   - **URL:** `/api/math/somador`
   - **Método:** `GET`
   - **Parâmetros:**
     - `numeros`: Lista de números separados por vírgula.

## Frontend - HTML, CSS e JavaScript

A parte frontend da aplicação consiste em uma interface simples onde os usuários podem interagir com a API.

### Instalação

Para o frontend, não há dependências externas, basta abrir o arquivo `index.html` em um navegador.

### Funcionalidades

O frontend possui duas partes principais:

1. **Escolha de Linguagem**
   - O usuário pode escolher entre **Java** e **JavaScript**. A interface é dividida em dois botões que ocupam 100% da largura da tela.

2. **Operações**
   - Quando o usuário seleciona **JavaScript**, ele pode acessar as operações matemáticas mencionadas anteriormente. Para **Java**, uma implementação similar deve ser feita, mas isso exige um ambiente de execução Java (como um servidor servlet) ou outro método para compilar e executar o código Java no navegador.

## Testes

Os testes para os serviços de operações matemáticas podem ser executados usando:

```bash
mvn test
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir um *pull request* ou relatar problemas.

### Considerações Finais
Esse README cobre tanto a parte do backend quanto do frontend, oferecendo uma visão abrangente do projeto. Você pode personalizá-lo ainda mais conforme necessário, especialmente para adicionar informações específicas sobre a implementação de Java e instruções para execução se optar por uma solução específica.
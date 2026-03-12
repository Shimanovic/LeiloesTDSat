# 🏷️ Sistema de Leilões - Java Desktop

## 📌 Descrição
Este projeto é um **sistema de gerenciamento de leilões** desenvolvido em **Java**, utilizando **Swing** para a interface gráfica e **MySQL** como banco de dados.

O sistema permite cadastrar e listar produtos que poderão participar de um leilão.  
O objetivo do projeto é demonstrar a integração entre **Java, banco de dados e interface gráfica**, utilizando boas práticas como o padrão **DAO**.

---

## 🚀 Tecnologias Utilizadas

- Java
- Java Swing
- MySQL
- JDBC
- NetBeans
- MySQL Connector

---

## 📂 Estrutura do Projeto

```
LeiloesTDSat
│
├── src
│   ├── cadastroVIEW.java
│   ├── listagemVIEW.java
│   ├── conectaDAO.java
│   ├── ProdutosDAO.java
│   └── ProdutosDTO.java
│
├── lib
│   └── mysql-connector-java.jar
│
├── build
│
└── nbproject
```

---

## 🧱 Arquitetura do Projeto

O sistema utiliza uma separação simples em camadas:

### 📦 DTO (Data Transfer Object)

Responsável por transportar os dados dentro da aplicação.

Arquivo:

```
ProdutosDTO.java
```

Exemplo de atributos:

- id
- nome
- valor
- status
- descricao

---

### 🗄 DAO (Data Access Object)

Responsável pela comunicação com o banco de dados.

Arquivo:

```
ProdutosDAO.java
```

Principais funções:

- Inserir produto
- Listar produtos
- Atualizar dados
- Buscar informações

---

### 🖥 VIEW (Interface Gráfica)

Responsável pela interação com o usuário.

Arquivos:

```
cadastroVIEW.java
listagemVIEW.java
```

Funcionalidades:

- Cadastro de produtos
- Listagem de produtos
- Interface gráfica em Java Swing

---

## 🗄 Banco de Dados

O sistema utiliza **MySQL**.

Exemplo de criação do banco:

```sql
CREATE DATABASE leiloes;

USE leiloes;

CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    valor DECIMAL(10,2),
    status VARCHAR(50),
    descricao TEXT
);
```

---

## 🔌 Configuração da Conexão

Arquivo:

```
conectaDAO.java
```

Exemplo de configuração:

```java
String url = "jdbc:mysql://localhost:3306/leiloes";
String user = "root";
String password = "senha";
```

Altere os dados conforme seu ambiente.

---

## ▶ Como Executar o Projeto

1. Instale o **Java JDK**
2. Instale o **MySQL**
3. Crie o banco de dados
4. Configure a conexão no arquivo `conectaDAO.java`
5. Abra o projeto no **NetBeans**
6. Execute a aplicação

---

## 📌 Funcionalidades

✔ Cadastro de produtos  
✔ Listagem de produtos  
✔ Integração com banco de dados  
✔ Interface gráfica com Java Swing  

---

## 🎓 Objetivo Acadêmico

Este projeto tem como objetivo demonstrar:

- Conexão Java com banco de dados
- Uso do padrão DAO
- Desenvolvimento de aplicações desktop
- Manipulação de dados com JDBC

---

# Microservices Java

Este repositório contém um conjunto de microserviços desenvolvidos em **Java**, organizados para facilitar a escalabilidade, manutenção e deploy utilizando **Docker**, com a orientação do professor **Luciano Rodrigo Ferreto**.

---

## Estrutura do Projeto

O projeto é composto pelos seguintes serviços:

| Serviço | Descrição |
|---------|-----------|
| `auth-service` | Serviço de autenticação e gerenciamento de usuários. |
| `config-service` | Serviço central de configuração, fornecendo propriedades para os outros serviços. |
| `discovery-service` | Serviço de descoberta (Eureka), para registrar e localizar outros serviços. |
| `gateway-service` | API Gateway que centraliza as requisições e faz roteamento para os microserviços. |
| `greeting-service` | Serviço de exemplo que retorna saudações. |
| `currency-service` | Serviço de conversão de moedas. |
| `order-service` | Gerenciamento de pedidos e integrações com outros serviços. |
| `product-service` | Serviço responsável pelo catálogo de produtos. |
| `configs/greeting-service` | Configurações externas do `greeting-service`. |

---

## Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot**
- **Spring Cloud Config**
- **Eureka Server (Discovery Service)**
- **Docker & Docker Compose**
- **Maven** para gerenciamento de dependências

---

## Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

- [Java JDK](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Maven](https://maven.apache.org/install.html)

---

## Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/Thaise-Zanin/microservices-java.git
cd microservices-java
```

2. Build e execução via Docker Compose:

```bash
docker compose up -d --build
```

3. Acesse os serviços no navegador ou via curl:

- Eureka Dashboard (Discovery Service): **http://localhost:8761**

---

## Observações

- Para resetar o banco de dados PostgreSQL, use:

```bash
docker compose down → para tudo e apaga volumes.

docker compose up -d → cria e inicia os containers em segundo plano.
```

# awsqueue

Projeto Spring Boot para simular o uso de **fila SQS** com **LocalStack** e validar o fluxo localmente sem depender da AWS real.

## Objetivo

- Subir o **LocalStack 3.8**
- Simular uma fila **SQS**
- Rodar a aplicação Spring Boot contra esse ambiente local

## Stack

- Java 21
- Spring Boot
- H2 Database
- LocalStack `3.8`

## Como subir

### 1. Iniciar o LocalStack

```bash
docker compose up -d
```

### 2. Rodar a aplicação

```bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
sdk use java 21.0.10-amzn
./mvnw spring-boot:run
```

## Acesso ao H2

- URL: `http://localhost:8080/h2-console/`
- JDBC URL: `jdbc:h2:mem:awsqueue`
- User: `sa`
- Password: vazio

## Observação

O ambiente LocalStack está configurado para expor apenas o serviço **SQS** na porta `4566`.

# Especificações do banco de dados

## Índice

- [Tecnologias](#tecnologias)
- [Sistema](#sistema)
- [Deploy](#deploy)
- [Tabelas](#tabelas)

## Tecnologias

- PostgreSQL X.X.X

## Deploy

```sh
terraform apply -f .
```

## Tabelas

> No banco de dados é possível especificar as relações das entidades

```mermaid
erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```

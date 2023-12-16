# Documentação com Markdown

## Índice

- [Descrição](#descrição)
- [Tecnologias](#tecnologias)
- [Deploy](#deploy)
- [Especificações](#especificações)
- [Git](#git)

## Descrição

> O arquivo `README.md` principal pode conter uma descrição mais geral do projeto inteiro contendo items como: especificações, organização do repositório e onde encontrar outras informações importantes.

O projeto foi desenvolvido com o objetivo de exemplificar a documentação de um projeto

### Schedule

```mermaid
gantt
    title Nova feature
    dateFormat  YYYY-MM-DD
    section Dev
    desenvolvimento     :a1, 2014-01-01, 30d
    integração          :a2, after a1, 20d
    section QA
    teste unitário      :after a1 2014-01-12  , 12d
    teste de integração :after a2, 24d
```

## Tecnologias

- Terraform X.X.X
- Terragrunt X.X.X

## Deploy

Subir a aplicação:

```sh
terragrunt apply
```

## Especificações

> Em subdiretórios é possível fazer uma especificação mais técnica de cada parte do projeto como a documentação do código do projeto, especificações do banco de dados, jornada do usuário, etc...

O projeto contava com s

Exemplo de documentação de cada parte do projeto:

- [backend](./backend)
- [database](./database)
- [frontend](./frontend)
- [IA](./ia)

## Git

> É possível exemplificar o funcionamento das branches

- `main`: Ambiente de produção
- `homol`: Ambiente de homologação
- `dev`: Ambiente de desenvolvimento

```mermaid
gitGraph
    commit
    branch homol
    branch dev
    commit
    commit
    checkout homol
    merge dev
    checkout main
    merge homol
    commit
    commit
```

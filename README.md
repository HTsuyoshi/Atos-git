# Documentação com Markdown

O arquivo `README.md` principal pode conter uma descrição mais geral do projeto inteiro contendo items como: especificações, organização do repositório e onde encontrar outras informações importantes.

Em subdiretórios é possível fazer uma especificação mais técnica de cada parte do projeto como a documentação do código do projeto, especificações do banco de dados, jornada do usuário, etc...

Exemplo de documentação de cada parte do projeto:

- [backend](./backend)
- [fronend](./frontend)
- [database](./database)
- [IA](./ia)

## Mermaid (Sem suporte para celular)

Para criar os seus flowcharts é possível usar o [editor online](https://mermaid.live/)

Exemplos de representação de infraestrutura usando `mermaid`

```mermaid
graph TD
    usuario[usuario] --> front[front_end]
    usuario[usuario] --> backend
    subgraph backend_network
    direction LR
    backend[backend] --> database[database]
    end
    style backend_network fill:#fff,stroke:#97f,stroke-width:2px,color:#000
```

Diagrama de estados

```mermaid
stateDiagram-v2
    [*] --> Carrinho_vazio
    Carrinho_vazio --> Carrinho_com_items
    Carrinho_com_items --> Carrinho_vazio
    Carrinho_com_items --> Finalizar_compra
    Finalizar_compra --> Pagamento
    Finalizar_compra --> Carrinho_com_items
    Finalizar_compra --> Carrinho_vazio
    Pagamento --> Pagamento_recusado
    Pagamento --> Pagamento_aceito
    Pagamento_aceito --> Enviado_para_entrega
    Pagamento_recusado --> Carrinho_com_items
    Enviado_para_entrega --> [*]
```

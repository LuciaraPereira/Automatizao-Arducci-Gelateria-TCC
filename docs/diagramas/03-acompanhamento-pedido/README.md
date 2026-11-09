# Acompanhamento de pedido

Referências: RF012–RF013.

Diagrama de cenário, elaborado para documentação. Status do pedido e status financeiro são distintos. Chat e avaliação dependem de pedido existente. Cancelamento além de Pendente é evolução de cenário, de prioridade baixa.

```mermaid
flowchart TD
 A[Abrir acompanhamento: cliente ou visitante] --> B{Existe pedido?}
 B -->|Não| C[Exibir estado vazio]
 B -->|Sim| D[Mostrar comanda, itens e situação do pagamento]
 D --> E[Pendente]
 E --> F[Em preparo]
 F --> G[Pronto]
 G --> H[Entregue ou finalizado]
 I[Funcionário autorizado atualiza fila operacional] --> F
 I --> G
 I --> H
 D --> J[Chat associado ao pedido]
 H --> K[Avaliação associada ao pedido]
 E --> L[Consultar fluxo de cancelamento]
 F --> L
 G --> L
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

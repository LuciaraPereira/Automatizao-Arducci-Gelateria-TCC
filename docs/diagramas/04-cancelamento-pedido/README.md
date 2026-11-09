# Cancelamento e avaliação após entrega

Referências: RF009–RF010 e RF020.

Diagrama de cenário, elaborado para documentação. Regra atualizada pela equipe: pode cancelar antes da entrega; após a entrega é necessária avaliação, podendo haver troca. No protótipo a ação direta existe apenas em Pendente. Não presumir estorno bancário nem retorno automático de alimento já preparado ao estoque.

```mermaid
flowchart TD
 A[Cliente ou visitante abre pedido] --> B{Pedido já entregue?}
 B -->|Não| C[Solicitar cancelamento e registrar motivo]
 C --> D[Registrar cancelamento conforme regra atualizada]
 D --> E{Houve pagamento?}
 E -->|Sim| F[Caixa avalia tratamento financeiro e registra decisão]
 E -->|Não| G[Encerrar comanda cancelada]
 F --> G
 B -->|Sim| H[Encaminhar ao caixa para avaliação do motivo]
 H --> I{Decisão do responsável}
 I -->|Troca autorizada| J[Registrar troca e atendimento]
 I -->|Outra solução autorizada| K[Registrar decisão e providência]
 I -->|Recusado| L[Registrar motivo e informar cliente]
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

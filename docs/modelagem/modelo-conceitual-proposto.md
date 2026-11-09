# Modelo conceitual complementar — proposta

Complemento de cenários, não substitui o modelo do TCC. Relação uma comanda por pedido corresponde à simulação atual; agrupamento futuro requer decisão da equipe. Cliente e mesa são opcionais no pedido.

```mermaid
erDiagram
 CLIENTE o|--o{ PEDIDO : realiza
 PEDIDO ||--|| COMANDA : identifica
 MESA o|--o{ PEDIDO : atende
 PEDIDO ||--|{ ITEM_PEDIDO : contem
 PRODUTO ||--o{ ITEM_PEDIDO : referencia
 PEDIDO ||--o{ PAGAMENTO : registra
 PEDIDO ||--o{ HISTORICO_STATUS : possui
 PEDIDO ||--o{ SOLICITACAO_CANCELAMENTO : recebe
 PRODUTO ||--o{ FICHA_TECNICA_ITEM : utiliza
 INSUMO ||--o{ FICHA_TECNICA_ITEM : compoe
 INSUMO ||--o{ MOVIMENTO_INSUMO : movimenta
 SABOR ||--o{ LOTE_GELATO : identifica
 LOTE_GELATO ||--o{ MOVIMENTO_GELATO : movimenta
 LOCAL_ESTOQUE ||--o{ MOVIMENTO_GELATO : registra
```

Pagamentos podem registrar tentativas, com apenas uma liquidação efetiva por valor devido. Consumo por ficha técnica, locais e lotes de gelato são propostas de implementação. Nome/preço dos itens devem ter registro histórico; dados pessoais opcionais precisam de política própria de retenção.

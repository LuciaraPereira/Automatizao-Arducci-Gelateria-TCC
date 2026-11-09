# Jornada de compra — Cliente Arducci

Referências: RF001–RF008.

Diagrama de cenário, elaborado para documentação. Cliente autenticado; cadastro novo mantém avatar vazio. Os cenários de cartão no protótipo não substituem o fluxo de cartão no caixa descrito no TCC.

```mermaid
flowchart TD
 A[Início] --> B[Login ou cadastro]
 B --> C[Home do Cliente Arducci]
 C --> D[Consultar categoria e produto]
 D --> E[Escolher sabores e complementos]
 E --> F[Sacola: revisar itens e quantidades]
 F --> G[Finalizar pedido]
 G --> H{Consumo}
 H -->|Balcão| I[Selecionar pagamento]
 H -->|Mesa| J[Informar número da mesa]
 J --> I
 I -->|PIX ou cartão: cenário demonstrativo| K[Confirmar pagamento simulado]
 I -->|Dinheiro no caixa| L[Gerar comanda pendente]
 L --> M[Administrador no Caixa confirma recebimento]
 K --> N[Acompanhar pedido]
 M --> N
 C --> O[Perfil ou sair]
 O -->|Logout| A
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

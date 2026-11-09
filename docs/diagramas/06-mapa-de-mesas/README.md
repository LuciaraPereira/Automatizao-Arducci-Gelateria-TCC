# Mapa de mesas e atendimento

Referências: RF007 e RF013.

Diagrama de cenário, elaborado para documentação. Mapa é operacional, sem delivery externo. Sincronização automática e liberação por todos os atendimentos ativos são propostas para implementação; não indicam integração já concluída.

```mermaid
flowchart TD
 A[Selecionar forma de consumo] --> B{Entrega à mesa?}
 B -->|Não| C[Atendimento no balcão]
 B -->|Sim| D[Informar número da mesa]
 D --> E[Validar mesa existente]
 E --> F[Associar pedido e comanda à mesa]
 F --> G[Exibir atendimento ativo no mapa]
 G --> H[Preparar e entregar pedido]
 H --> I{Restam atendimentos ativos na mesa?}
 I -->|Sim| G
 I -->|Não| J[Liberar mesa no mapa]
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

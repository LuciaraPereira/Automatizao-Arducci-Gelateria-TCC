# Gestão de estoque — gelatos

Referências: RF015 e RF018–RF019.

Diagrama de cenário, elaborado para documentação. Funcionário autorizado atualiza disponibilidade; Administrador gerencia estoque. Integração de lotes, transferências e consumo por porção é proposta. Conversões entre litros, massa e porção precisam ser definidas, sem equivalência automática.

```mermaid
flowchart TD
 A[Registrar entrada ou produção de gelato] --> B[Identificar sabor, lote, validade e unidade]
 B --> C[Registrar saldo na armazenagem]
 C --> D[Transferir para freezer ou balcão]
 D --> E[Registrar disponibilidade do sabor]
 E --> F[Venda ou produção consome porção definida]
 F --> G[Registrar baixa e conferir saldo]
 G --> H{Esgotou?}
 H -->|Sim| I[Marcar sabor indisponível]
 H -->|Não| J[Manter disponível]
 I --> K[Repor e conferir disponibilidade]
 K --> E
 G --> L[Alertar mínimo ou validade]
 M[Perda ou descarte com motivo] --> G
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

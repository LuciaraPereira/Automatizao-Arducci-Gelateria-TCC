# Gestão de estoque — insumos e produtos

Referências: RF017–RF019.

Diagrama de cenário, elaborado para documentação. Entrada, saída e mínimo estão no TCC. Lotes, validade e baixa por ficha técnica são detalhamentos propostos. Validar unidade e saldo; cancelamento não repõe insumo consumido automaticamente.

```mermaid
flowchart TD
 A[Administrador acessa estoque] --> B[Selecionar insumo e unidade]
 B --> C{Movimentação}
 C -->|Entrada| D[Registrar quantidade, lote e validade quando aplicável]
 C -->|Saída ou perda| E[Registrar quantidade e motivo]
 C -->|Ajuste| F[Registrar correção justificada]
 D --> G[Validar e registrar movimento]
 E --> G
 F --> G
 G --> H[Atualizar saldo e histórico]
 H --> I{Saldo atingiu mínimo?}
 I -->|Sim| J[Emitir alerta de reposição]
 I -->|Não| K[Manter acompanhamento]
 L[Proposta: produto com ficha técnica] --> M[Calcular consumo por quantidade produzida]
 M --> E
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

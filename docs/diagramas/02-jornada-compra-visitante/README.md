# Jornada de compra — Visitante

Referências: RF002–RF008.

Diagrama de cenário, elaborado para documentação. Visitante não acessa perfil. A exclusão de dados temporários é uma regra do cenário; retenção fiscal e financeira deve ser definida na implementação.

```mermaid
flowchart TD
 A[Início: Ver cardápio digital] --> B[Home visitante]
 B --> C[Escolher produto e personalização]
 C --> D[Revisar sacola]
 D --> E[Finalizar pedido]
 E --> F{Deseja se identificar?}
 F -->|Sim| G[Informar nome e WhatsApp opcionais]
 F -->|Não| H[Identificar somente pela comanda automática]
 G --> I[Escolher balcão ou informar mesa]
 H --> I
 I --> J{Pagamento}
 J -->|PIX| K[Confirmar pagamento simulado]
 J -->|Dinheiro| L[Comanda pendente no Caixa]
 L --> M[Administrador confirma recebimento]
 K --> N[Acompanhar pedido pela comanda]
 M --> N
 N --> O[Encerrar atendimento e limpar dados temporários]
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

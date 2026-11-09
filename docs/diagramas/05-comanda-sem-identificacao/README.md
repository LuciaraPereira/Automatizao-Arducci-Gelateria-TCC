# Processamento de comanda sem dados pessoais

Referências: RF006–RF008 e RF014.

Diagrama de cenário, elaborado para documentação. Comanda é gerada em todos os pedidos. Nome e WhatsApp opcionais não impedem a compra. O TCC também prevê cartão no caixa. CPF só integra a opção fiscal quando solicitado.

```mermaid
flowchart TD
 A[Visitante finaliza sem nome e WhatsApp] --> B[Gerar número único da comanda]
 B --> C[Associar itens, total e balcão ou mesa]
 C --> D{Forma de pagamento}
 D -->|PIX| E[Registrar confirmação simulada]
 D -->|Dinheiro no caixa| F[Listar comanda em pagamentos pendentes]
 F --> G[Caixa consulta número da comanda]
 G --> H[Mostrar itens e total sem inventar dados pessoais]
 H --> I[Confirmar recebimento uma única vez]
 I --> J[Atualizar pagamento e liberar continuidade do pedido]
 E --> J
 J --> K[Cliente acompanha pelo número da comanda]
```

[Editar fonte Mermaid](fluxo.mmd) · [Voltar ao índice](../README.md)

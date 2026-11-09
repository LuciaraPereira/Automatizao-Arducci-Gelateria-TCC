# Tabela 6 – Fluxo de Eventos: Autorizar Cancelamentos (Administrador)   
  
Caso de uso:   
  
Autorizar Cancelamentos   
Atores:   
  
Administrador  
Pré-condições:   
  
Um cliente solicitou o cancelamento de um pedido já pago ou em preparo.   
Pós-condições:   
  
O pedido é estornado financeiramente e os itens retornam ao estoque.   
Fluxo principal:  
1. O administrador recebe a notificação de solicitação de cancelamento no painel.  
2. O administrador acessa a tela "Autorizar cancelamentos".  
3. O administrador avalia o motivo e autoriza a devolução.  
4. O sistema registra o estorno financeiro nos relatórios.  
5. O sistema atualiza o status do pedido para o cliente.  
Fluxo alternativo:   
3a. O administrador avalia que o pedido já foi consumido ou não cabe estorno.  
3a.1. O administrador nega o cancelamento.  
3a.2. O sistema informa ao cliente a recusa do estorno.

---
Transcrição do texto original enviado pela equipe. [Arquivo original](../originais/tabelas-fluxos-eventos-tcc.txt).

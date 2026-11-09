# Tabela 2 – Fluxo de Eventos: Cancelar Pedido (Cliente)   
Caso de uso:  
  
Cancelar pedido  
Atores:   
  
Cliente  
Pré-condições:   
  
O cliente possui um pedido em andamento no sistema.   
Pós-condições:   
  
O pedido é cancelado e os itens são retirados da cesta, ou a solicitação é enviada para análise.   
Fluxo principal:   
1. O cliente acessa a tela de acompanhamento do pedido.  
2. O cliente clica no botão "Cancelar Pedido".  
3. O sistema cancela a transação imediatamente.  
4. O sistema esvazia a cesta e retorna ao cardápio.  
Fluxo alternativo:   
2a. O pedido já encontra-se com o status "Pago" ou "Em preparação".  
2a.1. O cliente clica em "Cancelar Pedido".  
2a.2. O sistema gera uma solicitação de cancelamento para o Administrador.  
2a.3. O sistema orienta o cliente a aguardar a autorização no caixa.

---
Transcrição do texto original enviado pela equipe. [Arquivo original](../originais/tabelas-fluxos-eventos-tcc.txt).

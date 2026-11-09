# Tabela 1 – Fluxo de Eventos: Realizar Pedido (Cliente)   
  
Caso de uso:   
  
Realizar Pedido (Engloba Consultar Cardápio, Finalizar Pedido e Gerar Comanda)   
Atores:   
  
Cliente  
Pré-condições:  
  
O cliente acessou o sistema (com credenciais ou como visitante).   
Pós-condições:   
  
O pedido é salvo no banco de dados e aguarda preparo ou pagamento no balcão.   
Fluxo principal:  
1. O cliente consulta o cardápio digital.  
2. O cliente decide personalizar o produto, selecionando sabores e complementos.  
3. O cliente adiciona o item e gerencia sua cesta de compras.  
4. O cliente aciona o botão "Finalizar Pedido".  
5. O sistema solicita a forma de pagamento e o cliente seleciona "PIX".  
6. O sistema exibe o QR Code e o cliente realiza o pagamento.  
7. O sistema confirma o pagamento, gera a "Comanda Online" e envia o pedido para a fila de preparo.  
Fluxo alternativo:   
5a. O cliente seleciona "Cartão/Dinheiro" como forma de pagamento.  
5a.1. O sistema gera a "Comanda Física" digitalmente.  
5a.2. O sistema orienta o cliente a dirigir-se ao caixa para pagamento.

---
Transcrição do texto original enviado pela equipe. [Arquivo original](../originais/tabelas-fluxos-eventos-tcc.txt).

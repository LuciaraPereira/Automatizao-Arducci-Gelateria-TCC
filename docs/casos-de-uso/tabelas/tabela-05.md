# Tabela 5 – Fluxo de Eventos: Registrar Movimentação de Estoque (Administrador)   
  
  
Caso de uso:   
  
Registrar Movimentação de Estoque   
Atores:   
  
Administrador  
Pré-condições:   
  
O administrador efetuou login no painel gerencial.   
Pós-condições:   
  
O saldo de insumos é atualizado no banco de dados.   
Fluxo principal:  
1. O administrador acessa a tela "Registrar movimentação de estoque".  
2. O administrador seleciona o insumo desejado.  
3. O administrador insere a quantidade e o motivo (entrada de fábrica ou saída/perda).  
4. O administrador confirma a operação.  
5. O sistema atualiza o saldo geral do estoque.  
Fluxo alternativo:   
  
3a. O administrador deseja criar um aviso de reposição para o insumo.  
3a.1. O administrador acessa "Configurar alertas de estoque".  
3a.2. O administrador define a quantidade mínima de segurança.  
3a.3. O sistema salva a regra e passa a emitir alertas quando o saldo atingir o limite.

---
Transcrição do texto original enviado pela equipe. [Arquivo original](../originais/tabelas-fluxos-eventos-tcc.txt).

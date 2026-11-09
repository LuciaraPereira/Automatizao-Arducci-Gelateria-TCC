# Mapeamento das telas e rastreabilidade dos requisitos

**Projeto:** Automação e Gestão — Arducci Gelateria e Açaiteria  
**Data da análise:** 9 de novembro de 2026  
**Base analisada:** [commit 17805df](https://github.com/fatecrl-ite004/Automatiza-o-Arducci-Gelateria/commit/17805df72e02f2045c40d97623f3f6d43c145b5d)

## 1. Objetivo

Relacionar **requisito → perfil → tela/fluxo → critério de aceite → evidência de teste**. Uma tela existente representa parte da solução; o atendimento do requisito deve ser confirmado pelas regras, integrações e testes correspondentes.

A matriz descreve um **protótipo construído por cenários**. Pagamentos, autenticação, notas fiscais e permissões são demonstrativos. Os refinamentos de cenário apontados como baixa prioridade não bloqueiam a apresentação; a priorização da versão final será definida em planejamento próprio.

### Fontes

- [Requisitos funcionais — RF001 a RF021](https://github.com/fatecrl-ite004/Automatiza-o-Arducci-Gelateria/blob/main/docs/requisitos/requisitos-funcionais.md).
- [Requisitos não funcionais — RNF01 a RNF08](https://github.com/fatecrl-ite004/Automatiza-o-Arducci-Gelateria/blob/main/docs/requisitos/requisitos-nao-funcionais.md).
- [Código e catálogo das telas](https://github.com/fatecrl-ite004/Automatiza-o-Arducci-Gelateria/tree/main/prototipo-mobile-desktop).
- [Abrir a apresentação](https://fatecrl-ite004.github.io/Automatiza-o-Arducci-Gelateria/prototipo-mobile-desktop/?device=desktop). Pressione **Esc** para alternar o formato e o fluxo.

### Legenda

| Situação | Significado |
| --- | --- |
| Representado | Tela e fluxo podem ser demonstrados. Não significa implementação de produção validada. |
| Parcial | Há telas ou parte do fluxo; falta regra, integração, persistência ou validação. |
| Refinamento de cenário | Há uma decisão de negócio ou ajuste documental a consolidar, sem bloquear a demonstração. |
| Cenário futuro | Parte do cenário será detalhada ou ampliada em uma próxima evolução. |

[Consultar os mapas do Cliente Arducci e do Visitante](mapas-cliente-e-visitante.md).

## 2. Matriz dos requisitos funcionais

A descrição dos cenários incorpora os papéis e a regra de entrega informados para este mapeamento. O alinhamento da redação dos RFs originais é um refinamento de baixa prioridade.

Todos os arquivos abaixo pertencem à pasta `prototipo-mobile-desktop/`.

| Requisito | Funcionalidade | Telas relacionadas | Situação no cenário | Prioridade do refinamento | Observações |
| --- | --- | --- | --- | --- | --- |
| RF001 | Cadastrar cliente | `tela-4.html`; `tela-40.html`; `tela-36.html` | **Representado** | A definir na evolução | Cadastro → boas-vindas → perfil do novo cliente. Conta e dados de contato são demonstrativos; não há cadastro de conta no servidor. |
| RF002 | Acessar o sistema ou pedir como visitante | `tela-17.html`; `tela-6.html`; `tela-34.html`; `tela-3.html`; `tela-23.html` | **Representado** | A definir na evolução | Login → cardápio do cliente; acesso sem cadastro → cardápio do visitante. Login e recuperação de senha são simulados. |
| RF003 | Consultar cardápio e disponibilidade | `tela-6.html`; `tela-34.html`;  telas de produtos | **Parcial** | A definir na evolução | Categorias e produtos estão disponíveis para consulta. Falta comprovar que um produto esgotado no operacional deixa de ser selecionável no cardápio. |
| RF004 | Personalizar produto | `tela-14.html / tela-22.html`; `tela-27.html / tela-1.html`; `tela-41.html / tela-8.html`; `tela-31.html / tela-32.html`; `tela-15.html / tela-37.html` | **Representado** | A definir na evolução | Cascão/Casquinha, Petit Gateau, Banana Split, Milk Shake e Açaí possuem escolhas de sabores ou complementos. Verificar limites e conteúdo enviado à sacola. |
| RF005 | Gerenciar cesta/sacola | `tela-19.html`; `tela-33.html` | **Representado** | A definir na evolução | Adicionar produtos, alterar quantidade, remover itens e recalcular totais. O nome usado na interface é Sacola. |
| RF006 | Revisar e finalizar pedido | `tela-19.html`; `tela-33.html`; `tela-0.html`; `tela-25.html` | **Representado** | A definir na evolução | Sacola → revisão do pedido → confirmação. O visitante pode deixar nome e WhatsApp vazios e utilizar a comanda automática. |
| RF007 | Selecionar pagamento, local de consumo e observações | `tela-0.html`; `tela-25.html`; `tela-29.html`; `tela-20.html`; `tela-26.html`; `tela-39.html`; `admin-8.html` | **Representado** | A definir na evolução | PIX, cartão do cliente logado e dinheiro no caixa estão representados. Observações ficam na sacola; balcão/mesa e número da mesa, na finalização. Pagamentos são simulados. |
| RF008 | Gerar comanda e encaminhar cartão/dinheiro ao caixa | `tela-0.html`; `tela-25.html`; `admin-8.html` | **Refinamento de cenário** | Baixa | A comanda e a pendência no Caixa representam o cenário presencial. As telas de cartão do cliente logado representam outra alternativa de apresentação. Consolidar na redação final se cartão será no aplicativo, no caixa ou em ambos. |
| RF009 | Cancelar pedido antes da entrega | `tela-10.html`; `tela-24.html` | **Parcial** | Baixa | Regra informada: o cliente pode cancelar antes da entrega. O protótipo já demonstra cancelamento em Pendente com motivo; ampliar a representação para Em preparo e Pronto é um refinamento de baixa prioridade. |
| RF010 | Encaminhar atendimento após a entrega | `tela-10.html`; `tela-24.html`; `admin-8.html` | **Parcial** | Baixa | Regra informada: após a entrega, a solicitação deve passar por avaliação do Administrador (Caixa/Gerente), podendo resultar em troca. O acompanhamento e o contato com o caixa apoiam o cenário; a decisão/troca ainda será detalhada. |
| RF011 | Acessar área operacional como funcionário | `admin-3.html`; `admin-1.html` | **Representado** | A definir na evolução | Selecionar Funcionário → Entrar no Sistema → Dashboard. Cabeçalho Funcionário Arducci e permissões da demonstração; autenticação real é pendência da versão final. |
| RF012 | Acompanhar fila em tempo real e por ordem de chegada | `admin-6.html`; `tela-10.html`; `tela-24.html` | **Parcial** | A definir na evolução | O KDS exibe pedidos e estados. A sincronização entre dispositivos e a ordem FIFO precisam ser validadas/implementadas; a lista local adiciona novos pedidos no início. |
| RF013 | Atualizar status e refletir no cliente | `admin-6.html`; `tela-10.html`; `tela-24.html` | **Parcial** | A definir na evolução | Mudanças entre Pendente, Em preparo, Pronto e Finalizado podem ser demonstradas. A atualização automática em tempo real em outra sessão/dispositivo ainda precisa ser comprovada. |
| RF014 | Processar pagamentos físicos — Administrador/Caixa | `admin-8.html`; `admin-3.html` | **Representado** | Baixa | Ator do cenário: Administrador, que reúne Caixa e Gerente. O Caixa tem etapas de pagamento e pendências digitais. Ajustar posteriormente o termo funcionário usado na redação original do RF014 para refletir esse ator. |
| RF015 | Atualizar disponibilidade no balcão e refletir no cardápio | `admin-7.html`; `admin-5.html`; `tela-6.html`; `tela-34.html` | **Parcial** | A definir na evolução | Sabores e estoque são telas relacionadas. Falta um fluxo integrado e verificável de marcar esgotado/disponível no operacional e atualizar a seleção do cliente. |
| RF016 | Gerenciar colaboradores e permissões | `admin-4.html`; `admin-13.html`; `admin-3.html` | **Parcial** | A definir na evolução | Há telas de funcionários, configurações e perfis. As permissões atuais são fixas da simulação; cadastro, edição, inativação e permissões por colaborador exigem persistência e autorização da versão final. |
| RF017 | Gerenciar produtos, descrições e preços | `admin-7.html`; `admin-5.html`; `admin-13.html`;  telas de produtos | **Parcial** | A definir na evolução | As interfaces de sabores/produtos e configurações estão mapeadas. Falta um catálogo central com CRUD e preços refletidos nos pedidos. O editor visual do mobile não substitui essa regra de negócio. |
| RF018 | Registrar entradas, perdas e ajustes de estoque | `admin-5.html` | **Parcial** | A definir na evolução | A tela Estoque possui formulário de movimentação. A validação deve comprovar alteração do saldo e registro de histórico, além da apresentação do formulário. |
| RF019 | Configurar estoque mínimo e alertas de reposição | `admin-5.html`; `admin-13.html`; `admin-1.html` | **Parcial** | A definir na evolução | Estoque, configurações e indicadores exibem pontos de configuração/alerta. Falta comprovar a regra automática de estoque mínimo e sua persistência com os saldos reais. |
| RF020 | Administrador avaliar pós-entrega e possível troca | `admin-8.html`; `admin-6.html`; `admin-14.html` | **Cenário futuro** | Baixa | Cenário de pós-entrega: Administrador avalia motivo e decide o atendimento, inclusive possível troca. Formalizar a decisão, o responsável e o vínculo com o pedido em uma evolução. O cancelamento da comanda do PDV tem finalidade própria e não representa todo o processo de pós-atendimento. |
| RF021 | Consultar relatórios de produtos e movimentações | `admin-11.html`; `admin-14.html`; `admin-1.html` | **Parcial** | A definir na evolução | Relatórios, Financeiro/DRE e Dashboard existem. A agregação de vendas confirmadas, produtos mais vendidos, filtros e totais reconciliados precisa ser validada sobre dados persistidos. |

## 3. Papéis e regras dos cenários

### 3.1 Administrador e Funcionário

| Perfil | Papel no cenário | Telas principais |
| --- | --- | --- |
| Administrador | Reúne as funções de **Caixa e Gerente**; executa recebimentos e gestão. | Dashboard, Caixa, Clientes, Funcionários, Estoque, Sabores, Financeiro, Mesas, Relatórios, Painel de Controle e Suporte. |
| Funcionário | Cargo com funções operacionais específicas, conforme as permissões demonstradas. | Dashboard, Acompanhamento de Pedidos, Estoque, Sabores, Mapa das Mesas e Suporte. |
| Cliente Arducci | Cliente cadastrado e logado, com perfil e fluxo próprio. | Cardápio, produtos, sacola, pagamento, acompanhamento e perfil. |
| Visitante | Acesso ao cardápio sem cadastro, com identificação opcional e comanda automática. | Cardápio, produtos, sacola, finalização e acompanhamento do visitante. |

No cenário atual, **Caixa, Clientes, Funcionários, Financeiro, Painel de Controle e Relatórios** ficam bloqueados para o perfil Funcionário. Essa separação é intencional. O RF014 deverá ter sua redação alinhada ao Administrador como ator de recebimento; esse ajuste é de **baixa prioridade** no protótipo.

### 3.2 Cancelamento antes da entrega e avaliação após a entrega

Regra de negócio informada para os cenários:

1. **Antes da entrega:** o cliente pode cancelar o pedido.
2. **Depois da entrega:** o atendimento depende de avaliação do motivo pelo Administrador (Caixa/Gerente), podendo resultar em troca.

Pagamento e entrega são marcos diferentes. A redação final de RF009, RF010 e RF020 deve refletir a regra escolhida para entrega e pós-atendimento.

**Representação atual:** o aplicativo demonstra o cancelamento em Pendente. A ampliação para os demais estados anteriores à entrega e o detalhamento da avaliação/troca pós-entrega são refinamentos de **baixa prioridade**, sem bloquear a apresentação dos cenários já existentes.

Propostas de redação para revisão da equipe:

- **RF009:** permitir que o cliente cancele o pedido antes da entrega, registrando o motivo.
- **RF010:** após a entrega, encaminhar a solicitação de atendimento para avaliação do motivo, incluindo a possibilidade de troca.
- **RF020:** permitir ao Administrador avaliar o atendimento pós-entrega e registrar a decisão e o responsável, vinculados ao pedido.

Essas propostas não renumeram requisitos nem alteram automaticamente os arquivos oficiais de requisitos.

### 3.3 Cenários de pagamento

O protótipo apresenta PIX, cartão e dinheiro em seus respectivos fluxos. O cenário presencial utiliza a comanda e o Caixa; outros caminhos demonstram possibilidades de pagamento no aplicativo.

Consolidar o canal definitivo de cartão no RF008 é um refinamento de **baixa prioridade**. A matriz mantém os cenários apresentados, sem exigir a retirada de telas.

### 3.4 Evolução posterior

A ligação definitiva entre disponibilidade, estoque, cardápio, relatórios e registros persistentes será tratada na evolução da aplicação. Esses pontos devem permanecer rastreáveis, com critérios de aceite próprios, sem serem confundidos com falhas da apresentação visual.

## 4. Requisitos não funcionais

Os RNFs são **transversais**: não correspondem a uma única tela. Exigem critérios mensuráveis e evidências de validação.

| Requisito | Qualidade | Onde se aplica | Evidência atual | Validação necessária |
| --- | --- | --- | --- | --- |
| RNF01 | Usabilidade | Todas as telas e fluxos dos três perfis | Há padrões de cabeçalho, navegação, seleção de sabores e feedback. | Validar com usuários: clareza dos rótulos, conclusão das tarefas, mensagens de erro e acessibilidade. |
| RNF02 | Responsividade | Cliente/visitante e administração em mobile, tablet e desktop | Existem os três formatos e menu hambúrguer nas larguras menores. | Testar em dispositivos e larguras reais, orientação, toque, rolagem, teclado e ausência de cortes/sobreposições. |
| RNF03 | Desempenho | Navegação, carregamento, consultas e confirmações | Há pré-carregamento e troca de tela quando o conteúdo fica pronto. | Definir metas de tempo com a equipe e medir tempos reais; a duração da animação não comprova desempenho. |
| RNF04 | Segurança e controle de acesso | Login, perfis e operações protegidas | Perfis e bloqueios existem no navegador, como demonstração. | Implementar autenticação e autorização no servidor; validar sessão, armazenamento seguro de senhas e rejeição de operações não autorizadas. |
| RNF05 | Integridade e confiabilidade | Pedidos, pagamentos, estoque, cancelamentos e documentos | Dados usam localStorage/sessionStorage; não há banco transacional. | Validar transações, concorrência, duplicidade de pagamento, histórico e retenção dos pedidos; distinguir exclusão de dados pessoais de registros financeiros. |
| RNF06 | Disponibilidade | GitHub Pages e futuros serviços da aplicação | O Pages hospeda a interface estática. Isso não valida a disponibilidade da aplicação final. | Verificar publicação e recursos, além de definir monitoramento e critérios de disponibilidade para API, banco e integrações. |
| RNF07 | Facilidade de manutenção | docs/, prototipo-mobile-desktop/ e módulos compartilhados | Há separação de documentação, recursos, estilos e scripts; parte da lógica também está nos HTMLs. | Manter componentes, organização, convenções e testes reproduzíveis na arquitetura final; atualizar esta matriz a cada mudança. |
| RNF08 | Compatibilidade | Todos os fluxos em navegadores suportados | A existência do protótipo não comprova execução em todos os navegadores. | Registrar testes em Chrome, Edge, Firefox e Safari, com versões, dispositivo, resultado e evidências. |

## 5. Roteiros de aceite a registrar

Estes roteiros são **propostas de validação**, não um relatório de testes de aceitação já aprovados. Para cada execução, registrar perfil, versão, navegador/dispositivo, resultado obtido, evidência e responsável.

| Teste | Requisitos | Ação | Resultado esperado |
| --- | --- | --- | --- |
| CT001 | RF001 | Preencher cadastro e confirmar. | Abrir boas-vindas e perfil do novo cliente, sem reutilizar dados de outra pessoa. |
| CT002 | RF002 | Entrar como cliente e depois como visitante. | Abrir o cardápio do modo correto e respeitar as opções disponíveis a cada perfil. |
| CT003 | RF003; RF015 | Marcar um produto como esgotado no operacional e consultar o catálogo. | Produto indisponível não pode ser adicionado; teste depende da integração pendente. |
| CT004 | RF004 | Escolher sabores e complementos; testar seleção vazia e acima do limite. | Bloquear seleção inválida e manter os sabores/itens escolhidos na sacola. |
| CT005 | RF005; RF006 | Alterar quantidades, remover produtos e finalizar. | Manter subtotal e total consistentes; impedir finalização de sacola vazia. |
| CT006 | RF007 | Informar observação e selecionar Receber na mesa. | Persistir observação, solicitar número da mesa e exibir o mesmo número na comanda. |
| CT007 | RF007; RF008; RF014 | Enviar pedido para pagar em dinheiro e abri-lo no Caixa. | Preencher comanda e dados informados, registrar recebimento e remover a pendência sem duplicar o pagamento. |
| CT008 | RF008 | Escolher cartão no aplicativo. | Demonstrar o cenário escolhido para cartão. Consolidar posteriormente no RF008 se o canal será aplicativo, Caixa ou ambos. |
| CT009 | RF009; RF010 | Apresentar cancelamento antes da entrega e atendimento depois da entrega, conforme os cenários informados. | Conforme a regra de cenário informada: antes da entrega pode cancelar; depois da entrega depende de avaliação ou possível troca. O protótipo demonstra atualmente a ação em Pendente. |
| CT010 | RF011; RF014; RF016 | Entrar como Funcionário e abrir as funções operacionais. | Funcionário acessa suas funções específicas; Administrador executa recebimentos no Caixa. Alinhar a redação do RF014 a esse ator. |
| CT011 | RF012; RF013 | Criar dois pedidos em sequência e atualizar seus estados. | Exibir ordem de chegada e refletir alterações no cliente, inclusive em outro dispositivo na versão final. |
| CT012 | RF016 | Cadastrar, editar e inativar colaborador e alterar suas permissões. | Persistir mudanças e negar acesso às operações revogadas. |
| CT013 | RF017 | Criar produto e alterar descrição/preço. | Refletir os dados no cardápio e no cálculo do próximo pedido. |
| CT014 | RF018; RF019 | Registrar entrada e perda até atingir estoque mínimo. | Atualizar saldo, registrar movimentação e emitir alerta no limite configurado. |
| CT015 | RF020 | Após a entrega, solicitar atendimento, informar o motivo e avaliar a possibilidade de troca. | Registrar decisão, responsável e data/hora e vincular o atendimento ao pedido; cenário a detalhar em uma evolução de baixa prioridade. |
| CT016 | RF021 | Consultar um período com vendas e cancelamentos conhecidos. | Relatórios e Financeiro devem apresentar totais coerentes com pagamentos e movimentações do período. |

### Exemplo de registro de execução

| Campo | Preenchimento |
| --- | --- |
| Teste / requisito | CT007 / RF007, RF008 e RF014 |
| Perfil | Administrador (Caixa/Gerente) |
| Versão | Hash do commit testado |
| Ambiente | Navegador, versão, dispositivo e tamanho de tela |
| Resultado esperado | Comanda carregada, recebimento registrado e pendência removida |
| Resultado obtido | Preencher após a execução |
| Situação | Aprovado, reprovado ou bloqueado |
| Evidência | Link para captura, vídeo ou relatório de teste |
| Responsável / data | Preencher após a execução |

## 6. Catálogo técnico das telas

Os nomes abaixo vêm dos catálogos `screens.json` e `admin-screens.json`. Não são novos números de requisito: os identificadores continuam sendo os arquivos HTML do projeto.

### 6.1 Cliente e visitante — 42 telas

| Arquivo | Nome no catálogo |
| --- | --- |
| `tela-0.html` | Finalizar pedido · Cliente |
| `tela-1.html` | Petit Gateau · Visitante |
| `tela-2.html` | Potes · Visitante |
| `tela-3.html` | Esqueci minha senha |
| `tela-4.html` | Cadastro |
| `tela-5.html` | Perfil · Cliente |
| `tela-6.html` | Cardápio · Cliente |
| `tela-7.html` | Self Service · Visitante |
| `tela-8.html` | Banana Split · Visitante |
| `tela-9.html` | Bebidas · Visitante |
| `tela-10.html` | Pedido · Cliente |
| `tela-11.html` | Picolés · Cliente |
| `tela-12.html` | Potes · Cliente |
| `tela-13.html` | Perfil · Preferências |
| `tela-14.html` | Cascão · Cliente |
| `tela-15.html` | Açaí · Cliente |
| `tela-16.html` | Perfil · Dados |
| `tela-17.html` | Login |
| `tela-18.html` | Paletas · Cliente |
| `tela-19.html` | Sacola · Cliente |
| `tela-20.html` | PIX · Visitante |
| `tela-21.html` | Apresentação |
| `tela-22.html` | Cascão · Visitante |
| `tela-23.html` | Nova senha |
| `tela-24.html` | Pedido · Visitante |
| `tela-25.html` | Finalizar pedido · Visitante |
| `tela-26.html` | Crédito e VR |
| `tela-27.html` | Petit Gateau · Cliente |
| `tela-28.html` | Bebidas · Cliente |
| `tela-29.html` | PIX · Cliente |
| `tela-30.html` | Paletas · Visitante |
| `tela-31.html` | Milk Shake · Cliente |
| `tela-32.html` | Milk Shake · Visitante |
| `tela-33.html` | Sacola · Visitante |
| `tela-34.html` | Cardápio · Visitante |
| `tela-35.html` | Self Service · Cliente |
| `tela-36.html` | Perfil · Fidelidade |
| `tela-37.html` | Açaí · Visitante |
| `tela-38.html` | Picolés · Visitante |
| `tela-39.html` | Débito |
| `tela-40.html` | Boas-vindas |
| `tela-41.html` | Banana Split · Cliente |

### 6.2 Site e administração — 15 telas

| Arquivo | Nome no catálogo |
| --- | --- |
| `admin-0.html` | Início · Site Arducci |
| `admin-1.html` | Dashboard |
| `admin-2.html` | Recuperação de senha · Administração |
| `admin-3.html` | Login · Administração |
| `admin-4.html` | Funcionários |
| `admin-5.html` | Estoque |
| `admin-6.html` | Acompanhamento de pedidos · KDS |
| `admin-7.html` | Sabores de gelato |
| `admin-8.html` | Caixa e PDV |
| `admin-9.html` | Suporte e ajuda |
| `admin-10.html` | Mesas e comandas |
| `admin-11.html` | Relatórios |
| `admin-12.html` | Clientes e Arducci Club |
| `admin-13.html` | Painel de controle |
| `admin-14.html` | Financeiro e DRE |

## 7. Funcionalidades adicionais do protótipo

Algumas telas apoiam funções que não estão descritas como requisitos próprios na lista atual, por exemplo:

- Perfil, fidelidade e prévia de tema claro/escuro.
- Mapa de mesas e suporte técnico.
- Comprovantes e prévias fiscais no Painel de Controle.
- Editor visual das 42 telas mobile.

Se permanecerem no escopo final do TCC, essas funções devem receber requisitos próprios ou ser vinculadas explicitamente a um requisito existente. Não atribuir um novo número RF sem aprovação da equipe.

## 8. Como manter a rastreabilidade

1. Manter os papéis e as regras de cenário registrados na seção 3 e alinhar a redação oficial dos requisitos.
2. Atualizar os requisitos e os casos de uso quando uma decisão alterar o escopo.
3. Vincular tarefas/issues e commits aos IDs RF/RNF envolvidos.
4. Executar os roteiros de aceite e anexar evidências.
5. Atualizar esta matriz quando uma regra, tela ou permissão mudar.

Sugestão de organização: manter este arquivo em `docs/rastreabilidade/` e criar na Wiki uma página **Mapeamento das telas**, com um link para esta versão no repositório.

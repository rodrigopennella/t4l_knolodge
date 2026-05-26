# Grupos de Permissão — Documentação de Uso

Guia completo do sistema de permissões do SAG. Aqui você aprende a criar grupos, associar usuários e entende o que cada permissão libera ou bloqueia no sistema.

---

## Índice

1. [Como funciona o sistema de permissões](#1-como-funciona-o-sistema-de-permissões)
2. [Criar um Grupo de Permissão](#2-criar-um-grupo-de-permissão)
3. [Associar um usuário a um grupo](#3-associar-um-usuário-a-um-grupo)
4. [Permissões por setor](#4-permissões-por-setor)
   - [Caixa](#41-caixa)
   - [Terminal](#42-terminal)
   - [Comandas](#43-comandas)
   - [Caderneta](#44-caderneta)
   - [Cadastros](#45-cadastros)
   - [Consultas](#46-consultas)
   - [Alterações](#47-alterações)
   - [Pedidos](#48-pedidos)
   - [Estoque](#49-estoque)
   - [NF-e](#410-nf-e)
   - [Financeiro](#411-financeiro)
   - [Relatórios](#412-relatórios)
   - [Outros](#413-outros)
5. [Exemplos de perfis sugeridos](#5-exemplos-de-perfis-sugeridos)

---

## 1. Como funciona o sistema de permissões

O SAG controla o que cada operador pode ou não fazer através de **grupos de permissão**. Todo usuário do tipo operador precisa estar associado a um grupo, e esse grupo define exatamente quais telas, ações e informações ele pode acessar.

### Tipos de usuário

| Tipo | O que pode fazer |
|---|---|
| **Administrador** | Acesso irrestrito a tudo. As permissões não se aplicam a este tipo. |
| **Operador** | Acesso limitado às permissões configuradas no grupo ao qual pertence. |

### Regras importantes

- Um operador **herda todas as permissões do grupo** ao qual está vinculado.
- Alterar as permissões de um grupo **aplica as mudanças imediatamente** para todos os usuários daquele grupo — sem necessidade de relogar.
- O **Grupo Admin** é reservado para administradores e não pode ser editado nem recriado com esse nome.
- Cada usuário pode pertencer a apenas um grupo.

---

## 2. Criar um Grupo de Permissão

**Outros → Grupos de Permissão → Novo**

1. Informe um **nome** para o grupo (ex: "Operador de Caixa", "Atendente Delivery", "Gerente").
2. Percorra as **13 abas de setores** e ative as permissões desejadas marcando os checkboxes.
3. Para permissões com valor numérico (como percentual máximo de desconto), informe o valor no campo correspondente.
4. Use os botões **Selecionar Todos** e **Desselecionar Todos** dentro de cada aba para agilizar a configuração.
5. Clique em **Salvar**.

---

## 3. Associar um usuário a um grupo

**Outros → Usuários → Cadastrar ou Editar usuário**

No cadastro do usuário, selecione o grupo desejado no campo **Grupo**. Ao salvar, o usuário passa a ter exatamente as permissões definidas naquele grupo.

---

## 4. Permissões por Setor

As permissões estão organizadas em 13 setores. A seguir, o detalhamento completo de cada uma.

---

### 4.1 Caixa

Controla as operações realizadas na **Frente de Caixa**.

| Permissão | O que libera |
|---|---|
| **Utiliza Caixa** | Permite que o operador acesse e opere o módulo de caixa. Sem esta permissão, o caixa fica inacessível. |
| **Abrir Gaveta** | Permite abrir a gaveta de dinheiro manualmente, fora de uma venda. |
| **Cancelar Item** | Permite remover um produto já lançado em uma venda em andamento. |
| **Cancelar Venda** | Permite cancelar uma venda inteira antes de finalizá-la. |
| **Cancelar Sangria** | Permite desfazer uma sangria (retirada de dinheiro) já registrada. |
| **Conceder Desconto** | Permite aplicar desconto em vendas. Ao ativar, informe também o **percentual máximo** permitido (ex: 10%). O sistema bloqueia descontos acima desse valor. |
| **Percentual máximo de desconto** | Define o limite máximo de desconto que o operador pode conceder. Só aparece quando "Conceder Desconto" está ativo. |
| **Finalizar Caixa** | Permite realizar o fechamento do caixa ao final do turno. |
| **Fechamento de Caixa — Lançar Valores** | Permite informar os valores em dinheiro durante o fechamento do caixa. Ao ativar, informe em quantos **dias anteriores** o operador pode alterar fechamentos já realizados. |
| **Dias para alterar fechamento** | Define quantos dias retroativos o operador pode lançar ou corrigir valores de fechamento. Só aparece quando "Lançar Valores" está ativo. |
| **Lançar Sangria** | Permite registrar retiradas de dinheiro do caixa (sangria). |
| **Quantidade acima de 99** | Permite lançar um produto com quantidade superior a 99 unidades em uma única venda. |
| **Venda com Estoque Negativo** | Permite finalizar uma venda mesmo que o produto não tenha estoque suficiente registrado. |
| **Devolução de Venda** | Permite registrar a devolução de uma venda completa. |
| **Devolução de Produto** | Permite registrar a devolução de um produto específico de uma venda. |
| **Colocar Venda em Espera** | Permite pausar uma venda em andamento para atender outra e retomá-la depois. |
| **Trocar Forma de Pagamento** | Permite alterar a forma de pagamento de uma venda já finalizada. |
| **Editar Taxa de Serviço** | Permite modificar o valor da taxa de serviço cobrada em uma venda (ex: taxa de garçom). |
| **Visualizar Últimas Vendas** | Permite consultar o histórico das vendas recentes realizadas no caixa. |

---

### 4.2 Terminal

Controla as operações realizadas no **Terminal** (PDV de mesas e comandas).

| Permissão | O que libera |
|---|---|
| **Utiliza Terminal** | Permite o acesso ao terminal de lançamento. Sem esta permissão, o terminal não abre. |
| **Cancelar Item** | Permite cancelar um produto já lançado em uma comanda aberta no terminal. |
| **Conceder Desconto** | Permite aplicar desconto em pedidos do terminal. Ao ativar, informe o **percentual máximo** permitido. |
| **Percentual máximo de desconto** | Limite máximo de desconto que o operador pode conceder no terminal. |
| **Lançar Item Após Prévia** | Permite adicionar novos itens a uma comanda depois que a prévia já foi impressa. |
| **Transferência de Comanda** | Permite mover itens ou transferir uma comanda inteira para outra mesa ou comanda. |

---

### 4.3 Comandas

Controla o gerenciamento de **comandas e mesas**.

| Permissão | O que libera |
|---|---|
| **Cadastrar** | Permite criar novas comandas ou mesas no sistema. |
| **Consultar** | Permite visualizar os dados e o histórico das comandas. |
| **Bloquear** | Permite bloquear o acesso a uma comanda específica. |
| **Desbloquear** | Permite liberar uma comanda que estava bloqueada. |
| **Excluir** | Permite excluir permanentemente uma comanda do sistema. |
| **Limpar** | Permite remover todos os itens de uma comanda de uma só vez, zerando-a. |

---

### 4.4 Caderneta

Controla as operações do sistema de **crédito e caderneta de clientes**.

| Permissão | O que libera |
|---|---|
| **Central de Caderneta** | Permite acessar o painel central de gerenciamento da caderneta, com extrato, relatórios e histórico. |
| **Recebimento** | Permite registrar pagamentos recebidos de clientes que têm saldo devedor na caderneta. |
| **Venda Sem Limite de Crédito** | Permite lançar compras na caderneta de um cliente mesmo que ele já tenha atingido o limite de crédito configurado. |
| **Consulta de Vendas** | Permite visualizar o histórico de compras realizadas na caderneta de cada cliente. |
| **Excluir Vendas** | Permite excluir registros de compras da caderneta. |
| **Consultar Pagamentos** | Permite visualizar o histórico de pagamentos feitos pelos clientes. |
| **Excluir Pagamentos** | Permite excluir registros de pagamentos da caderneta. |

---

### 4.5 Cadastros

Controla a **criação de novos registros** no sistema.

| Permissão | O que libera |
|---|---|
| **Produtos** | Permite cadastrar novos produtos. |
| **Grupos** | Permite criar grupos e categorias de produtos. |
| **Clientes** | Permite cadastrar novos clientes. |
| **Clientes — Financeiro** | Permite preencher e salvar os dados financeiros de um cliente (limite de crédito, condições de pagamento, etc.). |
| **Fornecedores** | Permite cadastrar novos fornecedores. |
| **Transportadoras** | Permite cadastrar novas transportadoras. |
| **Entregadores** | Permite cadastrar novos entregadores/motoboys. |
| **Receitas** | Permite cadastrar fichas técnicas e receitas de produtos. |
| **Produções** | Permite cadastrar e gerenciar dados de produção. |
| **Grupos de Impostos** | Permite criar classificações fiscais para os produtos. |
| **Grupos de Preços Diferenciados** | Permite criar tabelas de preços especiais para grupos de clientes. |
| **Grupos de Acompanhamentos** | Permite cadastrar adicionais e modificadores de produtos (ex: "sem cebola", "extra bacon"). |
| **Funcionários** | Permite cadastrar novos funcionários. |
| **Cotações** | Permite criar solicitações de cotação para fornecedores. |
| **Promoções** | Permite criar novas promoções e ofertas. |
| **Motivo de Cancelamento de Item** | Permite cadastrar os motivos disponíveis para cancelamento de itens. |
| **Programa de Fidelidade** | Permite configurar e gerenciar o programa de pontos e fidelidade. |
| **Pedido de Compra** | Permite criar pedidos de compra para fornecedores. |

---

### 4.6 Consultas

Controla a **visualização de dados** já cadastrados. Estas permissões dão acesso somente leitura — o operador vê, mas não altera.

| Permissão | O que libera |
|---|---|
| **Produtos** | Visualizar o cadastro de produtos. |
| **Grupos** | Visualizar grupos e categorias de produtos. |
| **Clientes** | Visualizar o cadastro de clientes. |
| **Fornecedores** | Visualizar o cadastro de fornecedores. |
| **Transportadoras** | Visualizar o cadastro de transportadoras. |
| **Entregadores** | Visualizar o cadastro de entregadores. |
| **Receitas** | Visualizar fichas técnicas e receitas. |
| **Produções** | Visualizar dados de produção. |
| **Grupos de Impostos** | Visualizar classificações fiscais. |
| **Grupos de Preços Diferenciados** | Visualizar tabelas de preços especiais. |
| **Grupos de Acompanhamentos** | Visualizar adicionais e modificadores de produtos. |
| **Funcionários** | Visualizar o cadastro de funcionários. |
| **Cotações** | Visualizar cotações enviadas a fornecedores. |
| **Promoções** | Visualizar promoções cadastradas. |
| **Vendas** | Visualizar o histórico completo de vendas realizadas. |
| **Sangrias** | Visualizar o histórico de retiradas (sangrias) do caixa. |
| **Programa de Fidelidade** | Visualizar pontuações e participantes do programa de fidelidade. |
| **Vouchers** | Visualizar vouchers emitidos e utilizados. |
| **Pedido de Compra** | Visualizar pedidos de compra criados. |

---

### 4.7 Alterações

Controla a **edição de registros** já existentes. Independente de ter permissão de consulta, o operador precisa desta permissão para modificar dados.

| Permissão | O que libera |
|---|---|
| **Produtos** | Editar dados de produtos já cadastrados (nome, preço, estoque mínimo, etc.). |
| **Produtos — Importar Excel** | Permite importar uma planilha para atualizar ou criar produtos em massa. |
| **Grupos** | Editar grupos e categorias de produtos. |
| **Clientes** | Editar dados de clientes cadastrados. |
| **Clientes — Financeiro** | Editar informações financeiras dos clientes (limite de crédito, condições). |
| **Fornecedores** | Editar dados de fornecedores. |
| **Transportadoras** | Editar dados de transportadoras. |
| **Entregadores** | Editar dados de entregadores. |
| **Receitas** | Editar fichas técnicas e receitas de produtos. |
| **Produções** | Editar dados de produção. |
| **Produções — Aprovar Solicitações** | Permite aprovar ou rejeitar solicitações enviadas para produção. |
| **Grupos de Impostos** | Editar classificações fiscais. |
| **Grupos de Preços Diferenciados** | Editar tabelas de preços especiais. |
| **Grupos de Acompanhamentos** | Editar adicionais e modificadores de produtos. |
| **Funcionários** | Editar dados de funcionários. |
| **Cotações** | Editar cotações já criadas. |
| **Promoções** | Editar promoções existentes. |
| **Pedido de Compra** | Editar pedidos de compra já criados. |

---

### 4.8 Pedidos

Controla as operações do **módulo de Pedidos e Delivery**.

| Permissão | O que libera |
|---|---|
| **Lançamento de Pedidos** | Permite criar novos pedidos. |
| **Consultar** | Permite visualizar a lista de pedidos e seus detalhes. |
| **Cancelar Item** | Permite cancelar um item específico dentro de um pedido. |
| **Cancelar Pedido** | Permite cancelar um pedido inteiro. |
| **Conceder Desconto** | Permite aplicar desconto em pedidos. Ao ativar, informe o **percentual máximo** permitido. |
| **Percentual máximo de desconto** | Limite máximo de desconto permitido em pedidos. |
| **Vincular Produtos das Integrações** | Permite associar produtos do SAG com produtos de plataformas externas (iFood, etc.). |
| **Alterar Pedidos** | Permite editar pedidos já lançados (produtos, quantidades, endereço, etc.). |
| **Alterar Pedidos em Entrega/Entregues** | Permite modificar pedidos que já saíram para entrega ou que foram marcados como entregues. |
| **Cancelar Item Antes de Finalizar** | Permite cancelar itens de um pedido antes que ele seja completamente finalizado. |

---

### 4.9 Estoque

Controla as operações do **módulo de Estoque**.

| Permissão | O que libera |
|---|---|
| **Entrada de Estoque** | Permite registrar entradas de produtos (recebimento de notas fiscais, compras). |
| **Consulta de Entrada de Estoque** | Permite visualizar o histórico de entradas realizadas. |
| **Saída de Estoque — Cadastro** | Permite registrar saídas avulsas de produtos (uso interno, perdas, amostras). |
| **Saída de Estoque — Consulta** | Permite visualizar o histórico de saídas registradas. |
| **Ajuste de Estoque** | Permite corrigir manualmente a quantidade de um produto no estoque. |
| **Configurações de Estoque** | Permite acessar as configurações administrativas do módulo de estoque. |
| **Salvar Inventário** | Permite salvar o progresso de uma contagem física de estoque. |
| **Processar Inventário** | Permite aplicar os resultados de uma contagem física, atualizando as quantidades no sistema. |
| **Importar Pedido de Compra** | Permite usar um pedido de compra já criado como base para dar entrada no estoque. |
| **Faturas com Valores Divergentes** | Permite registrar entradas de estoque quando o valor da nota fiscal difere do valor do pedido de compra. |

---

### 4.10 NF-e

Controla as operações de **Nota Fiscal Eletrônica**.

| Permissão | O que libera |
|---|---|
| **Emitir** | Permite gerar e transmitir novas notas fiscais eletrônicas. |
| **Consultar** | Permite visualizar o histórico de notas emitidas. |
| **Configurar** | Permite acessar e alterar as configurações de emissão de NF-e (certificado, série, ambiente). |
| **Consultar Notas Recebidas** | Permite visualizar as notas fiscais recebidas de fornecedores. |
| **Manifestar Notas Recebidas** | Permite confirmar ou rejeitar notas fiscais recebidas junto à Receita Federal. |

---

### 4.11 Financeiro

Controla as operações do **módulo Financeiro**.

| Permissão | O que libera |
|---|---|
| **Configurações** | Permite acessar e alterar as configurações do módulo financeiro (contas bancárias, categorias, espécies). |
| **Adicionar Contas a Pagar** | Permite registrar novas contas a pagar (fornecedores, despesas, obrigações). |
| **Adicionar Contas a Receber** | Permite registrar novas contas a receber (clientes, receitas, cobranças). |
| **Lançar Transferência Bancária** | Permite registrar movimentações entre contas bancárias do próprio estabelecimento. |
| **Efetivar Contas** | Permite confirmar o pagamento ou recebimento de uma conta, marcando-a como liquidada. |
| **Cancelar Contas** | Permite cancelar lançamentos financeiros. |
| **Alterar Contas** | Permite editar dados de contas a pagar ou receber ainda não efetivadas. |
| **Alterar Contas Efetivadas** | Permite modificar contas já liquidadas. Ao ativar, informe em quantos **dias** após a efetivação ainda é possível alterar. |
| **Dias para alterar efetivados** | Define o prazo (em dias) para que uma conta efetivada ainda possa ser modificada. |
| **Lançar Ajustes de Saldo** | Permite fazer correções manuais no saldo de uma conta bancária. |
| **Consultar** | Permite visualizar o extrato financeiro, contas a pagar e a receber. |
| **Central de Faturas** | Permite acessar e operar a central de emissão e controle de faturas/boletos. |
| **Lançar Extrato — Funcionário** | Permite registrar movimentações no extrato financeiro individual de um funcionário. |
| **Lançar Financeiro — Funcionário** | Permite lançar contas a pagar ou a receber vinculadas a funcionários. |
| **Conciliações** | Permite realizar a conciliação bancária e a conciliação de recebíveis (comparar extrato do banco com os lançamentos do sistema). |
| **Alterar Período Contábil** | Permite definir ou modificar a data de corte que bloqueia lançamentos retroativos. |

---

### 4.12 Relatórios

Controla o acesso a cada grupo de **relatórios** disponíveis no sistema.

| Permissão | O que libera |
|---|---|
| **Comandas** | Acesso aos relatórios do módulo de comandas e mesas. |
| **Produtos** | Acesso aos relatórios de produtos (mais vendidos, curva ABC, CMV, etc.). |
| **Fechamentos** | Acesso aos relatórios de fechamentos de caixa e divergências. |
| **Faturamento** | Acesso aos relatórios de faturamento (por dia, por turno, por espécie, etc.). |
| **Cupom** | Acesso aos relatórios de cupons fiscais emitidos e cancelados. |
| **Lucros** | Acesso aos relatórios de lucratividade e mark-up. |
| **Vendas** | Acesso aos relatórios de vendas (estatísticas, comparativos, por vendedor, etc.). |
| **Pedidos** | Acesso aos relatórios do módulo de pedidos e delivery. |
| **Estoque** | Acesso aos relatórios de estoque (consolidado, movimentação, inventário, etc.). |
| **Sangria** | Acesso ao relatório de sangrias e suprimentos do caixa. |
| **Itens Cancelados** | Acesso ao relatório de itens que foram cancelados em vendas. |
| **Outros** | Acesso a relatórios diversos (histórico de preços, programa de fidelidade, TEF, etc.). |
| **Consultas** | Acesso a relatórios gerais de consulta. |
| **Personalizados** | Acesso à aba de criação e execução de relatórios personalizados. |

> **Atenção:** Ter permissão em um grupo de relatórios dá acesso a **todos** os relatórios daquele grupo. Não é possível liberar apenas um relatório específico dentro de um grupo.

---

### 4.13 Outros

Permissões diversas que controlam funcionalidades específicas do sistema.

| Permissão | O que libera |
|---|---|
| **Gestão de Usuários** | Permite criar, editar, ativar, desativar e excluir usuários e grupos de permissão. |
| **Arquivos da Balança** | Permite gerenciar os arquivos de produtos enviados para a balança eletrônica. |
| **Alterar Status Impressora** | Permite ativar ou desativar impressoras cadastradas no sistema. |
| **Tela de Pedidos** | Permite acessar a tela avançada de acompanhamento de pedidos (produção, entregas, kanban). |
| **Módulo IA** | Permite acessar as funcionalidades de inteligência artificial disponíveis no SAG. |
| **Cadastrar Notificações** | Permite criar e editar notificações do sistema para os operadores. |
| **Gerenciar Notificações de Terceiros** | Permite gerenciar notificações oriundas de integrações externas. |
| **Auto Serviço** | Permite acessar e operar a tela de auto-atendimento (totem). |

---

## 5. Exemplos de Perfis Sugeridos

A seguir, sugestões de configuração para os perfis mais comuns em um estabelecimento.

---

### Operador de Caixa

Perfil básico para quem opera o caixa e não precisa acessar configurações.

| Setor | Permissões recomendadas |
|---|---|
| Caixa | Utiliza Caixa, Abrir Gaveta, Finalizar Caixa, Lançar Sangria, Venda com Estoque Negativo, Devolução de Venda, Colocar Venda em Espera, Visualizar Últimas Vendas |
| Caderneta | Recebimento |
| Consultas | Clientes, Produtos |

---

### Atendente de Delivery

Perfil para quem registra e acompanha pedidos, sem acesso ao caixa.

| Setor | Permissões recomendadas |
|---|---|
| Pedidos | Lançamento de Pedidos, Consultar, Cancelar Item, Cancelar Pedido |
| Cadastros | Clientes |
| Consultas | Clientes, Produtos, Pedido de Compra |
| Relatórios | Pedidos |

---

### Gerente Operacional

Perfil para supervisores com acesso amplo, mas sem configurações administrativas.

| Setor | Permissões recomendadas |
|---|---|
| Caixa | Todas, incluindo Cancelar Venda, Desconto (com % definido), Trocar Forma de Pagamento |
| Terminal | Todas |
| Comandas | Todas |
| Caderneta | Todas |
| Cadastros | Todas |
| Consultas | Todas |
| Alterações | Todas |
| Pedidos | Todas |
| Estoque | Todas |
| Relatórios | Todas |
| Financeiro | Consultar, Efetivar, Alterar Contas, Adicionar Contas a Pagar e Receber |

---

### Operador de Estoque

Perfil exclusivo para o setor de recebimento e controle de estoque.

| Setor | Permissões recomendadas |
|---|---|
| Estoque | Todas |
| Consultas | Produtos, Fornecedores |
| Cadastros | Pedido de Compra |
| Relatórios | Estoque |
| NF-e | Consultar, Consultar Notas Recebidas, Manifestar Notas Recebidas |

---

### Analista Financeiro

Perfil para responsável pelo financeiro, sem acesso ao caixa ou estoque.

| Setor | Permissões recomendadas |
|---|---|
| Financeiro | Todas |
| Relatórios | Faturamento, Lucros, Vendas, Outros |
| Consultas | Clientes, Fornecedores |

---

## Observações Gerais

- Permissões de **Consultar** e **Alterar** são independentes — um operador pode ter permissão para consultar clientes sem poder editá-los.
- Permissões com **campo de valor** (como percentual máximo de desconto ou dias para alterar fechamento) só têm efeito quando a permissão pai está ativa.
- Ao alterar as permissões de um grupo, **todos os operadores vinculados são afetados imediatamente**, sem necessidade de reiniciar o sistema.
- O usuário do tipo **Administrador** ignora completamente o sistema de permissões e tem acesso irrestrito a tudo.

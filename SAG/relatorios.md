# SAG — Relatórios

Módulo de geração de relatórios gerenciais e fiscais.

---

## Índice de Módulos

| Módulo | Caminho base | Qtd. |
|---|---|---|
| [Faturamento](#faturamento) | Relatórios → Faturamento | 13 |
| [Vendas](#vendas) | Relatórios → Vendas | 21 |
| [Estoque](#estoque) | Estoque → Relatórios | 14 |
| [Fechamentos de Caixa](#fechamentos-de-caixa) | Relatórios → Fechamentos de Caixa | 3 |
| [Financeiro](#financeiro) | Financeiro → Relatórios | 8 |
| [Lucro e MarkUp](#lucro-e-markup) | Relatórios → Lucro e MarkUp | 3 |
| [Notas Fiscais / Cupons](#notas-fiscais--cupons) | Relatórios → Notas | 8 |
| [Listagem](#listagem) | Relatórios → Listagem | 3 |
| [Funcionários / RH](#funcionários--rh) | Relatórios → Comissões | 1 |
| [Produção](#produção) | Produções → Relatórios | 1 |
| [Itens Cancelados](#itens-cancelados) | Relatórios → Itens Cancelados | 1 |
| [Comandas Abertas](#comandas-abertas) | Relatórios → Comandas Abertas | 1 |
| [Pedidos](#pedidos) | Pedidos → Relatórios | 12 |
| [Outros](#outros) | Relatórios → Outros | 13 |
| [Relatórios Personalizados](#relatórios-personalizados) | Relatórios → Personalizados | 1 |

---

## Faturamento

**Caminho base:** Relatórios → Faturamento

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Faturamento Geral | Relatórios → Faturamento → Geral | Total faturado no período, agrupável por Ano, Mês, Dia ou Hora. Suporta gráfico de linha. |
| Faturamento Por Dia/Hora | Relatórios → Faturamento → Por Dia/Hora | Faturamento distribuído por dia e hora; modo Detalhado ou Resumido. Suporta gráfico de nº de vendas ou valor. |
| Faturamento Por Espécies | Relatórios → Faturamento → Por Espécies | Faturamento segmentado por forma de pagamento (dinheiro, cartão, PIX, voucher etc.). |
| Faturamento Por Turno | Relatórios → Faturamento → Por Turno | Faturamento dividido em turnos configuráveis (início, término e virada de turno). |
| Faturamento Por Tipo de Venda | Relatórios → Faturamento → Por Tipo | Faturamento filtrado por tipo de operação (Venda, NF-e, Pedido), agrupável por Ano, Mês, Dia ou Hora. |
| Faturamento Por Usuário | Relatórios → Faturamento → Por Usuário | Total faturado por operador de caixa. Suporta gráfico comparativo entre operadores. |
| Faturamento Por Caixa | Relatórios → Faturamento → Por Caixa | Total faturado por equipamento/terminal de PDV no período. |
| Faturamento Por Tipo de Pedido | Relatórios → Faturamento → Por Tipo de Pedido | Faturamento por tipo de pedido (mesa, balcão, delivery etc.), agrupável por Ano, Mês, Dia ou Hora. |
| Faturamento Comparativo | Relatórios → Faturamento → Comparativo | Compara o faturamento de dois períodos distintos. Suporta gráfico de barras lado a lado. |
| Faturamento Consolidado | Relatórios → Faturamento → Consolidado | Visão totalizadora do faturamento no período, sem subdivisões. Leitura rápida do resultado geral. |
| Faturamento Por Projeção | Relatórios → Faturamento → Por Projeção | Projeta o faturamento futuro com base no histórico de um período de referência. |
| Faturamento Multi-Loja | Relatórios → Faturamento → Multi-Loja | Consolida e compara o faturamento de todas as unidades da rede. *Exibido somente com multi-loja habilitado.* |
| Faturamento Comparativo Multi-Loja | Relatórios → Faturamento → Comparativo Multi-Loja | Compara o faturamento de duas unidades da rede em dois períodos distintos. *Exibido somente com multi-loja habilitado.* |

---

## Vendas

**Caminho base:** Relatórios → Vendas

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Estatísticas de Vendas | Relatórios → Vendas → Estatísticas | Resumo estatístico: ticket médio, total de pedidos, média de itens por venda e outras métricas do período. |
| Curva ABC — Itens | Relatórios → Vendas → Curva ABC - Itens | Classifica produtos em A, B e C por participação no faturamento ou quantidade vendida. Filtrável por grupo, subgrupo e origem. |
| Curva ABC — Grupos | Relatórios → Vendas → Curva ABC - Grupos | Análise Curva ABC no nível de grupos e subgrupos de produtos. Agrupável por grupo ou por dia. |
| CMV Por Produto | Relatórios → Vendas → CMV por Produto | CMV item a item: preço de custo, preço de venda, qtd. vendida, total e percentual de CMV sobre a receita. |
| Vendas Por Produto | Relatórios → Vendas → Vendas por Produto | Produtos vendidos com quantidade e valor total. Filtrável por grupo, subgrupo e funcionário. |
| Comparativo de Produtos | Relatórios → Vendas → Comparativo de Produtos | Compara a venda de produtos entre dois períodos, com variação de quantidade e valor por item. |
| Desconto de Venda | Relatórios → Vendas → Desconto de Venda | Todos os descontos concedidos: usuário que autorizou, valor original, desconto aplicado e percentual. |
| Produtos Mais Vendidos | Relatórios → Vendas → Produtos Mais Vendidos | Ranking de produtos por maior volume, ordenável por quantidade ou valor. |
| Vendas Por Vendedor e Comandas | Relatórios → Vendas → Vendas por Vendedor e Comandas | Vendas por garçom/atendente vinculadas às comandas, com valor lançado por operador e total por comanda. |
| Vendas Por Caixa | Relatórios → Vendas → Vendas por Caixa | Vendas agrupadas por terminal de caixa, com totais e formas de pagamento por equipamento. |
| Vendas Por Grupo | Relatórios → Vendas → Vendas por Grupo | Vendas totalizadas por grupo de produtos, com participação de cada categoria no total do período. |
| Vendas Por Produtos e Funcionário | Relatórios → Vendas → Vendas por Produtos e Funcionário | Cruzamento de produtos vendidos × funcionário responsável, com quantidade e valor por operador. |
| Vendas Por Espécie | Relatórios → Vendas → Vendas por Espécie | Valores recebidos por forma de pagamento (dinheiro, crédito, débito, PIX, cheque etc.). |
| Vendas Por Turno | Relatórios → Vendas → Vendas por Turno | Vendas divididas em turnos configuráveis para análise de desempenho por período do dia. |
| Vendas Por Semana | Relatórios → Vendas → Vendas por Semana | Vendas distribuídas por dia da semana, identificando os dias de maior e menor movimento. |
| Vendas Por Cliente | Relatórios → Vendas → Vendas por Cliente | Histórico de compras por cliente: total consumido, quantidade de visitas e ticket médio no período. |
| Vendas — Multi-Loja | Relatórios → Vendas → Vendas - Multiloja | Consolida a venda de produtos entre todas as unidades da rede. *Exibido somente com multi-loja habilitado.* |
| Pesquisa de Vendas | Relatórios → Vendas → Pesquisa de Vendas | Consulta avançada de vendas por data, cliente, usuário, valor ou produto. Exibe os itens de cada venda. |
| Taxa de Serviço | Relatórios → Vendas → Taxa de Serviço | Valores cobrados como taxa de serviço (gorjeta) por usuário, turno ou dia. *Somente se taxa de serviço estiver habilitada.* |
| Vendas Por Usuário | Relatórios → Vendas por Usuário | Total vendido por funcionário/atendente, em modo analítico (detalhado) ou resumido. Filtrável por usuário. |
| Comparativo de Períodos | Relatórios → Vendas → Comparativo de Períodos | Compara vendas de produtos em dois intervalos de datas, com variação absoluta e percentual. |

---

## Estoque

**Caminho base:** Estoque → Relatórios

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Estoque Mínimo | Estoque → Relatórios → Estoque Mínimo | Produtos com saldo abaixo do nível mínimo configurado. Filtrável por grupo, subgrupo, departamento e local de estoque. |
| Estoque Máximo | Estoque → Relatórios → Estoque Máximo | Produtos com saldo acima do nível máximo configurado, indicando possíveis excessos. |
| Estoque Consolidado | Estoque → Relatórios → Estoque Consolidado | Saldo atual de todos os produtos, agrupável por grupo/subgrupo, local de estoque e departamento. |
| Histórico do Produto | Estoque → Relatórios → Histórico do Produto | Movimentação completa de entrada e saída de um produto específico no período: data, tipo de operação e quantidade. |
| Nível de Estoque | Estoque → Relatórios → Nível de Estoque | Saldo atual comparado com os limites mínimo e máximo cadastrados. Identifica produtos em situação crítica. |
| Saída de Estoque | Estoque → Relatórios → Saída de Estoque | Saídas de mercadoria no período (vendas, perdas, transferências) com data, produto, quantidade e responsável. |
| Entrada de Estoque | Estoque → Relatórios → Entrada de Estoque | Entradas de mercadoria no período (compras, devoluções de clientes) com data, fornecedor, produto e quantidade. |
| Transferência de Estoque | Estoque → Relatórios → Transferência de Estoque | Transferências de produtos entre locais de estoque ou unidades, com origem, destino e data. |
| Inventário Estoque | Estoque → Relatórios → Inventário Estoque | Ficha de inventário com saldos do sistema e campos em branco para preenchimento da contagem física. |
| Movimento de Estoque | Estoque → Relatórios → Movimento de Estoque | Todas as movimentações (entradas + saídas) do período com saldo inicial e saldo final. |
| Multiloja — Estoque Consolidado | Estoque → Relatórios → Multiloja - Estq. Consolidado | Saldo de estoque consolidado de todas as unidades da rede. *Somente com multi-loja habilitado.* |
| Lote — Validade | Estoque → Relatórios → Lote - Validade | Produtos controlados por lote com datas de validade e quantidades em estoque. Auxilia no controle PVPS. |
| Perda Por Faturamento | Estoque → Relatórios → Perda por Faturamento | Perdas de mercadorias no período relacionadas ao faturamento gerado. Auxilia no controle de desperdícios. |
| Ajuste de Estoque | Estoque → Relatórios → Ajuste de Estoque | Ajustes manuais de saldo no período: produto, quantidade ajustada, usuário responsável e motivo. |

---

## Fechamentos de Caixa

**Caminho base:** Relatórios → Fechamentos de Caixa

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Fechamento de Caixa | Relatórios → Fechamentos de Caixa → (selecionar fechamento) | Relatório completo de um fechamento específico: totais por forma de pagamento, sangrias, suprimentos, cancelamentos e resultado líquido. |
| Divergências de Fechamento de Caixa | Relatórios → Fechamento de Caixa → Divergências | Diferenças entre o valor calculado pelo sistema e o valor informado pelo operador no fechamento. Essencial para identificar inconsistências. |
| Sangrias | Relatórios → Entradas e Saidas | Todas as sangrias (retiradas de dinheiro) dos caixas no período: data, horário, usuário, valor e justificativa. |

---

## Financeiro

**Caminho base:** Financeiro → Relatórios

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Contas a Pagar | Financeiro → Relatórios → Contas a Pagar | Compromissos a pagar, filtrável por favorecido, categoria, conta bancária e situação (aberto/efetivado). Tipo de data: vencimento, pagamento, inserção ou competência. Disponível em modo analítico. |
| Acréscimos e Descontos — Pagos | Financeiro → Relatórios → Acréscimos e Descontos - Pagos | Acréscimos (juros/multas) e descontos aplicados nas quitações de contas a pagar do período. |
| Contas a Receber | Financeiro → Relatórios → Contas a Receber | Títulos a receber por credor, categoria e conta bancária. Mesmos filtros de situação e data das Contas a Pagar. |
| Acréscimos e Descontos — Recebidos | Financeiro → Relatórios → Acréscimos e Descontos - Recebidos | Acréscimos e descontos aplicados nos recebimentos de contas a receber do período. |
| Extrato | Financeiro → Relatórios → Extrato | Extrato de conta bancária ou caixa: lançamentos de débito e crédito com saldo progressivo. |
| Fluxo de Caixa | Financeiro → Relatórios → Fluxo de Caixa | Entradas e saídas financeiras do período com saldo diário e acumulado. |
| DRE — Demonstração de Resultado | Financeiro → Relatórios → DRE | DRE sintética: receitas, deduções, custos e despesas para apurar o lucro/prejuízo do período por categoria financeira. |
| Contas a Pagar Por Grupo Fornecedor | Financeiro → Relatórios → Contas a Pagar Por Grupo Fornecedor | Contas a pagar agrupadas por grupo/categoria de fornecedor com totais por agrupamento. |

---

## Lucro e MarkUp

**Caminho base:** Relatórios → Lucro e MarkUp

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Lucro | Relatórios → Lucro e MarkUp → Lucro | Lucro bruto confrontando receita de vendas com o CMV. Filtrável por grupo e subgrupo de produtos. |
| MarkUp | Relatórios → Lucro e MarkUp → MarkUp | Índice de mark-up (multiplicador sobre o custo) por produto ou grupo. Permite filtrar por faixa de mark-up. |
| Lucro Por Fornecedor | Relatórios → Lucro e MarkUp → Fornecedor | Lucro gerado pelos produtos de cada fornecedor, cruzando vendas com custo de aquisição. |

---

## Notas Fiscais / Cupons

**Caminho base:** Relatórios → Notas

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Cupons / Notas Emitidas — Geral | Relatórios → Notas → Geral | Todos os cupons e notas fiscais emitidos no período. Filtrável por tipo (NFC-e, NF-e ou ambas). Exibe nº, data, valor e situação. |
| Impostos das Notas Emitidas | Relatórios → Notas → Impostos | Valores de impostos (ICMS, PIS, COFINS etc.) das notas emitidas. Essencial para conciliação fiscal. |
| Itens Por Nota | Relatórios → Notas → Produtos | Produtos detalhados de cada nota/cupom: quantidade, valor unitário, total e tributação por item. |
| NFCe Inutilizadas | Relatórios → Notas → Inutilizadas | Números de NFC-e inutilizados perante a SEFAZ com motivo de cada inutilização. |
| Notas / Cupons Cancelados | Relatórios → Notas → Canceladas | Documentos fiscais cancelados no período: data, número, valor, tipo e motivo do cancelamento. |
| Notas Recebidas | Relatórios → Notas → Recebidas | Notas fiscais de entrada recebidas de fornecedores: data, fornecedor, valor e impostos. Filtrável por fornecedor. |
| CFOP | Relatórios → Notas → CFOP | Operações fiscais totalizadas por CFOP, separadas por entrada ou saída. Auxilia no preenchimento de declarações fiscais. |
| Cupons em Contingência | Relatórios → Notas → Contingência | Documentos emitidos em modo offline (sem conexão com a SEFAZ) com status de transmissão pendente. |

---

## Listagem

**Caminho base:** Relatórios → Listagem

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Listagem de Produtos | Relatórios → Listagem → Produto | Catálogo dos produtos cadastrados. Filtrável por nome/código, grupo, subgrupo e situação (ativo/inativo). |
| Listagem de Usuários | Relatórios → Listagem → Usuário | Usuários cadastrados, filtrável por perfil (Usuário/Administrador) e situação. |
| Listagem de Funcionários | Relatórios → Listagem → Funcionário | Funcionários cadastrados com nome, cargo e dados de contato. Filtrável por ativos. |

---

## Funcionários / RH

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Comissões de Funcionários | Relatórios → Comissões | Comissões devidas a cada funcionário com base nas regras e vendas do período. Versões analítica (por venda) e sintética (somente totais). Permite informar percentual de desconto sobre as comissões. |

---

## Produção

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Produção | Produções → Relatórios | Itens enviados à produção (cozinha, bar etc.) no período: produtos, quantidades, horários e status. Filtrável por grupo, subgrupo, status, origem e tipo de pedido. |

---

## Itens Cancelados

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Itens Cancelados | Relatórios → Itens Cancelados | Itens cancelados em vendas ou pedidos: data, horário, usuário, produto, quantidade e valor. Filtrável por usuário. |

---

## Comandas Abertas

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Comandas Abertas | Relatórios → Comandas Abertas | Comandas/mesas em aberto com nº da comanda, valor consumido e tempo decorrido desde a abertura. |

---

## Pedidos

**Caminho base:** Pedidos → Relatórios

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Produção (Pedidos) | Pedidos → Relatórios → Produção | Itens enviados à produção a partir de pedidos. Filtrável por tipo de data, grupo, subgrupo, status, origem e tipo (Pedido, Encomenda, Orçamento, Romaneio). |
| Pedidos Resumidos | Pedidos → Relatórios → Pedidos Resumidos | Pedidos do período de forma sintética, com totais por pedido sem detalhamento de itens. |
| Pedidos Por Origem | Pedidos → Relatórios → Pedidos Por Origem | Pedidos classificados por canal de origem (iFood, SAG, WhatsApp, telefone, balcão etc.) com volume e valor por canal. |
| Pedidos Completos | Pedidos → Relatórios → Pedidos Completos | Todos os pedidos com detalhamento completo: itens, quantidades, valores, status, forma de pagamento e dados do cliente. |
| Pedidos Por Entregador | Pedidos → Relatórios → Pedidos Por Entregador | Entregas por motoboy/entregador: quantidade de pedidos entregues e valor total por colaborador. |
| Pedidos Por Usuário | Pedidos → Relatórios → Pedidos Por Usuário | Pedidos agrupados e totalizados por operador/atendente no período. |
| Consulta de Vendas (Pedidos) | Pedidos → Relatórios → Consulta de Vendas | Pesquisa de vendas originadas de pedidos por data, cliente, usuário ou produto. Exibe detalhes de cada venda. |
| Produtos Por Pedido | Pedidos → Relatórios → Produtos por Pedido | Produtos de cada pedido com quantidade solicitada, valor unitário e total por item. |
| Resumo de Pedidos | Pedidos → Relatórios → Resumo de Pedidos | Painel de indicadores: total de pedidos, valor total, ticket médio e pedidos por hora no período. |
| Histórico dos Pedidos | Pedidos → Relatórios → Histórico dos Pedidos | Histórico cronológico de pedidos com status (aberto, fechado, cancelado). |
| Taxas Por Origem | Pedidos → Relatórios → Taxas por Origem | Valores de taxas (entrega, serviço etc.) segmentados por canal de origem dos pedidos. |
| Pedidos Alterados | Pedidos → Relatórios → Pedidos Alterados | Pedidos que sofreram modificações após o registro original: o que foi alterado, quem e quando. |

---

## Outros

**Caminho base:** Relatórios → Outros

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Prévias Impressas | Relatórios → Outros → Prévias Impressas | Histórico de prévias de conta entregues aos clientes antes do fechamento: data, horário, comanda e valor. |
| Previsão de Recebimentos | Relatórios → Outros → Previsão de Recebimentos | Recebimentos futuros projetados pelas taxas e prazos das operadoras de cartão, por bandeira e data de liquidação. |
| Histórico de Alteração de Preço | Relatórios → Outros → Histórico de Alteração de Preço | Alterações de preço de venda nos produtos: valor anterior, valor novo, data e usuário. Filtrável por produto, grupo ou subgrupo. |
| Histórico de Alteração de Custo | Relatórios → Outros → Histórico de Alteração de Custo | Alterações de preço de custo nos produtos: custo anterior, custo novo, data e usuário. |
| Idade do Produto | Relatórios → Outros → Idade do Produto | Produtos sem movimentação (giro zero), com base na data de cadastro, primeira venda ou última venda. |
| Transações TEF | Relatórios → Outros → Transações TEF | Transações de cartão via TEF no período: bandeira, modalidade (crédito/débito), NSU e valor. |
| Cancelamentos TEF | Relatórios → Outros → Cancelamentos TEF | Cancelamentos de transações via TEF: NSU, bandeira, data e valor. Auxilia na conciliação com operadoras. |
| Transferência de Itens entre Comandas | Relatórios → Outros → Transferência Itens Comanda | Itens movidos entre comandas/mesas: produto, quantidade, comanda origem, comanda destino e usuário. |
| Produto Por Fornecedor | Relatórios → Outros → Produto por Fornecedor | Produtos vinculados a cada fornecedor com código, descrição e preço de custo. Filtrável por fornecedor, grupo e subgrupo. |
| Análise de Venda | Relatórios → Outros → Análise de Venda | Vendas de produtos por canal de origem (venda direta, delivery etc.) com quantidade por produto e origem. Filtrável por grupo, subgrupo e insumos. |
| Cupons Utilizados | Relatórios → Outros → Cupons Utilizados | Cupons de desconto utilizados nas vendas: código, desconto, venda em que foi aplicado e validade. |
| Programa de Fidelidade | Relatórios → Outros → Programa de Fidelidade | Extrato de pontos dos clientes: pontos acumulados, resgatados e saldo atual por participante no período. |
| Vouchers | Relatórios → Outros → Vouchers | Vouchers gerados e/ou utilizados: código, valor, data de geração, validade e status (disponível/utilizado/vencido). |
| Cartão de Acesso | Relatórios → Cartão de Acesso | Cartão de acesso do cliente com código de identificação (código de barras ou QR Code) para controle de entrada. |

---

## Relatórios Personalizados

| Relatório | Caminho completo | Descrição |
|---|---|---|
| Relatórios Personalizados | Relatórios → Personalizados | Motor de relatórios dinâmicos com layouts e campos definidos pelo estabelecimento. O usuário seleciona as informações e filtros conforme a necessidade. |

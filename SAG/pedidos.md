# Módulo Delivery e Pedidos — Documentação de Uso

Guia completo dos módulos de Pedidos e Delivery do SAG: criar pedidos, acompanhar entregas, gerenciar entregadores, configurar origens e acessar relatórios.

---

## Índice

1. [Novo Pedido](#1-novo-pedido)
2. [Consulta de Pedidos](#2-consulta-de-pedidos)
3. [Visão Kanban de Pedidos](#3-visão-kanban-de-pedidos)
4. [Últimos Pedidos do Cliente](#4-últimos-pedidos-do-cliente)
5. [Detalhes do Pedido](#5-detalhes-do-pedido)
6. [Mudar Status do Pedido](#6-mudar-status-do-pedido)
7. [Mapa de Endereços](#7-mapa-de-endereços)
8. [Entregadores](#8-entregadores)
9. [Origens de Pedido](#9-origens-de-pedido)
10. [Integrações com Plataformas Externas](#10-integrações-com-plataformas-externas)
11. [Status Possíveis de um Pedido](#11-status-possíveis-de-um-pedido)
12. [Atalhos de Teclado](#12-atalhos-de-teclado)
13. [Relatórios de Pedidos](#13-relatórios-de-pedidos)

---

## 1. Novo Pedido

**Pedidos → Novo Pedido**

### Seção: Cliente

| Campo | O que preencher |
|---|---|
| **Telefone** | Digite o telefone para buscar o cliente — os dados são preenchidos automaticamente se já estiver cadastrado |
| **Nome do Cliente** | Exibido automaticamente após a busca |
| **Origem** | De onde veio o pedido: SAG, iFood, WhatsApp, telefone, balcão, etc. |
| **Código Externo** | Código do pedido em plataforma externa (ex: número do pedido no iFood) |
| **Tipo** | **Pedido** (padrão), **Encomenda** (data futura) ou **Orçamento** (para aprovação posterior) |

### Seção: Entrega ou Retirada

**Entrega:**
- Selecione **Entrega** e escolha o endereço do cliente.
- O sistema calcula a distância automaticamente via Google Maps.
- Se precisar recalcular, clique em **Recalcular Distância**.

**Retirada:**
- Selecione **Retirada** — campos de endereço ficam ocultos.
- Informe a **Data** e **Hora** combinadas para a retirada.
- Se o cliente vai pagar um sinal antecipado, informe no campo **Sinal**.

### Seção: Produtos

1. Busque o **Produto** pelo nome ou código.
2. Informe a **Quantidade** e clique em **Adicionar**.
3. Repita para todos os produtos.

Na lista de itens você pode editar, aplicar desconto ou cancelar um item já lançado.

### Totais

| Campo | Descrição |
|---|---|
| **Subtotal** | Soma de todos os itens sem desconto |
| **Desconto** | Desconto aplicado ao pedido |
| **Total** | Valor final a ser cobrado |

### Finalizar

- **Salvar** — registra o pedido com status **Em Andamento**.

> Se o cliente tiver observações cadastradas (ex: "interfone quebrado"), elas aparecem automaticamente na tela para orientar o atendente.

---

## 2. Consulta de Pedidos

**Pedidos → Consulta de Pedidos**

Painel central de acompanhamento de todos os pedidos.

### Filtros disponíveis

| Filtro | O que faz |
|---|---|
| **Filtrar Por** | Período por data do pedido ou data de retirada |
| **De / À** | Período de busca |
| **Status** | Em Andamento, Pronto, Em Entrega, Finalizado, Cancelado, etc. |
| **Tipo** | Pedido, Orçamento, Encomenda ou Todos |
| **Pagamento** | Pago, Não Pago ou Todos |
| **Entrega/Retirada** | Apenas entregas, apenas retiradas, ou todos |
| **Cliente** | Busca parcial pelo nome |
| **Telefone** | Busca pelo número |
| **Origem** | SAG, iFood, etc. |
| **Código** | Número do pedido ou código externo |
| **Consulta MultiLoja** | Pedidos de todas as filiais ao mesmo tempo |

### Cores da lista

| Cor | Situação |
|---|---|
| **Verde** | Pedido finalizado |
| **Vermelho** | Pedido cancelado |
| **Amarelo** | Pedido em entrega |
| **Cinza** | Retirada em andamento |
| **Branco** | Pedido em aberto / aguardando |

### Ações disponíveis por pedido

| Botão | O que faz |
|---|---|
| **Marcar como Pronto** | Pedido pronto para sair |
| **Marcar em Entrega** | Entregador saiu |
| **Finalizar** | Encerra o pedido como entregue e pago |
| **Cancelar** | Cancela o pedido |
| **Imprimir** | Imprime o pedido |
| **Emitir Cupom** | Emite o cupom fiscal |
| **Reimprimir Cupom** | Reimprime o cupom já emitido |
| **Enviar E-mail** | Envia o pedido por e-mail ao cliente |
| **Emitir NF-e** | Emite Nota Fiscal Eletrônica |
| **Vincular Comanda** | Associa o pedido a uma comanda do caixa |

### Alteração em lote

1. Ative **Alteração em Lote** no menu superior.
2. Selecione os pedidos marcando as caixas de seleção.
3. Escolha a ação: Pronto, Em Entrega, Cancelar, Emitir cupons ou Finalizar.

---

## 3. Visão Kanban de Pedidos

**Pedidos → Consulta Kanban**

Exibe os pedidos em colunas por status. Para mudar o status, **arraste o cartão** para a coluna desejada.

Colunas: **Em Andamento → Pronto → Em Entrega → Finalizado → Cancelado**

---

## 4. Últimos Pedidos do Cliente

**Pedidos → Últimos Pedidos** *(ou F7 na tela de novo pedido)*

1. Selecione o cliente e pressione **F7**.
2. Defina o período desejado.
3. A lista exibe todos os pedidos anteriores com data, tipo e valor total.
4. Clique em **Refazer Pedido** para criar um novo copiando todos os itens.

---

## 5. Detalhes do Pedido

**F4 na tela de pedidos**

| Campo | O que preencher |
|---|---|
| **Entregador** | Entregador responsável pela entrega |
| **Data e Hora de Retirada** | Horário previsto para entrega ou retirada |
| **Observações** | Anotações internas sobre o pedido |

---

## 6. Mudar Status do Pedido

Ao clicar em **Marcar em Entrega**, o sistema abre uma tela para definir como a entrega será feita.

### Aba: Interno

Para entregas feitas pelo próprio entregador do estabelecimento:

| Campo | O que preencher |
|---|---|
| **Entregador** | Entregador que vai sair |
| **Data de Retirada** | Data da saída para entrega |
| **Entregue** | Marque quando a entrega for confirmada |

### Aba: Externo

Para entregas via plataformas de logística (Loggi, iFood Delivery, Uber Direct, etc.):

1. Selecione a **plataforma de entrega**.
2. Clique em **Solicitar Entregador**.
3. Após aceite, clique em **Rastrear Entrega** para acompanhar a rota em tempo real.

---

## 7. Mapa de Endereços

**Pedidos → Mapa**

| Modo | O que exibe |
|---|---|
| **Mapa de Calor** | Regiões com maior concentração de pedidos |
| **Mapa de Pedidos** | Cada pedido como um ponto no mapa |

Na Consulta de Pedidos, expanda a linha do pedido para ver endereço completo, **Copiar Endereço** e **Copiar Link de Rastreio**.

---

## 8. Entregadores

### Cadastro de Entregadores

**Pedidos → Entregadores → Cadastrar**

| Campo | O que preencher |
|---|---|
| **Nome** | Nome completo |
| **CPF / RG / CNPJ / CNH** | Documentos |
| **Validade da CNH** | Data de vencimento |
| **Diária** | Valor da diária (se aplicável) |
| **Ativo** | Marque para aparecer nas listas de seleção |
| **Telefone / Celular / E-mail** | Contato |
| **CEP / Endereço** | Ao digitar o CEP, o endereço é preenchido automaticamente |

### Consulta de Entregadores

**Pedidos → Entregadores → Consultar**

- Marque **Apenas Ativos** para exibir somente entregadores disponíveis.
- Dê **duplo clique** para abrir e editar o cadastro.

---

## 9. Origens de Pedido

**Pedidos → Origens**

As origens identificam de onde cada pedido veio (SAG, iFood, WhatsApp, telefone, balcão, etc.).

### Como cadastrar uma origem

| Campo | O que preencher |
|---|---|
| **Descrição** | Nome da origem |
| **Cliente Padrão** | Cliente vinculado automaticamente (útil para origens sem cliente identificado) |
| **Delivery** | Marque se aceita pedidos para entrega |
| **Habilita Código Externo** | Marque se o pedido vem com código de plataforma externa |
| **Baixa Automática** | Pedidos pré-pagos são finalizados automaticamente |
| **Taxa Fixa / Taxa Porcentagem** | Taxas cobradas por pedido dessa origem |

---

## 10. Integrações com Plataformas Externas

> **ATENÇÃO:** As integrações de delivery (iFood, 99food, Keeta, OpenDelivery, etc.) são serviços Windows que rodam no servidor. O cliente **não tem acesso, não consegue visualizar e não sabe se está configurado**. Qualquer problema com integração → ESCALAR_SUPORTE imediatamente.

> **Código PDV:** Nas plataformas de integração (iFood, etc.), o campo chamado **"Código PDV"** corresponde ao **código do produto cadastrado no SAG** (Cadastros > Produtos > campo Código).

### Plataformas disponíveis para logística de entregadores

| Plataforma | Tipo |
|---|---|
| **Loggi** | Solicitação + rastreamento em tempo real |
| **iFood Delivery** | Solicitação via plataforma iFood |
| **Uber Direct** | Entregador via Uber |
| **BeDelivery / 99Food / Keeta / Loocal / OpenDelivery** | Plataformas regionais e abertas |

---

## 11. Status Possíveis de um Pedido

| Status | Significado |
|---|---|
| **Não Confirmado** | Pedido recebido aguardando confirmação |
| **Confirmado** | Confirmado, ainda não iniciado |
| **Em Andamento** | Em produção / sendo preparado |
| **Pronto** | Pronto para sair para entrega ou retirada |
| **Em Entrega** | Entregador a caminho |
| **Entregue** | Entrega confirmada |
| **Faturado** | Nota fiscal emitida |
| **Finalizado** | Entregue e pago |
| **Cancelado** | Cancelado pelo cliente ou estabelecimento |

**Fluxo normal:** Não Confirmado → Confirmado → Em Andamento → Pronto → Em Entrega → Entregue → Finalizado

---

## 12. Atalhos de Teclado — Novo Pedido

| Tecla | Função |
|---|---|
| **F1** | Cancela o item selecionado |
| **F2** | Consulta de produtos |
| **F3** | Cancela o pedido inteiro |
| **F4** | Detalhes do pedido (entregador, observações, data) |
| **F5** | Consulta de pedidos |
| **F6** | Vincula o pedido a uma comanda do caixa |
| **F7** | Últimos pedidos do cliente |
| **F10** | Inserir pizza |
| **F11** | Finalizar o pedido na caderneta |
| **F12** | Exibir o caixa |
| **Ctrl + D** | Desconto no item |
| **Ctrl + –** | Desconto no pedido inteiro |
| **ESC** | Sair |

---

## 13. Relatórios de Pedidos

**Pedidos → Relatórios**

Os relatórios ficam organizados em abas. Cada aba tem seus próprios filtros e botão **Gerar Relatório**.

---

### Produção

Exibe os itens que precisam ser produzidos no período, agrupando produtos de todos os pedidos.

**Tipos de relatório:**

| Tipo | O que exibe |
|---|---|
| **Pedido Resumido** | Lista pedidos com totais, sem detalhar itens |
| **Pedido Completo** | Cada pedido com todos os itens |
| **Total dos Produtos** | Quantidade total de cada produto nos pedidos |
| **Total dos Produtos com Receita** | Igual ao anterior + ficha técnica de cada produto |

---

### Pedidos Resumidos

Lista os pedidos com informações básicas: cliente, data, valor e status.

**Filtros:** Tipo de Data, Período, Status, Tipo, Cliente, Apenas Pagos, Agrupar por Cliente, Agrupar por Estabelecimento.

---

### Pedidos por Origem

Analisa quantos pedidos e qual o valor gerado por cada canal de venda.

**Filtros:** Tipo de Data, Período, Status, Origem, Cliente, Apenas Pagos, Agrupar por Dia, Gerar Gráfico.

---

### Pedidos Completos

Exibe o detalhamento completo: dados do cliente, endereço, itens, valores e formas de pagamento.

**Filtros:** Tipo de Data, Período, Status, Tipo, Cliente, Entregador, Apenas Pagos.

---

### Pedidos por Entregador

Exibe quantas entregas cada entregador realizou e o custo total. Usado para calcular o pagamento dos motoboys.

| Opção de cálculo | Como funciona |
|---|---|
| **Taxa de Entrega** | Usa o valor de frete cobrado em cada pedido |
| **Valor por Entrega** | Define um valor fixo por entrega realizada |

---

### Pedidos por Usuário

Mostra quantos pedidos cada operador registrou no período, com os valores correspondentes.

**Filtros:** Tipo de Data, Período, Usuário, Apenas Pagos, Incluir Orçamentos.

---

### Consulta de Vendas

Busca vendas associadas a pedidos com filtros detalhados: Período, Produto, Comanda, Valor da Venda, Tipo.

---

### Produtos por Pedido

Exibe quais produtos foram mais pedidos, com quantidades e valores.

**Agrupamentos:** Por Origem, Por Cliente ou Por Produto.

---

### Resumo de Pedidos

Exibe um resumo quantitativo agrupado por intervalo de tempo.

**Agrupamentos por tempo:** Por Dia, Por Hora (identifica picos), Por Mês, Sem Agrupamento.

---

### Histórico dos Pedidos

Exibe o histórico completo de alterações de um pedido específico — quem alterou, o que foi alterado e quando.

1. Informe o **Código do Pedido**.
2. Defina o **Período** se quiser restringir.
3. Clique em **Gerar Relatório**.

---

### Taxas por Origem

Analisa as taxas cobradas e custos gerados por cada origem de pedido. Útil para calcular a margem real por canal.

**Filtros:** Período, Origem, Agrupar, Incluir Meios de Pagamento.

---

### Exportar Dados

Exporta os pedidos do período em arquivo para uso em planilhas ou sistemas de BI.

| Opção | O que exporta |
|---|---|
| **Pedidos Detalhados** | Cada item de cada pedido em linhas separadas |
| **Pedidos Resumidos** | Um registro por pedido, sem detalhar itens |

**Exportar Multiloja** — exporta dados de todas as filiais em um único arquivo.

---

### Pedidos Alterados

Lista todos os pedidos modificados após o lançamento inicial: o que foi alterado, por quem e quando.

**Filtros:** Tipo de Data, Período, Status, Tipo, Origem, Cliente, Usuário, Código do Pedido.

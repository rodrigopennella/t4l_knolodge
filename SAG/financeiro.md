# Módulo Financeiro — Documentação de Uso

Guia completo das funcionalidades do módulo Financeiro do SAG. Aqui você encontra como lançar contas, efetivar pagamentos, realizar transferências, conciliar o banco e consultar relatórios financeiros.

---

## Índice

1. [Contas a Pagar e Receber](#1-contas-a-pagar-e-receber)
2. [Extrato Financeiro](#2-extrato-financeiro)
3. [Efetivar Contas](#3-efetivar-contas)
4. [Transferência Bancária](#4-transferência-bancária)
5. [Ajuste de Conta](#5-ajuste-de-conta)
6. [Conciliação Bancária](#6-conciliação-bancária)
7. [Lançamento de Comissões](#7-lançamento-de-comissões)
8. [Faturas](#8-faturas)
9. [Cadastros de Apoio](#9-cadastros-de-apoio)
10. [Relatórios Financeiros](#10-relatórios-financeiros)

---

## 1. Contas a Pagar e Receber

**Financeiro → Contas a Pagar** ou **Financeiro → Contas a Receber**

> **Importante:** Estas telas servem **exclusivamente para lançar novas contas**. Para **consultar, localizar ou verificar** lançamentos existentes — incluindo baixas em aberto — utilize o **Extrato** (seção 2).

Esta é a tela principal de lançamento financeiro. Utilize-a para registrar qualquer conta que o estabelecimento precisa pagar (fornecedor, aluguel, energia, etc.) ou receber (de clientes, contratos, etc.).

### Como lançar uma conta

Ao abrir a tela de cadastro, preencha as informações nas duas abas disponíveis:

### Aba: Informações

| Campo | O que preencher |
|---|---|
| **Descrição** | Nome ou identificação da conta (ex: "Conta de energia maio", "Parcela fornecedor X") |
| **Conta Bancária** | Conta do estabelecimento que será debitada ou creditada |
| **Espécie** | Forma de pagamento (dinheiro, boleto, transferência, etc.) |
| **Cliente / Fornecedor** | Quem vai receber ou quem cobrou. Digite o nome para buscar. |
| **Categoria** | Categoria financeira para organização e relatórios (ex: "Despesas Fixas", "Receitas de Vendas") |
| **Data de Vencimento** | Quando a conta vence ou deve ser recebida |
| **Data de Competência** | A qual período financeiro esta conta pertence (pode diferir do vencimento) |
| **Valor** | Valor total da conta |
| **NF Série / NF Número** | Número e série da nota fiscal vinculada, se houver |
| **Boleto** | Código do boleto, se aplicável |
| **Observação** | Qualquer anotação adicional sobre este lançamento |

Após preencher, você tem três opções:

- **Salvar** — salva a conta com status "Aguardando" (ainda não paga/recebida).
- **Salvar e Efetivar** — salva e já marca a conta como paga ou recebida.
- **Aguardando** — se a conta já estava efetivada, use este botão para revertê-la ao status pendente.

### Aba: Repetições

Use esta aba quando a conta se repete ao longo do tempo, como aluguel, mensalidades ou parcelas fixas.

1. Marque a opção **Repetir** para ativar.
2. Escolha o **Tipo de Repetição**: diariamente, semanalmente, quinzenalmente, mensalmente, semestralmente ou anualmente.
3. Informe o **Número de Repetições** (quantas vezes a conta vai se repetir).
4. O sistema gera automaticamente uma lista com todas as parcelas. Você pode editar individualmente a descrição, data, valor e boleto de cada parcela antes de salvar.

---

## 2. Extrato Financeiro

**Financeiro → Extrato**

> **Use o Extrato para consultar lançamentos.** Sempre que o cliente quiser localizar, verificar ou gerenciar entradas/saídas — baixas em aberto, vencidas, efetivadas — o caminho correto é aqui, não em Contas a Pagar/Receber.

O extrato é o painel central do financeiro. Aqui você visualiza, filtra e gerencia todas as contas lançadas — tanto a pagar quanto a receber — em um único lugar.

### Como filtrar o extrato

| Filtro | O que faz |
|---|---|
| **Período** | Intervalo rápido (hoje, últimos 7 dias, próximos 7 dias) ou período personalizado |
| **Tipo de Data** | Define se o período se refere à data de vencimento, pagamento, inserção ou competência |
| **Conta Bancária** | Exibe apenas movimentações de uma conta específica |
| **Status** | Filtra por: Todos, Aguardando, Efetivado, Vencido ou Cancelado |
| **Tipo** | Filtra por: Todos, A Pagar, A Receber ou Ajustes |
| **Forma de Pagamento** | Filtra por espécie de pagamento |
| **Categoria** | Filtra por categoria financeira |
| **Favorecido / Credor** | Filtra por cliente ou fornecedor específico |
| **Filtro Geral** | Campo de pesquisa livre por qualquer termo |

### Como ler a lista

- Valores em **azul** → entradas (a receber ou recebidos)
- Valores em **vermelho** → saídas (a pagar ou pagos)
- Linhas em **vermelho** → contas vencidas
- Linhas em **verde** → contas efetivadas
- Linhas em **cinza** → contas canceladas

Clique em uma linha para expandir os detalhes: espécie, usuário que lançou, data de pagamento, juros, desconto e nota fiscal vinculada.

### Ações disponíveis por conta

| Ação | Quando usar |
|---|---|
| **Efetivar** | Marcar a conta como paga ou recebida |
| **Alterar** | Editar os dados da conta |
| **Excluir / Cancelar** | Remover ou cancelar o lançamento |

### Operar várias contas ao mesmo tempo

Ative **Modificar Vários** para selecionar múltiplas contas e realizar ações em lote:

- **Efetivar Vários** — efetiva todas as contas selecionadas de uma vez
- **Aguardando** — reverte contas selecionadas para pendente
- **Agrupar** — agrupa contas relacionadas em um único registro
- **Cancelar Vários** — cancela todas as contas selecionadas

O rodapé exibe o **Saldo da Conta** bancária selecionada e o **Saldo do Filtro** com os valores efetivados no período.

Use **Exportar Excel** para baixar os dados filtrados em planilha.

---

## 3. Efetivar Contas

**Financeiro → Efetivar Contas** ou pelo botão **Efetivar Vários** no Extrato

Permite efetivar várias contas ao mesmo tempo, com a possibilidade de informar acréscimos (juros) e descontos individuais.

### Como usar

1. As contas selecionadas aparecem na lista.
2. Informe a **Data de Pagamento** no topo — ela será aplicada a todas as contas.
3. Se quiser usar a mesma conta bancária para todas, selecione-a no campo **Conta** do topo.
4. Para cada conta na lista, você pode ajustar:
   - **Valor** — alterar o valor original se necessário
   - **Acréscimo** — adicionar juros ou multas
   - **Desconto** — informar desconto concedido
   - **Valor Pago** — calculado automaticamente
5. O rodapé mostra os totais de valor, acréscimos, descontos e valor final pago.
6. Clique em **Efetivar** para confirmar.

---

## 4. Transferência Bancária

**Financeiro → Transferência Bancária**

Registra movimentações de dinheiro entre duas contas bancárias do próprio estabelecimento.

### Como registrar uma transferência

1. Em **Remetente**, selecione a conta de onde o dinheiro vai sair e a categoria financeira correspondente.
2. Em **Destinatário**, selecione a conta que vai receber e a categoria correspondente.
3. Informe o **Valor** da transferência.
4. Informe a **Data** da transferência.
5. Adicione uma **Observação** se necessário.
6. Clique em **Transferir** para confirmar.

> O sistema registra automaticamente uma saída na conta remetente e uma entrada na conta destinatária.

---

## 5. Ajuste de Conta

**Financeiro → Ajuste de Conta**

Use quando o saldo registrado no sistema não está igual ao saldo real da conta bancária e você precisa corrigi-lo manualmente.

### Como realizar um ajuste

1. Selecione a **Conta Bancária** que será ajustada.
2. O sistema exibe o **Saldo Atual** cadastrado.
3. Informe o **Novo Saldo** correto. O sistema calcula automaticamente a diferença.
4. Preencha a **Descrição** e escolha a **Categoria** e a **Espécie**.
5. Informe a **Data do Ajuste**.
6. Adicione uma **Observação** explicando o motivo.
7. Clique em **Salvar**.

---

## 6. Conciliação Bancária

**Financeiro → Conciliação Bancária**

Processo de comparar o que foi registrado no SAG com o que realmente aconteceu na conta bancária.

### Por arquivo OFX

**Financeiro → Conciliação Bancária → Importar OFX**

O arquivo OFX é o extrato eletrônico gerado pelo banco (disponível no internet banking).

1. Importe o arquivo OFX do seu banco.
2. O sistema lista todas as movimentações do extrato bancário.
3. Para cada movimentação, o sistema tenta identificar automaticamente o **Favorecido**, a **Categoria** e uma **Conta Vinculada** no financeiro do SAG.
4. Corrija ou confirme as associações não reconhecidas automaticamente.
5. Salve para registrar a conciliação.

### Por dia (espécies de pagamento)

**Financeiro → Conciliação Bancária → Por Dia**

Compara os valores apurados nas vendas (por espécie: cartão, dinheiro, PIX, etc.) com os valores inseridos manualmente ou recebidos do conciliador.

1. Informe o **Período** de conciliação.
2. Clique em **Pesquisar**.
3. Para cada espécie, o sistema exibe:
   - **Valor Apurado** — o que o SAG registrou nas vendas
   - **Valor Inserido** — o que foi efetivamente depositado/liquidado
   - **Diferença** — a divergência entre os dois
4. Corrija os valores inseridos conforme necessário.
5. Clique em **Salvar**.

O rodapé exibe o **Total Apurado**, **Total Inserido** e as **Diferenças**.

---

## 7. Lançamento de Comissões

**Financeiro → Lançamento de Comissões**

Calcula e lança as comissões dos funcionários com base nos fechamentos de caixa do período.

### Como usar

**Passo 1 — Selecione os fechamentos**
1. Informe o **Período** (data início e data término).
2. Clique em **Pesquisar**.
3. Selecione os fechamentos de caixa que serão base para o cálculo.

**Passo 2 — Revise as comissões**
- Para cada fechamento, o sistema lista os funcionários e suas comissões calculadas.
- Você pode editar a quantidade de **Pontos** de cada funcionário, se o sistema usar pontuação.

**Passo 3 — Ajuste os valores finais**

| Campo | Descrição |
|---|---|
| **Comissão Bruta** | Valor total calculado automaticamente |
| **Descontos** | Descontos a aplicar sobre a comissão |
| **Acréscimos** | Acréscimos sobre a comissão |
| **Comissão Líquida** | Valor final a ser pago (calculado automaticamente) |

**Passo 4 — Salve**
Clique em **Salvar** para registrar as comissões.

---

## 8. Faturas

**Financeiro → Faturas**

Permite emitir cobranças com código de barras ou por integração com serviços de cobrança (como PJBank), enviá-las por e-mail e controlar o recebimento.

### Central de Faturas

| Ação | Descrição |
|---|---|
| **Emitir** | Gera a fatura com código de barras |
| **Efetivar** | Marca a fatura como recebida |
| **Cancelar** | Cancela a emissão da fatura |
| **Gerar PDF** | Baixa o boleto em PDF |
| **Enviar E-mail** | Envia o boleto diretamente ao cliente por e-mail |
| **Alterar** | Edita o valor ou data de vencimento da fatura já emitida |

### Remessas

Agrupa faturas para envio em lote ao banco (arquivo de remessa). Utilizado quando a cobrança é feita via convênio bancário.

---

## 9. Cadastros de Apoio

### 9.1 Contas Bancárias

**Financeiro → Cadastros → Contas Bancárias**

| Campo | O que preencher |
|---|---|
| **Descrição** | Nome identificador da conta (ex: "Conta Corrente Bradesco", "Caixa Interno") |
| **Saldo Inicial** | Saldo no momento do cadastro |
| **Banco** | Número e nome do banco |
| **Agência** | Número da agência (use hífen para separar o dígito: ex: 1234-5) |
| **Conta Corrente** | Número da conta (use hífen para separar o dígito) |
| **Padrão** | Marque se esta é a conta principal, usada por padrão nos lançamentos |

---

### 9.2 Categorias Financeiras

**Financeiro → Cadastros → Categorias**

Organizam os lançamentos em grupos para relatórios e DRE. A estrutura é hierárquica — você pode criar categorias principais e subcategorias.

**Como cadastrar:**
1. Clique em **Adicionar** para criar uma nova categoria, ou clique com o botão direito em uma existente para criar subcategoria.
2. Informe a **Descrição**.
3. Selecione o **Tipo DRE** — define como a categoria aparece no relatório de Demonstração de Resultados.
4. Clique em **OK** para salvar.

Você pode **arrastar e soltar** as categorias para reorganizá-las. Clique duas vezes em uma para renomeá-la.

---

### 9.3 Espécies de Pagamento

**Financeiro → Cadastros → Espécies**

Cadastre e gerencie as formas de pagamento disponíveis (dinheiro, cartão, PIX, boleto, cheque, etc.).

- Clique em **Adicionar** para criar uma nova espécie.
- Na lista, você pode **Ativar** ou **Desativar** cada espécie.
- Espécies vinculadas ao caixa não podem ser editadas por aqui.

---

### 9.4 Período Contábil

**Financeiro → Extrato → Opções → Período Contábil**

Define uma data de bloqueio: nenhum lançamento poderá ser inserido com data anterior à configurada aqui. Protege o histórico financeiro já encerrado de alterações acidentais.

1. Informe a data de corte.
2. Clique em **Alterar** para confirmar.

> Use com cuidado — após definido, lançamentos retroativos à data informada serão bloqueados.

---

## 10. Relatórios Financeiros

**Relatórios → Financeiro**

O módulo oferece 8 análises financeiras. Todos possuem o botão **Gerar Relatório** para exportar ou imprimir.

---

### Contas a Pagar

| Filtro | Descrição |
|---|---|
| **Favorecido** | Filtra por fornecedor ou credor específico |
| **Categoria** | Filtra por categoria financeira |
| **Conta Bancária** | Filtra por conta do estabelecimento |
| **Situação** | Em Aberto, Efetivadas ou Ambas |
| **Tipo de Data** | Vencimento, Pagamento, Inserção ou Competência |
| **Período** | Data início e data término |
| **Analítico** | Exibe o detalhamento completo de cada conta |

---

### Acréscimos e Descontos — Pagos

Exibe os juros pagos e descontos obtidos nas contas a pagar efetivadas no período.

**Filtros:** Favorecido, Categoria, Conta Bancária, Tipo de Data, Período.
**Opção:** Suprimir Zerado — oculta linhas sem acréscimo ou desconto.

---

### Contas a Receber

| Filtro | Descrição |
|---|---|
| **Credor** | Filtra por cliente específico |
| **Categoria** | Filtra por categoria financeira |
| **Conta Bancária** | Filtra por conta do estabelecimento |
| **Situação** | Em Aberto, Efetivadas ou Ambas |
| **Tipo de Data** | Vencimento, Pagamento, Inserção ou Competência |
| **Período** | Data início e data término |

---

### Acréscimos e Descontos — Recebidos

Exibe os juros cobrados e descontos concedidos nas contas a receber efetivadas.

**Filtros:** Credor, Categoria, Conta Bancária, Tipo de Data, Período.
**Opção:** Suprimir Zerado — oculta linhas sem acréscimo ou desconto.

---

### Extrato

Relatório completo de todas as movimentações financeiras (entradas e saídas) no período.

| Filtro | Descrição |
|---|---|
| **Categoria** | Filtra por categoria financeira |
| **Conta Bancária** | Filtra por conta específica |
| **Tipo de Data** | Vencimento, Pagamento, Inserção ou Competência |
| **Período** | Data início e data término |
| **Apenas Efetivados** | Exibe somente lançamentos já pagos ou recebidos |
| **Agrupar** | Agrupa os lançamentos por categoria |

---

### Fluxo de Caixa

Mostra a projeção de entradas e saídas ao longo do período, permitindo visualizar o saldo disponível em cada data.

**Filtros:** Categoria, Conta Bancária, Tipo de Data, Período.
**Opção:** Apenas Efetivados — exibe somente o realizado, sem projeções.

---

### DRE — Demonstração do Resultado do Exercício

Relatório gerencial que apresenta o resultado financeiro do estabelecimento no período — receitas, despesas e lucro ou prejuízo.

| Filtro | Descrição |
|---|---|
| **Tipo de Categorização** | Por Conta (categorias financeiras) ou Por Produto (categorias de produtos) |
| **Tipo** | Resumido (visão consolidada) ou Analítico (detalhado por categoria) |
| **Tipo de Data** | Vencimento, Pagamento, Inserção ou Competência |
| **Período** | Data início e data término |

---

### Contas a Pagar por Grupo de Fornecedor

Agrupa as contas a pagar por grupo de fornecedor, facilitando a visão de quanto está comprometido com cada categoria (ex: alimentos, embalagens, serviços).

| Filtro | Descrição |
|---|---|
| **Situação** | Em Aberto, Efetivadas ou Ambas |
| **Tipo de Data** | Vencimento, Pagamento, Inserção ou Competência |
| **Período** | Data início e data término |

---

## Dicas Gerais

- **Categorias bem definidas** são essenciais para que o DRE e o Fluxo de Caixa reflitam a realidade do negócio. Estruture-as antes de começar a lançar.
- **Data de Vencimento vs. Data de Competência** — o vencimento é quando a conta deve ser paga; a competência é o período ao qual ela pertence. Para relatórios gerenciais, prefira filtrar por competência.
- **Período Contábil** deve ser ajustado após o fechamento de cada mês para proteger os lançamentos já auditados.
- **Agrupar contas** no extrato é útil quando você tem várias parcelas de um mesmo compromisso e quer visualizá-las como um único bloco.
- O **Saldo da Conta** exibido no rodapé do Extrato considera todos os lançamentos efetivados até a data atual, independente do filtro aplicado.
- Utilize a **Consulta de Totais** para uma visão rápida do resumo financeiro: total recebido, a receber, pago, a pagar e saldo previsto.

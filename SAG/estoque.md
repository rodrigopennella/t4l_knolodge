# Módulo de Estoque — Documentação de Uso

Guia completo das funcionalidades do módulo de Estoque do SAG. Aqui você encontra como realizar entradas, saídas, ajustes, transferências, pedidos de compra e consultar relatórios.

---

## Índice

1. [Entrada de Nota](#1-entrada-de-nota)
2. [Saída de Estoque](#2-saída-de-estoque)
3. [Ajuste de Estoque](#3-ajuste-de-estoque)
4. [Inventário de Produtos](#4-inventário-de-produtos)
5. [Transferência de Estoque](#5-transferência-de-estoque)
6. [Pedido de Compra](#6-pedido-de-compra)
7. [Cotação de Produtos](#7-cotação-de-produtos)
8. [Consultas](#8-consultas)
9. [Análise de Preço](#9-análise-de-preço)
10. [Locais de Estoque](#10-locais-de-estoque)
11. [Relatórios de Estoque](#11-relatórios-de-estoque)

---

## 1. Entrada de Nota

**Estoque → Entrada de Nota**

Esta tela é utilizada para registrar a entrada de produtos no estoque a partir de uma compra com fornecedor. Sempre que mercadoria chega ao estabelecimento acompanhada de uma Nota Fiscal, o lançamento deve ser feito aqui para que o estoque seja atualizado corretamente.

### Como acessar

Acesse pelo menu **Estoque → Entrada de Nota**. Você também pode consultar notas já lançadas em **Estoque → Consulta de Notas**.

### Como importar uma nota

O sistema oferece três formas de importar os dados da nota:

- **Arquivo XML** — importe diretamente o arquivo XML da Nota Fiscal Eletrônica (NF-e) recebida do fornecedor. O sistema preenche os campos automaticamente.
- **Chave de Consulta** — informe a chave de 44 dígitos da NF-e para buscar a nota diretamente na base da Receita Federal.
- **Notas Recebidas** — consulte as últimas NF-es recebidas eletronicamente e selecione a que deseja dar entrada.
- **Importar Pedido de Compra** — se você já criou um Pedido de Compra para este fornecedor, importe-o para agilizar o preenchimento.

### Aba: Dados da Nota

Preencha as informações gerais da nota fiscal:

| Campo | O que preencher |
|---|---|
| Número | Número da nota fiscal (até 9 dígitos) |
| Série | Série da nota (até 3 dígitos) |
| Data de Emissão | Data em que a nota foi emitida pelo fornecedor |
| Chave | Chave de 44 dígitos da NF-e (opcional, se importado por XML é preenchido automaticamente) |
| Fornecedor | Nome ou código do fornecedor. Se não estiver cadastrado, clique no botão ao lado para cadastrar um novo. |
| Pedido de Compras | Marque se esta nota está vinculada a um pedido de compra já registrado |
| Observação | Anotações internas sobre esta nota |

### Aba: Itens

Nesta aba você adiciona os produtos que chegaram na nota:

1. No campo **Produto**, busque pelo nome ou código do produto.
2. Informe a **Quantidade** recebida.
3. Informe o **Preço de Custo** (quanto você pagou por unidade) e o **Preço de Venda** sugerido.
4. Selecione o **Local de Estoque** onde os produtos serão armazenados.
5. Clique em **Inserir** para adicionar o item à lista.

Para cada item adicionado, você pode:
- **Editar Lote/Validade** — informar o lote e a data de vencimento do produto (ícone de calendário).
- **Editar Impostos** — ajustar os impostos vinculados ao item, como ICMS, IPI e DIFAL (ícone de imposto).
- **Alterar Informações** — modificar o item após inserção (ícone de atualizar).
- **Remover** — excluir o item da lista (ícone de lixeira).

Ao terminar de adicionar todos os produtos, clique em **Salvar** para confirmar a entrada no estoque.

> **Atenção:** Ao salvar, os produtos são adicionados ao estoque no local selecionado e o custo dos produtos é atualizado no cadastro.

---

## 2. Saída de Estoque

**Estoque → Saída de Estoque**

Utilize esta tela para registrar saídas de produtos do estoque que **não são originadas por vendas no caixa** — por exemplo: amostras enviadas, produtos usados internamente, perdas identificadas manualmente ou devoluções a fornecedor.

> As saídas realizadas pelo caixa (vendas) são lançadas automaticamente. Esta tela é apenas para saídas avulsas.

### Como registrar uma saída

1. Busque o **Produto** pelo nome ou código.
2. Informe a **Quantidade** a ser retirada do estoque.
3. Selecione o **Local de Estoque** de onde o produto sairá.
4. Clique em **Adicionar** para incluir o item na lista.
5. Repita o processo para todos os produtos que estão saindo.
6. No campo **Motivo**, selecione ou descreva o motivo da saída.
7. Informe a **Data da Saída** (data e hora exatas).
8. Se necessário, adicione uma **Observação**.
9. Clique em **Salvar** para confirmar.

---

## 3. Ajuste de Estoque

**Estoque → Ajuste de Estoque**

O ajuste de estoque é utilizado quando a quantidade registrada no sistema não corresponde à quantidade física real do produto. Isso pode ocorrer por perdas, erros de contagem ou divergências identificadas em inventários.

### Como realizar um ajuste

1. Busque o **Produto** pelo nome ou código. Somente produtos que possuem estoque registrado aparecem nesta busca.
2. Selecione o **Local de Estoque** correspondente.
3. O sistema exibe a **Quantidade Atual** do produto naquele local.
4. Informe a **Nova Quantidade** correta.
5. Adicione uma **Descrição** explicando o motivo do ajuste (ex: "Quebra identificada na contagem").
6. Clique em **Ajustar** para confirmar.

> O sistema solicita uma justificativa antes de aplicar o ajuste. Essa informação fica registrada no histórico para auditoria.

---

## 4. Inventário de Produtos

**Estoque → Inventário de Produtos**

O inventário é o processo de contar fisicamente todos os produtos do estoque e atualizar o sistema com as quantidades reais. É recomendado realizá-lo periodicamente para manter o estoque sempre preciso.

### Como realizar um inventário

**Passo 1 — Configure o inventário**
- Selecione o **Local de Estoque** que será inventariado.
- Informe a **Data de Referência** do inventário.

**Passo 2 — Filtre os produtos**
- Use os filtros de **Grupo**, **Subgrupo**, **Departamento** ou o campo de **Pesquisa** para localizar os produtos desejados.
- Marque a opção **Apenas Produtos Ativos** para não exibir produtos fora de linha.
- Clique em **Pesquisar** para listar os produtos.

**Passo 3 — Lance as quantidades**

Existem três formas de lançar:

- **Digitação manual** — na lista de produtos, clique no campo **Nova Qtd.** ao lado de cada produto e informe a quantidade contada.
- **Leitura por código de barras** — use um leitor de código de barras. A cada leitura, o produto é identificado e a quantidade incrementada automaticamente.
- **Importação por arquivo** — importe um arquivo de texto gerado por um coletor de dados.

**Passo 4 — Finalize**
- Use **Selecionar Tudo** / **Desselecionar Tudo** para controlar quais produtos serão processados.
- **Salvar e Sair** — salva o progresso sem processar (pode continuar depois).
- **Salvar e Processar** — aplica as novas quantidades ao estoque. Esta ação não pode ser desfeita.

---

## 5. Transferência de Estoque

**Estoque → Transferência de Estoque**

Use esta tela para mover produtos de um local de armazenamento para outro dentro do próprio estabelecimento. Por exemplo: transferir produtos do estoque central para o estoque da loja, ou de uma geladeira para outra.

### Como registrar uma transferência

1. Busque o **Produto** que será transferido.
2. Selecione o **Estoque de Origem** (de onde o produto sairá). O sistema exibe a quantidade disponível nesse local.
3. Selecione o **Estoque de Destino** (para onde o produto irá). O sistema exibe a quantidade atual nesse local.
4. Informe a **Quantidade a Transferir**.
5. Clique em **Inserir** para adicionar à lista.
6. Repita para todos os produtos que serão transferidos.
7. Informe o **Motivo** da transferência.
8. Clique em **Salvar** para confirmar.

---

## 6. Pedido de Compra

**Estoque → Pedido de Compra**

O pedido de compra é utilizado para registrar formalmente os produtos que você deseja comprar de um fornecedor. Ele pode ser gerado manualmente ou com base em sugestões automáticas do sistema.

### Como criar um pedido de compra

**Passo 1 — Selecione o fornecedor**
- No campo **Fornecedor**, busque pelo nome. Se não estiver cadastrado, clique no botão ao lado para adicionar.

**Passo 2 — Adicione os produtos**
- Busque o **Produto** pelo nome ou código.
- Informe a **Quantidade** que deseja comprar.
- Informe o **Custo** cobrado pelo fornecedor.
- Clique em **Adicionar**.

Você pode visualizar o **Estoque Atual** e o **Custo Atual** de cada produto antes de confirmar.

**Passo 3 — Use as sugestões automáticas (opcional)**

O sistema oferece três ferramentas no menu **Ferramentas** para auxiliar no preenchimento:

| Ferramenta | O que faz |
|---|---|
| **Análise de Vendas** | Sugere quantidades com base no histórico de vendas do período |
| **Produtos por Fornecedor** | Lista os produtos vinculados ao fornecedor selecionado |
| **Estoque Mínimo** | Sugere compras para os produtos que estão abaixo do mínimo configurado |

**Passo 4 — Revise e salve**
- O rodapé exibe o **Valor Total do Pedido**.
- Clique em **Salvar** para registrar o pedido.

> Após salvar, o pedido pode ser vinculado à Entrada de Nota quando a mercadoria chegar.

---

## 7. Cotação de Produtos

**Estoque → Cotação de Produtos**

A cotação permite comparar preços do mesmo produto entre diferentes fornecedores, facilitando a decisão de compra pelo melhor custo.

### Como criar uma cotação

**Passo 1 — Adicione os fornecedores**
- No campo **Fornecedor**, busque e clique em **Adicionar** para incluir cada fornecedor que será cotado.

**Passo 2 — Adicione os produtos**
- Busque o **Produto** e informe a **Quantidade** desejada.
- Clique em **Adicionar**.

**Passo 3 — Preencha os preços**
- A tela exibe uma grade comparativa: cada produto em linha, cada fornecedor em coluna.
- Preencha o **preço** e a **quantidade** que cada fornecedor oferece para cada produto.
- O sistema calcula automaticamente o **total por fornecedor**.

**Passo 4 — Salve a cotação**
- Clique em **Salvar Cotação** para registrar.
- Você pode exportar a cotação para uma planilha ou importá-la preenchida.

---

## 8. Consultas

### 8.1 Consulta de Notas

**Estoque → Consulta de Notas**

Pesquise todas as notas fiscais de entrada já registradas no sistema.

**Filtros disponíveis:**

| Filtro | Descrição |
|---|---|
| Fornecedor | Filtra por fornecedor específico |
| Data Início / Data Término | Define o período da pesquisa |
| Busca | Número da nota ou chave NF-e |
| Status | Todas, Concluídas ou Em Registro |
| Tipo de Data | Por data de inserção no sistema ou por data de emissão |

Clique em **Filtrar** para buscar. Dê **duplo clique** em uma nota para abri-la e editar.

---

### 8.2 Consulta de Saídas

**Estoque → Consulta de Saídas**

Pesquise as saídas avulsas de estoque registradas no sistema.

> Esta consulta **não inclui** as saídas geradas por vendas no caixa. Para isso, utilize os Relatórios de Estoque.

**Filtros disponíveis:** Produto, Período (com hora), botão **Filtrar**.

---

### 8.3 Consulta de Pedidos de Compra

**Estoque → Consulta de Pedidos de Compra**

Pesquise os pedidos de compra criados, filtrando por fornecedor e período.

---

### 8.4 Consulta de Cotações

**Estoque → Consulta de Cotações**

Pesquise e acesse cotações já salvas para reutilizá-las ou compará-las.

---

## 9. Análise de Preço

**Estoque → Análise de Preço**

Permite revisar e ajustar os preços de venda dos produtos com base no custo atual e no mark-up mínimo configurado. Ideal para atualizar preços em massa após uma entrada de nota com novos custos.

### Como usar

1. Use os filtros para encontrar os produtos que deseja revisar:
   - **Pesquisa** por nome ou código.
   - **Grupo** e **Subgrupo** para filtrar categorias.
   - **Somente Mark-up abaixo do mínimo** — exibe apenas os produtos onde o preço de venda está comprometendo a margem mínima.
   - **Recém Alterados** — exibe produtos cujo custo foi alterado nos últimos 1, 7, 15 ou 30 dias.
2. Clique em **Filtrar** para listar.
3. Na grade, você pode editar diretamente o **Custo** e o **Preço de Venda** de cada produto.
4. Clique em **✓ (Atualizar)** na linha do produto para confirmar a alteração, ou em **✗ (Voltar)** para desfazer.

---

## 10. Locais de Estoque

**Estoque → Locais de Estoque**

Cadastre e gerencie os locais físicos onde os produtos são armazenados (ex: "Estoque Central", "Câmara Fria", "Prateleira Loja").

### Como cadastrar um local

1. Clique em **Cadastro**.
2. Informe o nome do local.
3. Salve.

Na lista, você pode **alterar** o nome de um local ou **excluir** locais que não são mais utilizados. O local marcado como **Padrão** é o estoque principal do sistema.

---

## 11. Relatórios de Estoque

**Relatórios → Estoque**

O módulo de relatórios oferece 14 análises diferentes sobre o estoque. Todos os relatórios possuem o botão **Gerar Relatório** no canto inferior da tela.

---

### Estoque Mínimo

Exibe os produtos que estão com quantidade **abaixo do mínimo** configurado no cadastro do produto. Use para identificar o que precisa ser comprado.

**Filtros:** Grupo, Subgrupo, Departamento de Venda, Departamento de Produção, Local de Estoque.

**Opção:** Agrupar o resultado por grupo de produto.

---

### Estoque Máximo

Exibe os produtos que estão com quantidade **acima do máximo** configurado. Use para identificar excesso de mercadoria.

**Filtros:** Idênticos ao relatório de Estoque Mínimo.

---

### Estoque Consolidado

Exibe a posição completa do estoque — nome do produto, quantidade atual e valor em estoque — de todos os produtos cadastrados.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Grupo / Subgrupo / Departamento | Filtra por categoria de produto |
| Local de Estoque | Exibe apenas um local específico |
| Data | "Atual" (posição de hoje) ou "Outra Data" (posição histórica) |
| Exibir itens sem estoque | Inclui produtos com quantidade zero |
| Apenas produtos ativos | Oculta produtos fora de linha |
| Agrupar por grupo | Agrupa os produtos por categoria |

---

### Histórico do Produto

Exibe todas as movimentações de um produto específico: entradas, saídas, ajustes e transferências em um período.

**Filtros:** Produto (obrigatório), Data de Início, Local de Estoque.

---

### Nível de Estoque

Relatório visual do nível de estoque dos produtos em relação ao mínimo e máximo configurados. Permite identificar rapidamente produtos críticos.

**Filtros:** Grupo, Subgrupo, Departamento, Local de Estoque.

---

### Saída de Estoque

Exibe todas as saídas de produtos em um período, incluindo vendas realizadas no caixa.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Data Início / Data Término | Define o período |
| Produto | Filtra por produto específico |
| Motivo da Saída | Filtra por um motivo específico (perda, ajuste, etc.) |
| Incluir Vendas | Marcado por padrão — inclui as saídas geradas pelas vendas |

---

### Entrada de Estoque

Exibe todas as entradas de produtos registradas no período.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Data Início / Data Término | Define o período |
| Produto | Filtra por produto específico |
| Tipo de Data | Por data de inserção no sistema ou pela data da NF-e |
| Agrupamento | Sem agrupamento ou agrupado por nota fiscal |
| Tipo de Relatório | Resumido (totais por produto) ou Analítico (detalhado por nota) |

---

### Transferência de Estoque

Exibe o histórico de transferências realizadas entre locais de estoque.

**Filtros:** Data Início, Data Término, Produto, Estoque de Origem, Estoque de Destino.

---

### Inventário de Estoque

Exibe o histórico de inventários realizados, com as quantidades antes e depois da contagem.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Data Início / Data Término | Define o período |
| Tipo de Data | Por data de inserção ou por data de referência do inventário |
| Grupo / Subgrupo / Departamento | Filtra por categoria |
| Local de Estoque | Filtra por local específico |

---

### Movimento de Estoque

Relatório completo com **todas** as movimentações do estoque (entradas, saídas, transferências e ajustes) em um período. Ideal para auditoria.

**Filtros:** Data Início, Data Término, Grupo, Subgrupo, Departamento.

---

### Multiloja — Estoque Consolidado

Disponível apenas para estabelecimentos com mais de uma filial. Exibe o estoque consolidado de todas as unidades em uma única visão.

**Filtros:** Data (atual ou outra data), opção de incluir itens sem estoque.

---

### Lote — Validade

Exibe os produtos controlados por lote, com suas datas de vencimento. Ideal para gestão de produtos perecíveis e controle do prazo de validade.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Produto | Filtra por produto específico |
| Data Início / Data Término | Define o período |
| Ordenar por | Por nome do produto ou por data de validade |
| Filtro de Data | Por data de inserção do lote ou por data de vencimento |

---

### Perda por Faturamento

Apura a diferença entre o que foi vendido e o que efetivamente saiu do estoque, ajudando a identificar perdas não registradas.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Data Início / Data Término | Define o período |
| Produto | Filtra por produto específico |
| Grupo / Subgrupo / Departamento | Filtra por categoria |
| Motivo | Filtra por motivo de perda específico |
| Ocultar Matéria Prima | Remove insumos de produção do relatório |
| Agrupar por Grupo | Agrupa os resultados por categoria |

---

### Ajuste de Estoque

Exibe o histórico de todos os ajustes manuais realizados no estoque, com as quantidades anteriores, novas e os responsáveis pelo ajuste.

**Filtros:**

| Filtro | Descrição |
|---|---|
| Data Início / Data Término | Define o período |
| Produto | Filtra por produto específico |
| Grupo / Subgrupo / Departamento | Filtra por categoria |
| Local de Estoque | Filtra por local específico |
| Usuário | Filtra pelos ajustes realizados por um usuário específico |

---

## Dicas Gerais

- **Locais de Estoque** precisam estar cadastrados antes de realizar entradas, saídas ou transferências. Acesse em **Estoque → Locais de Estoque**.
- **Custo do produto** é atualizado automaticamente a cada Entrada de Nota. Revise os preços de venda após cada entrada usando a **Análise de Preço**.
- **Estoque Mínimo e Máximo** dos produtos são configurados no Cadastro de Produtos. Sem esses valores, os relatórios de Estoque Mínimo e Máximo não exibirão alertas.
- Para produtos com **lote e validade**, sempre preencha essas informações na Entrada de Nota para que o relatório de Lote — Validade funcione corretamente.
- O relatório de **Movimento de Estoque** é a fonte mais completa para auditorias, pois reúne todas as movimentações em um único lugar.

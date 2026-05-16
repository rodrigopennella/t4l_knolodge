# SAG — Relatórios

Módulo de geração de relatórios gerenciais e fiscais.

---

## Como Acessar

**Caminho:** Menu Principal > **Relatórios**

Selecione a categoria de relatório desejada, defina os filtros (período, caixa, produto, etc.) e clique em **Gerar**.

---

## Relatórios de Vendas

| Relatório | Descrição |
|---|---|
| Vendas Geral | Totais de vendas no período |
| Vendas por Caixa | Detalhamento por terminal de caixa |
| Vendas por Produto | Quais produtos venderam e quanto |
| Vendas por Grupo | Agrupado por categoria de produto |
| Vendas por Hora | Distribuição de vendas ao longo do dia |
| Vendas por Vendedor | Performance por atendente |
| Vendas por Forma de Pagamento | Totais por dinheiro, cartão, PIX, etc. |

**Filtros comuns:**
- Data inicial e data final
- Caixa específico
- Turno
- Produto ou grupo

---

## Relatórios de Cancelamentos

**Caminho:** Relatórios > **Itens Cancelados**

- Lista todos os cancelamentos no período
- Campos: data, item, valor, operador, motivo
- Útil para auditoria e controle de perdas

---

## Relatório de Fechamento de Caixa

**Caminho:** Relatórios > **Fechamento de Caixa**

Exibe o resumo de cada fechamento:
- Valor de abertura
- Entradas e saídas
- Total por forma de pagamento
- Diferença (sobra/falta)
- Operador responsável

---

## Relatório de Comissões

**Caminho:** Relatórios > **Comissões** (ou Financeiro > Comissões)

Lista as comissões calculadas por vendedor no período.

---

## Relatórios Fiscais

| Relatório | Descrição |
|---|---|
| Cupons Emitidos | Lista de CF-e / NFC-e emitidos |
| Cupons Cancelados | Documentos fiscais cancelados |
| Relatório SAT | Totais do SAT no período |
| Relatório NFC-e | Totais de notas fiscais emitidas |

---

## Consulta de Vendas (Cupom a Cupom)

**Caminho:** Relatórios > **Consultas** (ou Caixa > F10)

- Localiza uma venda específica pelo número, data ou CPF
- Exibe todos os itens e forma de pagamento
- Útil para verificar divergências

---

## Relatório de Estoque

**Caminho:** Relatórios > **Estoque** (ou Estoque > Consultas)

- Posição atual do estoque
- Movimentações (entradas e saídas) no período
- Produtos abaixo do estoque mínimo

---

## Relatório de Clientes

**Caminho:** Relatórios > **Clientes**

- Lista de clientes cadastrados
- Histórico de compras por cliente
- Saldo de caderneta (crédito)

---

## Dicas para Fechamento / Auditoria

Ao verificar divergências entre XML e relatório:
1. Gere o **Relatório de Cupons Emitidos** para o período
2. Compare com o arquivo XML gerado em **Ferramentas CFe > Arquivos XML**
3. Se houver diferença de CNPJ, filtre por estabelecimento separadamente
4. Para apuração fiscal, utilize os relatórios de SAT e NFC-e separadamente

---

## Relatórios Personalizados

**Relatórios → Personalizar**

Permite criar relatórios totalmente sob medida, combinando informações de diferentes partes do sistema — vendas, clientes, produtos, pedidos — sem depender de um relatório pronto. Os relatórios criados ficam salvos e podem ser reutilizados, editados ou removidos.

> **ATENÇÃO:** Os relatórios padrão do SAG são fixos — o cliente não consegue alterar colunas, ordenação ou layout. Se pedir personalização de relatório padrão → ESCALAR_SUPORTE. O relatório personalizado é a alternativa para criar visões sob medida.

### Visão Geral da Tela

**Painel esquerdo:** lista de relatórios salvos com botões **Novo**, **Editar** e **Remover**.

**Painel direito:** muda conforme a situação — filtros para gerar um relatório salvo, ou editor em 4 etapas ao criar/editar.

### Criar um Novo Relatório

Clique em **Novo**. O editor abre com quatro etapas em abas.

**Passo 1 — Nome e Tabelas**
1. Informe um **Nome** descritivo (ex: "Vendas por Cliente - Mês Atual"). Obrigatório.
2. Na lista da esquerda, clique em uma fonte de dados e clique **>>** para adicioná-la à lista da direita.
3. Clique em **Avançar →**.

> Ao adicionar uma segunda fonte relacionada, o sistema sugere o vínculo automaticamente na próxima etapa.

**Passo 2 — Colunas**
1. Expanda a fonte desejada na lista da esquerda.
2. Clique na coluna e clique **>>**.
3. Informe o **Título da Coluna** (nome que aparecerá no cabeçalho).
4. Arraste as colunas para definir a ordem de exibição.
5. Clique em **Avançar →**.

**Passo 3 — Vínculos entre Tabelas**

Quando o relatório usa mais de uma fonte, defina como elas se relacionam.

- **Vínculos automáticos:** o sistema detecta relações conhecidas e sugere automaticamente.
- **Adicionar manualmente:** clique em **Adicionar Vínculo** e informe Tipo, Tabela e Condição.

| Tipo | Quando usar |
|---|---|
| **INNER JOIN** | Apenas registros que existem nas duas fontes |
| **LEFT JOIN** | Todos da fonte principal, mesmo sem correspondência na segunda |

> Prefira **LEFT JOIN** quando a fonte secundária for opcional (ex: pedidos que podem não ter entregador).

**Passo 4 — Filtros**

Define quais campos de pesquisa aparecerão ao gerar o relatório. Filtros são opcionais.

Clique em **Adicionar Filtro** e informe Coluna, Título e Operador (=, >, <, >=, <=, contém).

> O sistema detecta o tipo de dado automaticamente: datas geram campos De/Até; textos geram busca por aproximação.

**Salvar:** clique em **Salvar**. Obrigatório ter nome, pelo menos uma fonte e pelo menos uma coluna.

### Gerar um Relatório Salvo

1. Clique no nome do relatório no painel esquerdo.
2. Preencha os filtros desejados (todos opcionais).
3. Clique em **Gerar Relatório**.

O relatório é exibido em formato **PDF** (orientação paisagem) e pode ser impresso ou exportado.

### Editar / Remover

- **Editar:** selecione o relatório > clique em **Editar** > faça as alterações > **Salvar**.
- **Remover:** selecione > clique em **Remover** > confirme. A exclusão é definitiva.

### Dicas

- Nomeie de forma descritiva — evite "Relatório 1".
- Comece com poucos campos — muitas colunas ficam difíceis de ler.
- Use filtros de data sempre que o relatório for de período variável.
- Teste com filtros em branco após criar para ver todos os dados disponíveis.

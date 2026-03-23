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

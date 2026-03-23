# SAG — Estoque

Módulo de controle de estoque: entradas, saídas, ajustes, inventário e pedidos de compra.

---

## Entrada de Estoque

**Caminho:** Menu Principal > **Estoque** > **Entrada de Estoque**

### Aba: Dados da Nota
| Campo | Observação |
|---|---|
| Número | Número da nota fiscal (máx. 9 caracteres) |
| Série | Série da nota (máx. 3 caracteres) |
| Data de Emissão | Data da nota do fornecedor |
| Chave | Chave de acesso da NF-e (44 dígitos) |
| Fornecedor | Seleção da lista de fornecedores cadastrados |
| Observações | Campo livre (máx. 2000 caracteres) |

### Aba: Itens
| Campo | Observação |
|---|---|
| Produto | Pesquisa por nome ou código |
| Quantidade | Qtd recebida |
| Preço de Custo | Valor de compra |
| Preço de Venda | Pode atualizar automaticamente |
| Estoque Atual | Exibido para referência |
| Unidade de Medida | Conforme cadastro do produto |

**Dados Fiscais por Item:**
- CST, ICMS, ICMS ST, IPI, CFOP, Desconto, Frete, Custo Real

**Botões:** Inserir Item / Cancelar Item

---

## Ajuste de Estoque

**Caminho:** Estoque > **Ajuste de Estoque**

Use quando a quantidade física diverge do sistema (inventário ou correção manual).

Campos:
- Produto
- Quantidade atual (sistema)
- Nova quantidade
- Motivo do ajuste (obrigatório — selecione da lista)

---

## Inventário de Produtos

**Caminho:** Estoque > **Inventário**

1. Gere a listagem de produtos
2. Preencha as quantidades físicas contadas
3. Aplique o inventário — o sistema ajusta as quantidades automaticamente

---

## Pedido de Compra

**Caminho:** Estoque > **Pedido de Compra**

### Criar Pedido
1. Selecione o **Fornecedor**
2. Adicione os produtos com quantidade e preço estimado
3. Salve o pedido

### Receber Pedido de Compra
1. Acesse **Consulta de Pedidos de Compra**
2. Selecione o pedido
3. Confirme o recebimento — gera entrada de estoque automaticamente

---

## Transferência de Estoque

**Caminho:** Estoque > **Transferência de Estoque**

Movimenta produtos entre locais de estoque (ex: depósito → frigobar).

Campos:
- Local de origem
- Local de destino
- Produto e quantidade

---

## Locais de Estoque

**Caminho:** Estoque > **Locais de Estoque**

Permite cadastrar múltiplos almoxarifados ou áreas de estoque (ex: depósito, cozinha, salão).

---

## Controle de Validade (Lote)

**Caminho:** Estoque > **Lote e Validade**

- Registra lote e data de validade na entrada
- Alerta produtos próximos ao vencimento

---

## Cotação de Preços

**Caminho:** Estoque > **Cotação**

Permite comparar preços de fornecedores para o mesmo produto.

| Tela | Função |
|---|---|
| Nova Cotação | Seleciona produtos e fornecedores para cotar |
| Consulta de Cotação | Histórico de cotações |
| Análise de Preço | Comparativo de preços |
| Estoque Mínimo | Lista produtos abaixo do mínimo configurado |

---

## Saída de Estoque

**Caminho:** Estoque > **Saída de Estoque**

Registra saída manual (uso interno, descarte, brinde).

Campos:
- Produto
- Quantidade
- Motivo

---

## Consultas de Estoque

| Tela | Caminho |
|---|---|
| Consulta de Notas | Estoque > Consultar Notas |
| Histórico de Saídas | Estoque > Consulta Saída de Estoque |
| Detalhe de Saída | Seleciona saída > Ver Detalhe |

---

## Parâmetros CFOP para Estoque

**Caminho:** Estoque > **Parâmetros CFOP**

Vincula os CFOP padrão para entradas e saídas conforme tipo de operação (compra, transferência, devolução, etc.).

> Configuração importante para correta emissão de NF-e de entrada.

# SAG — Financeiro

Módulo de gestão financeira: contas a pagar e receber, extrato, faturas e conciliação.

---

## Contas a Pagar e Receber

**Caminho:** Menu Principal > **Financeiro** > **Contas a Pagar/Receber**

### Campos da Listagem
- Descrição
- Tipo (Pagar / Receber)
- Valor
- Vencimento
- Status (Aberto / Efetivado / Cancelado)
- Categoria

### Filtros Disponíveis
- Por período (data de vencimento ou emissão)
- Por status
- Por categoria
- Por fornecedor/cliente

---

## Efetivar Contas

**Caminho:** Financeiro > **Efetivar Contas**

Tela: **Efetiva Contas**

1. Selecione o lançamento desejado
2. Informe:
   - **Data de pagamento**
   - **Forma de pagamento**
   - **Conta bancária**
   - **Valor pago** (pode diferir do valor original)
3. Clique em **Efetivar**

Para efetivar em lote: use **Efetivar Agrupamento**, selecione múltiplos lançamentos.

---

## Extrato

**Caminho:** Financeiro > **Extrato**

Exibe movimentações por conta bancária em um período selecionado.

Campos:
- Conta bancária (seleção)
- Período (data inicial e final)
- Saldo inicial / final
- Lista de movimentações (entrada/saída, data, descrição, valor)

---

## Conciliação Bancária

**Caminho:** Financeiro > **Conciliação Bancária por Dia**

Permite comparar lançamentos do SAG com o extrato real do banco.

### Importar OFX
1. Acesse **Financeiro > Arquivo OFX**
2. Importe o arquivo exportado pelo banco
3. O sistema compara automaticamente com os lançamentos existentes

---

## Faturas

**Caminho:** Financeiro > **Faturas** > **Central de Faturas**

Gerencia faturas de clientes com pagamento parcelado ou recorrente.

### Telas do Módulo Faturas
| Tela | Função |
|---|---|
| Central de Faturas | Listagem e gestão geral |
| Central de Remessa | Geração de arquivos de remessa bancária |
| Relatório de Faturas | Relatórios por período/cliente |
| Formas de Faturamento | Configuração de formas (boleto, PIX, etc.) |
| Formas de Emissão | Como a fatura é enviada ao cliente |

---

## Transferência Bancária

**Caminho:** Financeiro > **Transferência Bancária**

Campos:
- Conta de origem
- Conta de destino
- Valor
- Data
- Descrição/Histórico

---

## Comissões

**Caminho:** Financeiro > **Lançamento de Comissões**

- Registra comissões de vendedores/funcionários
- Pode ser baseado em percentual das vendas
- Gerado automaticamente se configurado nos parâmetros

---

## Período Contábil

**Caminho:** Financeiro > **Período Contábil**

Define os períodos fechados para impedir alterações em lançamentos de datas passadas.

---

## Categorias Financeiras

**Caminho:** Financeiro > **Categorias**

- Organiza receitas e despesas por tipo
- Permite renomear categorias existentes
- Usado nos relatórios para agrupamento de lançamentos

---

## Consulta de Totais

**Caminho:** Financeiro > **Consulta de Totais**

Exibe resumo consolidado de receitas e despesas por período, com agrupamento por categoria.

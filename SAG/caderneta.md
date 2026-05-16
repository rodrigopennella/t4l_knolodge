# Caderneta — Documentação de Uso

Guia completo do sistema de caderneta do SAG: como lançar compras no fiado, receber pagamentos, consultar extratos e acompanhar a situação de cada cliente.

---

## O que é a Caderneta?

A caderneta é o sistema de crédito do SAG. Ela permite que um cliente faça compras sem pagar na hora, acumulando um saldo devedor que será quitado posteriormente. Cada cliente tem um limite de crédito configurado, e o sistema controla automaticamente quanto cada um pode comprar.

---

## Índice

1. [Registrar uma Compra na Caderneta](#1-registrar-uma-compra-na-caderneta)
2. [Receber Pagamento de Caderneta](#2-receber-pagamento-de-caderneta)
3. [Central de Caderneta](#3-central-de-caderneta)
4. [Limite de Crédito](#4-limite-de-crédito)

---

## 1. Registrar uma Compra na Caderneta

### No caixa

1. Lance todos os produtos normalmente na Frente de Caixa.
2. Ao finalizar, clique no **Total** para ir ao pagamento.
3. Selecione **Caderneta** como forma de pagamento.
4. A tela de registro de caderneta será aberta.

### Na tela de lançamento

| Campo | O que exibe |
|---|---|
| **Cliente** | Busque pelo nome ou código do cliente |
| **Saldo Devedor Anterior** | Quanto o cliente já deve antes desta compra |
| **Limite de Crédito** | O limite total configurado para o cliente |
| **Limite Disponível** | Quanto o cliente ainda pode comprar |
| **Valor da Compra** | Total da venda que será lançado na caderneta |
| **Saldo Devedor Final** | Como ficará o saldo após este lançamento |
| **Limite Disponível Após** | Quanto restará de limite após a compra |

5. Confirme que há limite disponível e clique em **Salvar**.

> Se o cliente não tiver limite suficiente, o sistema exibirá um aviso e impedirá o lançamento.

---

## 2. Receber Pagamento de Caderneta

### Pelo caixa (forma rápida)

1. Pressione **F7** na Frente de Caixa.
2. Busque o cliente pelo nome ou código.
3. O sistema exibe o **saldo devedor atual**.
4. Informe o **valor pago**.
5. Se o cliente estiver quitando tudo, marque **Pagamento do Total** — o sistema zera a dívida automaticamente.
6. Clique em **Salvar**.

### Pela Central de Caderneta

Acesse **Principal → Caderneta → aba Recebimento**.

---

## 3. Central de Caderneta

**Principal → Caderneta**

### Aba Recebimento

Registra o pagamento de um cliente.

| Campo | O que preencher |
|---|---|
| **Cliente** | Nome ou código do cliente |
| **Saldo Devedor** | Exibido automaticamente após selecionar o cliente |
| **Data do Pagamento** | Data em que o pagamento foi efetuado |
| **Data de Competência** | Período financeiro ao qual o pagamento pertence |
| **Valor do Pagamento** | Quanto o cliente está pagando agora |
| **Pagamento do Total** | Marque para quitar toda a dívida de uma vez |

**Botões:**
- **Salvar** — registra o pagamento e atualiza o saldo.
- **Emitir Fatura** — gera boleto ou fatura para o cliente.
- **Consultar Vendas** — abre o histórico de compras do cliente.

---

### Aba Extrato

Exibe o histórico completo de movimentações da caderneta de um cliente.

| Filtro | Descrição |
|---|---|
| **Cliente** | Selecione o cliente |
| **Período** | Data início e data término |
| **Tipo de Extrato** | Resumido (totais agrupados) ou Detalhado (cada transação) |

O extrato mostra cada compra, cada pagamento, o saldo corrente a cada movimentação e as datas.

- **Gerar Relatório** — visualiza na tela.
- **Imprimir** — imprime na impressora térmica para entregar ao cliente.

---

### Aba Compras

Exibe as compras realizadas na caderneta em um período.

| Filtro | Descrição |
|---|---|
| **Cliente** | Opcional — em branco exibe todos |
| **Período** | Data início e data término |
| **Tipo de relatório** | Resumidas, Detalhadas ou Agrupadas por Produto |
| **Ordenação** | Por Cliente ou por Data |

---

### Aba Pagamentos

Exibe os pagamentos recebidos de clientes em um período.

| Filtro | Descrição |
|---|---|
| **Cliente** | Opcional — em branco exibe todos |
| **Período** | Data início e data término |
| **Ordenação** | Por Cliente ou por Data |

---

### Aba Resumo

Exibe a posição geral da caderneta de todos os clientes — quem deve e quanto.

| Filtro | Descrição |
|---|---|
| **Faixa de clientes** | De/até por código (ex: 1 a 9999) |
| **Mostrar apenas com saldo** | Somente clientes com saldo devedor |
| **Mostrar Funcionários** | Inclui cadernetas de funcionários |
| **Mostrar Clientes** | Inclui cadernetas de clientes |
| **Período** | Atual (posição de hoje) ou período personalizado |

> Use esta aba no final do mês para identificar todos os clientes inadimplentes de uma vez.

---

### Aba Canceladas

Exibe as transações de caderneta canceladas — útil para auditoria e verificação de estornos.

| Filtro | Descrição |
|---|---|
| **Cliente** | Opcional |
| **Período** | Data início e data término |
| **Origem** | Pagamentos cancelados, Vendas canceladas ou ambos |

---

## 4. Limite de Crédito

Cada cliente tem um limite de crédito individual, configurado em **Cadastros → Clientes → campo Limite de Caderneta**.

| Situação | O que acontece |
|---|---|
| Cliente com limite disponível | Lançamento realizado normalmente |
| Cliente próximo do limite | Sistema exibe aviso, mas permite o lançamento |
| Cliente sem limite disponível | Sistema bloqueia o lançamento |
| Cliente bloqueado pelo gerente | Sistema bloqueia independente do limite |

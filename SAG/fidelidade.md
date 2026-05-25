# Programa de Fidelidade — Documentação de Uso

Guia completo do módulo de Programa de Fidelidade do SAG. Explica o funcionamento do sistema de pontos, como configurar o programa, como os pontos são acumulados e resgatados, e onde cada função está localizada no sistema.

---

## O que é o Programa de Fidelidade?

O Programa de Fidelidade é um recurso do SAG que permite recompensar clientes recorrentes por meio de um sistema de pontos. A cada compra realizada, o cliente acumula pontos que, ao atingir uma determinada quantidade, podem ser trocados por benefícios — como desconto em dinheiro (cashback) ou produtos gratuitos.

Todo o fluxo é integrado ao processo de venda: os pontos são creditados automaticamente ao finalizar uma compra, e o resgate ocorre diretamente na tela de pagamento do caixa, sem a necessidade de sistemas externos.

---

## Índice

1. [Conceitos fundamentais](#1-conceitos-fundamentais)
2. [Onde fica no sistema](#2-onde-fica-no-sistema)
3. [Configurar o programa](#3-configurar-o-programa)
4. [Cadastrar benefícios](#4-cadastrar-benefícios)
5. [Como os pontos são acumulados](#5-como-os-pontos-são-acumulados)
6. [Como funciona a expiração dos pontos](#6-como-funciona-a-expiração-dos-pontos)
7. [Como o cliente resgata os pontos](#7-como-o-cliente-resgata-os-pontos)
8. [Consultar o extrato de um cliente](#8-consultar-o-extrato-de-um-cliente)
9. [Relatório do programa de fidelidade](#9-relatório-do-programa-de-fidelidade)
10. [Regras e restrições importantes](#10-regras-e-restrições-importantes)

---

## 1. Conceitos Fundamentais

### Programa

O programa é o conjunto de regras que define como os pontos são gerados. Ele possui nome, período de vigência, forma de acúmulo e prazo de expiração dos pontos.

**Só pode haver um programa ativo por vez.** Criar um novo programa exige que o anterior esteja encerrado ou desativado.

### Pontuação

É o valor base que determina quanto o cliente precisa acumular para resgatar benefícios. Por exemplo: se a pontuação for **50**, o cliente precisa de 50 pontos para fazer qualquer resgate.

### Forma de acúmulo

| Forma | Como funciona |
|---|---|
| **Por Valor** | O cliente ganha pontos com base no valor total gasto. Quanto mais gasta, mais pontos acumula |
| **Por Número de Pedidos** | O cliente ganha 1 ponto a cada compra realizada, independentemente do valor |

### Benefício

| Tipo | Como funciona |
|---|---|
| **Cashback** | O cliente troca pontos por um desconto em reais diretamente na compra atual |
| **Produto** | O cliente troca pontos por um produto específico, que é adicionado à compra com desconto integral |

### Extrato

Histórico de movimentações do cliente no programa — toda vez que pontos são acumulados ou gastos, uma entrada é registrada.

---

## 2. Onde fica no sistema

| Área | Para que serve |
|---|---|
| **Cadastros → Programa de Fidelidade** | Criar e gerenciar programas e benefícios |
| **Consultas → Extratos de Fidelidade** | Consultar o histórico de pontos dos clientes |
| **Relatórios → Outros → Programa de Fidelidade** | Gerar relatórios de acúmulo e resgate |
| **Caixa (tela de pagamento)** | Onde o resgate de pontos ocorre durante a venda |

---

## 3. Configurar o Programa

**Caminho:** Cadastros → **Programa de Fidelidade** → **Cadastrar Novo**

| Campo | O que preencher |
|---|---|
| **Nome** | Nome do programa (ex: "Fidelidade 2025", "Club VIP") |
| **Ativo** | Marque para ativar. Apenas um programa pode estar ativo por vez |
| **Forma de Acúmulo** | **Por Valor** ou **Por Número de Pedidos** |
| **Pontuação** | Limite mínimo de pontos que o cliente precisa para resgatar |
| **Início** | Data e hora em que o programa começa a valer |
| **Término** | Data e hora em que o programa encerra |
| **Dias para Expiração dos Pontos** | Quantidade de dias que os pontos permanecem válidos após serem ganhos |

> **Atenção:** Não é possível excluir um programa que já tenha movimentações — use a opção **Desativar**.
> **Atenção:** Não é possível alterar a **Forma de Acúmulo** após o programa ter gerado movimentações.

---

## 4. Cadastrar Benefícios

Acesse o programa na listagem, clique em **Editar** e na seção de benefícios clique em **Adicionar**.

| Campo | O que preencher |
|---|---|
| **Tipo** | **Cashback** (desconto em dinheiro) ou **Produto** (item gratuito) |
| **Produto** | Visível somente para tipo Produto — selecione o item |
| **Valor** *(cashback)* | Valor em reais de desconto ao resgatar |
| **Quantidade** *(produto)* | Número de pontos necessários para resgatar o produto |
| **Ativo** | Marque para que o benefício apareça disponível para resgate |

**Exemplos:**

| Cenário | Tipo | Configuração |
|---|---|---|
| 100 pontos = R$ 10,00 de desconto | Cashback | Valor = 10,00 |
| 50 pedidos = café grátis | Produto | Produto = Café, Quantidade = 50 |

> **Atenção:** Não é possível excluir um benefício que já foi resgatado — use a opção **Desativar**.

---

## 5. Como os Pontos são Acumulados

Os pontos são creditados automaticamente ao finalizar uma venda com **cliente identificado**. Nenhuma ação manual do operador é necessária.

| Forma de acúmulo | Cálculo |
|---|---|
| **Por Valor** | Valor total da venda = pontos gerados (R$ 75,00 → 75 pontos) |
| **Por Número de Pedidos** | Cada venda concluída gera exatamente 1 ponto |

**Condições para acumular:**
- Cliente deve estar **identificado** na venda
- Deve haver um programa de fidelidade **ativo**
- A venda deve estar dentro do **período de vigência** do programa

---

## 6. Como Funciona a Expiração dos Pontos

O campo **Dias para Expiração dos Pontos** define por quantos dias cada ponto permanece válido após ser ganho. O sistema considera automaticamente apenas as movimentações dos últimos N dias ao calcular o saldo.

**Exemplo:** Programa com 30 dias de expiração. Cliente tem 40 pontos ganhos há 35 dias e 20 pontos ganhos há 10 dias → saldo válido = **20 pontos** (os 40 antigos já expiraram).

---

## 7. Como o Cliente Resgata os Pontos

O resgate ocorre **durante o pagamento de uma venda no caixa**, na tela de formas de pagamento.

1. Ao avançar para o pagamento, o sistema verifica automaticamente se o cliente tem pontos suficientes
2. Se houver saldo válido, uma mensagem aparece: *"O cliente possui pontos para resgate no PROGRAMA DE FIDELIDADE"*
3. O operador pressiona **F7** (ou clica no botão correspondente) para abrir a tela de resgate
4. O operador vê: nome do cliente, saldo atual, benefícios disponíveis e saldo após o resgate
5. O operador seleciona o benefício e clica em **Resgatar**
6. O desconto é aplicado automaticamente:
   - **Cashback** → valor em reais lançado como desconto
   - **Produto** → item adicionado à venda com 100% de desconto
7. A mensagem muda para *"Benefício resgatado!"* e o botão F7 é ocultado

### Cashback com valor personalizado

Para o tipo **Cashback**, o cliente pode escolher **quanto do saldo quer usar** — não precisa resgatar tudo de uma vez. O operador informa o valor desejado e o sistema calcula os pontos a descontar.

---

## 8. Consultar o Extrato de um Cliente

**Caminho:** Consultas → **Extratos de Fidelidade**

| Filtro | O que faz |
|---|---|
| **Cliente** | Selecione pelo nome ou código |
| **Tipo de Movimentação** | Todos / somente Acúmulo / somente Gasto |

A lista exibe: código da movimentação, nome do cliente, tipo, valor de pontos, data e hora.

---

## 9. Relatório do Programa de Fidelidade

**Caminho:** Relatórios → Outros → **Programa de Fidelidade**

| Filtro | O que faz |
|---|---|
| **Período** | Intervalo de datas das movimentações |
| **Cliente** | Filtrar por cliente específico ou todos |
| **Tipo de Movimentação** | Acúmulos, gastos ou ambos |

O relatório é organizado por programa e por cliente. Exibe: código, cliente, tipo, pontos, programa, data/hora. No rodapé: total de pontos acumulados e total de pontos resgatados no período.

---

## 10. Regras e Restrições Importantes

| Situação | Regra |
|---|---|
| **Programas simultâneos** | Apenas um programa pode estar ativo por vez |
| **Alteração da forma de acúmulo** | Não permitida após o programa ter gerado movimentações |
| **Exclusão de programa** | Não permitida se houver movimentações — use Desativar |
| **Exclusão de benefício** | Não permitida se já foi resgatado — use Desativar |
| **Cliente obrigatório** | Pontos só são gerados em vendas com cliente identificado |
| **Vigência do programa** | Vendas fora do período de início/término não geram pontos |
| **Expiração automática** | Pontos mais antigos que o prazo configurado são ignorados no saldo |
| **Resgate mínimo** | O cliente precisa atingir o valor de Pontuação configurado para resgatar |
| **Resgate no ato da compra** | O resgate só pode ser feito durante o pagamento de uma venda ativa no caixa |

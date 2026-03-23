# SAG — Produção e Comandas

Módulos de gerenciamento de mesas, comandas e controle de produção.

---

## Comandas

### O que é uma Comanda
Registro de pedido vinculado a uma mesa ou cliente. Itens são lançados na comanda e pagos ao final.

### Abrir Comanda
**Caminho:** Caixa > **F4** (Consulta de Comandas)

1. Pressione **F4** para consultar comandas abertas
2. Para nova comanda: selecione **Nova Comanda**
3. Informe o número da mesa ou o nome do cliente
4. Lance os produtos na comanda

### Lançar Itens na Comanda
1. Com a comanda aberta, adicione produtos normalmente
2. Cada lançamento é associado à comanda
3. Múltiplos atendentes podem lançar na mesma comanda

### Inserir Comanda Parcial
- Pressione **Ctrl + F** para inserir itens de uma comanda no caixa parcialmente
- Útil quando parte da conta é paga por um cliente em um grupo

### Comandas em Espera
- Comanda que ainda não teve o pagamento iniciado
- Aparecem na tela de **Comandas em Espera**
- Podem ser retomadas a qualquer momento

### Fechar Comanda (Pagamento)
1. Acesse a comanda via **F4**
2. Selecione a comanda desejada
3. Revise os itens lançados
4. Pressione **F12** ou **Finalizar**
5. Escolha a forma de pagamento
6. Confirme o pagamento — comanda é fechada

### Terminal de Comandas
**Caminho:** Menu Principal > **Terminal de Comandas**

Interface otimizada para garçons ou atendentes lançarem pedidos diretamente nas mesas, via tablet ou computador na área de atendimento.

---

## Produção

### O que é o Módulo de Produção
Controla o fluxo de preparo dos pedidos: do lançamento no caixa até a entrega ao cliente.

### Acompanhamento de Produção
**Caminho:** Menu Principal > **Acompanhamento** (ou via tela de produção)

Exibe os pedidos em fila organizados por impressora/setor:
- Pedidos **pendentes** (aguardando preparo)
- Pedidos **em produção**
- Pedidos **prontos** (aguardando retirada/entrega)

### Regras de Impressão (Roteamento para Produção)

**Caminho:** Configurações > **Regras de Impressão**

Define qual grupo/categoria de produto vai para qual impressora de produção.

Exemplo:
- Grupo "Bebidas" → Impressora do Balcão
- Grupo "Salgados" → Impressora da Cozinha
- Grupo "Pizzas" → Impressora da Pizzaria

**Como configurar:**
1. Acesse **Configurações > Regras de Impressão**
2. Selecione o grupo ou categoria
3. Associe à impressora correta
4. Defina o número de vias (geralmente 1)
5. Salve e teste com um pedido

> Se itens estão saindo na impressora errada, revise as Regras de Impressão.

---

## Acompanhamentos e Variações de Produto

**Caminho:** Cadastros > **Grupos de Acompanhamento**

Configura extras e variações dos produtos:
- **Adicionais:** ingredientes extras pagos (ex: queijo extra)
- **Opções:** escolhas sem custo adicional (ex: ponto da carne)
- **Variações:** versões do produto (ex: tamanho P, M, G)
- **Obrigatórios:** o cliente precisa escolher para confirmar o pedido

---

## Receitas

**Caminho:** Cadastros > **Receitas**

Vincula ingredientes (itens de estoque) a um produto final.
- Ao vender o produto, o estoque dos ingredientes é baixado automaticamente
- Útil para controle de custo de produção

---

## Tela de Pedidos (Produção / Cozinha)

Interface exibida na cozinha ou área de produção mostrando os pedidos em tempo real:
- Número do pedido
- Itens a preparar
- Mesa ou cliente
- Tempo desde o lançamento
- Botão para marcar como **Pronto**

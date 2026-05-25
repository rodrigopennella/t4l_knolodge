# SAG — Produção e Comandas

Módulos de gerenciamento de mesas, comandas e controle de produção.

---

## O que é uma Comanda

Registro numérico no qual produtos são lançados. Pode ser denominada como **mesa**, **comanda**, ou ambos, dependendo da configuração do estabelecimento.

---

## Comandas — Visualização e Controle

**Caminho:** Menu Principal > **Comandas**

Tela para **visualizar e controlar** todas as comandas do sistema (bloquear, desbloquear, limpar, adicionar). Não é utilizada para lançar produtos.

### Status das Comandas

| Status | Significado |
|---|---|
| **Fechada** | Comanda não está aberta em nenhum terminal. Pode ter itens lançados. |
| **Aberta** | Comanda está aberta em algum terminal no momento. |
| **Bloqueada** | Comanda bloqueada — não pode receber lançamentos. |

### Adicionar Novas Comandas
Para criar comandas no sistema:

1. Acesse **Menu Principal > Comandas**
2. Pressione **F6 — Adicionar Comandas**
3. Informe a quantidade ou intervalo de comandas a criar
4. Confirme

> Se o estabelecimento utiliza **catraca** ou **comandas com RFID**, não orientar pelo passo a passo acima — transferir ao suporte T4L para melhor orientação.

### Atalhos da Tela de Comandas

| Tecla | Função |
|---|---|
| F2 | Limpar Comanda (remove todos os itens) |
| F3 | Bloquear Comanda (individual) |
| F4 | Desbloquear Comanda (individual) |
| F5 | Liberar Comanda |
| F6 | Adicionar Comandas (criar novas) |
| F7 | Excluir Comandas |
| F8 | Bloquear Comandas (em lote) |
| F9 | Desbloquear Comandas (em lote) |

Ícones por comanda na lista:
- **Lixeira** — limpa os itens da comanda
- **Cadeado** — bloquear/desbloquear

---

## Terminal de Comandas — Lançamento de Produtos

**Caminho:** Menu Principal > **Terminal de Comandas**

Interface para **lançar produtos em comandas**. Utilizada por garçons ou atendentes para registrar pedidos diretamente nas mesas ou pontos de atendimento.

### Fluxo de Uso
1. Insira o **Operador** (código de login do atendente)
2. Insira o número da **Comanda**
3. Insira os **Produtos** (por código, nome ou leitor de código de barras)

### Tela do Terminal de Comandas
A tela exibe:
- **Operador** — nome do usuário logado
- **Comanda** — número da comanda com nome da mesa (ex: "Comanda: 1 (Mesa 11)")
- **Total** — valor total da comanda (R$)
- **Campo Produto** — para inserção de novos itens
- **Lista de itens** — tabela com #, Código, Descrição, Preço, Qtd, Total, Data Hora, Usuário

### Atalhos do Terminal de Comandas
| Tecla | Função |
|---|---|
| F1 | Cancela Item |
| F2 | Pesquisar Produtos |
| F3 | Comandas Abertas |
| F4 | Limpar Comanda |
| F7 | Imprimir Prévia |
| F8 | Transferir Comanda |
| F9 | Finalizar no Caixa |
| F11 | Transferir Itens |
| F12 | Finalizar Terminal |
| Ctrl + D | Desconto no Item |
| Ctrl + - | Desconto na Comanda |
| Back | Cancela Item Selecionado |

---

## Produção

### O que é o Módulo de Produção
Controla o fluxo de preparo dos pedidos: do lançamento no caixa até a entrega ao cliente.

**Caminho:** Aba **Produções** na barra superior

O módulo inclui:
| Tela | Função |
|---|---|
| **Receitas** | Cadastro de receitas com ingredientes e quantidades |
| **Nova Produção** | Solicitar produção baseada em uma receita cadastrada |
| **Consultar Produção** | Consultar produções já realizadas |
| **Embalagens** | Cadastro de embalagens usadas na produção |
| **Relatórios** | Relatórios de produção |

### Nova Produção (Solicitar Produção Simplificada)
1. No campo **Produto**, pesquise o produto final
2. Selecione a **Receita** associada
3. Selecione o **Estoque** (ex: Padrão)
4. O campo **Qtd. Receita** é preenchido automaticamente
5. Informe a **Qtd a Produzir**
6. Clique em **Adicionar**
7. O item aparece na lista de **Solicitações** (Receita + Qtd a Produzir)
8. Clique em **Salvar Solicitações** para confirmar

> A produção utiliza a receita cadastrada para baixar os ingredientes do estoque automaticamente. Para dúvidas complexas sobre configuração de receitas e produção, entre em contato com o suporte técnico.

### Receitas
**Caminho:** Produções > **Receitas** (ou Cadastros > **Receitas**)

Vincula ingredientes (itens de estoque) a um produto final.
- Ao vender o produto ou solicitar produção, o estoque dos ingredientes é baixado automaticamente
- Útil para controle de custo de produção

### Acompanhamento de Produção
**Caminho:** Menu Principal > **Acompanhamento** (ou via tela de produção)

Exibe os pedidos em fila organizados por impressora/setor:
- Pedidos **pendentes** (aguardando preparo)
- Pedidos **em produção**
- Pedidos **prontos** (aguardando retirada/entrega)

### Regras de Impressão (Roteamento para Produção)

Define qual grupo/categoria de produto vai para qual impressora de produção.

Exemplo:
- Grupo "Bebidas" → Impressora do Balcão
- Grupo "Salgados" → Impressora da Cozinha
- Grupo "Pizzas" → Impressora da Pizzaria

> Configuração feita exclusivamente pela equipe técnica T4L. Se itens estão saindo na impressora errada, acionar suporte técnico.

---

## Tela de Pedidos (KDS — Kitchen Display System)

**Caminho:** Menu Principal > **Tela de Pedidos**

Interface exibida na cozinha ou área de produção mostrando os pedidos em tempo real (similar aos painéis de redes de fast food):
- Número do pedido
- Itens a preparar
- Mesa ou cliente
- Tempo desde o lançamento
- Botão para marcar como **Pronto**

---

## Acompanhamentos e Variações de Produto

**Caminho:** Cadastros > **Grupos de Acompanhamento**

Configura extras e variações dos produtos:
- **Adicionais:** ingredientes extras pagos (ex: queijo extra)
- **Opções:** escolhas sem custo adicional (ex: ponto da carne)
- **Variações:** versões do produto (ex: tamanho P, M, G)
- **Obrigatórios:** o cliente precisa escolher para confirmar o pedido

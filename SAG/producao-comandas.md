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

---

## Terminal de Comandas

**Caminho:** Menu Principal > **Terminal de Comandas**

Interface dedicada para lançamento de produtos em comandas. Otimizada para garçons ou atendentes lançarem pedidos diretamente nas mesas, via tablet ou computador na área de atendimento.

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

## Tela de Comandas (Gestão)

**Caminho:** Menu Principal > **Comandas**

Tela para visualização e gestão de todas as comandas do sistema. Exibe:

### Painel Esquerdo — Lista de Comandas
| Coluna | Descrição |
|---|---|
| CMD | Número da comanda |
| STATUS | Fechada / Aberta / Bloqueada |
| ÚLTIMO USO | Data e hora do último lançamento |
| TOTAL | Valor total da comanda |

Filtros:
- Tipo: Ambas / Abertas / Fechadas
- Checkbox: Em Uso
- Campo de pesquisa por número de comanda

### Painel Direito — Detalhes da Comanda
Ao selecionar uma comanda, exibe os itens:
| Coluna | Descrição |
|---|---|
| CÓDIGO | Código do produto |
| DESCRIÇÃO | Nome do produto |
| QUANTIDADE | Qtd lançada |
| TOTAL | Valor total do item |
| DATA E HORA | Momento do lançamento |
| OPERADOR | Quem lançou o item |

### Atalhos da Tela de Comandas
| Tecla | Função |
|---|---|
| F2 | Limpar Comanda (remove todos os itens) |
| F3 | Bloquear Comanda (individual) |
| F4 | Desbloquear Comanda (individual) |
| F5 | Liberar Comanda |
| F6 | Adicionar Comandas (criar novas comandas) |
| F7 | Excluir Comandas |
| F8 | Bloquear Comandas (em lote) |
| F9 | Desbloquear Comandas (em lote) |

Ícones por comanda:
- Ícone de lixeira: excluir
- Ícone de cadeado: bloquear/desbloquear

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

**Caminho:** Config. Terminal > **Impressoras** (seção Terminal PC e Pedidos)

Define qual grupo/categoria de produto vai para qual impressora de produção.

Exemplo:
- Grupo "Bebidas" → Impressora do Balcão
- Grupo "Salgados" → Impressora da Cozinha
- Grupo "Pizzas" → Impressora da Pizzaria

> Se itens estão saindo na impressora errada, revise as Regras de Impressão.

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

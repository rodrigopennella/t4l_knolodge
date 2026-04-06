# SAG — Pedidos e Delivery

Módulo de gerenciamento de pedidos para delivery, retirada e mesas.

---

## Novo Pedido

**Caminho:** Menu Principal > **Novo Pedido** ou aba **Delivery** > **Novo Pedido**

> O atalho "Novo Pedido" em Principal e em Delivery abre a mesma tela.

### Tela de Pedido

**Seção Cliente (topo):**
| Campo | Observação |
|---|---|
| Telefone | Busca por telefone do cliente (com DDD) |
| Botão Pesquisar (lupa) | Busca na base de clientes cadastrados |
| Botão Editar (lápis) | Edita dados do cliente selecionado |
| Cliente | Nome exibido após seleção |

**Tipo de Entrega:**
- **Entrega:** seleciona endereço do cliente, com opção de calcular distância
- **Retirada:** cliente retira no local

**Origem e Tipo (canto superior direito):**
- **Origem:** SagDelivery, iFood, WhatsApp, Telefone, etc. (seleção dropdown)
- **Tipo:** Pedido / Encomenda / Orçamento (seleção por radio button)

**Seção Produtos:**
| Campo | Observação |
|---|---|
| Produto | Código do produto (digitação ou leitor) |
| Descrição | Nome do produto (preenchido automaticamente) |
| Preço | Valor unitário |
| Qtd | Quantidade |
| Total | Valor total do item |

**Lista de itens:** Tabela com #, Código, Descrição, Preço, Qtd, Total

**Totais (rodapé):**
- Subtotal
- Desconto
- Total (R$)

### Atalhos da Tela de Pedido
| Tecla | Função |
|---|---|
| F1 | Cancela Item |
| F2 | Consulta Produtos |
| F3 | Cancelar Pedido |
| F4 | Detalhes do Pedido |
| F5 | Consulta de Pedidos |
| F6 | Pedido Vinculado a Comanda |
| F7 | Últimos Pedidos Realizados |
| F10 | Inserir Pizza |
| F11 | Finalizar na Caderneta |
| F12 | Exibir Caixa |
| Ctrl + D | Desconto Item |
| Ctrl + - | Desconto no Pedido |
| ESC | Sair |

---

## Adicionar Produtos ao Pedido

1. Selecione o cliente e tipo de entrega
2. No campo **Produto**, insira o código ou pesquise com F2
3. Informe a quantidade no campo **Qtd**
4. Pressione **Enter** para adicionar
5. Para produtos com acompanhamentos obrigatórios, o sistema solicita a seleção antes de confirmar

### Produtos com Acompanhamento
- O sistema exibe a tela de **Acompanhamentos** automaticamente
- Tipos: opcionais, obrigatórios, adicionais pagos, variações

### Pedido de Pizza
- Pressione **F10** para inserir pizza
- Selecione o **Tamanho**
- Selecione os **Sabores** (1 ou mais, conforme tamanho)
- Selecione a **Borda** (se disponível)
- Confirme o pedido

---

## Consulta de Pedidos

**Caminho:** Aba **Delivery** > **Consulta de Pedidos** ou Caixa > **F8**

Tela completa de gerenciamento de pedidos com filtros avançados:

### Filtros Disponíveis
| Filtro | Opções |
|---|---|
| Filtrar por | Data pedido (padrão) |
| Período | Data inicial e final |
| Status | Todos / Em Andamento / Finalizado / Cancelado |
| Tipo | Todos / Pedido / Encomenda / Orçamento |
| Pagamento | Todos / formas específicas |
| Ent/Ret | Todos / Entrega / Retirada |
| Cliente | Pesquisa por nome |
| Telefone | Pesquisa por telefone |
| Origem | Todas / SagDelivery / iFood / WhatsApp / etc. |
| Cod | Código do pedido |

### Colunas da Lista
| Coluna | Descrição |
|---|---|
| CÓDIGO | Número do pedido (com ícone de origem, ex: WhatsApp) |
| CLIENTE | Nome do cliente |
| DATA | Data e hora do pedido |
| STATUS | Em Andamento / Finalizado / Cancelado |
| TEL | Telefone do cliente |
| TOTAL | Valor total (R$) |
| TIPO | Pedido / Encomenda / Orçamento |

### Ações por Pedido (ícones à direita)
Cada pedido exibe ícones de ação:
- Ícone de moto/entregador — associar entregador
- Ícone de impressora — reimprimir pedido
- Ícone de check verde — marcar como finalizado
- Ícone de WhatsApp — enviar mensagem ao cliente
- Outros ícones de gerenciamento

---

## Módulo Delivery

**Caminho:** Aba **Delivery** na barra superior

O módulo Delivery concentra as funcionalidades específicas de delivery:
- **Novo Pedido** — mesma tela acessível em Principal
- **Consulta de Pedidos** — gerenciamento completo com filtros
- **Relatórios** — relatórios específicos de delivery

### Relatórios de Delivery
**Caminho:** Delivery > **Relatórios**

| Relatório | Descrição |
|---|---|
| Produção | Relatório de produção dos pedidos |
| Pedidos Resumidos | Resumo de pedidos por período |
| Pedidos Por Origem | Agrupado por canal (iFood, WhatsApp, balcão, etc.) |
| Pedidos Completos | Detalhamento completo de cada pedido |
| Pedidos Por Entregador | Performance por entregador |
| Pedidos Por Usuário | Pedidos lançados por operador |
| Consulta de Vendas | Vendas originadas de pedidos |
| Produtos por Pedido | Detalhamento de produtos em cada pedido |
| Resumo de Pedidos | Totais consolidados |
| Histórico dos Pedidos | Histórico completo de alterações |
| Taxas por Origem | Taxas de entrega por canal |
| Exportar Dados | Exportação de dados para planilha |
| Pedidos Alterados | Pedidos que sofreram alterações |

### Filtros dos Relatórios
- Tipo de Data (Pedido)
- Formato (Pedido Resumido, etc.)
- Agrupar por grupo / subgrupo
- Período
- Grupo / SubGrupo
- Status
- Cliente
- Tipo
- Origem

---

## Integrações de Delivery

O SAG possui integração com diversas plataformas de delivery:
- **iFood**
- **99food**
- **Keeta**
- **OpenDelivery**
- Entre outras

> As integrações são sempre configuradas por um técnico da T4L. Taxas de entrega e taxa de serviço também são configuráveis pela equipe técnica.

### Configurar Integração (via técnico)
1. Acesse **Configurações > Integrações** (ou Config. Global > Delivery)
2. Selecione a plataforma desejada
3. Informe as credenciais da integração
4. Habilite a sincronização
5. Pedidos passam a aparecer automaticamente no SAG

### Problemas com Integrações
- Se pedidos não chegam: verifique se a integração está habilitada
- Se pagamento não passa: verifique as configurações de pagamento
- Reinicie o serviço de integração se necessário
- Para problemas na plataforma do parceiro (iFood, etc.), contate o suporte da plataforma diretamente

---

## Romaneio de Entregas

**Caminho:** Menu Principal > **Romaneio**

Módulo voltado para fábricas e operações de distribuição. Tem estrutura semelhante ao delivery, mas focado em:
- Emissão de NF-e para entregas
- Geração de boletos
- Geração de faturas
- Organização de rotas de entrega

---

## Caderneta nos Pedidos

- Na tela de Novo Pedido, pressione **F11** para finalizar na caderneta
- O valor do pedido fica registrado para pagamento futuro
- Consulta e recebimento: via **Caderneta** no menu Principal ou **F7** no caixa

---

## Programa de Fidelidade (Pedidos)

- Pontos são acumulados automaticamente nas vendas
- Consulta: Caixa > **Ctrl + L**
- Resgate de pontos: disponível na finalização do pedido conforme configuração

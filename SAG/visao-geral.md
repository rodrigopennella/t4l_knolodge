# SAG — Visão Geral do Sistema

O SAG é um sistema de PDV (Ponto de Venda) para Windows, desenvolvido para estabelecimentos de food service como padarias, restaurantes, mercados, lanchonetes e fábricas. Funciona como um ERP organizado em abas na barra de navegação superior.

---

## Barra de Navegação Superior (Abas Principais)

O sistema é dividido nas seguintes abas, acessíveis pela barra superior:

| Aba | Função Principal |
|---|---|
| **Dashboard** | Resultados do faturamento diário, semanal e mensal do estabelecimento |
| **IA** | Módulo de inteligência artificial integrado ao SAG |
| **Principal** | Tela principal com atalhos para Caixa, Terminal de Comandas, Caderneta, Comandas, Novo Pedido e Tela de Pedidos |
| **Cadastros** | Produtos, Clientes, Fornecedores, Funcionários, Grupos, Promoções, etc. |
| **Produções** | Receitas, Nova Produção, Consultar Produção, Embalagens, Relatórios |
| **Estoque** | Entrada de Nota, Relatórios, Locais de Estoque, Estoque Atual, Ajustes, Inventário, Pedido de Compra, etc. |
| **Financeiro** | Contas a Pagar/Receber, Contas Bancárias, Categorias, Conciliação, Extratos, Relatórios |
| **Delivery** | Consulta de Pedidos, Novo Pedido, Relatórios específicos de delivery |
| **Romaneio** | Módulo voltado para fábricas e distribuição — emissão de NF-e, boletos e faturas |
| **NFe** | Emitir, Gerenciar, Configuração, Inutilizar, NFe Recebidas, Vendas, Pedidos, Perfil de Impostos, Exportar |
| **Relatórios** | Fechamento de Caixa, Faturamento, Consultas, Itens Cancelados, Notas, Vendas, Listagem, Caderneta, Comissões, etc. |
| **Outros** | Central de Usuários, Ferramentas, Grupo de Permissões, Certificado Digital, Licença, TEF, Impressoras Remotas, Etiquetas, Config Espécies, Cartão de Acesso, Lei do Imposto, Ferramentas CFe, Conf. Dispositivos Móveis, Configurações de Tela de Pedidos, Arqs. da Balança, Dados Cadastrais |

---

## Canto Superior Direito — Configurações e Acesso

No canto superior direito da tela, além do nome do usuário logado, existem os seguintes acessos:

| Item | Função |
|---|---|
| **Suporte** | Acesso ao suporte T4L |
| **Config. Terminal** | Configurações específicas por terminal/caixa (impressoras, NFC-e, TEF, caixa, balança, personalizar, delivery, outros). Acesso restrito a técnicos. |
| **Config. Global** | Configurações que valem para todo o sistema (Email, Caixa, Delivery, Romaneio, Comandas, Estoque, Financeiro, Etiquetadora, Outros, Módulos, Autoatendimento, NFC-e). Acesso restrito a técnicos. |

> **Config. Terminal** define comportamentos por máquina (ex: qual impressora usar, se pede CPF, se utiliza comandas, se lança valores no fechamento). **Config. Global** define comportamentos para o sistema todo (ex: taxa de serviço, taxa de entrega, DDD padrão, integrações logísticas).

---

## Dashboard

**Caminho:** Aba **Dashboard** na barra superior

Tela de acompanhamento dos resultados do negócio. Exibe:

**Seção Hoje:**
- Vendas (quantidade)
- Ticket Médio (R$)
- Faturamento (R$)
- Pedidos (quantidade)
- Itens Cancelados (quantidade)

**Seção Últimos 30 Dias:**
- Vendas (quantidade)
- Ticket Médio (R$)
- Faturamento (R$)
- Item Mais Vendido (produto, quantidade e percentual do faturamento)

**Gráfico:**
- Faturamento por Dia — gráfico dos últimos 30 dias mostrando o faturamento dia a dia

---

## Módulo IA

**Caminho:** Aba **IA** na barra superior (identificada com badge "NEW")

Módulo de inteligência artificial integrado ao SAG. A IA consegue:
- Orientar o cliente em dúvidas sobre relatórios
- Gerar informações e análises puxando dados do banco de dados do estabelecimento

**Plano de uso:**
- 20 perguntas gratuitas para todos os clientes
- Após as 20 perguntas, o módulo se torna pago
- A opção de pagamento aparece em tela para o cliente (necessário ter permissão de usuário)

---

## Tela Principal

**Caminho:** Aba **Principal** na barra superior

Tela com atalhos em cards coloridos para os módulos mais usados:

| Card | Função |
|---|---|
| **Caixa** | Abre a Frente de Caixa (PDV) para efetuar vendas |
| **Terminal de Comandas** | Terminal de lançamento de produtos em comandas (fluxo: Operador > Comanda > Produtos) |
| **Caderneta** | Gerenciamento de caderneta — recebimento, extrato, compras, pagamentos, resumo, canceladas |
| **Comandas** | Visualização e gestão das comandas (status, bloqueio, exclusão, etc.) |
| **Novo Pedido** | Atalho para cadastrar um pedido no delivery (mesma tela do módulo Delivery) |
| **Tela de Pedidos** | Tela tipo KDS (Kitchen Display System) — semelhante ao painel de pedidos de redes de fast food |

---

## Estrutura de Módulos

```
SISTEMA SAG
├── Dashboard (Faturamento diário/semanal/mensal)
├── IA (Inteligência Artificial integrada)
├── Principal
│   ├── Caixa (Frente de Caixa / PDV)
│   ├── Terminal de Comandas
│   ├── Caderneta
│   ├── Comandas
│   ├── Novo Pedido
│   └── Tela de Pedidos (KDS)
├── Cadastros
│   ├── Produtos
│   ├── Clientes
│   ├── Grupos
│   ├── Funcionários
│   ├── Cupom Desconto
│   ├── Entregadores
│   ├── Programa de Fidelidade
│   ├── Transportadoras
│   ├── Fornecedores
│   ├── Alteração de Preço Programada
│   ├── Grupos de Impostos
│   ├── Grupos de Acompanhamento
│   ├── Grupo de Preço Diferenciado
│   └── Promoção
├── Produções
│   ├── Receitas
│   ├── Nova Produção
│   ├── Consultar Produção
│   ├── Embalagens
│   └── Relatórios
├── Estoque
│   ├── Entrada de Nota
│   ├── Relatórios
│   ├── Locais de Estoque
│   ├── Estoque Atual
│   ├── Consulta de Notas
│   ├── Saída de Produtos
│   ├── Ajuste de Estoque
│   ├── Transferência de Estoque
│   ├── Inventário
│   ├── Pedido de Compra
│   ├── Cotação
│   ├── Produtos Fornecedores
│   ├── CFOP Parametrização
│   └── Análise de Preços
├── Financeiro
│   ├── Contas a Pagar
│   ├── Contas a Receber
│   ├── Contas Bancárias
│   ├── Categorias
│   ├── Conciliação Bancária
│   ├── Transferência Bancária
│   ├── Extratos
│   ├── Relatórios
│   ├── Ajuste de Conta
│   ├── Espécies
│   ├── Central de Faturas
│   └── Conciliação de Recebíveis
├── Delivery
│   ├── Novo Pedido
│   ├── Consulta de Pedidos
│   └── Relatórios (Produção, Pedidos Resumidos, Por Origem, Completos, Por Entregador, Por Usuário, Consulta de Vendas, Produtos por Pedido, Resumo, Histórico, Taxas por Origem, Exportar Dados, Pedidos Alterados)
├── Romaneio (Fábricas — NF-e, boletos, faturas)
├── NFe
│   ├── Emitir
│   ├── Gerenciar
│   ├── Configuração
│   ├── Inutilizar
│   ├── NFe Recebidas
│   ├── Vendas
│   ├── Pedidos
│   ├── Perfil de Impostos
│   └── Exportar
├── Relatórios
│   ├── Fechamento de Caixa
│   ├── Faturamento
│   ├── Consultas
│   ├── Itens Cancelados
│   ├── Notas
│   ├── Vendas
│   ├── Listagem
│   ├── Caderneta
│   ├── Entradas e Saídas
│   ├── Comandas Abertas
│   ├── Venda por Usuário
│   ├── Comissões
│   ├── Lucros e Mark Up
│   └── Outros
├── Outros
│   ├── Central de Usuários
│   ├── Ferramentas
│   ├── Grupo de Permissões
│   ├── Arqs. da Balança
│   ├── Etiquetas
│   ├── Impressoras Remotas
│   ├── Dados Cadastrais
│   ├── Certificado Digital
│   ├── Licença
│   ├── Config Espécies
│   ├── Cartão de Acesso
│   ├── Lei do Imposto
│   ├── Ferramentas CFe
│   ├── TEF
│   ├── Conf. Dispositivos Móveis
│   └── Configurações de Tela de Pedidos
└── Integrações
    ├── iFood
    ├── 99food
    ├── Keeta
    ├── OpenDelivery
    ├── TEF / SiTef
    ├── Multiloja
    └── Automatizador
```

---

## Login

- Campo: **Usuário**
- Campo: **Senha**
- Após login, o menu superior exibe: **Alterar Senha** e **Sair**

---

## Atalhos de Teclado — Frente de Caixa

| Tecla | Função |
|---|---|
| F1 | Outras Funções (abre caixa de seleção: 1-Abrir Gaveta, 2-Venda em Espera, 3-Comandas Abertas, 4-Caixa em Espera, 5-Devolução de Venda, 6-Devolução de Produto, 7-Central NFC-e, 8-Central de Ajustes TEF, 9-Bloqueia Tela Caixa) |
| F2 / Enter | Iniciar Venda (sem pedir CPF) |
| F3 | Iniciar Venda (solicita CPF primeiro) |
| F4 | Consulta de Comandas |
| F5 | Cancelar Item |
| F6 | Cancelar Venda |
| F7 | Pagamento de Caderneta |
| F8 | Consulta de Pedidos (abre tela para inserir código do pedido em aberto para finalização no caixa) |
| F9 | Consulta de Produtos |
| F10 | Últimas Vendas efetuadas |
| F11 | Entradas e Saídas (Sangria — registrar saídas e entradas de valores físicos) |
| F12 | Finalizar Caixa (pergunta confirmação; se habilitado no Config. Terminal e o usuário tiver permissão, aparece a função de lançar valores reais para o fechamento) |
| Ctrl + D | Desconto no Item |
| Ctrl + - | Desconto na Venda |
| Ctrl + E | Venda em Espera (se tem comanda vinculada, pergunta se deseja voltar para comanda original; se não tem, pede a comanda) |
| Ctrl + U | Última Venda |
| Ctrl + F | Inserir Comanda Parcial (inserir um ou mais produtos das comandas) |
| Ctrl + L | Extrato Programa de Fidelidade |

---

## Atalhos — Tela de Formas de Pagamento

| Tecla | Função |
|---|---|
| F1 | Inserir CPF |
| F2 | Pesquisa Cliente |
| F3 | Inserir Observação |
| F4 | Inserir Voucher |
| F5 | Inserir Cupom Desconto |
| F6 | Cadastrar |

---

## Atalhos — Terminal de Comandas

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

## Atalhos — Tela de Comandas (Gestão)

| Tecla | Função |
|---|---|
| F2 | Limpar Comanda |
| F3 | Bloquear Comanda |
| F4 | Desbloquear Comanda |
| F5 | Liberar Comanda |
| F6 | Adicionar Comandas |
| F7 | Excluir Comandas |
| F8 | Bloquear Comandas (lote) |
| F9 | Desbloquear Comandas (lote) |

---

## Atalhos — Tela de Novo Pedido

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

## Arquitetura Geral

- **Servidor:** computador central que hospeda o banco de dados. Todos os caixas e tablets se conectam a ele.
- **Caixas:** estações que rodam o SAG conectadas ao servidor pela rede local.
- **Tablets/Celulares:** usam o app SAG para lançar pedidos e comandas, sincronizando com o servidor.
- **Acesso remoto:** via AnyDesk, o suporte pode acessar o computador do cliente remotamente.

---

## Tipos de Estabelecimento Atendidos

| Tipo | Funcionalidades Mais Usadas |
|---|---|
| Padaria | Caixa, Balança, Produção, Caderneta |
| Restaurante | Comandas, Mesas, Produção, Relatórios |
| Pizzaria | Cadastro de Pizza, Acompanhamentos, Comandas |
| Mercado | Caixa, Estoque, NFC-e, Balança |
| Lanchonete | Caixa, Pedidos, Totem de Auto-Atendimento |
| Delivery | Pedidos, iFood, 99food, Keeta, OpenDelivery, Romaneio |
| Fábrica | Romaneio, NF-e, Boletos, Faturas |

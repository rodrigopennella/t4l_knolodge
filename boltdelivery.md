# BoltDelivery — Plataforma de Delivery Online

O **BoltDelivery** é uma plataforma de delivery web desenvolvida e gerenciada pela T4L. Permite que o estabelecimento ofereça um cardápio online próprio — o cliente acessa pelo navegador, faz o pedido e ele aparece automaticamente no SAG.

Site: https://boltdelivery.com.br/

---

## O que é

- Aplicativo 100% web (sem instalação — funciona no navegador)
- O cliente final acessa o cardápio do estabelecimento, escolhe os produtos e realiza o pedido
- Os pedidos chegam ao estabelecimento em tempo real
- Suporta **pedidos** comuns e **encomendas** (data futura)
- Integra com o módulo de Delivery do SAG

---

## Integração com o SAG

Os pedidos realizados pelo BoltDelivery chegam ao SAG como qualquer outro pedido de delivery — aparecem na **Consulta de Pedidos** e no **Kanban de Pedidos** com a origem identificada como BoltDelivery.

> Qualquer problema na integração entre BoltDelivery e SAG → **ESCALAR_SUPORTE**.

---

## Interface da Plataforma (Painel do Estabelecimento)

O painel de gerenciamento do BoltDelivery é acessado via navegador. Possui as seguintes abas:

| Aba | Função |
|---|---|
| **Pedidos** | Lista os pedidos do dia. Filtro "mostrar finalizados" para incluir pedidos já concluídos. Botão de atualização manual (ícone laranja). |
| **Cardápio** | Cadastro e gerenciamento dos produtos disponíveis para o cliente final |
| **Clientes** | Base de clientes que já realizaram pedidos |
| **Usuários** | Gerenciamento de usuários com acesso ao painel |
| **Marketing** | Ferramentas de divulgação e promoções |
| **Relatórios** | Relatórios de pedidos e vendas |
| **Personalizar** | Personalização visual da loja (cores, logo, banner) |
| **Configs** | Configurações gerais da loja (horários, taxas, endereço) |

### Indicadores do painel

- **Nome do estabelecimento e CNPJ** exibidos no topo direito
- **Status "em atividade"** (ponto verde) — indica que a loja está aberta e aceitando pedidos

### Tela de Pedidos

- Painel dividido em duas colunas: lista de pedidos (esquerda) e detalhes do pedido selecionado (direita)
- Exibe a data selecionada para consulta
- Toggle **"mostrar finalizados"** para alternar entre pedidos ativos e concluídos
- Quando nenhum pedido está selecionado, a coluna direita exibe "nenhum pedido selecionado"

---

## Responsabilidade de Suporte

O BoltDelivery é gerenciado pela T4L. Problemas com a plataforma (acesso, cardápio, pedidos não chegando, integração com SAG) devem ser escalados ao suporte T4L.

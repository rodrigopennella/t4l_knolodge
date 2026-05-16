# Auto-Atendimento — Documentação de Uso

Guia completo dos sistemas de auto-atendimento do SAG: totem de pedidos, auto-serviço com balança e pagamento de comanda pelo próprio cliente.

---

## Visão Geral

| Modalidade | Para que serve | Exemplo de uso |
|---|---|---|
| **Totem de Pedidos** | Cliente monta o próprio pedido na tela | Restaurante, pizzaria, lanchonete |
| **Auto-Serviço com Balança** | Produto pesado automaticamente na balança | Padaria, açougue, rotisserie |
| **Pagamento de Comanda** | Cliente paga a comanda sem passar pela fila do caixa | Bar, restaurante com mesas |

> **Configuração:** Todas as modalidades são configuradas pela equipe técnica T4L antes do uso. O cliente operador não acessa essas configurações.

---

## 1. Totem de Pedidos

O cliente faz todo o pedido na tela, monta combinações, escolhe acompanhamentos e paga sem precisar de um atendente.

### Tela Inicial

- Exibe tela de boas-vindas com logo/imagem do estabelecimento e mensagem **"Toque para começar"**.
- Enquanto não há interação, pode exibir vídeo ou imagem promocional em segundo plano.

### Tipo de Pedido

| Opção | Quando usar |
|---|---|
| **Comer Aqui** | Consumo no local |
| **Para Viagem** | Embalado para levar |

### Cardápio e Categorias

- **Coluna esquerda:** lista de categorias em botões verticais (Pizzas, Bebidas, Lanches, etc.)
- **Coluna direita:** produtos da categoria selecionada com foto, nome, descrição e preço.

### Adicionar Produto

- Se o produto tiver **acompanhamentos obrigatórios:** o sistema exibe as opções antes de continuar.
- Se tiver **acompanhamentos opcionais:** exibe adicionais com preços, o cliente pode selecionar ou ignorar.
- Na **tela de resumo do item:** cliente define a quantidade e clica em **Adicionar ao Carrinho**.

### Adicionar Pizza

1. **Tamanho** — pequena, média, grande, família, etc.
2. **Sabor** — sabor principal entre os disponíveis.
3. **Sabores Adicionais** — meio a meio ou mais sabores (opcional, pode ter custo extra).
4. **Resumo** — exibe tamanho, sabores, adicionais e preço final.

### Carrinho e Revisão

A qualquer momento o cliente pode ver os itens adicionados:
- Nome, configurações, quantidade, preço e subtotal de cada item.
- Botão **X** para remover um item.
- Pode voltar ao cardápio para adicionar mais itens.

### Informar Nome

Antes de pagar, o cliente informa o nome para identificação do pedido. Um teclado virtual aparece na tela. Em alguns casos, pode ser solicitado o CPF.

### Pagamento

| Forma | Como funciona |
|---|---|
| **Dinheiro** | Cliente informa o valor. Sistema exibe o troco. Operador recebe e confirma. |
| **Débito** | Cliente aproxima/insere o cartão na maquininha. Sistema aguarda aprovação. |
| **Crédito** | Igual ao débito. Cliente pode escolher parcelamento. |
| **PIX** | Sistema gera QR Code. Cliente escaneia. Sistema confirma automaticamente. |

### Finalização

- Tela de agradecimento com **número do pedido** para acompanhar o preparo.
- Pode exibir o **tempo estimado** de preparo.
- Após alguns segundos, volta ao início automaticamente.
- O pedido é enviado automaticamente para a produção (cozinha ou balcão).

---

## 2. Auto-Serviço com Balança

Sistema para estabelecimentos que vendem produtos a peso: padarias, açougues, rotisseries.

### Como funciona

1. O cliente coloca o prato ou embalagem na **balança**.
2. A câmera ou sensor identifica o produto.
3. A tela exibe: nome do produto, preço por quilo, peso medido e valor total.
4. O sistema gera o cupom ou etiqueta de peso automaticamente.
5. O cliente retira o produto com o cupom e vai ao caixa pagar (ou o pagamento é integrado diretamente).

### O que aparece na tela

| Informação | Descrição |
|---|---|
| Imagem ao vivo | Câmera exibe o que está sendo pesado em tempo real |
| Preço unitário | Valor por kg ou unidade |
| Quantidade pesada | Peso registrado pela balança |
| Total | Valor calculado automaticamente |
| Mensagem promocional | Exibida no rodapé quando não há produto na balança |

---

## 3. Pagamento de Comanda pelo Cliente

Permite que o próprio cliente pague sua comanda sem chamar um atendente ou ir até o caixa. Indicado para bares e restaurantes com mesas e comanda numerada.

### Fluxo de uso

1. **Identificação:** Cliente escaneia o QR Code ou código de barras da comanda em um terminal disponível no ambiente.
2. **Resumo:** Tela exibe todos os itens consumidos com valores e total da comanda.
3. **Pagamento:**

| Opção | Como funciona |
|---|---|
| **Dinheiro** | Cliente informa quanto vai pagar. Sistema calcula o troco. |
| **Débito / Crédito** | Cliente usa a maquininha. |
| **PIX** | Sistema gera QR Code para leitura pelo celular. |

4. **Confirmação:** Após o pagamento, a comanda é encerrada automaticamente e o cliente recebe confirmação na tela.

### Pagamento parcial (mais de uma pessoa)

1. O primeiro cliente seleciona quais itens são seus.
2. Paga apenas pelo valor dos itens selecionados.
3. A comanda continua aberta com o restante para os demais pagarem.

---

## Problemas Comuns

| Situação | Encaminhamento |
|---|---|
| Totem não inicia / tela preta | ESCALAR_SUPORTE |
| Produto não aparece no cardápio do totem | Verificar se está ativo em Cadastros → Produtos; se persistir: ESCALAR_SUPORTE |
| Balança não pesa / valor incorreto | ESCALAR_SUPORTE |
| Pagamento de comanda não abre / erro ao escanear | ESCALAR_SUPORTE |
| Qualquer configuração dos sistemas | Acesso exclusivo da equipe técnica T4L → ESCALAR_SUPORTE |

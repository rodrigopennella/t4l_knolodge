# Caixa — Documentação de Uso

Guia completo da operação de caixa no SAG: abertura, venda, pagamentos, descontos, devoluções, sangria e fechamento.

---

## Índice

1. [Abertura do Caixa](#1-abertura-do-caixa)
2. [Frente de Caixa](#2-frente-de-caixa)
3. [Lançar Produtos](#3-lançar-produtos)
4. [Aplicar Desconto](#4-aplicar-desconto)
5. [Cancelar Item ou Venda](#5-cancelar-item-ou-venda)
6. [Formas de Pagamento](#6-formas-de-pagamento)
7. [Comandas em Espera](#7-comandas-em-espera)
8. [Últimas Vendas e Reimpressão](#8-últimas-vendas-e-reimpressão)
9. [Devolução de Venda](#9-devolução-de-venda)
10. [Sangria e Suprimento](#10-sangria-e-suprimento)
11. [Bloquear o Caixa](#11-bloquear-o-caixa)
12. [Fechamento do Caixa](#12-fechamento-do-caixa)
13. [Outras Funções](#13-outras-funções)

---

## 1. Abertura do Caixa

Antes de realizar qualquer venda, o operador precisa abrir o caixa para registrar o troco inicial disponível.

1. Ao iniciar o sistema, a tela de abertura de caixa abre automaticamente.
2. Informe o **Troco Inicial** — o valor em dinheiro físico que está no caixa no início do turno.
3. Se precisar contar as cédulas, use o botão da **Calculadora de Cédulas**.
4. Clique em **Abrir Caixa** para confirmar.

---

## 2. Frente de Caixa

| Área | O que exibe |
|---|---|
| **Campo Comanda** | Entrada do número da comanda |
| **Campo Produto** | Entrada do código ou EAN do produto |
| **Painel esquerdo** | Nome, valor unitário, quantidade e total do item |
| **Lista central** | Todos os itens lançados na venda atual |
| **Barra de totais** | Subtotal, desconto e valor total |
| **Rodapé** | Botões de função (F1 a F12) |

### Atalhos de teclado — Frente de Caixa

| Tecla | Função |
|---|---|
| **F1** | Menu completo de funções |
| **F3** | Inicia uma nova venda |
| **F4** | Lista de comandas em aberto |
| **F5** | Cancela o item selecionado |
| **F6** | Cancela a venda inteira |
| **F7** | Pagamento de caderneta |
| **F8** | Consulta pedidos de delivery |
| **F9** | Consulta produtos |
| **F10** | Exibe as últimas vendas |
| **F11** | Sangria / Entradas e Saídas |
| **F12** | Fecha o caixa |

---

## 3. Lançar Produtos

1. Pressione **F3** para iniciar uma nova venda.
2. Escaneie o código de barras ou digite o código manualmente no campo **Produto** e pressione **Enter**.
3. Ajuste a **Quantidade** se necessário.
4. O produto é adicionado à lista central automaticamente.
5. Repita para os demais produtos.

### Lançar com comanda

1. Digite o número da comanda no campo **Comanda** antes de lançar produtos.
2. O sistema associa os itens àquela comanda.
3. A comanda pode ser retomada depois sem perder os itens.

### Observação em um item

1. Após lançar o item, selecione-o na lista.
2. Acesse **F1 → Observação do Item**.
3. Digite a observação e confirme.

---

## 4. Aplicar Desconto

### Desconto em um item — Ctrl + D

1. Pressione **Ctrl + D**
2. Se houver um item pré-selecionado na lista, o desconto é aplicado diretamente a ele
3. Se nenhum item estiver selecionado, o sistema pede o **índice do item** — número exibido na coluna **#** à esquerda da lista
4. Escolha o tipo: **Porcentagem (%)** ou **Preço de Venda (R$)**
5. Informe o valor e confirme

> Também funciona no **Terminal de Comandas** e no **Delivery** para desconto em item.

---

### Desconto na venda inteira — Ctrl + -

1. Pressione **Ctrl + -** durante a venda
2. Escolha o tipo: **Porcentagem (%)** ou **Preço de Venda (R$)**
3. Informe o valor e confirme

> Para que o desconto na venda funcione, é necessário que a espécie **Desconto** esteja cadastrada nas formas de pagamento. Sem ela, o **Ctrl + -** não funciona.

---

### Desconto pela tela de pagamento

Na tela de formas de pagamento, se a espécie **Desconto** estiver cadastrada, basta clicar sobre ela para aplicar o desconto na venda — funciona da mesma forma que o **Ctrl + -**.

---

> Descontos podem exigir permissão configurada no Grupo de Permissões do usuário.

---

## 5. Cancelar Item ou Venda

### Cancelar um item

1. Selecione o item na lista central.
2. Pressione **F5**.
3. Informe o motivo do cancelamento.
4. O item é removido e o total é recalculado.

### Cancelar a venda inteira

1. Pressione **F6** e confirme.
2. Todos os itens são removidos e a venda é encerrada sem registro.

> O cancelamento pode exigir senha do gerente, conforme configuração.

---

## 6. Formas de Pagamento

Após lançar todos os produtos, clique no **Total** para acessar a tela de pagamento.

### Dinheiro

1. Selecione **Dinheiro**.
2. Informe o valor recebido do cliente.
3. O sistema calcula o troco automaticamente.
4. Confirme para finalizar.

### Cartão de Débito ou Crédito

1. Selecione **Débito** ou **Crédito**.
2. O sistema aciona a maquininha (TEF) automaticamente.
3. Siga as instruções na maquininha.
4. Após aprovação, a venda é concluída.

Para **parcelamento no crédito:** selecione o número de parcelas antes de acionar a maquininha.

### PIX

1. Selecione **PIX**.
2. O sistema gera um QR Code na tela.
3. O cliente escaneia e realiza o pagamento.
4. A venda é encerrada automaticamente após confirmação.

> O QR Code tem tempo de expiração. Se expirar, cancele e gere novamente.

### Múltiplas Formas de Pagamento

1. Selecione a primeira forma e informe o valor parcial.
2. Selecione a segunda forma e informe o restante.
3. O sistema controla a diferença e o troco automaticamente.

---

## 7. Comandas em Espera

Quando uma venda é iniciada mas não finalizada:

1. Pressione **F4** para abrir a lista de **Comandas em Espera**.
2. Clique na comanda desejada para retomá-la.
3. O sistema carrega todos os itens já lançados.

---

## 8. Últimas Vendas e Reimpressão

### Consultar vendas recentes

1. Pressione **F10**.
2. Escolha quantas vendas exibir (10, 25, 50 ou 300).
3. Marque **Todos os Caixas** para ver vendas de outros terminais.
4. Clique duas vezes em uma venda para ver os detalhes.

### Reimprimir um cupom

1. Abra a venda em **Últimas Vendas**.
2. No rodapé da tela de detalhes:
   - **F1** — Reimprimir cupom fiscal
   - **F2** — Reimprimir com CPF do cliente
   - **F3** — Reimprimir cupom simples (não fiscal)

---

## 9. Devolução de Venda

1. Acesse **F1 → Devolução** ou abra a venda original em **Últimas Vendas**.
2. Informe a **quantidade** devolvida de cada produto.
3. O sistema calcula o valor total a ser devolvido.
4. Escolha como será feita a devolução:
   - **Gerar Voucher** — cria um crédito (vale) para uso futuro
   - **Estorno direto** — dependendo da forma de pagamento original
5. Confirme.

---

## 10. Sangria e Suprimento

### Sangria — Retirada de dinheiro do caixa

1. Pressione **F11**.
2. Selecione **Saída**.
3. Informe o **Valor**, o **Motivo** e uma **Observação** se necessário.
4. Clique em **Salvar**.

### Suprimento — Adição de dinheiro ao caixa

1. Pressione **F11**.
2. Selecione **Entrada**.
3. Informe o valor e o motivo e salve.

### Pagamento direto pelo caixa

Para registrar um pagamento a fornecedor feito com dinheiro do caixa:

1. Pressione **F11** > aba **Pagamentos**.
2. Informe o **Valor**, o **Fornecedor** e uma **Descrição**.
3. Salve.

---

## 11. Bloquear o Caixa

1. Acesse **F1 → Bloquear Caixa**.
2. O sistema solicita confirmação por senha.
3. O caixa fica bloqueado — nenhuma venda pode ser realizada.
4. Para desbloquear, informe a senha do operador.

---

## 12. Fechamento do Caixa

1. Pressione **F12**.
2. O sistema exibe o resumo: total de vendas por forma de pagamento, entradas e saídas.
3. Informe o **valor físico** em dinheiro no caixa (contagem real).
4. O sistema aponta a **diferença** entre o esperado e o informado.
5. Confirme para encerrar o turno.

### Relatórios gerados no fechamento

| Relatório | O que informa |
|---|---|
| **Relatório de Fechamento** | Resumo completo do caixa do turno |
| **Mapa de Vendas** | Vendas organizadas por produto ou grupo |
| **Divergências** | Diferença entre o esperado e o informado |

---

## 13. Outras Funções (F1)

| Função | O que faz |
|---|---|
| **Abrir Gaveta** | Abre a gaveta da registradora sem realizar venda |
| **Encerrar Operador** | Troca o operador sem fechar o caixa |
| **Cupom Não Fiscal** | Emite comprovante sem valor fiscal (uso interno) |
| **Promoções Aplicadas** | Exibe promoções ativas na venda atual |
| **Observação da Venda** | Adiciona anotação geral à venda |
| **Pagamento Parcial de Comanda** | Paga apenas alguns itens da comanda, o restante fica em aberto |
| **Taxa de Serviço** | Exibe e ajusta a taxa de serviço da venda |
| **Inserir CPF/CNPJ** | Associa o CPF ou CNPJ do cliente à nota fiscal |
| **Consultar Produto** | Busca preço e estoque sem lançar na venda |

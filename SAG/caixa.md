# SAG — Caixa / Frente de Caixa

Módulo principal de atendimento ao cliente e registro de vendas.

---

## Abertura de Caixa

**Caminho:** Tela Principal > **Caixa**

Ao abrir o módulo Caixa, o sistema apresenta a tela **Abrir Caixa** com:
- Campo: **Valor de Abertura** (troco inicial)
- Botão: **Abrir**

Após a abertura, a **Frente de Caixa** é exibida.

---

## Tela da Frente de Caixa

A tela é dividida em painéis:

| Painel | Descrição |
|---|---|
| Comanda | Número da comanda em uso |
| Produto | Lista de itens adicionados à venda |
| Dados da Venda | Subtotal, desconto, taxa de serviço, total |
| NumPad | Teclado numérico para entrada de quantidades/valores |
| Funções | Botões de ação rápida |

### Campos de Totais Exibidos
- **Sub Total**
- **Desconto**
- **Taxa de Serviço** (exibida condicionalmente)
- **Troco** (exibido condicionalmente)
- **Total da Venda**

---

## Realizar uma Venda

1. Pressione **F3** para iniciar nova venda
2. Informe CPF/CNPJ do cliente (ou pressione **Enter** para continuar sem)
3. Adicione os produtos (pelo código, nome ou pelo painel de produtos)
4. Ajuste quantidades se necessário
5. Pressione **F12** ou clique em **Finalizar** para ir ao pagamento
6. Selecione a forma de pagamento na tela **Formas de Pagamento**
7. Confirme o pagamento

---

## Formas de Pagamento

Tela: **Formas de Pagamento**

Formas disponíveis (conforme configuração do estabelecimento):
- Dinheiro
- Cartão de Crédito / Débito (via TEF/Pinpad)
- PIX (tela específica: **Pagamento PIX**)
- Vale Refeição (VR)
- Caderneta (crédito do cliente)
- Outros (conforme cadastro)

**Campos na tela de pagamento:**
- Forma de pagamento selecionada
- Valor a pagar
- Valor recebido (para dinheiro)
- Troco calculado automaticamente

---

## Consultar Últimas Vendas

- Pressione **F10** ou acesse **Últimas Vendas**
- Exibe histórico de vendas recentes
- Permite inserir CPF em venda já finalizada: selecione a venda > pressione **F2**

---

## Cancelar Item

1. Selecione o item na lista de produtos da venda
2. Pressione **F5** ou clique em **Cancelar Item**
3. Selecione o **Motivo do Cancelamento**
4. Confirme

---

## Cancelar Venda

1. Pressione **F6** ou clique em **Cancelar Venda**
2. Confirme o cancelamento
3. A venda é registrada como cancelada nos relatórios

---

## Desconto

- **Desconto no item:** Ctrl + D
- **Desconto na venda:** Ctrl + -
- Tela: **Aplica Desconto** — campo para informar valor ou percentual

---

## Venda em Espera

- Pressione **Ctrl + E** para colocar a venda em espera
- A venda fica suspensa e pode ser retomada depois
- Para retomar: use a opção de consulta de vendas em espera

---

## Entradas e Saídas de Caixa

- Pressione **F11**
- **Entrada:** registro de valor recebido fora de venda (ex: troco recebido)
- **Saída (Sangria):** retirada de valor do caixa
  - Campo: **Valor**
  - Campo: **Motivo**

---

## Fechamento de Caixa

1. Pressione **F12** ou clique em **Finalizar Caixa**
2. O sistema exibe o resumo de movimentações por forma de pagamento
3. Confira os valores
4. Confirme o fechamento

> Se o caixa não fechar por erro, verifique se há NFC-e pendente ou venda aberta.

---

## Consulta de Produtos (F9)

- Pressione **F9**
- Pesquise produto por nome ou código
- Exibe preço e estoque disponível

> Atenção: feche essa consulta antes de iniciar outra operação para evitar travamentos.

---

## Consulta de Pedidos (F8)

- Pressione **F8**
- Lista pedidos pendentes do delivery ou mesa
- Permite lançar itens de um pedido no caixa

---

## Devoluções

- **Devolução de Item:** tela **Devolução de Produto**
- **Devolução de Venda Completa:** tela **Devolução de Venda**
- Selecione a venda original para processar a devolução

---

## Programa de Fidelidade

- Pressione **Ctrl + L** para consultar extrato de pontos do cliente
- Pontos são creditados automaticamente nas vendas conforme configuração

---

## Auto-Atendimento (Totem)

Quando o estabelecimento possui totem de auto-atendimento:
- O cliente navega pelo **Cardápio** na tela do totem
- Seleciona produtos, acompanhamentos e personalizações
- Finaliza com pagamento via dinheiro, cartão ou PIX
- O pedido é enviado automaticamente para a produção

---

## Observações de Venda

- Use a opção **Observação** para adicionar notas à venda
- A observação aparece no cupom/ticket de produção

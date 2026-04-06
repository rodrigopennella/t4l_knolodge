# SAG — Caixa / Frente de Caixa

Módulo principal de atendimento ao cliente e registro de vendas. É a tela mais utilizada do sistema.

---

## Abertura de Caixa

**Caminho:** Tela Principal > **Caixa**

Ao abrir o módulo Caixa, o sistema apresenta a tela **Abrir Caixa** com:
- Campo: **Valor de Abertura** (troco inicial)
- Botão: **Abrir**

Após a abertura, a **Frente de Caixa** é exibida.

---

## Tela da Frente de Caixa

A tela exibe os seguintes elementos:

| Elemento | Descrição |
|---|---|
| Comanda | Campo para inserir número da comanda (por digitação ou leitor de código de barras) |
| Produto | Campo para inserir código do produto (por digitação, código de barras ou leitor) |
| Descrição | Nome do produto inserido |
| Valor Unitário | Preço unitário do produto |
| Quantidade | Quantidade do produto |
| Total do Produto | Valor total do item |
| Lista de itens | Tabela com #, Código, Descrição, Preço, Qtd, Total, Data Hora, Usuário, Comanda |
| Sub Total | Subtotal da venda |
| Desconto | Valor de desconto aplicado |
| Total da Venda | Valor final a pagar |

### Barra de Atalhos (Rodapé)
A barra inferior da Frente de Caixa exibe os atalhos disponíveis:
F1 - Outras Funções | F3 - Iniciar Venda | F4 - Consulta de Comandas | F5 - Cancelar Item | F6 - Cancelar Venda | F7 - Pagamento de Caderneta | F8 - Consulta de Pedidos | F9 - Consulta de Produtos | F10 - Últimas Vendas | F11 - Entradas e Saídas | F12 - Finalizar Caixa | Ctrl+E - Venda em Espera | Ctrl+D - Desconto | Ctrl+- - Desconto na Venda | Ctrl+U - Última Venda | Ctrl+F - Inserir Comanda Parcial

---

## Realizar uma Venda

### Venda Simples (sem comanda)

1. Pressione **Enter** ou **F2** para iniciar a venda (sem CPF)
   - Ou pressione **F3** para iniciar a venda com CPF (o sistema solicita o CPF primeiro)
2. No campo **Produto**, insira o código do produto de uma das formas:
   - Digitando o código e pressionando **Enter**
   - Bipando o código de barras com o leitor
   - Usando o formato quantidade antes do produto: `0,010*código` (ex: `0,500*123` para 500g do produto 123)
3. O produto aparece na lista de itens da venda
4. Repita o passo 2 para adicionar mais produtos
5. Ao finalizar os itens, o sistema apresenta a tela de **Formas de Pagamento**
6. Selecione a forma de pagamento (digitando o código numérico correspondente)
7. Informe o valor e confirme com **Enter**

### Venda com Comanda

1. No campo **Comanda**, insira o número da comanda (por digitação ou bipando com leitor)
2. No campo **Produto**, insira o código do produto
3. Insira a quantidade (antes ou depois do produto, dependendo da configuração)
4. Pressione **Enter**
5. Na tela de **Formas de Pagamento**, selecione a forma e confirme

### Inserção de Quantidade

A quantidade pode ser informada de duas formas:
- **Depois do produto:** insira o produto, depois altere a quantidade no campo correspondente
- **Antes do produto (formato multiplicador):** digite `quantidade*código` no campo produto (ex: `0,010*55` para 10g do produto 55)

> A opção "Quantidade Antes do Produto" pode ser habilitada em **Config. Terminal > Caixa**.

---

## Formas de Pagamento

Ao finalizar a inserção de produtos, a tela **Formas de Pagamento** é exibida.

### Como Funciona
- As formas de pagamento são listadas com um **código numérico à esquerda** e o **nome à direita**
- O operador **digita o código numérico** da forma desejada para selecioná-la
- O sistema abre a tela **Realiza Pagamento** com o valor total preenchido
- O operador pode alterar o valor (para pagamento parcial) e confirmar

### Formas Disponíveis (conforme configuração do estabelecimento)

| Código | Forma |
|---|---|
| 1 | Dinheiro |
| 2 | Cartão Débito |
| 3 | Cartão Crédito |
| 4 | PIX |
| 5 | QR Code |
| 6 | Caderneta |
| 7 | Desconto |
| 13 | iFood |
| 14 | Incentivo Parceiro |
| 15 | Ticket |
| 16 | No Bairro |

> Os códigos e formas variam conforme o cadastro de cada estabelecimento.

### Pagamento Parcial (Misto)
Para pagar com mais de uma forma de pagamento:
1. Selecione a primeira forma de pagamento (ex: Dinheiro)
2. Informe um valor **menor** que o total da venda
3. Confirme — o sistema mantém a tela de formas de pagamento aberta com o saldo restante
4. Selecione a segunda forma de pagamento (ex: Cartão)
5. Informe o valor restante e confirme

### Tela "Realiza Pagamento"
Exibe:
- **Total** da venda (R$)
- **Nome da forma** selecionada com campo de valor editável
- **Troco** calculado automaticamente (para dinheiro)
- Botões: **Sair** / **Salvar**
- Atalho: **F1 - Repique**

### Atalhos na Tela de Formas de Pagamento
| Tecla | Função |
|---|---|
| F1 | Inserir CPF |
| F2 | Pesquisa Cliente |
| F3 | Inserir Observação |
| F4 | Inserir Voucher |
| F5 | Inserir Cupom Desconto |
| F6 | Cadastrar |

---

## Atalhos Completos da Frente de Caixa

### F1 — Outras Funções
Abre uma caixa de seleção com as seguintes opções:

| Opção | Função |
|---|---|
| 1 | Abrir Gaveta de Dinheiro |
| 2 | Colocar Venda em Espera |
| 3 | Comandas Abertas |
| 4 | Caixa em Espera |
| 5 | Devolução de Venda |
| 6 | Devolução de Produto |
| 7 | Central NFC-e (central de envio, validação e verificação de problemas com NFC-e) |
| 8 | Central de Ajustes TEF |
| 9 | Bloqueia Tela Caixa |

### F2 / Enter — Iniciar Venda
Inicia uma nova venda sem solicitar CPF.

### F3 — Iniciar Venda com CPF
Solicita o CPF/CNPJ do cliente antes de iniciar a venda.

### F4 — Consulta de Comandas
Abre a tela de consulta de comandas abertas para seleção.

### F5 — Cancelar Item
1. Selecione o item na lista de produtos da venda
2. Pressione **F5**
3. Selecione o **Motivo do Cancelamento**
4. Confirme

### F6 — Cancelar Venda
1. Pressione **F6**
2. Confirme o cancelamento
3. A venda é registrada como cancelada nos relatórios

### F7 — Pagamento de Caderneta
Abre a tela de recebimento de caderneta. Permite que o cliente pague valores pendentes registrados na caderneta.

> É necessário ter um caixa aberto para receber valores de caderneta.

### F8 — Consulta de Pedidos
Abre uma tela para inserir o código do pedido em aberto, para finalização no caixa.

### F9 — Consulta de Produtos
Pesquise produto por nome ou código. Exibe preço e estoque disponível.

> Atenção: feche essa consulta antes de iniciar outra operação para evitar travamentos.

### F10 — Últimas Vendas
Exibe histórico de vendas recentes. Permite inserir CPF em venda já finalizada: selecione a venda > pressione **F2**.

### F11 — Entradas e Saídas (Sangria)
Função de sangria no caixa. Serve para registrar:
- **Entrada:** valor recebido fora de venda (ex: troco recebido)
- **Saída (Sangria):** retirada de valor do caixa
  - Campo: **Valor**
  - Campo: **Motivo**

### F12 — Finalizar Caixa
1. Pressione **F12**
2. O sistema pergunta se tem certeza que deseja finalizar
3. Se confirmado, e se habilitado no **Config. Terminal** (opção "Lançar Valores ao Finalizar Caixa") e o usuário tiver permissão, aparece a função de **lançar valores reais** para o fechamento
4. O sistema exibe o resumo de movimentações por forma de pagamento
5. Confira os valores e confirme o fechamento

> Se o caixa não fechar por erro, verifique se há NFC-e pendente ou venda aberta.

### Ctrl + D — Desconto no Item
Aplica desconto ao item selecionado.

### Ctrl + - — Desconto na Venda
Aplica desconto ao total da venda. Tela: **Aplica Desconto** — campo para informar valor ou percentual.

### Ctrl + E — Venda em Espera
Coloca a venda atual em espera:
- Se a venda **tem comanda vinculada**: pergunta se deseja voltar para a comanda original
- Se **não tem comanda**: pede o número da comanda
- A venda fica suspensa e pode ser retomada depois

### Ctrl + U — Última Venda
Exibe os detalhes da última venda realizada.

### Ctrl + F — Inserir Comanda Parcial
Permite inserir um ou mais produtos de uma comanda no caixa, sem trazer todos os itens. Útil quando parte da conta é paga por um cliente em um grupo.

### Ctrl + L — Extrato Programa de Fidelidade
Consulta o extrato de pontos do cliente no programa de fidelidade.

---

## Consultar Últimas Vendas

- Pressione **F10** ou acesse **Últimas Vendas**
- Exibe histórico de vendas recentes
- Permite inserir CPF em venda já finalizada: selecione a venda > pressione **F2**

---

## Devoluções

Acessíveis via **F1 > Outras Funções**:
- **Opção 5 — Devolução de Venda:** devolução completa de uma venda
- **Opção 6 — Devolução de Produto:** devolução de item específico
- Selecione a venda original para processar a devolução

---

## Programa de Fidelidade

- Pressione **Ctrl + L** para consultar extrato de pontos do cliente
- Pontos são creditados automaticamente nas vendas conforme configuração

---

## Caderneta (Fiado)

A Caderneta é a função que permite ao cliente registrar vendas no sistema para pagamento futuro.

### No Caixa
- **F7 — Pagamento de Caderneta:** abre tela de recebimento (precisa de caixa aberto)
- Na tela de Formas de Pagamento, a opção **6 — Caderneta** registra a venda na caderneta do cliente

### Tela de Gerenciamento de Caderneta
**Caminho:** Tela Principal > **Caderneta**

Abas disponíveis:
| Aba | Função |
|---|---|
| **Recebimento** | Receber pagamento de caderneta (mesma função do F7 no caixa — necessita caixa aberto) |
| **Extrato** | Extrato completo das movimentações da caderneta do cliente |
| **Compras** | Histórico de compras realizadas na caderneta |
| **Pagamentos** | Histórico de pagamentos efetuados |
| **Resumo** | Resumo geral da caderneta |
| **Canceladas** | Registros cancelados |

Campos da tela de Recebimento:
- Cliente (pesquisa)
- Saldo Devedor
- Data do Pagamento
- Data de Competência
- Valor do Pagamento
- Pagamento do Total (checkbox)

---

## Auto-Atendimento (Totem)

Quando o estabelecimento possui totem de auto-atendimento:
- O cliente navega pelo **Cardápio** na tela do totem
- Seleciona produtos, acompanhamentos e personalizações
- Finaliza com pagamento via dinheiro, cartão ou PIX
- O pedido é enviado automaticamente para a produção

---

## Observações de Venda

- Use a opção **Observação** (F3 na tela de Formas de Pagamento) para adicionar notas à venda
- A observação aparece no cupom/ticket de produção

---

## Configurações que Afetam o Caixa

As seguintes opções em **Config. Terminal > Caixa** alteram o comportamento da Frente de Caixa:

| Opção | Efeito |
|---|---|
| Acionamento Automático da Gaveta | Abre a gaveta automaticamente ao finalizar venda |
| Utiliza Comandas | Habilita o uso de comandas no caixa |
| Quantidade Antes do Produto | Permite inserir quantidade no formato multiplicador (ex: 0,500*código) |
| Utiliza Balança | Integra com balança para peso automático |
| Inicia Venda com Enter | Enter inicia a venda (em vez de F3) |
| Lançar Valores ao Finalizar Caixa | Exibe tela de lançamento de valores reais no fechamento |
| Caixa Utiliza Taxa de Serviço | Habilita taxa de serviço nas vendas |
| Comanda Apenas com Leitor | Exige leitor de código de barras para comanda |
| Avisa Quantidade maior que 99 | Alerta quando quantidade excede 99 |
| Avisa Sangria quando Valor é superior à X | Alerta para sangria quando o caixa acumula valor alto |
| F4 Abre Terminal | F4 abre o Terminal de Comandas em vez da consulta |
| Caixa Solicita Vendedor Antes de Concluir a Venda | Solicita identificação do vendedor |

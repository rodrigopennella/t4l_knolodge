# NF-e — Guia de Emissão Passo a Passo

Guia completo para emitir uma Nota Fiscal Eletrônica pelo SAG, desde a abertura do editor até a autorização pela SEFAZ.

---

## Formas de Iniciar uma NF-e

O SAG oferece três pontos de entrada para criar uma NF-e. Escolha o que melhor se encaixa na sua situação:

| Forma | Quando usar |
|---|---|
| **Emitir** (tela principal) | Criar a nota do zero, preenchendo todos os campos manualmente |
| **Consulta de Vendas** | Aproveitar uma venda já registrada no caixa para gerar a nota automaticamente |
| **Consulta de Pedidos** | Aproveitar um pedido do módulo Delivery para gerar a nota automaticamente |

Para acessar, vá até a tela principal do SAG e localize o painel de **NF-e**. Clique na opção desejada.

---

## Importar a partir de uma Venda ou Pedido

Se você vai criar a nota a partir de uma venda ou pedido já lançado, siga estas etapas antes de prosseguir para o editor:

1. Clique em **Consulta de Vendas** ou **Consulta de Pedidos**.
2. Use os filtros disponíveis (cliente, código, período, valor) para localizar o registro desejado.
3. Marque a caixa de seleção ao lado de cada venda ou pedido que deseja incluir na nota.
4. Clique em **Nova Nota**.
5. O editor será aberto com os produtos e valores já preenchidos. Continue a partir da **Aba 1 — Cabeçalho**.

> Se a nota for preenchida do zero, clique em **Emitir** na tela principal e o editor abrirá vazio.

---

## O Editor da NF-e

O editor é dividido em **oito abas**. Percorra cada uma em ordem antes de emitir.

---

## Aba 1 — Cabeçalho

Esta aba define as informações gerais da operação fiscal.

### Campos obrigatórios

| Campo | O que preencher |
|---|---|
| **Natureza da Operação** | Descrição da operação. Exemplos: "Venda de Mercadorias", "Remessa para Conserto", "Devolução de Compra" |
| **Documento** | Tipo de movimentação: **Saída** (quando você vende) ou **Entrada** (quando você compra) |
| **Finalidade** | Finalidade da nota: Normal, Complementar, Ajuste ou Devolução de Mercadoria |
| **Destino** | Onde a operação ocorre: **Operação Interna** (mesmo estado), **Interestadual** (outro estado) ou **Exterior** |
| **Atendimento** | Como o atendimento foi feito: presencial, pela internet, telefone, entrega a domicílio, entre outros |

### Campos opcionais

| Campo | O que preencher |
|---|---|
| **Intermediador** | Se a venda foi feita por plataforma de terceiros (marketplace), selecione a opção correspondente |
| **Consumidor Final** | Marque esta caixa quando a venda for diretamente para o consumidor final |
| **Data de Saída/Entrada** | Data em que a mercadoria saiu ou chegou, caso diferente da data de emissão |

Após preencher, clique na próxima aba.

---

## Aba 2 — Destinatário

Esta aba identifica quem está recebendo a nota.

### Selecionar o destinatário

No campo **Cliente**, comece a digitar o nome ou o código do cliente. O sistema exibirá sugestões conforme você digita. Clique no cliente correto para selecioná-lo — os dados de CPF/CNPJ e endereço serão preenchidos automaticamente.

> Caso o cliente não esteja cadastrado, clique no botão **Adicionar novo cliente** para cadastrá-lo diretamente nesta tela.

### Conferir os dados preenchidos

Após selecionar o cliente, confira os campos exibidos:

**Dados de identificação:**
- Nome ou Razão Social
- CPF ou CNPJ
- Inscrição Estadual (IE) ou RG
- Tipo de contribuinte (Não Contribuinte, Contribuinte ICMS ou Contribuinte Isento)

**Endereço:**
- CEP — ao informar o CEP e sair do campo, o sistema preenche automaticamente rua, bairro, cidade e estado
- Número e Complemento (preencher manualmente)

**Contato:**
- E-mail
- Telefone

> Caso o destinatário seja estrangeiro, marque a caixa **Estrangeiro**. Novos campos serão exibidos para preenchimento do país e identificação estrangeira.

---

## Aba 3 — Produtos

Esta aba é onde você adiciona os itens da nota.

### Adicionar um produto

1. No campo de pesquisa, comece a digitar o nome ou código do produto.
2. Selecione o produto na lista de sugestões.
3. Informe a **quantidade**.
4. Clique em **Adicionar**.
5. O produto aparecerá na grade abaixo com código, descrição, NCM, CFOP, valor unitário, quantidade e valor total.

Repita o processo para todos os produtos da nota.

### Editar um produto adicionado

Clique no botão de edição ao lado do produto na grade. Uma janela de detalhes será aberta com as seguintes seções:

**Seção Dados:**

| Campo | O que preencher |
|---|---|
| **Descrição** | Nome do produto na nota (pode ser diferente do cadastro) |
| **CFOP** | Código fiscal da operação — selecione conforme o tipo de venda |
| **Unidade** | Unidade de medida (UN, KG, CX, etc.) |
| **NCM** | Código de classificação fiscal do produto. Use o botão de pesquisa para localizar |
| **CEST** | Código para substituição tributária, quando aplicável |
| **EAN** | Código de barras do produto, quando houver |
| **Observação** | Informação adicional referente ao item, quando necessário |

**Seção Valores:**

| Campo | O que preencher |
|---|---|
| **Valor Unitário** | Preço por unidade do produto |
| **Quantidade** | Quantidade deste item na nota |
| **Valor Total** | Calculado automaticamente (Valor Unitário × Quantidade) |
| **Frete** | Valor do frete atribuído a este item, se aplicável |
| **Desconto** | Valor de desconto concedido no item |
| **Seguro** | Valor de seguro, se aplicável |
| **Despesas** | Outras despesas acessórias, se aplicável |

> **Atenção com o Valor Total:** após alterar o Valor Unitário ou a Quantidade, clique em outro campo antes de salvar para garantir que o Total seja recalculado corretamente.

**Seções tributárias (ICMS, PIS/COFINS, IPI, ICMS ST):**

Estas seções contêm os campos tributários do produto. Normalmente são preenchidas automaticamente com base no perfil fiscal configurado para o produto. Alterações nestas seções devem ser feitas apenas com orientação contábil.

Após revisar, clique em **Salvar** para confirmar o produto.

### Remover um produto

Clique no botão de exclusão ao lado do produto na grade para removê-lo da nota.

---

## Aba 4 — Transporte

Define como e por quem a mercadoria será transportada.

### Campo obrigatório

**Modalidade de Frete:** selecione como o frete está sendo contratado:

| Opção | Significado |
|---|---|
| **CIF** | Frete por conta do remetente (sua empresa paga) |
| **FOB** | Frete por conta do destinatário (o cliente paga) |
| **Terceiros** | Frete contratado por terceiros |
| **Próprio pelo Remetente** | Sua empresa usa frota própria para entregar |
| **Próprio pelo Destinatário** | O cliente usa frota própria para retirar |
| **Sem Transporte** | Não há movimentação física de mercadoria |

### Transportadora (opcional)

Se houver transportadora envolvida, pesquise e selecione no campo **Transportadora**. Os dados serão preenchidos automaticamente. Caso necessário, informe também:

- Placa do veículo
- Estado de emplacamento
- Registro RNTC

Para informar volumes (quantidade de volumes, espécie, marca, peso bruto e líquido), clique em **Volumes**.

---

## Aba 5 — Totais

Esta aba é apenas informativa. Todos os campos são calculados automaticamente pelo sistema com base nos produtos e tributos informados.

Confira os valores antes de prosseguir:

- Base de Cálculo do ICMS
- Valor do ICMS
- Base de Cálculo do ICMS ST
- Valor do ICMS ST
- PIS e COFINS
- Subtotal dos Produtos
- Frete, Desconto e IPI
- **Total da Nota** — valor final que constará no documento fiscal

Não há nada a preencher nesta aba. Se algum valor parecer incorreto, volte à aba de Produtos e verifique os valores e as informações tributárias dos itens.

---

## Aba 6 — Faturas

Esta aba registra as condições de pagamento da nota (parcelamento).

> Esta aba é **opcional**. Se a nota não precisar de discriminação de parcelas, pode ser ignorada.

### Gerar parcelas automaticamente

1. Selecione a **Espécie** (forma de pagamento: duplicata, cheque, etc.).
2. Informe o número de **Parcelas**.
3. Informe a **Data** do primeiro vencimento.
4. Clique em **Gerar** — o sistema dividirá o valor total igualmente entre as parcelas.

### Ajustar manualmente

Após gerar, os valores e datas de cada parcela ficam disponíveis para edição direta na grade. Clique na célula que deseja alterar.

> O total das parcelas deve ser exatamente igual ao valor total da nota. Caso haja divergência, o sistema alertará antes de emitir.

---

## Aba 7 — Referências

Esta aba vincula a nota atual a outros documentos fiscais anteriores, quando necessário.

> Esta aba é **opcional**. Use apenas quando a nota fizer referência a outro documento (ex: notas de devolução que referenciam a nota original).

### Tipos de referência disponíveis

| Tipo | Quando usar |
|---|---|
| **NF-e** | Referenciar outra nota fiscal eletrônica (informe a chave de acesso de 44 dígitos) |
| **CT-e** | Referenciar um conhecimento de transporte eletrônico |
| **Nota Fiscal** | Referenciar uma nota fiscal em papel (modelo 1 ou 1-A) |
| **Cupom Fiscal** | Referenciar um cupom fiscal emitido por ECF |

Selecione o tipo, preencha os dados solicitados e clique em **Adicionar**. Repita para cada referência necessária.

---

## Aba 8 — Adicionais

Esta aba permite incluir informações complementares e configurar endereço de entrega diferente.

### Informações de texto (opcionais)

| Campo | Para que serve |
|---|---|
| **Informações para o Fisco** | Texto que aparece na nota destinado à Receita (ex: referência a legislação, regime especial) |
| **Informações do Contribuinte** | Texto para o destinatário (ex: número do pedido, observações comerciais) |

### Endereço de Entrega (opcional)

Se a mercadoria for entregue em um endereço diferente do cadastrado para o destinatário, marque a opção de **Endereço de Entrega** e preencha o endereço completo.

### Pessoas Autorizadas (opcional)

Informe o CPF ou CNPJ de pessoas autorizadas a retirar o XML da nota junto à SEFAZ. Insira o número e clique em **Adicionar**.

---

## Validar, Salvar e Emitir

Após percorrer todas as abas, você tem três opções no rodapé do editor:

| Botão | O que faz |
|---|---|
| **Salvar** | Salva o rascunho da nota com status **Em Digitação**. A nota não é enviada à SEFAZ. Pode ser reaberta e editada depois. |
| **Validar** | Gera o XML e assina digitalmente, mas não envia à SEFAZ. Útil para conferir se há erros antes de emitir. A nota fica com status **Pronta**. |
| **Emitir** | Gera o XML, assina e envia imediatamente à SEFAZ para autorização. |

> **Recomendação:** clique em **Validar** antes de **Emitir** para garantir que todos os campos estão corretos e não há pendências tributárias.

---

## Após a Emissão

### Se a nota for **Autorizada**

A SEFAZ retorna a aprovação e o status da nota muda para **Autorizada** (fundo verde no Gerenciador). Os seguintes botões ficam disponíveis:

- **DANFE** — gera o documento auxiliar em PDF para impressão ou envio
- **XML** — exporta o arquivo XML para arquivamento
- **E-mail** — envia a nota para o e-mail do destinatário
- **Carta de Correção** — cria uma carta para corrigir informações que não alteram o valor da nota
- **Cancelar** — cancela a nota (disponível somente dentro do prazo legal permitido)

### Se a nota for **Rejeitada**

O sistema exibe uma mensagem com o motivo da rejeição informado pela SEFAZ. A nota fica com status **Rejeitada** (fundo vermelho). Para corrigir e reenviar:

1. No **Gerenciador**, filtre por **Rejeitada**.
2. Selecione a nota e clique em **Alterar**.
3. Corrija o campo indicado no motivo da rejeição.
4. Clique em **Emitir** novamente.

> Consulte o guia [NF-e — Erros, Rejeições e Soluções](nfe-erros.md) para orientações detalhadas sobre cada tipo de rejeição e como resolvê-la.

### Se a nota ficar **Em Processamento**

A SEFAZ recebeu a nota mas ainda não concluiu a análise. O sistema consulta o status automaticamente a cada alguns segundos. Aguarde — a nota será atualizada para Autorizada ou Rejeitada assim que a SEFAZ responder.

---

## Acompanhar Todas as Notas — Gerenciador

Para ver todas as notas emitidas, acesse o painel de NF-e na tela principal e clique em **Gerenciar**.

O Gerenciador exibe todas as notas com seus respectivos status:

| Status | Cor | Significado |
|---|---|---|
| Em Digitação | Branco | Rascunho salvo, não enviado |
| Pronta | Branco | Validada, aguardando emissão |
| Em Processamento | Amarelo | Enviada, aguardando resposta da SEFAZ |
| Autorizada | Verde | Aprovada pela SEFAZ |
| Rejeitada | Vermelho | Devolvida com erro — requer correção |
| Denegada | Vermelho | Bloqueada pela SEFAZ — não pode ser reaproveitada |
| Cancelada | Cinza | Cancelada após autorização |

Use o filtro de status no topo para localizar rapidamente as notas em cada situação.

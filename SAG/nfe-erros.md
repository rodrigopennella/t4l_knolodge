# NF-e — Erros, Rejeições e Soluções

Guia de referência para identificar e resolver os erros mais comuns na emissão de NF-e no SAG. Os erros estão organizados por momento em que ocorrem: antes do envio, durante o envio e após o retorno da SEFAZ.

---

## Como interpretar os erros

Ao tentar emitir uma nota, os erros podem aparecer em dois momentos:

- **Antes do envio:** o próprio SAG detecta que algum dado está incorreto ou faltando e exibe um aviso. A nota não é enviada.
- **Após o envio:** a SEFAZ analisa a nota e devolve um retorno. Se houver problema, a nota fica com status **Rejeitada** ou **Denegada** e o motivo é exibido na tela.

---

## Parte 1 — Erros Detectados pelo SAG (antes do envio)

Estes erros aparecem assim que você tenta Validar ou Emitir a nota. O sistema indica qual aba e qual campo precisa ser corrigido.

---

### Erros na Aba Cabeçalho

| Mensagem | Causa | O que fazer |
|---|---|---|
| Preencha a Natureza da Operação | O campo está em branco | Informe uma descrição da operação (ex: "Venda de Mercadorias") |
| Escolha o tipo de documento | Nenhuma opção selecionada | Selecione **Saída** ou **Entrada** conforme a operação |
| Escolha a finalidade | Nenhuma opção selecionada | Selecione a finalidade (Normal, Complementar, Ajuste ou Devolução) |
| Escolha o destino da operação | Nenhuma opção selecionada | Selecione Interna, Interestadual ou Exterior |
| Escolha o tipo de atendimento | Nenhuma opção selecionada | Selecione a forma de atendimento utilizada |

---

### Erros na Aba Destinatário

| Mensagem | Causa | O que fazer |
|---|---|---|
| CNPJ inválido | O número de CNPJ informado não passa na validação | Verifique se o CNPJ está correto. Confira dígitos verificadores |
| CPF inválido | O número de CPF informado não passa na validação | Verifique se o CPF está correto. Confira dígitos verificadores |
| Email inserido inválido | O e-mail não está em formato válido | Corrija o e-mail do destinatário (ex: nome@empresa.com.br) |

---

### Erros na Aba Produtos

| Mensagem | Causa | O que fazer |
|---|---|---|
| Selecione um produto | Tentou adicionar sem escolher o produto | Selecione o produto no campo de pesquisa antes de clicar em Adicionar |
| A quantidade deve ser maior que zero | Quantidade zerada ou vazia | Informe uma quantidade válida antes de adicionar |
| A nota não possui nenhum produto | A grade de produtos está vazia | Adicione ao menos um produto antes de emitir |

---

### Erros na Aba Transporte

| Mensagem | Causa | O que fazer |
|---|---|---|
| Preencha o nome da transportadora | O campo de nome está vazio mesmo com transportadora selecionada | Verifique se a transportadora está corretamente cadastrada com nome ou razão social |
| CNPJ da transportadora inválido | O CNPJ da transportadora não é válido | Acesse o cadastro da transportadora e corrija o CNPJ |
| CPF da transportadora inválido | O CPF do transportador autônomo não é válido | Corrija o CPF no cadastro do transportador |

---

### Erros na Aba Faturas

| Mensagem | Causa | O que fazer |
|---|---|---|
| Valor total das faturas difere do valor total da nota | A soma das parcelas não bate com o total da nota | Ajuste os valores das parcelas até que a soma seja exatamente igual ao total da nota |

---

### Erros na Aba Referências

| Mensagem | Causa | O que fazer |
|---|---|---|
| Preencha a chave da nota referenciada | A chave de acesso está em branco | Informe a chave de acesso de 44 dígitos da nota que está sendo referenciada |
| O tamanho da chave não confere | A chave tem mais ou menos dígitos do que o esperado | A chave de acesso deve ter exatamente 44 dígitos. Confira o número informado |
| A série da nota referenciada é inválida | O número de série preenchido não é aceito | Verifique a série da nota original e informe corretamente |

---

### Erros de Certificado Digital

O certificado digital é obrigatório para assinar e enviar a nota à SEFAZ. Se houver problema com ele, a nota não poderá ser emitida.

| Mensagem | Causa | O que fazer |
|---|---|---|
| Nenhum certificado digital configurado | Não há certificado cadastrado no sistema | Acesse as configurações da NF-e e cadastre um certificado digital válido (arquivo A1 ou leitor A3) |
| O certificado digital está vencido | O certificado expirou | Renove o certificado junto à autoridade certificadora (Serpro, Serasa, etc.) e atualize nas configurações da NF-e |

---

### Erro de Cadastro do Estabelecimento

| Mensagem | Causa | O que fazer |
|---|---|---|
| Atualize o cadastro do estabelecimento | Dados do emitente estão incompletos ou desatualizados | Acesse as configurações do estabelecimento no SAG e verifique CNPJ, endereço, regime tributário e demais dados obrigatórios |

---

## Parte 2 — Retornos da SEFAZ após o Envio

Após enviar a nota, a SEFAZ retorna um status. Veja abaixo o que cada situação significa e como agir.

---

### Nota Autorizada

| Status | Significado |
|---|---|
| **100 — Autorizada** | A nota foi aprovada e está válida. Nenhuma ação necessária. |
| **150 — Autorizada anteriormente** | A nota já havia sido autorizada em um envio anterior. O sistema recupera a autorização automaticamente. |

---

### Nota em Processamento

| Status | Significado | O que fazer |
|---|---|---|
| **103 — Em Processamento** | A SEFAZ recebeu a nota mas ainda não concluiu a análise | Aguarde. O SAG consulta o status automaticamente. A nota será atualizada em breve |

---

### Nota Duplicada

| Situação | Significado | O que fazer |
|---|---|---|
| **Emitida com duplicidade** | Uma nota com os mesmos dados já foi autorizada anteriormente | O sistema tenta recuperar a autorização original automaticamente. Se não conseguir, localize a nota original no Gerenciador e utilize a já autorizada |

---

### Nota Denegada

Uma nota **Denegada** é bloqueada pela SEFAZ por questões cadastrais graves, geralmente relacionadas à situação fiscal do emitente ou do destinatário. Diferente da rejeição, a nota denegada **não pode ser corrigida e reenviada com o mesmo número** — ela consome a numeração.

| Causa comum | O que fazer |
|---|---|
| Destinatário com inscrição estadual cancelada ou baixada | Verifique a situação cadastral do destinatário na Receita Estadual antes de emitir. Se confirmado, a operação pode não ser possível. |
| Emitente com restrições na SEFAZ | Consulte seu contador — pode haver pendências fiscais no CNPJ do emitente |

> Em caso de nota denegada, entre em contato com seu contador para avaliar a situação e os próximos passos.

---

### Nota Rejeitada — Erros Mais Comuns

Uma nota rejeitada pode ser corrigida e reenviada. Localize a nota no Gerenciador (filtro: **Rejeitada**), clique em **Alterar**, faça a correção e clique em **Emitir** novamente.

---

#### Rejeições relacionadas a valores

**"Valor do Produto difere do Valor Unitário de Comercialização e Quantidade Comercial"**

- **O que significa:** o valor total do item na nota não bate com o cálculo de Valor Unitário × Quantidade.
- **Causas possíveis:**
  - O Valor Unitário foi editado manualmente mas o Total não foi recalculado antes de salvar.
  - A nota foi gerada a partir de uma venda com desconto proporcional que deslocou os valores.
  - A quantidade tem muitas casas decimais e o arredondamento gerou diferença.
- **Como corrigir:**
  - Abra o editor do produto na aba Produtos.
  - Na aba Valores, ajuste o Valor Unitário de forma que Valor Unitário × Quantidade resulte exatamente no Valor Total exibido.
  - Se houver desconto, considere embutir o desconto no Valor Unitário em vez de lançá-lo no campo Desconto separado.
  - Clique em outro campo após alterar os valores, antes de salvar, para garantir o recálculo automático.

---

**"Valor total da NF-e difere do somatório dos itens"**

- **O que significa:** o total geral da nota não corresponde à soma dos totais de cada produto.
- **Como corrigir:** verifique se todos os produtos estão com valores corretos e se não há campos de frete, seguro ou desconto no cabeçalho que estejam criando divergência. Corrija e reemita.

---

#### Rejeições relacionadas a CFOP

**"CFOP inválido para a operação"** ou **"CFOP não permitido para o destino informado"**

- **O que significa:** o código CFOP do produto não corresponde ao tipo de operação ou ao destino da nota.
- **Como corrigir:** o CFOP é definido dentro do **Grupo de Imposto** vinculado ao produto. Acesse **Cadastros > Produtos** > selecione o produto > aba **Imposto** > clique em 🔄 para editar o Grupo de Imposto e corrija o CFOP. Em caso de dúvida, consulte seu contador.

---

#### Rejeições relacionadas a NCM

**"NCM inválido"** ou **"NCM não informado"**

- **O que significa:** o código NCM do produto está incorreto, incompleto ou ausente.
- **Como corrigir:** abra o editor do produto, localize o campo NCM e use o botão de pesquisa para encontrar o código correto. O NCM deve ter 8 dígitos.

---

#### Rejeições relacionadas ao destinatário

**"CPF/CNPJ do destinatário inválido"**

- **O que significa:** o número informado não é válido.
- **Como corrigir:** acesse a aba Destinatário, confira o CPF ou CNPJ e corrija se necessário. Lembre-se de atualizar também o cadastro do cliente para evitar o mesmo problema em futuras emissões.

**"Destinatário não identificado"** ou **"Dados do destinatário incompletos"**

- **O que significa:** informações obrigatórias do destinatário estão faltando.
- **Como corrigir:** verifique na aba Destinatário se nome, endereço completo (incluindo CEP, cidade e estado) estão preenchidos.

---

#### Rejeições relacionadas ao emitente

**"CNPJ do emitente não cadastrado na SEFAZ"** ou **"Inscrição Estadual inválida"**

- **O que significa:** os dados do seu estabelecimento junto à SEFAZ estão divergentes.
- **Como corrigir:** acesse as configurações do estabelecimento no SAG e verifique CNPJ, Inscrição Estadual e regime tributário. Em caso de dúvida, consulte seu contador.

---

#### Rejeições relacionadas ao certificado ou assinatura

**"Assinatura inválida"** ou **"Certificado não confiável"**

- **O que significa:** houve problema na assinatura digital da nota.
- **Como corrigir:** verifique se o certificado digital configurado é válido e não expirou. Acesse as configurações da NF-e e recarregue o certificado. Se o problema persistir, entre em contato com o suporte.

---

#### Rejeições relacionadas à numeração

**"Número de NF-e já utilizado"**

- **O que significa:** o número da nota já foi usado em uma emissão anterior.
- **Como corrigir:** o SAG gerencia a numeração automaticamente. Verifique se não houve configuração manual de número incorreta. Consulte o suporte se o problema persistir.

**"Série inválida para o ambiente"**

- **O que significa:** a série configurada não é permitida para o ambiente atual (produção ou homologação).
- **Como corrigir:** acesse as configurações da NF-e e verifique a série configurada. Em ambiente de produção, a série deve ser diferente da série usada em homologação.

---

## Parte 3 — Erros de Comunicação com a SEFAZ

Estes erros não são rejeições — são falhas de conexão ou de disponibilidade do serviço.

---

### Divergência de Horário

| Mensagem | Causa | O que fazer |
|---|---|---|
| A SEFAZ rejeitou a emissão por divergência de horário | O horário do computador está muito diferente do horário do servidor da SEFAZ | Acesse as configurações de data e hora do computador e sincronize com um servidor de horário na internet. Após corrigir, tente emitir novamente |

---

### Serviço Temporariamente Indisponível

| Mensagem | Causa | O que fazer |
|---|---|---|
| A consulta foi rejeitada pelo SEFAZ, aguarde alguns minutos | A SEFAZ está com instabilidade momentânea ou realizando manutenção | Aguarde de 5 a 15 minutos e tente emitir novamente. Não é necessário alterar nenhum dado da nota |

---

### Erro de Conexão

| Mensagem | Causa | O que fazer |
|---|---|---|
| Não foi possível emitir a nota / Erro ao emitir NF-e | Sem acesso à internet ou firewall bloqueando a comunicação | Verifique se o computador tem acesso à internet. Se tiver, verifique com o responsável de TI se há bloqueio de firewall para os serviços da SEFAZ |

---

### Não foi possível consultar a situação da nota

| Causa | O que fazer |
|---|---|
| A nota ficou com status Em Processamento e o SAG não conseguiu obter a resposta | Aguarde alguns minutos e acesse o Gerenciador. Selecione a nota e use o botão **Consultar Status** para forçar uma nova consulta |

---

## Parte 4 — Após a Autorização: Erros de DANFE e XML

| Mensagem | Causa | O que fazer |
|---|---|---|
| Erro ao gerar DANFE | Problema na geração do documento auxiliar em PDF | Tente gerar novamente. Se persistir, entre em contato com o suporte |
| Erro ao gerar XML | Problema ao exportar o arquivo da nota | Tente exportar novamente. Verifique se há espaço em disco disponível |
| Email inválido | O e-mail do destinatário está incorreto | Corrija o e-mail no cadastro do cliente e tente enviar novamente pelo botão E-mail no Gerenciador |

---

## Resumo Rápido de Ações

| Situação | Ação recomendada |
|---|---|
| Nota com erro de preenchimento | Corrija o campo indicado e tente emitir novamente |
| Nota Rejeitada por divergência de valor | Edite o produto, ajuste Valor Unitário × Quantidade e reemita |
| Nota Rejeitada por CFOP ou NCM incorreto | Corrija no editor do produto e reemita |
| Nota Rejeitada por dados do destinatário | Corrija o cadastro do cliente e reemita |
| Nota Denegada | Consulte seu contador — não pode ser reaproveitada |
| Nota Em Processamento | Aguarde o retorno automático da SEFAZ |
| Certificado vencido | Renove o certificado e atualize nas configurações |
| Erro de horário | Sincronize o relógio do computador e reemita |
| Serviço indisponível | Aguarde alguns minutos e tente novamente |
| Erro de conexão | Verifique internet e configurações de firewall |

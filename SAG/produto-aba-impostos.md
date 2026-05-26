# Alteração de Produto — Aba Impostos

Documentação detalhada da aba **Impostos** na tela de Alteração de Produto do SAG. Esta aba centraliza toda a configuração tributária do produto, permitindo que cada estabelecimento utilize um grupo de imposto diferente para o mesmo item.

---

## Visão Geral da Aba

Ao abrir a tela de Alteração de Produto e acessar a aba **Impostos**, você encontra uma seção chamada **Grupo de Imposto**. É nela que o sistema vincula as configurações tributárias ao produto.

A tela é composta por:

- Dois botões de ação globais no topo da seção.
- Uma tabela listando todos os estabelecimentos com seu respectivo grupo de imposto configurado.
- Um campo de **CEST** abaixo da tabela, visível quando aplicável.

---

## O que é um Grupo de Imposto e quais campos ele contém?

Um **Grupo de Imposto** é um perfil tributário reutilizável que reúne em um único cadastro todas as informações fiscais necessárias para que o sistema emita documentos corretamente.

Ao vincular um grupo ao produto, o SAG passa a saber automaticamente, para cada operação fiscal, quais códigos e alíquotas usar — sem que o operador precise preencher nada manualmente na hora da emissão.

### Campos que compõem um Grupo de Imposto

**Identificação e operação:**
- Nome descritivo do grupo
- Regime tributário para o qual o grupo se aplica (Simples Nacional ou Regime Normal)
- CFOP — código que classifica o tipo de operação fiscal (venda, remessa, devolução, etc.)

**ICMS:**
- CST ou CSOSN — código de situação tributária do ICMS
- Origem da mercadoria
- Alíquota do ICMS
- Modalidade e redução da base de cálculo
- Configurações de ICMS Substituição Tributária (MVA, alíquota ST, base ST)
- Código de benefício fiscal

**IPI:**
- CST do IPI
- Código de enquadramento do produto
- Alíquota do IPI

**PIS:**
- CST do PIS
- Alíquota e base de cálculo
- Alíquota e base de PIS Substituição Tributária

**COFINS:**
- CST do COFINS
- Alíquota e base de cálculo
- Alíquota e base de COFINS Substituição Tributária

**CBS e IBS (Reforma Tributária):**
- Classificação tributária do produto
- Percentuais de IBS estadual e municipal
- Percentual de CBS
- Configurações de Imposto Seletivo, regime especial, crédito presumido e monofásico (quando aplicável)

> Para criar ou editar grupos, acesse **Cadastros → Grupos de Imposto**. Consulte [Grupo de Imposto](grupo-de-imposto.md) para o passo a passo completo.

---

## Como funciona o vínculo por estabelecimento?

A tabela exibida na aba Impostos possui quatro colunas:

| Coluna | O que exibe |
|---|---|
| **Cod** | Código numérico de identificação do estabelecimento |
| **Estabelecimento** | Nome fantasia ou razão social da loja |
| **Regime** | Regime tributário daquela loja (Simples Nacional ou Regime Normal) |
| **Grupo de Imposto** | O grupo atualmente vinculado ao produto naquele estabelecimento |

### Um produto, grupos diferentes por estabelecimento

Sim — **um produto pode e frequentemente deve ter grupos de imposto diferentes por estabelecimento**. Isso ocorre porque:

- Estabelecimentos com regimes tributários distintos precisam de regras fiscais diferentes para o mesmo produto.
- A legislação estadual pode exigir CFOPs ou alíquotas diferentes entre estados onde a empresa opera.
- Algumas filiais podem ter benefícios fiscais específicos que não se aplicam às demais.

### Como o sistema filtra os grupos disponíveis

Quando você clica no campo de grupo de imposto de uma linha, o sistema exibe **somente os grupos compatíveis com o regime tributário daquela loja**. Lojas do Simples Nacional não verão grupos do Regime Normal e vice-versa.

---

## O que faz cada botão da linha da tabela?

Cada linha da tabela possui cinco botões à direita do campo de grupo de imposto:

### ✨ Sugestão da I.A. (por linha)

Abre a janela de **Sugestão de Imposto por Inteligência Artificial** para aquele estabelecimento específico. A IA analisa o produto (descrição, NCM, código de barras) e o estabelecimento (nome, regime) e apresenta:

- Todos os campos tributários sugeridos (CST, CFOP, alíquotas de ICMS, PIS, COFINS e IPI)
- Uma **justificativa em texto** explicando o raciocínio por trás de cada sugestão
- A indicação de se já existe um grupo compatível ou se um novo precisará ser criado

Ao clicar em **Aplicar**, o sistema vincula o grupo sugerido àquela linha.

> Se o NCM ou o código de barras não estiverem preenchidos, a IA ainda funciona mas avisa que a precisão pode ser menor.

### ＋ Criar novo grupo

Abre diretamente o formulário de **cadastro de um novo Grupo de Imposto**, já filtrado para o regime tributário daquela linha. Após salvar, o grupo é automaticamente vinculado à linha.

### 🔄 Editar grupo

Abre o formulário de **edição do grupo de imposto atualmente selecionado** na linha.

> Alterações feitas aqui afetam **todos os produtos** que utilizam o mesmo grupo — não apenas o produto atual.

### ✖ Remover grupo

**Limpa o grupo de imposto da linha**, removendo o vínculo entre o produto e o grupo naquele estabelecimento. O produto passa a não ter tributação definida para aquela loja até que um novo grupo seja vinculado. Não exclui o grupo do cadastro.

### Campo de seleção (autocomplete)

Campo de texto com busca automática. Ao clicar ou digitar, exibe os grupos disponíveis para o regime daquele estabelecimento.

---

## O que faz o botão "Aplicar a todos do mesmo regime"?

Botão global no topo da seção, visível somente quando o produto está vinculado a mais de um estabelecimento.

Ao clicar:
1. Identifica o grupo de imposto da linha selecionada
2. Lê o regime tributário daquela linha
3. Aplica o mesmo grupo a **todos os outros estabelecimentos com o mesmo regime**

**Exemplo:** cinco filiais no Simples Nacional e uma no Regime Normal. Ao definir o grupo correto na primeira filial do Simples e clicar no botão, o sistema aplica o mesmo grupo às outras quatro automaticamente. A filial do Regime Normal não é afetada.

---

## O que é o botão "Sugestão da I.A." global (topo da seção)?

Botão global que funciona de forma semelhante ao botão de IA por linha, mas com escopo maior:

| Característica | Botão Global (topo) | Botão por Linha |
|---|---|---|
| **Referência usada** | Primeiro estabelecimento da lista | O estabelecimento daquela linha específica |
| **Onde aplica o resultado** | Nas linhas de mesmo regime do estabelecimento consultado | Somente na linha clicada |
| **Quando usar** | Quando todos os estabelecimentos do mesmo regime podem compartilhar a mesma sugestão | Quando um estabelecimento específico precisa de análise individual |

> Ao aplicar qualquer sugestão da IA, o sistema exibe aviso informando que a sugestão é gerada automaticamente e que a conferência com o contador é sempre recomendada.

---

## Campo CEST

Abaixo da tabela, pode aparecer o campo **CEST** (Código Especificador da Substituição Tributária). Este campo é exibido somente quando o grupo de imposto vinculado ao produto utiliza ICMS Substituição Tributária — situação em que o CEST é obrigatório na nota fiscal.

- Informe o código CEST correto para o produto (7 dígitos)
- Em caso de dúvida, consulte a tabela de CEST disponível na legislação ou com seu contador

---

## Resumo dos Botões

| Botão | Escopo | O que faz |
|---|---|---|
| **✨ Sugestão da I.A.** (topo) | Global | Sugere grupo via IA com base no primeiro estabelecimento e aplica nas linhas de mesmo regime |
| **Aplicar a todos do mesmo regime** (topo) | Global | Copia o grupo da linha selecionada para todas as linhas do mesmo regime |
| **✨** (por linha) | Individual | Sugere grupo via IA para aquele estabelecimento específico |
| **＋** (por linha) | Individual | Abre o cadastro de um novo grupo já filtrado pelo regime da linha |
| **🔄** (por linha) | Individual | Abre a edição do grupo atualmente selecionado naquela linha |
| **✖** (por linha) | Individual | Remove o vínculo do grupo naquela linha |

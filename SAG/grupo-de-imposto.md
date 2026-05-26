# Grupo de Imposto — Documentação de Uso

Guia completo sobre o cadastro e uso dos Grupos de Imposto no SAG. Aqui você aprende o que é um grupo, quais informações ele armazena, como criá-lo e como as telas do sistema estão vinculadas a ele.

---

## O que é um Grupo de Imposto?

Um **Grupo de Imposto** é um conjunto de configurações tributárias que define como um produto deve ser tributado em uma operação fiscal. Em vez de preencher alíquotas, códigos e situações tributárias produto a produto, você cria um grupo com todas essas informações e simplesmente o vincula aos produtos que seguem aquela tributação.

Quando o sistema gera uma NF-e, uma nota de entrada ou um cupom fiscal, ele consulta o grupo de imposto vinculado ao produto naquele estabelecimento e aplica automaticamente todas as alíquotas e códigos corretos no documento.

### Por que usar grupos?

- Evita retrabalho: produtos com a mesma tributação compartilham o mesmo grupo
- Garante consistência: ao alterar uma alíquota no grupo, todos os produtos vinculados são atualizados de uma só vez
- Reduz erros: a configuração tributária fica centralizada e revisada em um único lugar

---

## O que um Grupo de Imposto contém

Ao criar ou editar um grupo de imposto, o sistema armazena as seguintes informações:

### Identificação

| Campo | O que define |
|---|---|
| **Descrição** | Nome que identifica o grupo (ex: "Venda Simples Nacional — Alimentos") |
| **Regime Tributário** | Se o grupo é para empresas do **Simples Nacional** ou do **Regime Normal** (Lucro Presumido / Real) |
| **CFOP** | Código que classifica o tipo de operação fiscal (venda, remessa, devolução, etc.) |

### ICMS

| Campo | O que define |
|---|---|
| **CST / CSOSN** | Código de situação tributária do ICMS. No Simples Nacional é chamado CSOSN; no Regime Normal, CST |
| **Origem** | Origem da mercadoria (nacional, importada, etc.) |
| **Alíquota do ICMS** | Percentual de ICMS sobre a operação |
| **Modalidade da Base de Cálculo** | Como a base de cálculo do ICMS é determinada |
| **Redução da Base** | Percentual de redução aplicado sobre a base de cálculo, quando houver benefício fiscal |
| **MVA ST** | Margem de Valor Agregado para cálculo do ICMS por Substituição Tributária |
| **Alíquota ICMS ST** | Alíquota do ICMS Substituição Tributária |
| **Código de Benefício** | Código do benefício fiscal, quando aplicável à operação |

### IPI (Imposto sobre Produtos Industrializados)

| Campo | O que define |
|---|---|
| **CST do IPI** | Código de situação tributária do IPI |
| **Código de Enquadramento** | Código que classifica o produto para fins de IPI |
| **Alíquota do IPI** | Percentual de IPI sobre a operação |

### PIS

| Campo | O que define |
|---|---|
| **CST do PIS** | Código de situação tributária do PIS |
| **Alíquota do PIS** | Percentual de PIS sobre a operação |
| **Base de Cálculo do PIS** | Percentual da base sobre a qual o PIS incide |
| **Alíquota PIS ST** | Alíquota de PIS por Substituição Tributária, quando aplicável |
| **Base PIS ST** | Base de cálculo do PIS ST |

### COFINS

| Campo | O que define |
|---|---|
| **CST do COFINS** | Código de situação tributária do COFINS |
| **Alíquota do COFINS** | Percentual de COFINS sobre a operação |
| **Base de Cálculo do COFINS** | Percentual da base sobre a qual o COFINS incide |
| **Alíquota COFINS ST** | Alíquota de COFINS por Substituição Tributária, quando aplicável |
| **Base COFINS ST** | Base de cálculo do COFINS ST |

### CBS e IBS (Reforma Tributária)

Campos destinados ao novo sistema tributário em implantação no Brasil:

| Campo | O que define |
|---|---|
| **Classificação Tributária** | Código de classificação do produto na nova estrutura tributária |
| **IBS — Parte Estadual** | Percentual do Imposto sobre Bens e Serviços destinado ao estado |
| **IBS — Parte Municipal** | Percentual do IBS destinado ao município |
| **CBS** | Percentual da Contribuição sobre Bens e Serviços |
| **Imposto Seletivo** | Campos opcionais para produtos sujeitos ao Imposto Seletivo |
| **Regime Especial** | Configurações de regimes especiais de tributação, quando aplicável |
| **Crédito Presumido** | Percentual de crédito presumido, quando aplicável |
| **Monofásico** | Configuração para produtos com tributação monofásica |

---

## Tela de Listagem de Grupos

**Caminho:** Cadastros → **Grupos de Imposto**

A tela de listagem exibe todos os grupos cadastrados com as colunas:

| Coluna | O que exibe |
|---|---|
| **Código** | Número de identificação único do grupo |
| **Descrição** | Nome do grupo |
| **Regime** | Regime tributário do grupo |

### Filtrar grupos

Use o campo de pesquisa no topo para filtrar por código ou descrição. Clique em **Filtrar** para aplicar.

### Ações disponíveis por linha

| Botão | O que faz |
|---|---|
| **Aplicar** | Abre uma janela para vincular o grupo em lote a um ou mais grupos/subgrupos de produtos |
| **Editar** | Abre o cadastro do grupo para alteração |
| **Excluir** | Remove o grupo permanentemente, incluindo todos os vínculos com produtos |

> **Atenção:** Excluir um grupo remove também o vínculo dele com todos os produtos que o utilizam. Os produtos ficarão sem grupo de imposto configurado até que um novo seja atribuído.

---

## Como Criar um Novo Grupo

1. Na tela de listagem, clique em **Cadastrar Novo**
2. Preencha o campo **Descrição** com um nome claro (ex: "Simples Nacional — Bebidas")
3. Selecione o **Regime Tributário**: Simples Nacional ou Regime Normal
4. Selecione o **CFOP** correspondente à operação
5. Percorra as abas e configure cada tributo: ICMS, IPI, PIS, COFINS e CBS/IBS
6. Clique em **Salvar**

Ao salvar, o sistema pode oferecer a opção de aplicar automaticamente o grupo a um grupo ou subgrupo de produtos — útil para vinculação em massa logo na criação.

---

## Detalhamento das Abas do Cadastro

### Aba ICMS

É a aba principal e a mais completa. O conteúdo muda de acordo com o regime tributário selecionado.

**Para o Simples Nacional:**
- O campo de situação tributária exibe os códigos CSOSN (400, 500, 201, 202, etc.)
- Há sub-abas para configurar o **ICMS normal** e o **ICMS ST** separadamente
- Campo para alíquota de **Crédito do Simples** conforme o CSOSN escolhido

**Para o Regime Normal:**
- O campo de situação tributária exibe os códigos CST (00, 10, 20, 30, 40, 41, 50, 51, 60, 70, 90)
- Há sub-abas para **ICMS** e **ICMS ST** com campos detalhados de base de cálculo, modalidade, MVA e alíquotas
- Campo opcional para **Código de Benefício Fiscal**

### Aba IPI

Preencha somente se o produto for sujeito ao IPI:
- **CST do IPI:** selecione a situação tributária correta
- **Código de Enquadramento:** informe o código referente ao produto
- **Alíquota:** campo habilitado conforme o CST selecionado

### Aba PIS

- Selecione o **CST do PIS**
- Informe a **alíquota** e a **base de cálculo**, quando aplicável
- Para operações com PIS Substituição Tributária, preencha também os campos de **Alíquota ST** e **Base ST**

### Aba COFINS

Funciona de forma idêntica à aba PIS, mas para o tributo COFINS.

### Aba CBS / IBS

Destinada à Reforma Tributária. Preencha apenas se o seu contador orientar:
- Selecione a **Classificação Tributária** do produto
- Informe os percentuais de **IBS Estadual**, **IBS Municipal** e **CBS**
- Se o produto for sujeito ao Imposto Seletivo, ative a seção correspondente e preencha o código e a alíquota

---

## Como Editar e Excluir um Grupo

### Editar

1. Na listagem, clique em **Editar** ao lado do grupo desejado
2. O cadastro abre com todos os dados já preenchidos
3. Faça as alterações necessárias em qualquer aba
4. Clique em **Salvar**

> Alterações em um grupo afetam automaticamente todos os produtos vinculados a ele. Não é necessário atualizar produto por produto.

### Excluir

1. Na listagem, clique em **Excluir** ao lado do grupo desejado
2. O sistema pede confirmação
3. Confirme para remover o grupo e todos os seus vínculos com produtos

> A exclusão é permanente. Produtos que utilizavam o grupo ficam sem tributação definida.

---

## Aplicar um Grupo a Produtos em Lote

O botão **Aplicar** em cada linha da listagem abre uma janela onde você seleciona um ou mais **grupos de produtos** (categorias) ou **subgrupos** do cadastro.

Ao confirmar, o sistema vincula o grupo de imposto a todos os produtos pertencentes às categorias selecionadas — útil para configurar tributação em massa quando há muitos produtos na mesma categoria fiscal.

---

## Como o Grupo se Conecta aos Produtos

O vínculo entre um produto e um grupo de imposto é feito **por estabelecimento**:

- Um mesmo produto pode ter grupos de imposto diferentes em cada filial
- O sistema respeita o regime tributário de cada estabelecimento: lojas do Simples Nacional só enxergam grupos do Simples; lojas do Regime Normal só enxergam grupos do Regime Normal
- A configuração é feita na tela de **Alteração de Produto**, na aba **Impostos**

Para entender em detalhes como funciona essa tela e os botões de cada linha, consulte [Produto — Aba Imposto](produto-aba-impostos.md).

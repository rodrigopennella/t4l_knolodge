# SAG — Cadastros

Módulo para gerenciamento de clientes, fornecedores, produtos, usuários e demais registros do sistema.

---

## Cadastro de Clientes

**Caminho:** Menu Principal > **Cadastros** > **Clientes**

### Aba: Geral

**Seção Informações:**
| Campo | Tipo | Observação |
|---|---|---|
| Nome / Razão Social | Texto | Máx. 80 caracteres |
| Ativo | Caixa de seleção | Marcar para cliente ativo |
| Código | Numérico | Gerado automaticamente |
| CPF / CNPJ | Texto | Máx. 18 caracteres |
| IE / RG | Texto | Máx. 13 caracteres (exibido conforme tipo) |
| Data de Nascimento / Abertura | Data | |
| Nome Fantasia | Texto | Máx. 80 caracteres (CNPJ) |
| Responsável | Texto | Máx. 30 caracteres |
| CRT | Lista | 1-Simples Nacional / 2-Simples Nacional Excesso / 3-Regime Normal / 4-MEI |
| Tipo Contribuinte | Lista | 9-Não Contribuinte / 1-Contribuinte ICMS / 2-Contribuinte Isento |

**Seção Telefones:**
- Adicionar múltiplos telefones
- Campos: **Telefone** (máx. 14 caracteres) e **Descrição** (máx. 100 caracteres)
- Botões: **Adicionar Telefone** / **Excluir Telefone**

**Botão:** Consultar CNPJ (preenche dados automaticamente via Receita Federal)

---

## Cadastro de Produtos

**Caminho:** Menu Principal > **Cadastros** > **Produtos**

### Campos Principais
| Campo | Observação |
|---|---|
| Código | Identificador do produto |
| Descrição | Nome exibido no caixa e relatórios |
| Ativo | Produto disponível para venda |
| Preço de Venda | Valor cobrado ao cliente |
| Preço de Custo | Valor de aquisição |
| Unidade de Medida | Ex: UN, KG, LT |
| Grupo / Categoria | Classificação para impressão e relatórios |
| Estoque Mínimo | Alerta de reposição |

### Aba: Imposto

Define a configuração tributária do produto por estabelecimento. Não há campos diretos de CST ou CFOP — toda a tributação é gerenciada por **Grupos de Imposto**.

- Cada estabelecimento pode ter um grupo de imposto diferente para o mesmo produto
- O sistema exibe apenas grupos compatíveis com o regime tributário de cada loja
- Sem um Grupo de Imposto vinculado, o produto não emite NFC-e ou NF-e

> Para detalhes sobre esta aba e seus botões, consulte [Produto — Aba Imposto](produto-aba-impostos.md).
> Para criar ou editar grupos, consulte [Grupo de Imposto](grupo-de-imposto.md).

### Cadastro de Pizza
**Caminho:** Cadastros > **Pizzas**
- Cadastro de **Tamanhos**
- Cadastro de **Sabores** com preços por tamanho
- Cadastro de **Acompanhamentos** (bordas, extras)

### Menu Opções — Cadastros > Produtos

**Caminho:** Cadastros > Produtos > **Opções**

O botão "Opções" na tela de produtos oferece as seguintes funcionalidades:

| Opção | O que faz |
|---|---|
| **Importar/Exportar Excel** | Importa ou exporta a lista de produtos em planilha |
| **Histórico do Produto** | Exibe o histórico de alterações do produto selecionado |
| **Alterar Colunas** | Permite escolher quais colunas são exibidas na listagem de produtos |
| **Ocultar Inativos** | Oculta da lista os produtos com flag "Ativo" desmarcada |
| **Ocultar Matéria Prima** | Oculta da lista os produtos cadastrados como matéria prima |

> **Para ver produtos inativos:** acesse Cadastros > Produtos > Opções e verifique se "Ocultar Inativos" está ativado. Se estiver, desative para que os inativos apareçam na listagem. Por padrão, todos os produtos (ativos e inativos) aparecem na lista.

#### Importar / Exportar Excel

**Caminho:** Cadastros > Produtos > **Opções** > **Importar/Exportar Excel**

| Opção | O que faz |
|---|---|
| **Exportar Excel Produtos** | Gera uma planilha com todos os produtos cadastrados (código, descrição, preço, etc.) |
| **Importar Excel Produtos** | Atualiza ou cria produtos em massa a partir de uma planilha preenchida |

> Use a exportação para obter a planilha de produtos atualizada — útil para enviar à contabilidade, auditar o cadastro ou preparar uma importação em lote.

#### Atenção ao importar

Na tela de importação, o sistema exibe checkboxes para selecionar quais campos serão atualizados (Descrição, Preço, Cod. Barras, NCM, Grupo de Imposto, Estoque, etc.). **Selecione apenas os campos que foram realmente alterados na planilha.** Marcar campos desnecessários pode sobrescrever dados corretos já cadastrados no sistema.

---

## Cadastro de Fornecedores

**Caminho:** Menu Principal > **Cadastros** > **Fornecedores**

Campos principais:
- Nome / Razão Social
- CNPJ
- Contato / Telefone
- Endereço

---

## Cadastro de Funcionários

**Caminho:** Menu Principal > **Cadastros** > **Funcionários**

Campos principais:
- Nome
- CPF
- Cargo / Função
- Acesso ao sistema (vinculado ao usuário)

---

## Usuários e Permissões

**Caminho:** Outros > **Central de Usuários**

### Criar Novo Usuário
1. Clique em **Novo**
2. Informe:
   - **Login** (nome de acesso)
   - **Senha**
3. Selecione o **Grupo de Permissão**
4. Clique em **Salvar**

### Grupos de Permissão
**Caminho:** Outros > **Grupo de Permissões**

- Cada grupo define quais módulos e ações o usuário pode realizar
- Exemplos de grupos: Administrador, Caixa, Gerente, Suporte
- Para alterar permissões: selecione o grupo > marque/desmarque as funcionalidades por aba de setor
- Alterações no grupo aplicam-se **imediatamente** a todos os usuários vinculados, sem necessidade de relogar

> Para o detalhamento completo de cada permissão disponível, consulte [Grupos de Permissão](grupos-permissoes.md).

### Alterar Senha
- O próprio usuário pode alterar: menu superior > **Alterar Senha**
- Administrador pode redefinir: Usuários > selecione o usuário > altere a senha

### Cartão de Acesso (código de barras)

**Caminho:** Outros > **Cartão de Acesso**

Gera um cartão em PDF com o logo da loja e um código de barras vinculado ao usuário. O cartão pode ser bipado nos caixas para autorizar operações que exigem confirmação de gerente (como cancelamentos), sem precisar digitar senha.

**Como gerar:**
1. Acesse **Outros → Cartão de Acesso**
2. Selecione o usuário desejado
3. Informe a **senha de login** desse usuário para confirmar
4. O sistema gera um PDF com o cartão pronto para impressão

---

## Cadastro de Promoções

**Caminho:** Cadastros > **Promoções**

- Configure produtos com preço especial em períodos definidos
- Campos: produto, valor promocional, data início, data fim, dias da semana
- Use **Iniciar Promoção** para ativar manualmente

---

## Cupons de Desconto

**Caminho:** Cadastros > **Cupons de Desconto**

- Código do cupom
- Tipo de desconto (percentual ou valor fixo)
- Validade
- Limite de uso

---

## Cadastro de Estabelecimentos / Filiais

**Caminho:** Cadastros > **Estabelecimentos**

Usado em ambiente multiloja para cadastrar filiais e suas configurações específicas.

---

## Cadastro de Transportadoras / Entregadores

**Caminho:** Cadastros > **Transportadoras** / **Entregadores**

Usado no módulo de delivery e romaneio de entregas.

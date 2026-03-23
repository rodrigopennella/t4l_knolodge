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

### Aba: Impostos NFE/NFCE
| Campo | Observação |
|---|---|
| CST | Classificação Tributária (obrigatório para emissão fiscal) |
| CFOP | Código Fiscal de Operações (consultar contabilidade) |
| ICMS | Alíquota |
| PIS / COFINS | Alíquotas |

> Produtos com CST ou CFOP incorretos não emitem NFC-e. Consulte a contabilidade para os valores corretos.

### Cadastro de Pizza
**Caminho:** Cadastros > **Pizzas**
- Cadastro de **Tamanhos**
- Cadastro de **Sabores** com preços por tamanho
- Cadastro de **Acompanhamentos** (bordas, extras)

### Importação de Produtos
- Possível importar via planilha Excel
- **Caminho:** Cadastros > Produtos > **Importar**

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

**Caminho:** Menu Principal > **Usuários** (ou Configurações > Usuários)

### Criar Novo Usuário
1. Clique em **Novo**
2. Informe:
   - **Login** (nome de acesso)
   - **Senha**
3. Selecione o **Grupo de Permissão**
4. Clique em **Salvar**

### Grupos de Permissão
**Caminho:** Usuários > **Grupos**

- Cada grupo define quais módulos e ações o usuário pode realizar
- Exemplos de grupos: Administrador, Caixa, Gerente, Suporte
- Para alterar permissões: selecione o grupo > **Permissões** > marque/desmarque as funcionalidades

### Alterar Senha
- O próprio usuário pode alterar: menu superior > **Alterar Senha**
- Administrador pode redefinir: Usuários > selecione o usuário > altere a senha

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

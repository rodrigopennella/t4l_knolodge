# Balança Etiquetadora

Equipamento utilizado para pesagem e etiquetagem de produtos, comum em padarias, mercados e açougues. A etiqueta impressa na balança contém informações como peso, preço, código de barras e validade.

---

## Integração com o SAG

A comunicação entre o SAG e a balança é feita via **MGV** (aplicativo externo de gerenciamento de balança). O SAG exporta um arquivo com as informações dos produtos; esse arquivo é importado no MGV, que então envia os dados para a balança.

**Informações enviadas pelo SAG:**
- Código do produto
- Descrição
- Validade
- Código de barras
- Preço

**Caminho no SAG:** Outros → **Arqs. de Balança**

---

## Modelos Suportados

### Toledo
Três arquivos de exportação disponíveis:

| Arquivo | Conteúdo |
|---|---|
| `itensmgv` | Arquivo principal de itens para o MGV |
| `txitens` | Arquivo de itens em formato texto |
| `txinfo` | Arquivo com a observação do produto |

### Filizola
| Arquivo | Conteúdo |
|---|---|
| `cadtxt` | Arquivo de cadastro de produtos |

---

## Processo de Importação no MGV

> O MGV é um aplicativo externo ao SAG — seu processo de importação e configuração não faz parte do escopo de suporte do Cláudio.
>
> Se o cliente precisar de orientação sobre o MGV → **ESCALAR_SUPORTE** para atendimento especializado.

# SAG — NFC-e

Módulo fiscal para emissão de documentos eletrônicos ao consumidor final.

---

## Conceitos

| Sigla | Nome | Uso |
|---|---|---|
| NFC-e | Nota Fiscal de Consumidor Eletrônica | Emitida diretamente pelo SAG na venda ao consumidor final |
| NF-e | Nota Fiscal Eletrônica | Para vendas entre empresas (B2B) |
| XML | Arquivo eletrônico | Representação digital do documento fiscal |
| Certificado Digital | Arquivo de autenticação | Obrigatório para emissão de NFC-e |

---

## NFC-e — Emissão na Venda

A NFC-e é emitida automaticamente ao finalizar a venda, desde que:
- O caixa tenha NFC-e habilitado
- O cliente informe CPF/CNPJ (ou a venda seja sem identificação, conforme legislação estadual)
- Os produtos tenham CST e CFOP configurados corretamente

---

## NFC-e — Problemas Frequentes

### Erro ao emitir — produto sem configuração fiscal
- Acesse: **Cadastros > Produtos** > selecione o produto > aba **Imposto**
- Verifique se o produto tem um **Grupo de Imposto** vinculado — sem ele, a emissão não funciona
- Verifique e corrija o **CST** e o **CFOP** (consulte a contabilidade)

### NFC-e não emite mas venda passa
- Verifique se NFC-e está habilitado no caixa específico
- Reinicie o SAG após qualquer alteração de configuração

---

## SAT / CF-e — Descontinuado

O SAT (Sistema Autenticador e Transmissor) foi descontinuado em 2025.
Estabelecimentos que utilizavam SAT para emissão de cupom fiscal devem
migrar para **NFC-e**, que passa a ser o único modelo aceito para emissão
de cupom ao consumidor final.

> Dúvidas sobre a migração: entrar em contato com o suporte T4L.

---

## XML — Envio e Consulta

### Enviar XMLs por E-mail
1. Acesse: **Outros > Ferramentas CFe > Arquivos XML**
2. Defina o período
3. Marque **Compactar em arquivo único**
4. Marque **Enviar por e-mail**
5. Informe os e-mails destinatários
6. Clique em **Gerar**

### Validar XML com Relatório
Se houver divergência entre XML e relatório de vendas:
1. Compare o relatório de vendas do SAG com o arquivo XML gerado
2. Se necessário, reimporte o XML pela opção correspondente no menu
3. Consulte o suporte se a divergência persistir

---

## Certificado Digital

O certificado digital é obrigatório para emissão de NFC-e. Existem dois tipos:

| Tipo | Formato | Descrição |
|---|---|---|
| **A1** | Arquivo `.pfx` | Arquivo digital salvo no computador — o mais comum |
| **A3** | Token/cartão físico | Dispositivo físico conectado por USB |

### Aplicar Certificado A1 no SAG

1. Acesse **Outros > Certificado Digital**
2. Selecione o tipo **A1**
3. Clique em buscar arquivo e selecione o arquivo `.pfx`
4. Informe a **senha do certificado**
5. Clique em **Salvar**
6. **Feche e reabra o SAG** para aplicar

### Informações Importantes

- O certificado pode ser aplicado em **qualquer computador que tenha o SAG instalado**
- Qualquer usuário consegue aplicar seguindo o passo a passo acima
- Validade: geralmente 1 ou 3 anos — monitorar vencimento
- Se certificado **vencido**: o cliente renova junto à contabilidade ou certificadora e fornece novo arquivo `.pfx`
- Se o cliente tiver dificuldade após seguir os passos: acionar suporte T4L para auxílio remoto via AnyDesk

### Erros Comuns

| Mensagem | Causa | Ação |
|---|---|---|
| "Certificado vencido" | Certificado expirou | Renovar com a contabilidade |
| "Senha incorreta" | Senha do `.pfx` errada | Confirmar senha com quem gerou o certificado |
| NFC-e não emite após aplicar | SAG não foi reiniciado | Fechar e reabrir o SAG |

---

## NF-e

Para emissão de nota fiscal eletrônica entre empresas (B2B), consulte os guias específicos:

- [Guia de Emissão Passo a Passo](nfe-emissao.md)
- [Erros, Rejeições e Soluções](nfe-erros.md)

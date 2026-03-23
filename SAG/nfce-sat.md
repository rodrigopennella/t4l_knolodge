# SAG — NFC-e, SAT e NF-e

Módulo fiscal para emissão de documentos eletrônicos.

---

## Conceitos

| Sigla | Nome | Uso |
|---|---|---|
| NFC-e | Nota Fiscal de Consumidor Eletrônica | Emitida diretamente pelo SAG na venda ao consumidor |
| SAT / CF-e | Sistema Autenticador e Transmissor / Cupom Fiscal Eletrônico | Equipamento homologado que emite CF-e (usado em SP) |
| NF-e | Nota Fiscal Eletrônica | Para vendas entre empresas (B2B) |
| XML | Arquivo eletrônico | Representação digital do documento fiscal |
| Certificado Digital | Arquivo de autenticação | Obrigatório para emissão de NFC-e |

---

## NFC-e — Configuração Inicial

**Caminho:** Menu Principal > **NFC-e**

Para que a NFC-e funcione, é necessário:
1. **Credenciais geradas** pela contabilidade (junto à SEFAZ do estado)
2. **Certificado Digital** instalado no computador servidor
3. Configuração das credenciais no SAG

### Verificar Configuração
1. Acesse **NFC-e** no menu principal
2. Verifique se os dados de credencial estão preenchidos
3. Se aparecer botão **Validar Online**, clique nele para sincronizar a licença
4. Feche e abra o SAG novamente após configurar

---

## NFC-e — Emissão na Venda

A NFC-e é emitida automaticamente ao finalizar a venda, desde que:
- O caixa tenha NFC-e habilitado
- O cliente informe CPF/CNPJ (ou a venda seja sem identificação, conforme legislação estadual)
- Os produtos tenham CST e CFOP configurados corretamente

---

## NFC-e — Problemas Frequentes

### "Sem configuração NFC-e"
- Verifique se as credenciais foram geradas com a contabilidade
- Verifique se o certificado digital está instalado
- Acesse NFC-e no SAG e preencha os dados

### Erro ao emitir — produto sem configuração fiscal
- Acesse: **Cadastros > Produtos** > selecione o produto > aba **Impostos NFE/NFCE**
- Verifique e corrija o **CST** e o **CFOP** (consulte a contabilidade)

### NFC-e não emite mas venda passa
- Verifique se NFC-e está habilitado no caixa específico
- Reinicie o SAG após qualquer alteração de configuração

---

## SAT / CF-e (São Paulo)

O SAT é um equipamento físico conectado ao computador. O SAG envia as informações e o SAT emite o CF-e.

**Verificar se SAT está funcionando:**
1. Verifique se o equipamento SAT está ligado e com luz indicadora ativa
2. No SAG, acesse **Ferramentas** > **SAT** para testar comunicação
3. Se não responder, verifique a conexão USB

### Gerar Arquivos XML do SAT
1. Acesse: **Outros > Ferramentas CFe > Arquivos XML**
2. Configure as opções:
   - **Gerar CF-e Cancelados:** marque se necessário
   - **Compactar em arquivo único:** recomendado
   - **Enviar por e-mail:** informe os destinatários
3. Clique em **Gerar**

---

## NF-e — Emissão

**Caminho:** Menu Principal > **NF-e**

Usado para emitir nota fiscal em compras/vendas entre empresas.

### Campos Principais
- **Destinatário:** CNPJ, Razão Social
- **Produtos:** código, quantidade, valor, CFOP, CST, ICMS, IPI
- **Transporte:** transportadora, volumes
- **Pagamento:** forma e valor

### Processo
1. Acesse **NF-e**
2. Preencha os dados do destinatário
3. Adicione os produtos com dados fiscais corretos
4. Clique em **Transmitir** para enviar à SEFAZ
5. Após aprovação, o XML e DANFE ficam disponíveis para download/envio

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

- O certificado digital (arquivo `.pfx` ou `.p12`) deve ser instalado no **computador servidor**
- Tipo: e-CNPJ (emitido em nome da empresa)
- Validade: geralmente 1 ou 3 anos — monitorar vencimento
- Em caso de vencimento: adquirir novo certificado com certificadora e reinstalar

> O SAG não armazena nem gerencia certificados digitais diretamente — a instalação é feita no sistema operacional Windows.

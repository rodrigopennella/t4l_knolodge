# SAG — Configurações

Módulo de parametrização do sistema, impressoras, integrações e permissões.

---

## Visão Geral das Configurações

O SAG possui dois níveis de configuração, acessíveis no canto superior direito da tela:

| Configuração | Escopo | Acesso |
|---|---|---|
| **Config. Terminal** | Configurações por máquina/caixa | Técnicos |
| **Config. Global** | Configurações para todo o sistema | Técnicos |

Além disso, existem configurações acessíveis pela aba **Outros** na barra superior.

---

## Config. Terminal (Por Máquina)

**Caminho:** Canto superior direito > **Config. Terminal**

Configurações específicas para cada terminal/caixa. Dividido em abas:

### Aba: Impressoras
Configuração de impressoras para cada contexto:

**Frente de Caixa:**
- Configuração de Impressora (ex: EPSON TM-T20)
- Nº vias da Venda
- Opções de impressão: Lançamentos do Fechamento, Comprovante Cancelamento, Saldo na Caderneta, Ticket dos Itens, Comprovante Desconto
- Seção "Imprimir Fechamento": Totais das Vendas, Totais no Caixa, Divergências do Fechamento, Mapa de Vendas, Detalhamento Sangrias, Divergências do Fech. Tabelas
- Nº de vias (Caderneta) e Nº de vias (Sangria)

**Terminal PC:**
- Configuração de Impressora
- Nº vias
- Imprimir Produção (checkbox)

**Pedidos:**
- Configuração de Impressora
- Nº vias
- Imprimir Produção (checkbox)
- Imprimir Senha — Tipo Pedido (Retirada, etc.)

### Aba: NFC-e
Configurações de emissão de Nota Fiscal de Consumidor Eletrônica para este terminal.

### Aba: TEF
Configurações de Transferência Eletrônica de Fundos (pagamento com cartão/PIX) para este terminal.

### Aba: Terminal PC
Configurações específicas do terminal de comandas.

### Aba: Caixa
Opções de comportamento do caixa neste terminal:

| Opção | Descrição |
|---|---|
| Acionamento Automático da Gaveta | Abre gaveta ao finalizar venda |
| Utiliza Comandas | Habilita uso de comandas |
| Quantidade Antes do Produto | Permite formato multiplicador (0,500*código) |
| Utiliza Balança | Integra com balança de peso |
| F4 Abre Terminal | F4 abre Terminal de Comandas em vez de consulta |
| Pagamento acima do saldo (Caderneta) | Permite pagar valor acima do saldo |
| Avisa Quantidade maior que 99 | Alerta para quantidades altas |
| Lançar Valores ao Finalizar Caixa | Exibe tela de valores reais no fechamento |
| Caixa Utiliza Taxa de Serviço | Habilita taxa de serviço |
| Taxa de Serviço Automática | Aplica taxa automaticamente |
| Caixa Solicita Vendedor Antes de Concluir a Venda | Pede identificação do vendedor |
| Utiliza acompanhamentos | Habilita acompanhamentos nos produtos |
| Inicia Venda com Enter | Enter inicia venda (em vez de só F3) |
| Caixa imprime descritivo venda | Imprime descrição na venda |
| Fechar Caixa Apenas Sem Comanda Aberta | Impede fechamento com comandas em aberto |
| Avisa item duplicado | Alerta ao inserir item já na venda |
| Mostra Observação do Item | Exibe observações dos itens |
| Solicita NSU para espécies sem TEF | Pede NSU para pagamentos fora do TEF |
| Comanda Apenas com Leitor | Exige leitor para comanda |
| Solicita cadastro de cliente | Solicita cadastro ao finalizar |
| Imprimir senha venda | Imprime senha da venda |
| Utiliza Tela Espelho — Ip Espelho | Habilita tela espelho (segundo monitor) |
| Avisa Sangria quando Valor é superior à | Define valor para alerta de sangria |
| Tipo Caixa | Normal ou outros tipos |

### Aba: Balança
Configurações de integração com balança de peso.

### Aba: Personalizar
Personalizações visuais e comportamentais do terminal.

### Aba: Delivery
Configurações de delivery específicas para este terminal.

### Aba: Outros
Configurações adicionais do terminal.

---

## Config. Global (Todo o Sistema)

**Caminho:** Canto superior direito > **Config. Global**

Configurações que valem para todo o sistema. Dividido em abas:

### Aba: Email
Configurações de envio de e-mail pelo sistema.

### Aba: Caixa
| Campo/Opção | Descrição |
|---|---|
| Taxa de Serviço | Produto e percentual da taxa de serviço |
| Mensagem Taxa | Texto exibido ao cliente (ex: "Taxa de Serviço Opcional") |
| Contra Vale | Configuração de contra vale |
| Desconto Padrão | Percentual de desconto padrão |
| Nº de Vendas em Espera | Limite de vendas em espera |
| Caixa apenas um dia | Caixa só funciona no dia da abertura |
| Caixa aviso sonoro para produto inexistente | Alerta sonoro para código inválido |
| Permite desconto no pagamento de caderneta | Habilita desconto na caderneta |
| Agrupa produtos na impressão | Agrupa itens iguais |
| Taxa de serviço seletiva | Taxa de serviço pode ser selecionada por item |
| Venda apenas com comanda | Obriga uso de comanda para vender |
| Imprimir senha venda | Imprime senha da venda |
| Quantidade de dígitos senha | Define tamanho da senha |
| Origem senha venda | Código Venda ou outro |

### Aba: Delivery
| Campo/Opção | Descrição |
|---|---|
| Integra Pedidos com Comandas | Pedidos de delivery geram comanda |
| Reimprimir Pedido Alterado | Reimprime ao alterar pedido |
| Imprime Código de Barras | Imprime código de barras no pedido |
| Gerar Código de Controle | Gera código de controle |
| Delivery Exige Entregador | Obriga selecionar entregador |
| Exibe Distância na Observação | Mostra distância no pedido |
| Ordena por | Grupo ou outra opção |
| DDD Telefone | DDD padrão (ex: 11) |
| Email Pedido | E-mail para envio de pedidos |
| Taxa de Entrega | Produto cadastrado como taxa |
| Tipo de Cálculo | Por Cliente ou outro |
| Observação Padrão | Texto padrão nos pedidos |
| Integrações logísticas | Botão para configurar integrações |

### Aba: Romaneio
Configurações específicas do módulo de romaneio (fábricas).

### Aba: Comandas
Configurações globais de comportamento das comandas.

### Aba: Estoque
Configurações globais de estoque.

### Aba: Financeiro
Configurações globais do módulo financeiro.

### Aba: Etiquetadora
Configurações de impressão de etiquetas.

### Aba: Outros
Configurações diversas.

### Aba: Módulos
Habilitação e configuração de módulos do sistema.

### Aba: Autoatendimento
Configurações do totem de auto-atendimento.

### Aba: NFC-e
Configurações globais de emissão de NFC-e.

---

## Aba Outros — Configurações Adicionais

**Caminho:** Aba **Outros** na barra superior

Funcionalidades de configuração e administração:

| Item | Função |
|---|---|
| **Central de Usuários** | Gerenciamento de usuários do sistema |
| **Ferramentas** | Ferramentas de manutenção e diagnóstico |
| **Grupo de Permissões** | Configuração de grupos de permissão |
| **Arqs. da Balança** | Arquivos de integração com balança |
| **Etiquetas** | Configuração e impressão de etiquetas |
| **Impressoras Remotas** | Gerenciamento de impressoras em rede |
| **Dados Cadastrais** | Dados do estabelecimento |
| **Certificado Digital** | Instalação e gerenciamento do certificado digital |
| **Licença** | Informações da licença do sistema |
| **Config Espécies** | Configuração de espécies de pagamento |
| **Cartão de Acesso** | Configuração de cartões de acesso |
| **Lei do Imposto** | Configurações de lei do imposto |
| **Ferramentas CFe** | Ferramentas para CF-e/SAT (geração de XML, etc.) |
| **TEF** | Configurações de TEF/SiTef |
| **Conf. Dispositivos Móveis** | Configuração de tablets e celulares |
| **Configurações de Tela de Pedidos** | Configurações do KDS (Tela de Pedidos) |

---

## Impressoras

**Caminho:** Config. Terminal > **Impressoras**

### Cadastrar Impressora
1. Acesse Config. Terminal > Impressoras
2. Clique em **Nova** (ícone +)
3. Informe:
   - **Nome** (identificação interna)
   - **Tipo** (USB, rede, serial)
   - **Endereço/Porta** (conforme tipo)
4. Clique em **Testar** para verificar a comunicação
5. Salve

### Regras de Impressão
Configuradas na aba Impressoras do Config. Terminal, nas seções:
- **Frente de Caixa** — impressora e vias para cupom do cliente
- **Terminal PC** — impressora e vias para terminal de comandas
- **Pedidos** — impressora e vias para pedidos de delivery

---

## Formas de Pagamento

**Caminho:** Configurações > **Formas de Pagamento** (ou via cadastro em Outros)

- Habilitar ou desabilitar formas de pagamento disponíveis no caixa
- Cada forma tem um código numérico que o operador usa para selecioná-la
- Configurar campos e comportamento de cada forma
- Formas comuns: Dinheiro, Cartão Débito, Cartão Crédito, PIX, QR Code, Caderneta, Desconto, iFood, Ticket, etc.

---

## Integrações

O SAG possui integrações com diversas plataformas:

| Integração | Função |
|---|---|
| iFood | Receber pedidos do iFood automaticamente |
| 99food | Receber pedidos do 99food |
| Keeta | Receber pedidos do Keeta |
| OpenDelivery | Protocolo aberto de delivery |
| TEF / SiTef | Gateway de pagamento com cartão/PIX |
| Balança | Integração com balanças de peso |
| Multiloja | Sincronização com outras filiais |

> Todas as integrações são configuradas pela equipe técnica da T4L.

---

## Licença do Sistema

**Caminho:** Outros > **Licença**

- Exibe informações da licença ativa
- Número de caixas contratados
- Módulos habilitados
- Validade

> Se o sistema exibir alerta de licença expirada ou inválida, entre em contato com o suporte T4L.

---

## Programa de Fidelidade

**Caminho:** Cadastros > **Programa de Fidelidade**

- Define regras de acúmulo de pontos (ex: R$ 1,00 = 1 ponto)
- Define regras de resgate
- Configura validade dos pontos

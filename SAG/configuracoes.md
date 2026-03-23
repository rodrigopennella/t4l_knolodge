# SAG — Configurações

Módulo de parametrização do sistema, impressoras, integrações e permissões.

---

## Configurações Gerais

**Caminho:** Menu Principal > **Configurações**

Parâmetros gerais do estabelecimento:
- Nome e dados do estabelecimento
- Comportamento do caixa (emissão automática de NFC-e, solicitar CPF, etc.)
- Configurações de impressão padrão
- Integrações habilitadas

---

## Impressoras

**Caminho:** Configurações > **Impressoras**

### Cadastrar Impressora
1. Acesse Configurações > Impressoras
2. Clique em **Nova**
3. Informe:
   - **Nome** (identificação interna)
   - **Tipo** (USB, rede, serial)
   - **Endereço/Porta** (conforme tipo)
4. Clique em **Testar** para verificar a comunicação
5. Salve

### Regras de Impressão
**Caminho:** Configurações > **Regras de Impressão**

Define qual grupo/categoria de produto imprime em qual impressora.

| Campo | Descrição |
|---|---|
| Grupo / Categoria | Categoria de produto (ex: Bebidas, Salgados) |
| Impressora | Impressora de destino |
| Número de Vias | Quantas cópias imprimir (padrão: 1) |

**Para configurar:**
1. Selecione o grupo/categoria
2. Escolha a impressora
3. Defina o número de vias
4. Salve
5. Teste com um pedido real

---

## Formas de Pagamento

**Caminho:** Configurações > **Formas de Pagamento**

- Habilitar ou desabilitar formas de pagamento disponíveis no caixa
- Configurar se aceita VR (vale refeição), cartões específicos, etc.
- Configurar campos e comportamento de cada forma

---

## Tabelas de Preço

**Caminho:** Configurações > **Tabelas de Preço**

- Permite criar múltiplas tabelas (ex: balcão, delivery, atacado)
- Associar tabelas a clientes, horários ou canais de venda
- O caixa aplica automaticamente a tabela correta conforme a regra

---

## Integrações

**Caminho:** Configurações > **Integrações**

| Integração | Função |
|---|---|
| iFood | Receber pedidos do iFood automaticamente |
| TEF / SiTef | Gateway de pagamento com cartão/PIX |
| Balança | Integração com balanças de peso |
| Multiloja | Sincronização com outras filiais |

### Configurar iFood
1. Acesse Configurações > Integrações > iFood
2. Informe as credenciais da integração
3. Habilite o recebimento de pedidos
4. Verifique se os produtos do SAG estão vinculados ao cardápio do iFood

---

## Configurações de Caixa

**Caminho:** Configurações > **Caixa** (ou parâmetros do terminal)

Configurações específicas por terminal:
- Habilitar / desabilitar NFC-e neste caixa
- Impressora padrão para cupom do cliente
- Solicitar CPF na venda
- Exibir taxa de serviço
- Comportamento ao finalizar venda

---

## Automatizador

**Caminho:** Menu Principal > **Automatizador** (ou Configurações > Automatizador)

Permite agendar tarefas automáticas:
- Backup automático do banco de dados
- Sincronização com multiloja
- Envio de relatórios por e-mail

**Como configurar um serviço:**
1. Acesse Automatizador > **Cadastro de Serviços**
2. Selecione o tipo de serviço
3. Configure horário e frequência
4. Ative o serviço

**Consultar histórico:** Automatizador > **Consultar Serviços**

---

## Multiloja

**Caminho:** Menu Principal > **Multiloja**

Gerencia a sincronização de dados entre unidades de uma rede:
- Produtos e preços
- Cadastro de clientes
- Relatórios consolidados

---

## Licença do Sistema

**Caminho:** Menu Principal > **Licença**

- Exibe informações da licença ativa
- Número de caixas contratados
- Módulos habilitados
- Validade

> Se o sistema exibir alerta de licença expirada ou inválida, entre em contato com o suporte T4L.

---

## Programa de Fidelidade

**Caminho:** Configurações > **Programa de Fidelidade**

- Define regras de acúmulo de pontos (ex: R$ 1,00 = 1 ponto)
- Define regras de resgate
- Configura validade dos pontos

---

## Programa de Recompensa

**Caminho:** Configurações > **Programa de Recompensa**

Versão alternativa/complementar ao programa de fidelidade com mecânicas de cashback ou benefícios diferenciados.

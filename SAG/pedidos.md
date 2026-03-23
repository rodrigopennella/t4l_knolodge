# SAG — Pedidos e Delivery

Módulo de gerenciamento de pedidos para delivery, retirada e mesas.

---

## Tela de Pedidos

**Caminho:** Menu Principal > **Pedidos**

### Seção: Cliente
| Campo | Observação |
|---|---|
| Telefone | Busca por telefone do cliente |
| Botão Pesquisar Cliente | Busca na base de clientes cadastrados |
| Botão Alterar Cliente | Edita dados do cliente selecionado |
| Nome do Cliente | Exibido após seleção |

### Tipo de Entrega
- **Entrega:** seleciona endereço do cliente, com opção de calcular distância
- **Retirada:** cliente retira no local

### Origem do Pedido
- Seleção de qual canal originou o pedido (balcão, telefone, iFood, WhatsApp, etc.)
- Campo: **Código Externo** (exibido conforme a origem selecionada)

### Tipo de Pedido
- **Pedido:** venda normal de delivery
- **Encomenda:** pedido para data futura
- **Orçamento:** proposta sem confirmação

---

## Adicionar Produtos ao Pedido

1. Selecione o cliente e tipo de entrega
2. Clique em **Adicionar Produto**
3. Pesquise o produto por nome ou código
4. Informe a quantidade
5. Para produtos com acompanhamentos obrigatórios, o sistema solicita a seleção antes de confirmar

### Produtos com Acompanhamento
- O sistema exibe a tela de **Acompanhamentos** automaticamente
- Tipos: opcionais, obrigatórios, adicionais pagos, variações

### Pedido de Pizza
- Selecione o **Tamanho**
- Selecione os **Sabores** (1 ou mais, conforme tamanho)
- Selecione a **Borda** (se disponível)
- Confirme o pedido

---

## Consultar Pedidos

**Caminho:** Caixa > **F8** ou Menu > **Pedidos** > Consultar

- Filtre por status: pendente, em produção, pronto, entregue
- Filtre por período, cliente ou número
- Selecione um pedido para ver detalhes ou lançar no caixa

---

## Integração com iFood

**Caminho:** Configurações > **Integrações** > iFood

### Ativar Integração
1. Acesse Configurações > Integrações
2. Selecione iFood
3. Informe as credenciais da integração (fornecidas pelo iFood)
4. Habilite a sincronização
5. Pedidos do iFood passarão a aparecer automaticamente no SAG

### Problemas com iFood
- Se pedidos não chegam: verifique se a integração está habilitada
- Se pagamento não passa: verifique as configurações de pagamento do iFood
- Reinicie o serviço de integração se necessário
- Para problemas persistentes na plataforma iFood, contate o suporte do iFood diretamente

---

## Terminal de Pedidos

**Caminho:** Menu Principal > **Terminal de Pedidos**

Interface alternativa para lançamento de pedidos de mesa ou balcão, otimizada para telas sensíveis ao toque.

---

## Romaneio de Entregas

**Caminho:** Menu Principal > **Romaneio**

Organiza as entregas por rota ou entregador.

- Selecione os pedidos a serem entregues
- Associe ao entregador
- Imprima o romaneio de saída
- Ao retornar, registre as entregas realizadas

---

## Programa de Fidelidade (Pedidos)

- Pontos são acumulados automaticamente nas vendas
- Consulta: Caixa > **Ctrl + L**
- Resgate de pontos: disponível na finalização do pedido conforme configuração

---

## Caderneta (Crédito do Cliente)

**Caminho:** Caixa > **F7** (Pagamento de Caderneta)

- Cliente possui saldo de crédito cadastrado
- Pagamentos com caderneta debitam esse saldo
- Administrador pode consultar e recarregar o saldo pela tela de **Caderneta**

# Equipamentos — Catraca (Controle de Acesso)

## O que é

A catraca é um equipamento de controle de acesso utilizado em estabelecimentos como academias, clubes, buffets e refeitórios. Ela libera ou bloqueia a entrada do cliente com base em uma condição definida — no caso dos estabelecimentos integrados ao SAG, essa condição é a **existência de uma comanda aberta e válida**.

Modelos comuns nos estabelecimentos atendidos: **Henry**, **G7 Acesso**, **Teletronic**, **Blantec**, entre outros.

---

## Integração com o SAG

A T4L realiza a **integração entre o SAG e o software da catraca**, permitindo que a catraca consulte as comandas abertas no sistema para liberar ou bloquear o acesso do cliente.

**O que a T4L faz:**
- Configura e mantém a integração entre o SAG e o aplicativo da catraca
- Realiza reparos rápidos de comunicação quando o aplicativo da catraca trava ou para de responder

**O que a T4L NÃO faz:**
- Suporte direto ao equipamento físico da catraca (manutenção, defeitos de hardware, travamento mecânico)
- Configurações internas do software próprio do fabricante da catraca
- Para problemas no equipamento em si, o cliente deve acionar o fornecedor/fabricante da catraca

---

## Problemas Comuns e Como Atender

### Aplicativo da catraca travado / parado / sem resposta

**Sintomas:** A catraca parou de liberar acesso, o aplicativo de integração não responde, clientes presos na entrada.

**Solução:** ESCALAR_SUPORTE — o técnico T4L acessa remotamente e reinicia o serviço de integração.

> Não há ação que o cliente possa realizar por conta própria. Transferir para o suporte sem tentar guiar.

---

### Catraca não libera mesmo com comanda aberta

**Sintomas:** O cliente tem comanda aberta no SAG, mas a catraca não libera a passagem.

**Verificar antes de escalar:**
1. O SAG está aberto e funcionando no servidor?
2. O servidor está ligado e com internet?

- Se o SAG estiver com problema: resolver o problema do SAG primeiro
- Se o SAG estiver ok e a catraca ainda não liberar: ESCALAR_SUPORTE

---

### Problema físico na catraca (travada, barreira quebrada, não gira)

**Sintomas:** A catraca está mecanicamente travada, a barreira não gira ou apresenta defeito físico visível.

**Solução:** Esse tipo de problema é de responsabilidade do **fornecedor/fabricante da catraca** — orientar o cliente a acionar o suporte do fabricante (Henry, G7 Acesso, Teletronic, Blantec, etc.).

> A T4L não realiza manutenção física no equipamento.

---

## Resumo de Encaminhamento

| Situação | Encaminhamento |
|---|---|
| Aplicativo de integração travado/parado | ESCALAR_SUPORTE |
| Catraca não libera com SAG funcionando | ESCALAR_SUPORTE |
| Catraca não libera por problema no SAG | Resolver o SAG primeiro |
| Defeito físico no equipamento | Fabricante da catraca |

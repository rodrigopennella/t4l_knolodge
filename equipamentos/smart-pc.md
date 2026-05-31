# Smart PC — Terminal Android de Comandas

O **Smart PC** é um tablet Android com entradas USB embutidas, fornecido para lançamento de comandas no salão. Os modelos utilizados incluem **Sunmi** e **M10** — todos se referem ao mesmo tipo de equipamento. Ele roda o app **SAG Terminal** e se comunica com o servidor SAG pela rede local (Wi-Fi).

---

## Quando o Smart PC para de comunicar com o SAG

Se o terminal não está enviando ou recebendo dados do SAG, siga esta ordem de verificação:

### 1. Verificar conexão de rede

Alguns terminais usam Wi-Fi, outros rede cabeada — verificar qual o caso antes de orientar.

**Wi-Fi:**
- Acesse **Configurações do Android** > **Wi-Fi**
- Confirme que está conectado à rede do estabelecimento
- Se não estiver: reconectar à rede correta e testar

**Rede cabeada:**
- Verificar se o cabo está bem encaixado no terminal e no switch/roteador
- Se o cabo estiver ok e ainda sem conexão → ESCALAR_SUPORTE

### 2. Verificar Data e Hora

Data/hora incorreta no Android causa falha na comunicação com o banco de dados do SAG.

- Acesse **Configurações do Android** > **Data e Hora** (ou "Gerenciamento Geral" dependendo da versão)
- Confirme que a data e hora estão corretas
- Se estiver errada: corrigir manualmente ou ativar **"Data e hora automáticas"** (sincroniza pela internet)

> **Por que isso importa:** o SAG valida o timestamp das requisições. Se o horário do terminal estiver muito defasado em relação ao servidor, a comunicação é recusada.

### 3. Reiniciar o SAG Mobile

- Feche o **SAG Terminal** completamente (remover da lista de apps recentes)
- Abra novamente
- Testar se a comunicação voltou

---

## Se nenhum dos passos resolver

Escalar para o suporte T4L → **ESCALAR_SUPORTE**

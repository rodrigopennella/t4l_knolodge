# SAG Mobile — Aplicativo para Lançamento de Comandas

Aplicativo Android para lançamento de produtos em comandas diretamente pelo celular ou tablet, sem depender de um terminal fixo.

**Nomes alternativos usados pelos clientes:** aplicativo do celular, app, palmtop, palm, aplicativo para garçom, T.A.

---

## O que é

O SAG Mobile é a versão mobile do terminal de comandas do SAG. Garçons e atendentes podem lançar pedidos diretamente pelo celular ou tablet Android, e os itens são enviados automaticamente para a produção (cozinha/bar) e registrados no sistema.

---

## Plataforma

- **Sistema operacional:** Android exclusivamente
- **iOS (iPhone/iPad):** não suportado
- **Disponível na Google Play Store:** não — o download é feito com orientação da equipe técnica T4L

---

## Download e Instalação

> O aplicativo **não está disponível na Google Play Store**. O download e a configuração inicial devem ser feitos com orientação da equipe técnica T4L.
>
> Clientes que perguntarem onde baixar devem ser direcionados para o suporte técnico: **ESCALAR_SUPORTE**

---

## Requisitos

- Celular ou tablet Android
- Conexão Wi-Fi na mesma rede do servidor SAG
- Servidor SAG ligado e com o sistema aberto

---

## Uso Básico

1. Abrir o aplicativo SAG Mobile no celular/tablet
2. Fazer login com usuário e senha do SAG
3. Selecionar a comanda (ou criar uma nova)
4. Adicionar os produtos do pedido
5. Confirmar — os itens são enviados para a produção automaticamente

---

## Problemas Frequentes

> **Diagnostique primeiro.** Antes de qualquer checklist, pergunte qual a mensagem na tela — ou peça uma foto:
> *"Aparece alguma mensagem na tela? Se puder, me diz o que está escrito ou me manda uma foto."*
> O suporte consegue analisar a foto e identificar o erro na hora. Mensagem específica = causa específica: vá direto ao caso correspondente abaixo, sem percorrer passos genéricos.

### Triagem por mensagem

| Mensagem na tela | Causa | Ação |
|---|---|---|
| "Falha na comunicação com a API" | API (serviço IIS) no servidor não responde | Confirmar servidor ligado + SAG aberto + mesma rede → se persistir, escalar |
| "Comanda inexistente" | API do app desatualizada vs. servidor | Escalar — sem ação do cliente |
| "Falha na conexão" (genérica, sem detalhe) | Conexão local do dispositivo | Checklist abaixo |

### "Falha na comunicação com a API"
- A API do app é um serviço simples no **IIS do servidor**, que mantém os arquivos de comunicação do SAG Mobile. A mensagem aparece quando essa API não responde.
- O cliente **não tem acesso** a esse serviço e não consegue reiniciá-lo.
- Esse erro é do **lado do servidor** — não fique pedindo para checar cabo/Wi-Fi repetidamente.
1. Confirmar que o servidor está ligado e com o SAG aberto
2. Confirmar que o dispositivo está na mesma rede do servidor
3. Se as duas condições estiverem ok e o erro continuar: **ESCALAR_SUPORTE**

### Aplicativo não conecta / "Falha na conexão" (sem mensagem específica)
1. Verificar se o Wi-Fi do celular está ligado e conectado à mesma rede do servidor
2. Verificar se o servidor está ligado e com o SAG aberto
3. Fechar o app e abrir novamente
4. Se persistir: acionar suporte técnico T4L

### Produto não aparece no aplicativo
1. Verificar se o produto está ativo no SAG: Cadastros > Produtos > campo Ativo marcado
2. Fechar e abrir o app para sincronizar
3. Se ainda não aparecer: acionar suporte técnico T4L

### "Comanda inexistente" no aplicativo
- Causa: a versão da API do app pode estar desatualizada em relação ao SAG
- Solução: **ESCALAR_SUPORTE** — não há ação possível pelo cliente

### App parou de funcionar após atualização do SAG
- Causa: atualizações do sistema podem exigir nova versão do app
- Solução: **ESCALAR_SUPORTE** — técnico orienta sobre atualização do aplicativo

### Cliente quer instalar em iPhone / iPad
- O SAG Mobile é exclusivo para Android
- iPhones e iPads não são suportados
- Para dispositivos iOS: **ESCALAR_SUPORTE** para avaliar alternativas

### Cliente quer baixar o app por conta própria
- O app não está na Google Play Store
- O download deve ser feito com orientação da equipe técnica T4L → **ESCALAR_SUPORTE**

---

## Quando Encaminhar para Suporte Técnico

- Solicitação de download ou instalação do aplicativo
- Configuração inicial e vinculação ao servidor
- Problemas de sincronização que não se resolvem com reinicialização do app
- Dispositivo iOS (não suportado)
- App desatualizado após atualização do SAG

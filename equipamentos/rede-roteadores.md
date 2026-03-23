# Equipamentos — Rede e Roteadores

Guia de suporte para infraestrutura de rede em estabelecimentos de food service.

---

## Arquitetura de Rede Típica

```
Internet
    │
  Modem/Roteador do provedor
    │
  Roteador Wi-Fi (doméstico ou empresarial)
    ├── [Cabo] Servidor (computador principal do SAG)
    ├── [Cabo ou Wi-Fi] Caixa 1
    ├── [Cabo ou Wi-Fi] Caixa 2
    ├── [Wi-Fi] Tablet de comandas
    └── [Wi-Fi] Impressora de rede (cozinha)
```

**Recomendação:** o servidor e os caixas principais devem usar cabo de rede (mais estável que Wi-Fi).

---

## Problemas de Conectividade

### SAG não conecta ao servidor

**Causas comuns:**
- Servidor desligado
- Roteador/modem sem energia
- Caixa e servidor em redes diferentes (ranges diferentes)
- IP do servidor mudou (falta de IP fixo)

**Solução:**
1. Verifique se o servidor está ligado
2. Verifique se o roteador está com as luzes normais
3. Reinicie o roteador
4. Aguarde 2-3 minutos
5. Tente conectar novamente

---

### Wi-Fi instável / cai frequentemente

**Causas comuns:**
- Roteador antigo ou sobrecarregado
- Muitos dispositivos conectados
- Distância excessiva entre o roteador e o dispositivo
- Interferência de outros roteadores no mesmo canal

**Solução:**
1. Reinicie o roteador
2. Verifique quantos dispositivos estão conectados (limite do roteador doméstico: ~15-20)
3. Para uso crítico: use cabo de rede em vez de Wi-Fi
4. Se o roteador for muito antigo: substituir por um modelo mais recente
5. Posicionar o roteador em local central e elevado

---

### Tablet perde conexão durante o serviço

1. Verifique a intensidade do sinal Wi-Fi no local do tablet
2. Se o sinal estiver fraco: aproximar o roteador ou adicionar um repetidor
3. Verifique se o tablet está conectando na rede correta (não em rede de vizinho)
4. Reinicie o roteador e o tablet

---

## IP Fixo para o Servidor

O servidor do SAG deve ter um **IP fixo** (estático) na rede para que os caixas e tablets sempre saibam onde encontrá-lo.

### Como verificar se o servidor tem IP fixo
- O IP do servidor não deve mudar quando o roteador é reiniciado
- Configure no roteador o "DHCP Reservation" (reserva de IP) para o MAC address do servidor, ou
- Configure um IP estático diretamente nas configurações de rede do Windows do servidor

> A configuração de IP fixo deve ser feita por técnico responsável. Valores incorretos podem derrubar toda a rede.

---

## Switch (Hub de Rede)

Usado quando há mais dispositivos com fio do que portas no roteador.

**Instalação básica:**
1. Conecte o switch a uma porta do roteador (cabo de rede)
2. Conecte os dispositivos (servidor, caixas) às portas do switch
3. Não requer configuração — funciona automaticamente (plug & play)

**Problemas com switch:**
- Porta com defeito: tente outra porta no switch
- Switch sobreaquecendo: verifique ventilação
- Sem luz indicadora em uma porta: cabo com defeito ou dispositivo desligado

---

## Nobreak (UPS)

Protege o servidor e equipamentos de quedas de energia.

**Recomendação de uso:**
- Conectar o **servidor** ao nobreak (prioridade máxima)
- Conectar o **roteador** ao nobreak (mantém a rede durante queda)
- Impressoras podem ficar fora do nobreak

**Manutenção:**
- A bateria do nobreak tem vida útil de 2-4 anos
- Sinais de bateria fraca: alarme frequente, não sustenta por muito tempo
- Troca de bateria: feita pelo técnico ou fabricante

**Em caso de queda de energia:**
- O nobreak emite um alarme sonoro
- O servidor continua operando pelo tempo de autonomia da bateria
- Salve o que for necessário e encerre o servidor antes da bateria acabar

---

## Roteadores Wi-Fi Domésticos

Equipamentos comuns nos estabelecimentos atendidos.

**Limitações do roteador doméstico:**
- Número máximo de dispositivos: ~15-20
- Alcance: até 30-50m sem obstáculos
- Não é indicado para ambientes com muitas paredes ou andares diferentes

**Quando recomendar substituição:**
- Wi-Fi cai constantemente mesmo após reinicializações
- Muitos dispositivos conectados e rede lenta
- Equipamento com mais de 4-5 anos
- Estabelecimento com mais de uma área de atendimento

---

## Checklist de Rede para Novos Estabelecimentos

- [ ] Servidor com IP fixo (reserva no roteador)
- [ ] Servidor conectado por cabo ao roteador/switch
- [ ] Caixas principais com cabo de rede
- [ ] Roteador em local central e elevado
- [ ] Nobreak protegendo servidor e roteador
- [ ] Rede separada para clientes (se oferecer Wi-Fi aos consumidores)
- [ ] Todas as impressoras configuradas e testadas no SAG
- [ ] Tablets sincronizando corretamente com o servidor

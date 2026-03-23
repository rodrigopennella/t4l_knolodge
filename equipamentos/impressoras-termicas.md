# Equipamentos — Impressoras Térmicas

Guia de suporte para impressoras térmicas usadas em estabelecimentos de food service.

---

## Tipos de Uso

| Uso | Descrição |
|---|---|
| Cupom do cliente | Impressora no caixa — imprime o cupom/nota do consumidor |
| Produção / Cozinha | Impressora na cozinha — imprime os pedidos para preparo |
| Balcão / Bar | Impressora no balcão — imprime pedidos de bebidas/lanches |
| Etiqueta | Impressora de etiquetas para peso ou embalagem |

---

## Conexão com o SAG

As impressoras podem ser conectadas de duas formas:

### USB
- Cabo USB conectado diretamente ao computador
- Aparece como impressora no Windows
- Configurada no SAG por nome de dispositivo ou porta

### Rede (TCP/IP)
- Impressora conectada ao Wi-Fi ou cabo de rede
- Configurada no SAG pelo endereço IP da impressora
- Recomendada para impressoras de cozinha distantes do caixa

---

## Configuração no SAG

**Caminho:** Configurações > **Impressoras**

1. Clique em **Nova**
2. Informe o nome (ex: "Cozinha", "Caixa 1")
3. Selecione o tipo de conexão (USB ou Rede)
4. Informe a porta (USB) ou IP (Rede)
5. Clique em **Testar**
6. Salve

**Regras de Impressão:**
- **Caminho:** Configurações > **Regras de Impressão**
- Associa grupos/categorias de produtos a impressoras específicas

---

## Problemas Frequentes e Soluções

### Impressora não imprime nada
1. Verifique se está ligada (luz acesa)
2. Abra e feche a tampa do papel
3. Desconecte e reconecte o cabo USB (tente outra porta)
4. Reinicie a impressora
5. No SAG, acesse Configurações > Impressoras > **Testar**

### Impressão em branco (papel sai sem texto)
- O papel térmico foi colocado ao contrário
- O lado sensível ao calor deve ficar voltado para baixo (face interna do rolo)
- Retire o papel, vire e recoloque

### Impressão cortada ou incompleta
- O papel pode ter acabado no meio da impressão
- Verifique e reponha o papel
- Se papel está cheio e o problema persiste, pode ser entupimento ou sujeira no cabeçote

### Impressora desliga sozinha durante uso
- Provável problema na fonte de alimentação
- Verifique o cabo de energia e tente outra tomada
- Se persistir, a fonte precisa ser trocada

### Pedido saindo na impressora errada
- Verifique as **Regras de Impressão** no SAG
- O produto pode estar no grupo/categoria incorreto
- Veja: **Configurações > Regras de Impressão**

### Muitas vias sendo impressas
- Acesse: **Configurações > Regras de Impressão**
- Ajuste o campo **Número de Vias** para 1

---

## Teste de Impressão Manual

Para testar a impressora independente do SAG:

1. Desligue a impressora
2. Pressione e segure o botão de alimentação de papel
3. Ligue a impressora mantendo o botão pressionado
4. Solte quando começar a imprimir
5. Uma página de teste com configurações será impressa

---

## Manutenção Preventiva

- **Limpeza do cabeçote:** use cotonete com álcool isopropílico levemente umedecido. Passe suavemente no cabeçote térmico (barra metálica que toca o papel). Faça quando a impressão ficar fraca ou manchada.
- **Troca de papel:** sempre usar papel térmico de qualidade (80mm x 80mm é o padrão mais comum)
- **Limpeza externa:** use pano seco ou levemente umedecido — evite líquidos na entrada de papel

---

## Especificações Comuns

| Parâmetro | Valor Típico |
|---|---|
| Largura do papel | 80mm (mais comum) ou 58mm |
| Diâmetro máximo do rolo | 80mm |
| Conexão | USB + Ethernet (dupla) |
| Velocidade | 150-250mm/s |
| Temperatura de armazenamento do papel | Ambiente seco, longe de calor e luz solar |

---

## Quando Encaminhar para Manutenção

- Cabeçote com risco ou dano físico
- Fonte defeituosa (desliga durante operação)
- Motor de papel não avança
- Conector USB danificado
- Impressão sempre com faixas brancas mesmo após limpeza

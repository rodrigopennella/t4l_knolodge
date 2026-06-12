# Procedimentos Padrão de Suporte

Passo a passo para as situações mais frequentes no atendimento.

---

## PROC-01: Impressora Não Imprime

1. Pergunte: a impressora está ligada? (luz acesa)
2. Peça para abrir e fechar a tampa do papel
3. Peça para desconectar o cabo USB e reconectar em **outra porta USB**
4. Peça para reiniciar a impressora (desligar pelo cabo/botão e religar)
5. Se não funcionar: verificar se o cabo USB está com defeito (trocar cabo)
6. Se ainda não funcionar: testar a impressora em outro computador para isolar o problema
7. Se problema confirmado no hardware: encaminhar para manutenção
8. Se hardware OK e ainda não imprime: **acionar suporte técnico T4L** para verificar configuração no SAG

---

## PROC-02: Caixa Sem Conexão ao Servidor

> A T4L gerencia modem, roteador, switches e cabeamento na maioria dos estabelecimentos. Orientar os passos básicos abaixo e, se não resolver, escalar para o suporte.

1. Pergunte: o computador servidor está ligado? (verifique fisicamente)
2. Há internet no estabelecimento? (testar abrindo um site no celular)
   - **Sem internet em nenhum dispositivo:** orientar o cliente a ligar para a operadora
   - **Com internet:** prosseguir
3. É acesso interno ou externo ao estabelecimento?
   - Se **externo** (fora do estabelecimento): ESCALAR_SUPORTE (porta 3306 ou DDNS)
   - Se **interno:** prosseguir
4. Só esse computador ou todos estão sem conexão?
   - **Todos:** ESCALAR_SUPORTE imediatamente (pode ser banco de dados ou servidor)
   - **Só um:** prosseguir
5. Verificar se o roteador/modem está com as luzes normais
6. Verificar se o cabo de rede está bem conectado nas duas pontas (no caixa e no roteador/switch)
7. Reiniciar o roteador (desligar da tomada, aguardar 30s, religar) e aguardar 2 minutos
8. Se não resolver: ESCALAR_SUPORTE

---

## PROC-03: Não Consegue Emitir NFC-e

1. Pergunte: já emitia antes ou nunca funcionou?
2. Se nunca funcionou: verificar com a contabilidade se as credenciais foram geradas
3. Acesse **NFC-e** no menu do SAG
4. Se aparecer **Validar Online**: clicar
5. Feche o SAG completamente e abra novamente
6. Teste com uma venda
7. Se erro mencionar produto específico: verificar **Cadastros > Produtos > aba Impostos > CST e CFOP**
8. Se persistir: acessar remotamente via AnyDesk para diagnóstico

---

## PROC-04: Cliente Quer Enviar XML para a Contabilidade

1. Acesse: **Outros > Ferramentas CFe > Arquivos XML**
2. Defina o período (ex: mês anterior)
3. Marque: **Gerar CF-e Cancelados** (se solicitado)
4. Marque: **Compactar em arquivo único**
5. Marque: **Enviar por e-mail**
6. Informe o e-mail do destino
7. Clique em **Gerar**
8. Confirme que o e-mail foi recebido

---

## PROC-05: Criar Novo Usuário no SAG

1. Acesse: **Outros > Central de Usuários**
2. Clique em **Novo**
3. Preencha:
   - **Login:** nome de acesso (sem espaços, sem acento)
   - **Senha:** senha inicial (avisar o usuário para trocar depois)
4. Selecione o **Grupo de Permissão** adequado (Caixa, Gerente, Admin)
5. Clique em **Salvar**
6. Teste o login com o novo usuário

---

## PROC-06: Reconfigurar Regra de Impressão

> Regras de impressão são configuradas exclusivamente pela equipe técnica T4L via Config. Terminal. O cliente não acessa essas configurações.

1. Acionar acesso remoto (AnyDesk) ao servidor do cliente
2. No SAG: Config. Terminal > Impressoras
3. Identificar o grupo/categoria com problema
4. Selecionar a impressora correta no campo correspondente
5. Ajustar o número de vias (normalmente 1)
6. Salvar
7. Pedir ao cliente para lançar um produto daquela categoria para testar

---

## PROC-07: Produto Inativo Travando Pedido no Tablet

1. No SAG: **Cadastros > Produtos**
2. Pesquise o produto em questão
3. Marque o campo **Ativo**
4. Salve
5. No tablet: feche e abra o app
6. Aguarde a sincronização
7. Confirme que o pedido pode ser finalizado

---

## PROC-08: Tablet Não Está Sincronizando

1. Verifique se o Wi-Fi do tablet está conectado na rede do estabelecimento
2. Pergunte: o servidor está ligado e com SAG aberto?
3. Feche o app no tablet e abra novamente
4. Se não resolver: verifique se o IP do servidor foi alterado
5. Nas configurações do app, verifique o endereço do servidor
6. Se o IP mudou: atualize o endereço do servidor no app
7. Teste novamente

---

## PROC-09: Restaurar Backup do Banco de Dados

> **Atenção:** este procedimento apaga dados posteriores ao backup. Confirmar com o cliente antes.

1. Identificar o arquivo de backup mais recente na pasta de backups do servidor
2. Fechar SAG em todas as máquinas
3. Parar o serviço de banco de dados
4. Restaurar o backup
5. Iniciar o serviço de banco de dados
6. Abrir SAG no servidor para verificar
7. Liberar os demais caixas

---

## PROC-10: Acesso Remoto via AnyDesk

1. Peça ao cliente para abrir o **AnyDesk** no computador com problema
2. Solicite o número de 9 dígitos exibido na tela ("Seu Endereço")
3. Conecte usando esse número
4. O cliente deve aceitar a conexão na tela dele
5. Após resolver: feche a conexão
6. Informe ao cliente o que foi feito e como evitar o problema novamente

---

## PROC-11: Verificar Fechamento de Caixa com Erro

1. Verifique se há vendas em aberto (não finalizadas): F10 > consultar vendas pendentes
2. Verifique se há NFC-e pendente de transmissão
3. Verifique se o servidor tem acesso à internet (necessário para transmitir notas)
4. Se houver erro específico: anote a mensagem de erro completa
5. Tente fechar em outro caixa temporariamente
6. Se necessário, acesse remotamente via AnyDesk para diagnóstico

---

## PROC-13: Aplicar Certificado Digital no SAG

> O próprio cliente consegue seguir este procedimento. Só acionar suporte se houver muita dificuldade.

1. Ter em mãos o arquivo `.pfx` (fornecido pela certificadora ou contabilidade)
2. Abrir o SAG em qualquer computador que tenha o sistema instalado
3. Acessar **Outros > Certificado Digital**
4. Selecionar tipo **A1**
5. Clicar em buscar arquivo → selecionar o `.pfx`
6. Inserir a **senha do certificado**
7. Clicar em **Salvar**
8. Fechar e reabrir o SAG
9. Testar emissão de NFC-e

**Observações:**
- Se a senha estiver errada: confirmar com quem gerou o certificado (certificadora ou contabilidade)
- Se NFC-e ainda não emitir após aplicar: verificar se as credenciais (CSC/ID Token) estão preenchidas no menu NFC-e
- Se o cliente não conseguir após seguir os passos: transferir para o suporte

---

## PROC-14: Renovar ou Adquirir Novo Certificado Digital

> Use este procedimento quando o cliente precisa **renovar** um certificado vencido/prestes a vencer, ou **adquirir** o primeiro certificado. O SAG tem um botão direto que encaminha para o site da autoridade certificadora parceira (CertBr).

### Passo 1 — Verificar a situação atual no SAG

1. Acessar **Outros > Certificado Digital**
2. A tela mostrará o status do certificado atual:
   - **Certificado configurado**: exibe validade e tipo (A1 Arquivo)
   - Dois botões disponíveis: **Trocar Certificado** e **Adquirir Novo Certificado**

### Passo 2 — Solicitar o novo certificado

3. Clicar em **Adquirir Novo Certificado**
4. O SAG abrirá o navegador no site da **CertBr** (`certbr.gfsis.com.br`) — parceira da T4L
5. No site, preencher:
   - **Tipo:** E-CNPJ (pessoa jurídica) ou E-CPF (pessoa física)
   - **Tipo de mídia:** Sem Mídia (para A1 — arquivo digital, sem token USB)
   - **Validade:** 1 ano ou 2 anos
6. Clicar em **Próximo** e preencher o cadastro e pagamento
7. Após confirmação, a CertBr entrará em contato para agendar o atendimento por **videoconferência**

> **Requisito para videoconferência:** o cliente precisa ter CNH válida **ou** já ter feito um certificado digital anteriormente. Em caso de dúvidas: (37) 98840-5093 | contato@certbr.com | Formiga — Rua Silviano Brandão, 55 3º andar, Centro

### Passo 3 — Aplicar o certificado recebido

8. Após receber o arquivo `.pfx` da CertBr, seguir o **PROC-13** para aplicar no SAG

**Observações:**
- O botão "Trocar Certificado" faz o mesmo que aplicar um `.pfx` já em mãos (substitui o atual)
- Não oriente o cliente a contatar a contabilidade para renovar — o caminho correto é o botão no SAG que já aponta para a CertBr

---

## PROC-12: Cliente com Divergência no Relatório de Caixa

1. Pergunte o período com divergência
2. Acesse: **Relatórios > Consultas** — filtre pelo período exato
3. Compare com o relatório de **Cupons Emitidos**
4. Verifique se há cancelamentos não computados
5. Gere o relatório por **Forma de Pagamento** para detalhar
6. Compare com extrato bancário se for divergência de cartão/PIX
7. Se houver cancelamento indevido: verifique relatório de **Itens Cancelados** com responsável

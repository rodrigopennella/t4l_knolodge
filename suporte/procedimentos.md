# Procedimentos Padrão de Suporte

Passo a passo para as situações mais frequentes no atendimento.

---

## PROC-01: Impressora Não Imprime

1. Pergunte: a impressora está ligada? (luz acesa)
2. Peça para abrir e fechar a tampa do papel
3. Peça para desconectar o cabo USB e reconectar em **outra porta USB**
4. Peça para reiniciar a impressora (desligar pelo cabo/botão e religar)
5. No SAG: **Configurações > Impressoras > Testar**
6. Se não funcionar: verificar se o cabo USB está com defeito (trocar cabo)
7. Se ainda não funcionar: testar a impressora em outro computador para isolar o problema
8. Problema confirmado no hardware: encaminhar para manutenção

---

## PROC-02: Caixa Sem Conexão ao Servidor

1. Pergunte: o computador servidor está ligado? (verifique fisicamente)
2. O modem/roteador está com as luzes normais?
3. Peça para reiniciar o roteador (desligar da tomada, aguardar 30s, religar)
4. Aguarde 2 minutos e teste novamente
5. Se não resolver: reinicie o servidor
6. Aguarde 3-5 minutos e teste
7. Se ainda sem conexão: verifique se caixa e servidor estão na mesma rede

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

1. Acesse: **Usuários** (ou **Configurações > Usuários**)
2. Clique em **Novo**
3. Preencha:
   - **Login:** nome de acesso (sem espaços, sem acento)
   - **Senha:** senha inicial (avisar o usuário para trocar depois)
4. Selecione o **Grupo de Permissão** adequado (Caixa, Gerente, Admin)
5. Clique em **Salvar**
6. Teste o login com o novo usuário

---

## PROC-06: Reconfigurar Regra de Impressão

1. Acesse: **Configurações > Regras de Impressão**
2. Identifique o grupo/categoria com problema
3. Selecione a impressora correta no campo correspondente
4. Ajuste o número de vias (normalmente 1)
5. Salve
6. Peça ao cliente para lançar um produto daquela categoria para testar
7. Confirme se saiu na impressora correta e com a quantidade de vias correta

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

> Executado pelo técnico T4L via AnyDesk ou com o cliente acompanhando.

1. Receber o arquivo `.pfx` do cliente (via e-mail ou WhatsApp)
2. No computador **servidor**, abrir o SAG
3. Acessar **Outros > Certificado Digital**
4. Selecionar tipo **A1**
5. Clicar em buscar arquivo → selecionar o `.pfx` recebido
6. Inserir a **senha do certificado** (fornecida pelo cliente ou pela certificadora)
7. Clicar em **Salvar**
8. Fechar e reabrir o SAG
9. Testar emissão de NFC-e com uma venda de teste

**Observações:**
- Se a senha estiver errada: confirmar com o cliente ou com quem gerou o certificado
- Se NFC-e ainda não emitir após aplicar: verificar se as credenciais (CSC/ID Token) estão preenchidas no menu NFC-e
- Certificado deve ser aplicado **apenas no servidor**, não nos caixas

---

## PROC-12: Cliente com Divergência no Relatório de Caixa

1. Pergunte o período com divergência
2. Acesse: **Relatórios > Consultas** — filtre pelo período exato
3. Compare com o relatório de **Cupons Emitidos**
4. Verifique se há cancelamentos não computados
5. Gere o relatório por **Forma de Pagamento** para detalhar
6. Compare com extrato bancário se for divergência de cartão/PIX
7. Se houver cancelamento indevido: verifique relatório de **Itens Cancelados** com responsável

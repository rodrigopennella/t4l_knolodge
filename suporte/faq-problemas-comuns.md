# FAQ — Problemas Mais Comuns

Baseado em 6 meses de histórico de atendimentos de suporte.

---

## 1. Impressora Não Imprime

**Sintomas:** Pedidos não saem na impressora, cupom em branco, sem resposta.

**Solução:**
1. Verifique se a impressora está ligada (luz indicadora acesa)
2. Abra e feche a tampa do papel
3. Desconecte e reconecte o cabo USB
4. Tente outra porta USB do computador
5. Reinicie a impressora (desligue e religue)
6. No SAG, envie um teste de impressão: **Configurações > Impressoras > Testar**
7. Se nada funcionar, pode ser problema no hardware da impressora

> Se a impressora está imprimindo em uma posição errada (ex: café saindo na cozinha), veja [Regras de Impressão](../SAG/configuracoes.md#regras-de-impressão).

---

## 2. "Erro ao Tentar Logar" / "Falha de Acesso ao Servidor" / Caixa Offline

**Sintomas:** SAG não abre, tela de carregamento infinita, "sem conexão com o servidor", "erro ao tentar logar".

**Primeiro perguntar: só esse computador ou todos estão com problema?**

**Apenas um computador:**
1. Verifique se há internet nesse computador
2. É acesso **interno** (dentro do estabelecimento) ou **externo** (de outro local)?
   - Se **externo**: a porta 3306 pode ter fechado no modem → acionar suporte
   - Se **interno**: verifique se está abrindo o SAG correto (existem dois aplicativos: interno e externo — são diferentes)
3. Reinicie o roteador (desligar 30s, religar) e aguarde 2 minutos
4. Se persistir: acionar suporte

**Todos os computadores ao mesmo tempo ("sistema parado"):**
- Acionar suporte imediatamente — pode ser falha no banco de dados ou servidor desligado

---

## 3. SAG Lento / Travando

**Sintomas:** Sistema demora para responder, trava ao abrir telas.

**Solução:**
1. Feche a tela de **Consulta de Produtos** se estiver aberta em segundo plano
2. Feche outras aplicações abertas no computador
3. Reinicie o computador
4. Abra o SAG novamente
5. Se o problema for frequente, o computador pode precisar de upgrade de hardware (RAM)

---

## 4. Erro ao Fazer Login

**Sintomas:** "Usuário ou senha incorretos", acesso negado.

**Solução:**
1. Confirme login e senha com o administrador do sistema
2. Feche o SAG completamente
3. Aguarde alguns segundos e abra novamente
4. Tente novamente com as credenciais corretas
5. Se necessário, o administrador redefine a senha em: **Usuários > selecione o usuário > altere a senha**

---

## 5. NFC-e Não Emite / Erro Fiscal

**Sintomas:** "Sem configuração NFC-e", erro ao efetivar conta, nota não sai.

**Solução:**
1. Acesse: **Menu NFC-e** no SAG
2. Verifique se as credenciais estão configuradas (consulte a contabilidade se não estiverem)
3. Se aparecer o botão **Validar Online**, clique nele
4. Feche o SAG completamente e abra novamente
5. Tente emitir novamente
6. Se erro for "produto sem configuração fiscal": acesse **Cadastros > Produtos > aba Impostos NFE/NFCE** e corrija o CST e CFOP

---

## 6. PIX / Cartão Não Passa

**Sintomas:** TEF com erro, pinpad não responde, pagamento estorna sozinho.

**Solução:**
1. Desconecte o pinpad e reconecte em outra porta USB
2. Reinicie o SAG
3. Faça um teste com uma venda pequena
4. Se continuar com erro, verifique se o TEF está configurado corretamente
5. Verifique se NFC-e está habilitado no caixa (pode estar causando conflito)

---

## 7. Tablet / Celular Não Sincroniza

**Sintomas:** Produtos não aparecem no app, pedidos não chegam ao caixa.

**Solução:**
1. Feche o app no tablet/celular e abra novamente
2. Verifique se o tablet está na mesma rede Wi-Fi do servidor
3. Verifique se o servidor está ligado e com o SAG aberto
4. Se produtos não aparecem: verifique se o produto está ativo no SAG (**Cadastros > Produtos > Ativo = marcado**)
5. Sincronize manualmente: dentro do app, acesse as configurações e force a sincronização

---

## 8. Produto Inativo Causando Travamento

**Sintomas:** Pedido do tablet fica pendente e não finaliza, lançamento trava.

**Solução:**
1. No SAG, acesse **Cadastros > Produtos**
2. Localize o produto com problema
3. Marque a opção **Ativo**
4. Salve
5. Sincronize o tablet novamente

---

## 9. Impressora Imprimindo Muitas Vias / Pedido Saindo na Impressora Errada

**Sintomas:** Saindo 2 ou 3 vias quando deveria ser 1, ou pedido imprimindo na impressora incorreta.

**Solução:** Acionar suporte — a configuração de número de vias e regras de impressão fica em Config. Terminal, que é de acesso exclusivo dos técnicos T4L.

---

## 10. Pedidos do iFood (ou Outra Plataforma) Não Chegam no SAG

**Sintomas:** Pedido feito na plataforma não aparece no SAG ou não imprime.

**Fluxo correto de integração:**
Plataforma envia pedido → pedido integra → aparece em **Delivery > Consulta de Pedidos** → então imprime

**Diagnóstico:**
1. Verificar em **Delivery > Consulta de Pedidos** se o pedido aparece
2. Se **não aparece**: problema de integração → acionar suporte (configuração de integração é restrita a técnicos)
3. Se **aparece mas não imprime**: problema de impressora → seguir procedimento de impressora
4. Verificar também: servidor com internet e SAG aberto no servidor

---

## 11. Relatório com Valores Divergentes

**Sintomas:** Relatório do SAG não bate com extrato fiscal ou caixa.

**Solução:**
1. Acesse: **Relatórios > Consultas**, filtre pelo período exato
2. Compare com o relatório SAT/NFC-e separadamente
3. Para verificação cupom a cupom: **Relatórios > Cupons Emitidos**
4. Gere o XML do período: **Outros > Ferramentas CFe > Arquivos XML**
5. Se houver diferença de CNPJ, filtre por estabelecimento separadamente

---

## 12. Comanda Não Carrega / Vazia

**Sintomas:** Comanda abre vazia, não aparece os itens lançados.

**Solução:**
1. Feche o SAG e abra novamente
2. Acesse a comanda novamente via **F4**
3. Se o problema persistir, pode ser corrupção de dados — contate o suporte

---

## 13. Não Consegue Fechar o Caixa

**Sintomas:** Erro ao tentar fazer fechamento, caixa não fecha.

**Solução:**
1. Verifique se há vendas abertas (não finalizadas)
2. Verifique se há NFC-e pendente de transmissão
3. Verifique se o servidor está com internet (necessário para transmitir notas pendentes)
4. Tente fechar de outro caixa temporariamente
5. Contate o suporte se o erro persistir com mensagem de erro específica

---

## 14. Servidor Caiu / Banco de Dados Offline

**Sintomas:** Todos os caixas perdem conexão simultaneamente.

**Solução:**
1. Verifique se o computador servidor está ligado
2. Reinicie o servidor
3. Aguarde 3-5 minutos para o banco de dados subir completamente
4. Teste a conexão de um caixa
5. Se o banco de dados não subir, contate o suporte imediatamente — pode ser necessário restaurar backup

---

## 15. Wi-Fi Caindo / Instável

**Sintomas:** Conexão cai com frequência, tablets ficam offline.

**Solução:**
1. Reinicie o roteador (desligue da tomada, aguarde 30s, religue)
2. Verifique se o servidor tem IP fixo na rede (importante para estabilidade)
3. Se muitos dispositivos na rede: considere um roteador com maior capacidade
4. Para dispositivos críticos (caixa principal): use cabo de rede ao invés de Wi-Fi
5. Se problema persistir, contate o provedor de internet

---

## 16. SAG Não Abre / Trava na Inicialização

**Sintomas:** Tela de carregamento não passa, SAG fecha sozinho ao abrir.

**Solução:**
1. Reinicie o computador
2. Verifique se o servidor está ligado antes de abrir o SAG
3. Certifique-se que o SAG está atualizado na versão mais recente
4. Verifique se há espaço em disco no computador
5. Contate o suporte se o erro persistir

---

## 17. Erro de Permissão / "Sem Acesso"

**Sintomas:** Usuário tenta acessar uma função e recebe mensagem de "sem permissão".

**Solução:**
1. O administrador deve acessar: **Usuários > Grupos de Permissão**
2. Selecione o grupo do usuário
3. Habilite a permissão necessária
4. O usuário deve fazer logout e login novamente para as permissões serem aplicadas

---

## 18. Produto Não Aparece no Caixa

**Sintomas:** Produto cadastrado não aparece na busca do caixa.

**Solução:**
1. Verifique se o produto está **Ativo**: **Cadastros > Produtos > campo Ativo marcado**
2. Verifique se o produto tem **preço de venda** cadastrado
3. Verifique se o produto está vinculado ao **grupo correto**
4. Salve o produto e tente novamente no caixa

---

## 19. Impressora Desliga Sozinha

**Sintomas:** Impressora apaga a luz e para de funcionar durante o uso.

**Solução:**
1. Pode ser problema na fonte de alimentação da impressora
2. Verifique o cabo de energia e tente outra tomada
3. Se o problema persistir, a fonte provavelmente precisa ser trocada
4. Contate o suporte para avaliação do hardware

---

## 20. Não Consegue Emitir Relatório Fiscal para Contabilidade

**Sintomas:** Contador solicita XML, não sabe como gerar.

**Solução:**
1. Acesse: **Outros > Ferramentas CFe > Arquivos XML**
2. Defina o período (mês de referência)
3. Marque: **Compactar em arquivo único**
4. Marque: **Enviar por e-mail**
5. Informe o e-mail do contador
6. Clique em **Gerar**
7. O arquivo ZIP com os XMLs será enviado automaticamente

---

## 21. SAG Pede Atualização ao Abrir / Tela de Login Diferente

**Sintomas:** Ao abrir o SAG e fazer login, aparece aviso pedindo para atualizar o sistema.

**Causa:** O banco de dados foi atualizado (pelo suporte T4L), mas o SAG estava aberto naquela máquina durante a atualização e ainda está na versão antiga.

**Solução:**
1. Feche o SAG completamente
2. Abra o SAG novamente
3. Faça o login normalmente
4. Quando aparecer a solicitação de atualização, clique em **Atualizar**
5. Aguarde a atualização concluir
6. O SAG abrirá normalmente na nova versão

---

## 22. "Obrigatório adicionar um Grupo de Imposto" ao Cadastrar Produto

**Sintomas:** Ao salvar um produto, aparece mensagem de erro sobre Grupo de Imposto obrigatório.

**Causa:** A partir da versão **25.10** do SAG, todos os produtos exigem um grupo de imposto configurado.

**Solução:**
1. No cadastro do produto, acesse a aba **Impostos**
2. Na seção **Grupo de Imposto**, pesquise e selecione o grupo correspondente no campo de busca
3. Para ver ou editar o conteúdo do grupo, clique em **Editar**
4. Salve o produto (botão **Alterar**)

> **Qual grupo de imposto usar?** Depende do tipo de produto e do regime tributário do estabelecimento. Em caso de dúvida, consulte a **contabilidade** do cliente.

---

## 23. Data/Hora Desincronizada no Tablet Após Queda de Energia

**Sintomas:** Terminal de comandas (tablet Sunmi, M10 ou similar) para de comunicar com o sistema após queda de energia. Pedidos não chegam, app trava ou não sincroniza.

**Causa:** Tablets Android perdem a configuração de data e hora após queda de energia, e sem a hora correta a comunicação com o banco de dados para.

**Solução:**
1. No tablet, acesse **Configurações > Data e hora**
2. Corrija a data e hora para os valores atuais
3. Feche e abra o aplicativo no tablet
4. A comunicação com o sistema voltará automaticamente

---

## 24. Acesso Externo ao SAG Não Funciona ("Falha na conexão com o servidor")

**Sintomas:** O SAG não abre em um computador fora do estabelecimento (acesso remoto/externo), mesmo com o servidor funcionando normalmente para os outros caixas locais.

**Causa:** O acesso externo ao SAG funciona via abertura da **porta 3306** no modem + DDNS gerenciado pela T4L (ou VPN). Se essa porta foi fechada, o acesso externo para de funcionar.

**Solução:** Escalar para o suporte T4L — o técnico reconfigura o encaminhamento de porta (port forwarding) no modem do estabelecimento.

> Esse problema não tem solução pelo lado do cliente. Acionar suporte.

---

## 28. "Cupom de Desconto Indisponível para Uso!"

**Sintomas:** Mensagem de aviso ao tentar usar cupom de desconto no caixa.

**Causa:** O cupom atingiu o limite de usos cadastrado ou não existe no sistema.

**Solução:**
1. Acesse **Cadastros > Cupom de Desconto**
2. Localize o cupom utilizado
3. Verifique se está **ativo** e se ainda há **usos disponíveis**
4. Se necessário, aumente o limite de usos ou cadastre um novo cupom

---

## 26. Erro de Rejeição Fiscal na NFC-e ou NF-e (ICMS ST, CST, CFOP)

**Sintomas:** Mensagens como "Rejeição: BC ICMS ST difere da somatória dos itens", "Produto sem configuração fiscal", ou outros erros da SEFAZ ao emitir nota.

**Solução:**
1. Identifique o produto que está causando o erro (normalmente a mensagem indica o item)
2. Acesse **Cadastros > Produtos** > selecione o produto
3. Vá até a aba **Impostos NFE/NFCE**
4. Verifique se os campos **CST** e **CFOP** estão preenchidos corretamente
5. Em caso de dúvida sobre os valores corretos, consulte a **contabilidade**
6. Salve e tente emitir novamente

> Se o erro persistir após verificar e corrigir os impostos, transferir para o suporte — pode envolver configuração fiscal específica da SEFAZ do estado.

---

## 27. Erro no Romaneio: "O Total das Faturas Não Pode ser Diferente do Total do Pedido"

**Sintomas:** Ao tentar salvar ou alterar um pedido no módulo Romaneio, aparece mensagem de erro sobre divergência entre total do pedido e total das faturas.

**Causa:** As faturas vinculadas ao pedido estão com valores desatualizados em relação ao total do pedido (comum após alteração de itens, descontos ou datas).

**Solução:**
1. Na tela do pedido, clique em **Gerar Faturas** novamente
2. O sistema recalcula e atualiza os valores das faturas para bater com o total do pedido
3. Finalize o pedido normalmente

> Se o erro persistir após Gerar Faturas, transferir para o suporte.

---

## 25. "Comanda Inexistente" no App (Celular/Tablet)

**Sintomas:** Ao tentar lançar produtos pelo app no celular ou tablet, aparece erro "Comanda inexistente" mesmo para comandas que existem no sistema.

**Causa:** A API do aplicativo não foi atualizada automaticamente junto com uma atualização do sistema SAG. Há incompatibilidade de versão entre o app e o servidor.

**Solução:** Escalar para o suporte T4L — o técnico realiza a atualização da API. Não há ação do lado do cliente.

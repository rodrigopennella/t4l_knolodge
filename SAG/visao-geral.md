# SAG — Visão Geral do Sistema

O SAG é um sistema de PDV (Ponto de Venda) desenvolvido para estabelecimentos de food service como padarias, restaurantes, mercados e lanchonetes.

---

## Estrutura de Módulos

```
SISTEMA SAG
├── Caixa (Frente de Caixa)
├── Terminal de Comandas
├── Pedidos / Delivery
├── Estoque
├── Financeiro
├── Relatórios
├── Configurações
├── Usuários
├── Cadastros
│   ├── Clientes
│   ├── Fornecedores
│   ├── Funcionários
│   ├── Produtos
│   └── Estabelecimentos
├── Operacional
│   ├── Comandas / Mesas
│   ├── Produção
│   ├── Romaneio
│   └── Caderneta
└── Integrações
    ├── NF-e / NFC-e
    ├── TEF / SiTef
    ├── Multiloja
    └── Automatizador
```

---

## Tela Principal

Ao abrir o SAG, o usuário vê o **Dashboard Principal** com tiles (botões de módulo). Os módulos disponíveis dependem da licença e das permissões do usuário logado.

### Login
- Campo: **Usuário**
- Campo: **Senha**
- Após login, o menu superior exibe: **Alterar Senha** e **Sair**

---

## Atalhos de Teclado Globais (Frente de Caixa)

| Tecla | Função |
|---|---|
| F1 | Outras Funções |
| F3 | Iniciar Venda |
| F4 | Consulta de Comandas |
| F5 | Cancelar Item |
| F6 | Cancelar Venda |
| F7 | Pagamento de Caderneta |
| F8 | Consulta de Pedidos |
| F9 | Consulta de Produtos |
| F10 | Últimas Vendas |
| F11 | Entradas e Saídas |
| F12 | Finalizar Caixa |
| Ctrl + E | Venda em Espera |
| Ctrl + D | Desconto no Item |
| Ctrl + - | Desconto na Venda |
| Ctrl + U | Última Venda |
| Ctrl + F | Inserir Comanda Parcial |
| Ctrl + L | Extrato Prog. Fidelidade |

---

## Arquitetura Geral

- **Servidor:** computador central que hospeda o banco de dados. Todos os caixas e tablets se conectam a ele.
- **Caixas:** estações que rodam o SAG conectadas ao servidor pela rede local.
- **Tablets/Celulares:** usam o app SAG para lançar pedidos e comandas, sincronizando com o servidor.
- **Acesso remoto:** via AnyDesk, o suporte pode acessar o computador do cliente remotamente.

---

## Tipos de Estabelecimento Atendidos

| Tipo | Funcionalidades Mais Usadas |
|---|---|
| Padaria | Caixa, Balança, Produção, Caderneta |
| Restaurante | Comandas, Mesas, Produção, Relatórios |
| Pizzaria | Cadastro de Pizza, Acompanhamentos, Comandas |
| Mercado | Caixa, Estoque, NFC-e, Balança |
| Lanchonete | Caixa, Pedidos, Totem de Auto-Atendimento |
| Delivery | Pedidos, iFood, Romaneio |

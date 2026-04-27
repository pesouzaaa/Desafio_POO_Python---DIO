# 🏦 Sistema Bancário — Python OOP
 
Sistema bancário orientado a objetos desenvolvido em Python, com suporte a múltiplos clientes, contas correntes, depósitos, saques e extrato de transações.
 
---
 
## 📋 Descrição
 
Este projeto simula as operações básicas de um banco utilizando os princípios da **Programação Orientada a Objetos (POO)**. O sistema permite cadastrar clientes (pessoa física), criar contas correntes vinculadas a eles e realizar transações financeiras com controle de histórico.
 
O código é estruturado com classes abstratas, herança e encapsulamento, seguindo boas práticas de design com Python.
 
---
 
## 🚀 Funcionalidades
 
| Opção | Funcionalidade              |
|-------|-----------------------------|
| `d`   | Depositar valor na conta     |
| `s`   | Sacar valor da conta         |
| `e`   | Exibir extrato               |
| `nu`  | Cadastrar novo cliente       |
| `nc`  | Criar nova conta corrente    |
| `lc`  | Listar todas as contas       |
| `q`   | Sair do sistema              |
 
---
 
## 🧱 Estrutura das Classes
 
```
Cliente
└── PessoaFisica
 
Conta
└── ContaCorrente
 
Historico
 
Transacao (ABC)
├── Saque
└── Deposito
```
 
### Descrição das classes
 
- **`Cliente`** — Classe base para clientes. Armazena endereço, lista de contas e permite realizar transações.
- **`PessoaFisica`** — Herda de `Cliente`. Adiciona nome, CPF e data de nascimento.
- **`Conta`** — Conta genérica com saldo, número, agência e histórico de transações.
- **`ContaCorrente`** — Herda de `Conta`. Adiciona limite de saque (R$ 500) e limite de quantidade de saques (3 por sessão).
- **`Historico`** — Armazena todas as transações realizadas em uma conta.
- **`Transacao`** — Classe abstrata base para transações.
- **`Saque`** / **`Deposito`** — Implementações concretas de `Transacao`.
---
 
## ⚙️ Regras de Negócio
 
- Cada cliente é identificado pelo **CPF**.
- Uma conta corrente possui:
  - Limite de saque de **R$ 500,00** por operação.
  - Máximo de **3 saques** por sessão.
- O histórico registra tipo, valor e data/hora de cada transação.
- Não é possível cadastrar dois clientes com o mesmo CPF.
---
 
## 🛠️ Tecnologias Utilizadas
 
- **Python 3.x**
- Módulos: `abc`, `datetime`, `textwrap`
---
 
## ▶️ Como Executar
 
1. Certifique-se de ter o **Python 3** instalado.
2. Clone ou baixe o arquivo do projeto.
3. Execute no terminal:
```bash
python sistema_bancario.py
```
 
4. Navegue pelo menu interativo no terminal.
---
 
## 📌 Observações
 
- O sistema roda inteiramente no terminal (CLI).
- Atualmente, quando um cliente possui mais de uma conta, o sistema sempre utiliza a primeira conta cadastrada. *(FIXME registrado no código)*
- O projeto não possui persistência de dados — as informações são perdidas ao encerrar o programa.
---
 
## 👨‍💻 Autor: Pedro Souza
 
Desenvolvido como projeto de estudo de **Programação Orientada a Objetos com Python**.

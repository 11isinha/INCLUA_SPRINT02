# 🔐 Especificação de Requisitos – Cadastro e Autenticação (Projeto INCLUA)

Este documento detalha os requisitos funcionais, não funcionais, histórias de usuário e critérios de aceitação referentes ao **cadastro, autenticação, controle de acesso e segurança** do sistema **INCLUA**.

---

## 1. Requisitos Funcionais (RF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RF01** | Cadastro e autenticação de usuários para acesso às funcionalidades do INOVA. | Must Have (Obrigatório) | Usuário consegue cadastrar-se, autenticar-se e acessar as funções permitidas. |
| **RF02** | Cadastro e gerenciamento das informações das academias. | Must Have (Obrigatório) | Academia cadastrada com dados básicos, localização e recursos de acessibilidade. |

---

## 2. Requisitos Não Funcionais (RNF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RNF01** | Proteção de dados pessoais e conformidade com a LGPD (Lei nº 13.709/2018). | Must Have (Obrigatório) | Dados protegidos e acessos controlados conforme as permissões do sistema. |
| **RNF04** | Segurança contra acessos indevidos, entradas maliciosas e exposição indevida de dados. | Must Have (Obrigatório) | Autenticação, autorização e validações impedem acessos não permitidos. |

### Detalhamento Técnico
* **Segurança:** O sistema deverá utilizar autenticação e autorização, validação das entradas, proteção de sessão e mecanismos de prevenção contra vulnerabilidades comuns, como **XSS** e **CSRF**. Informações sensíveis deverão ser protegidas.
* **Legislação e Privacidade:** O tratamento de dados pessoais no cadastro e autenticação deverá respeitar a **LGPD (Lei nº 13.709/2018)** e os princípios aplicáveis à privacidade e à proteção de dados.

---

## 3. Histórias de Usuário e Critérios de Aceitação (BDD)

### US01 – Criar conta no sistema
> **Como** usuário, **eu quero** criar uma conta no INCLUA, **para que** eu possa utilizar as funcionalidades que exigem identificação. *(5 Story Points • Must Have)*

* **Cenário:** Cadastro de usuário
  * **DADO QUE** o usuário está na tela de cadastro
  * **E** informa os dados obrigatórios válidos
  * **QUANDO** ele confirmar o cadastro
  * **ENTÃO** o sistema deve criar a conta
  * **E** apresentar uma mensagem de confirmação.

---

### US02 – Realizar login no sistema
> **Como** usuário, **eu quero** fazer login no sistema, **para que** eu possa acessar meu perfil e registrar ou acompanhar ocorrências. *(3 Story Points • Must Have)*

* **Cenário:** Autenticação bem-sucedida
  * **DADO QUE** o usuário possui credenciais válidas
  * **QUANDO** informar seus dados e clicar em Entrar
  * **ENTÃO** o sistema deve autenticar o usuário
  * **E** direcioná-lo para a área inicial permitida.

---

### US09 – Cadastrar e atualizar informações do estabelecimento
> **Como** responsável pela academia, **eu quero** cadastrar e atualizar as informações do estabelecimento, **para que** os usuários tenham acesso a dados atualizados. *(5 Story Points • Must Have)*

* **Cenário:** Atualização dos dados da academia
  * **DADO QUE** o responsável está autenticado e possui permissão
  * **QUANDO** alterar os dados da academia e salvar
  * **ENTÃO** o sistema deve atualizar as informações
  * **E** disponibilizar os dados atualizados aos usuários conforme as regras de publicação.

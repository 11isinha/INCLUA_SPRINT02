# ♿ Especificação de Requisitos – Acessibilidade das Funcionalidades (Projeto INCLUA)

Este documento detalha os requisitos funcionais, não funcionais, histórias de usuário e critérios de aceitação voltados à **acessibilidade física das academias mapeadas** e à **acessibilidade digital da interface** do **INCLUA**.

---

## 1. Requisitos Funcionais (RF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RF05** | Filtro de academias por recursos de acessibilidade. | Must Have (Obrigatório) | Ao selecionar um recurso, o sistema apresenta academias compatíveis com o filtro. |
| **RF09** | Atualização dos recursos de acessibilidade da academia. | Should Have (Importante) | Alterações salvas aparecem nas informações da academia após atualização. |

---

## 2. Requisitos Não Funcionais (RNF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RNF03** | Interface responsiva e acessível, com abordagem *Mobile First*. | Must Have (Obrigatório) | Interface utilizável em diferentes dispositivos e com recursos básicos de acessibilidade. |
| **RNF05** | Compatibilidade com navegadores modernos e dispositivos móveis. | Should Have (Importante) | Principais telas funcionam adequadamente nos ambientes previstos. |

### Detalhamento Técnico
* **Acessibilidade Digital e Usabilidade:** A interface deverá considerar **contraste adequado, legibilidade, foco visível, navegação por teclado quando aplicável, identificação clara dos controles e linguagem compreensível**.
* **Responsividade:** A solução deverá ser responsiva, priorizando a experiência em dispositivos móveis (*Mobile First*) para garantir que todas as funcionalidades sejam operáveis em diferentes tamanhos de tela.

---

## 3. Histórias de Usuário e Critérios de Aceitação (BDD)

### US05 – Filtrar academias por recursos de acessibilidade
> **Como** pessoa com necessidade de acessibilidade, **eu quero** filtrar academias pelos recursos disponíveis, **para que** eu possa encontrar um local adequado às minhas necessidades. *(5 Story Points • Must Have)*

* **Cenário:** Filtro por acessibilidade
  * **DADO QUE** existem academias com recursos de acessibilidade cadastrados
  * **QUANDO** o usuário selecionar um recurso no filtro
  * **ENTÃO** o sistema deve exibir academias compatíveis com o recurso selecionado.

---

### US06 – Consultar recursos de acessibilidade da academia
> **Como** usuário, **eu quero** consultar os detalhes de uma academia, **para que** eu possa verificar sua localização e seus recursos antes de visitá-la. *(3 Story Points • Must Have)*

* **Cenário:** Consulta dos detalhes da academia
  * **DADO QUE** o usuário selecionou uma academia
  * **QUANDO** acessar seus detalhes
  * **ENTÃO** o sistema deve exibir informações cadastrais, localização e recursos de acessibilidade disponíveis.

---

### US10 – Informar recursos de acessibilidade do estabelecimento
> **Como** responsável pela academia, **eu quero** informar os recursos de acessibilidade disponíveis, **para que** usuários possam encontrar a academia pelos filtros. *(5 Story Points • Must Have)*

* **Cenário:** Cadastro de recursos de acessibilidade
  * **DADO QUE** o responsável possui permissão para editar a academia
  * **QUANDO** selecionar e salvar os recursos disponíveis
  * **ENTÃO** os recursos devem aparecer no perfil da academia
  * **E** ficar disponíveis para os filtros de pesquisa.

---

### US15 – Utilizar interface responsiva e acessível
> **Como** usuário, **eu quero** utilizar uma interface responsiva e acessível, **para que** eu consiga usar o INOVA em diferentes dispositivos. *(5 Story Points • Must Have)*

* **Cenário:** Uso em dispositivo móvel
  * **DADO QUE** o usuário acessa o INOVA por celular ou tablet
  * **QUANDO** navegar pelas telas principais
  * **ENTÃO** a interface deve se adaptar ao tamanho da tela
  * **E** os controles essenciais devem permanecer utilizáveis.

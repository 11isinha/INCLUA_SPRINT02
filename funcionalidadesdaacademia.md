# 🔍 Documentação das Funcionalidades de Pesquisa de Academias
---

## 🎯 Objetivo

Especificar e documentar o comportamento técnico, as regras de negócio e os critérios de aceitação das funcionalidades responsáveis pela **pesquisa, filtragem por acessibilidade, visualização detalhada e localização em mapa** das academias cadastradas na plataforma.

---

## ⚙️ Requisitos Funcionais Abrangidos

| Código | Funcionalidade | Prioridade MoSCoW | Descrição Técnica |
| :--- | :--- | :--- | :--- |
| **RF03** | Busca e visualização de academias | Must Have (Obrigatório) | Permitir que o usuário pesquise por termos (nome, bairro ou endereço) e visualize a lista de academias cadastradas no sistema. |
| **RF04** | Mapa interativo de academias | Must Have (Obrigatório) | Exibir as academias com localização geográfica válida em um mapa interativo, permitindo clicar nos pontos para consultar seus detalhes. |
| **RF05** | Filtro por recursos de acessibilidade | Must Have (Obrigatório) | Permitir que o usuário filtre os resultados selecionando recursos específicos de acessibilidade (ex.: rampa de acesso, banheiro adaptado, estacionamento, equipamentos adaptados). |

---

## 📖 Histórias de Usuário e Critérios de Aceitação (BDD)

### US03 – Pesquisar academias
> **Como** usuário, **eu quero** pesquisar academias, **para que** eu possa encontrar um estabelecimento de meu interesse.

* **Cenário:** Pesquisa de academia por termo.
  * **DADO QUE** existem academias cadastradas no sistema.
  * **QUANDO** o usuário informar um termo de busca.
  * **ENTÃO** o sistema deve apresentar a lista de estabelecimentos correspondentes.

---

### US04 – Visualizar academias no mapa
> **Como** usuário, **eu quero** visualizar academias em um mapa, **para que** eu possa localizar estabelecimentos com mais facilidade.

* **Cenário:** Exibição de pontos no mapa.
  * **DADO QUE** existem academias com localização cadastrada.
  * **QUANDO** o usuário abrir a visualização de mapa.
  * **ENTÃO** o sistema deve exibir as academias nos respectivos pontos geográficos.
  * **E** permitir consultar os detalhes de cada estabelecimento.

---

### US05 – Filtrar academias por recursos de acessibilidade
> **Como** pessoa com necessidade de acessibilidade, **eu quero** filtrar academias pelos recursos disponíveis, **para que** eu possa encontrar um local adequado às minhas necessidades.

* **Cenário:** Aplicação de filtro de acessibilidade.
  * **DADO QUE** existem academias com recursos de acessibilidade cadastrados.
  * **QUANDO** o usuário selecionar um ou mais recursos no filtro.
  * **ENTÃO** o sistema deve exibir apenas as academias compatíveis com os critérios selecionados.

---

### US06 – Consultar detalhes da academia
> **Como** usuário, **eu quero** consultar os detalhes de uma academia, **para que** eu possa verificar sua localização e seus recursos antes de visitá-la.

* **Cenário:** Visualização do perfil completo da academia.
  * **DADO QUE** o usuário selecionou uma academia na lista ou no mapa.
  * **QUANDO** acessar sua página de detalhes.
  * **ENTÃO** o sistema deve exibir informações cadastrais, endereço/localização e a lista completa de recursos de acessibilidade disponíveis.

---

## 🛡️ Requisitos Não Funcionais Aplicáveis

* **Desempenho (`RNF02`):** As consultas de busca, filtragem e carregamento do mapa devem apresentar tempo de resposta **inferior a 2 segundos** em condições normais de uso.
* **Responsividade e Acessibilidade (`RNF03`):** Os campos de busca, filtros e cartões de resultado devem seguir abordagem *Mobile First*, com contraste adequado, foco visível e navegação acessível por teclado e leitores de tela.

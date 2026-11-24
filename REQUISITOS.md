# 📋 Especificação de Requisitos – Projeto INOVA

## 1. Matriz Estruturada de Requisitos

A matriz abaixo apresenta os requisitos funcionais e não funcionais do **INOVA**, relacionando código, tipo, descrição da necessidade técnica, prioridade segundo o método **MoSCoW** e critério principal de aceite[cite: 2].

### ⚙️ Requisitos Funcionais (RF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RF01** | Cadastro e autenticação de usuários para acesso às funcionalidades do INOVA. | Must Have (Obrigatório) | Usuário consegue cadastrar-se, autenticar-se e acessar as funções permitidas. |
| **RF02** | Cadastro e gerenciamento das informações das academias. | Must Have (Obrigatório) | Academia cadastrada com dados básicos, localização e recursos de acessibilidade. |
| **RF03** | Busca e visualização de academias disponíveis no sistema. | Must Have (Obrigatório) | Usuário consegue pesquisar e visualizar academias cadastradas. |
| **RF04** | Mapa para localizar academias cadastradas. | Must Have (Obrigatório) | Mapa exibe academias com localização válida e permite consultar seus detalhes. |
| **RF05** | Filtro de academias por recursos de acessibilidade. | Must Have (Obrigatório) | Ao selecionar um recurso, o sistema apresenta academias compatíveis com o filtro. |
| **RF06** | Registro de acidentes e problemas relacionados a equipamentos. | Must Have (Obrigatório) | Usuário consegue registrar uma ocorrência com categoria e descrição. |
| **RF07** | Acompanhamento do status das ocorrências registradas. | Must Have (Obrigatório) | Usuário consegue consultar o status atualizado de sua ocorrência. |
| **RF08** | Gestão das ocorrências pela academia responsável. | Must Have (Obrigatório) | Responsável autorizado consegue visualizar e atualizar ocorrências da academia. |
| **RF09** | Atualização dos recursos de acessibilidade da academia. | Should Have (Importante) | Alterações salvas aparecem nas informações da academia após atualização. |
| **RF10** | Histórico das alterações realizadas nas ocorrências. | Should Have (Importante) | O sistema registra alterações relevantes de status e acompanhamento. |
| **RF11** | Notificações sobre mudanças relevantes no acompanhamento. | Should Have (Importante) | Usuário recebe informação quando houver alteração relevante em sua ocorrência. |
| **RF12** | Indicadores básicos sobre ocorrências registradas. | Could Have (Desejável) | Área de gestão apresenta dados consolidados para acompanhamento. |

---

### 🛡️ Requisitos Não Funcionais (RNF)

| Código | Descrição da Necessidade Técnica | Prioridade MoSCoW | Critério de Aceite Principal |
| :--- | :--- | :--- | :--- |
| **RNF01** | Proteção de dados pessoais e conformidade com a LGPD (Lei nº 13.709/2018). | Must Have (Obrigatório) | Dados protegidos e acessos controlados conforme as permissões do sistema. |
| **RNF02** | Tempo de resposta adequado para as principais operações do sistema. | Should Have (Importante) | Operações principais apresentam resposta inferior a 2 segundos em condições normais de uso. |
| **RNF03** | Interface responsiva e acessível, com abordagem *Mobile First*. | Must Have (Obrigatório) | Interface utilizável em diferentes dispositivos e com recursos básicos de acessibilidade. |
| **RNF04** | Segurança contra acessos indevidos, entradas maliciosas e exposição indevida de dados. | Must Have (Obrigatório) | Autenticação, autorização e validações impedem acessos não permitidos. |
| **RNF05** | Compatibilidade com navegadores modernos e dispositivos móveis. | Should Have (Importante) | Principais telas funcionam adequadamente nos ambientes previstos. |

---

## 2. Detalhamento dos Requisitos Não Funcionais

Os requisitos não funcionais definem os padrões de qualidade que o **INOVA** deverá respeitar durante sua implementação e utilização[cite: 2]:

* **Desempenho:** As principais operações deverão apresentar tempo de resposta adequado, tendo como referência uma resposta **inferior a 2 segundos** em condições normais de uso[cite: 2].
* **Segurança:** O sistema deverá utilizar autenticação e autorização, validação das entradas, proteção de sessão e mecanismos de prevenção contra vulnerabilidades comuns, como **XSS** e **CSRF**[cite: 2]. Informações sensíveis deverão ser protegidas[cite: 2].
* **Legislação e Privacidade:** O tratamento de dados pessoais deverá considerar a **LGPD (Lei nº 13.709/2018)** e os princípios aplicáveis à privacidade e à proteção de dados[cite: 2].
* **Acessibilidade:** A interface deverá considerar contraste adequado, legibilidade, foco visível, navegação por teclado quando aplicável, identificação clara dos controles e linguagem compreensível[cite: 2]. A solução deverá ser responsiva, priorizando a experiência em dispositivos móveis[cite: 2].

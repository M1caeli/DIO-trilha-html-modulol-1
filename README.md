# kindersys-education

## 🌟 Visão Geral do Projeto

[cite_start]O **Kindersys** é uma plataforma de desenvolvimento de sistemas focada em inovar a comunicação e a gestão das creches no Brasil[cite: 11]. [cite_start]Nosso principal objetivo é estabelecer uma **conexão transparente** entre creches, professores e responsáveis [cite: 18][cite_start], otimizando o acompanhamento do desenvolvimento escolar e oferecendo maior controle sobre o bem-estar da criança[cite: 18, 19].

[cite_start]Esta Prova de Conceito (PoC) foca na jornada essencial da **Agenda Digital**, que é o cerne da nossa proposta de **Comunicação Eficiente e Ágil** [cite: 21][cite_start], eliminando falhas na comunicação e a dependência de métodos manuais[cite: 21, 28].

## ✅ Justificativa da Prova de Conceito (PoC)

[cite_start]A jornada escolhida para a PoC é o fluxo de **Registro e Consulta da Agenda Digital**[cite: 143].

* [cite_start]**Impacto e Viabilidade:** É a jornada mais simples e de maior impacto [cite: 143][cite_start], pois atende diretamente à necessidade de **Transparência e Praticidade para os Pais** [cite: 25] [cite_start]e de **Otimização da Gestão Interna para a Creche**[cite: 26].
* [cite_start]**Valor para o Usuário (Persona Eloise, Mãe Atarefada):** Permite que Eloise, que tem o tempo escasso [cite: 62][cite_start], acesse a qualquer momento as informações diárias de alimentação, sono, atividades e humor do filho [cite: 78][cite_start], recebendo notificações importantes em tempo real[cite: 65].
* [cite_start]**Valor para a Creche (Persona Sandra, Gestora):** Reduz o tempo que as professoras gastam preenchendo agendas de papel [cite: 93] [cite_start]e proporciona uma visão geral e controle sobre alimentação, frequência e ocorrências[cite: 95].

## ⚙️ Pilha Tecnológica (Tech Stack)

[cite_start]A seleção da pilha tecnológica (Passo 2) foi feita visando a agilidade no desenvolvimento da PoC, que envolve um sistema orientado a dispositivos móveis e baseado na Web[cite: 3].

| Camada | Tecnologia Escolhida | Justificativa |
| :--- | :--- | :--- |
| **Frontend** | React | Alta produtividade, ecossistema robusto e flexibilidade para interface móvel/web. |
| **Backend/API** | Node.js (Express) | Performance em I/O e uso de JavaScript, que facilita a integração de ponta a ponta. |
| **Banco de Dados** | MongoDB (NoSQL) | [cite_start]Flexibilidade na modelagem de dados do Registro Diário (que podem ser variáveis) [cite: 155] e facilidade de integração com Node.js. |

## 👥 Membros da Equipe

| Nome do Membro | Função no Projeto (Grupo 29) |
| :--- | :--- |
| [cite_start]**Evelin Silveira Rocha** [cite: 4] | [cite_start]Membro 1 (Planejamento e Arquitetura) [cite: 134] |
| [cite_start]**Gabriel Santos Rezende** [cite: 5] | [cite_start]Membro 2 (Desenvolvimento Backend/API) [cite: 138] |
| [cite_start]**Hannah Yumi Castro Ito** [cite: 6] | [cite_start]Membro 3 (Implementação de BD / Documentação / Entrega) [cite: 138, 140] |
| [cite_start]**Hyury Freitas Gomes** [cite: 7] | [cite_start]Membro 4 (Modelagem / Frontend Professor) [cite: 137, 138] |
| [cite_start]**Micaeli Ferreira Alcantara** [cite: 8] | [cite_start]Membro 5 (Modelagem / Frontend Responsável / Entrega) [cite: 137, 138, 140] |

## 💻 Instruções de Execução

Este repositório está dividido em diretórios `backend` e `frontend`.

### 1. Pré-requisitos

* Node.js e NPM instalados.
* MongoDB em execução.

### 2. Configuração e Inicialização

1.  **Clone o Repositório** (Passo 4):
    ```bash
    git clone [https://github.com/evelinnrocha1-hub/kindersys-education.git](https://github.com/evelinnrocha1-hub/kindersys-education.git)
    cd kindersys-education
    ```
2.  **Inicialize o Backend** (Passos 7 e 8):
    ```bash
    cd backend
    npm install
    # Configure a string de conexão do MongoDB no arquivo .env
    npm start 
    ```
    *A API deve estar rodando e integrada ao banco de dados.*
3.  **Inicialize o Frontend** (Passo 9):
    ```bash
    cd ../frontend
    npm install
    npm start 
    ```
    *A aplicação deve abrir no seu navegador.*

### 3. Fluxo de Teste (Testes de Ponta a Ponta)

[cite_start]O teste (Passo 10) segue o fluxo de registro e consulta da Agenda Digital[cite: 145].

1.  [cite_start]**Ação do Professor**[cite: 146]:
    * [cite_start]Faz **Login**[cite: 146].
    * [cite_start]Acessa e seleciona o aluno[cite: 147].
    * [cite_start]Registra as informações do dia (alimentação, sono, humor, atividades)[cite: 148, 155].
    * [cite_start]O sistema atualiza os relatórios **automaticamente**[cite: 149].

2.  [cite_start]**Ação do Responsável**[cite: 150]:
    * [cite_start]Faz **Login**[cite: 150].
    * [cite_start]Consulta o **Relatório Diário** do filho[cite: 151, 157].
    * [cite_start]Verifica a exibição dos dados de Alimentação, Sono, Humor e Atividades[cite: 157].

## 🎨 Modelagem de Dados Mínima (Passo 5)

[cite_start]A estrutura de dados mínima para o Registro Diário deve mapear as informações que o professor registra e que o pai consulta[cite: 137].

| Campo | Tipo | Descrição |
| :--- | :--- | :--- |
| `aluno_id` | ObjectId | Chave estrangeira para identificar a criança. |
| `data_registro` | Date | Data em que o registro foi realizado. |
| `alimentacao` | String/Objeto | O que comeu/rejeitou, quantidades. |
| `sono` | String/Objeto | Horário e duração do sono/descanso. |
| `humor` | String | Humor e comportamento (alegre, irritado, etc.). |
| `atividades` | String/Array | Descrição das atividades realizadas no dia. |

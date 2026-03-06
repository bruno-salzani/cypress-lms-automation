# 🚀 Test Automation - Neolude LMS Platform (Cypress)

![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Framework](https://img.shields.io/badge/Framework-Cypress-green)
![Stack](https://img.shields.io/badge/Stack-Node.js%20%7C%20JavaScript-blue)

Este projeto foi desenvolvido para automatizar o processo de criação de cursos na plataforma LMS Neolude, eliminando tarefas manuais repetitivas e aumentando a eficiência operacional do time de implantação.

A solução utiliza **Cypress** para execução automatizada ponta a ponta, com foco em escalabilidade, padronização e mitigação de erros humanos.

---

# 🎯 Objetivo do Projeto

Automatizar o fluxo completo de criação de cursos, incluindo:

- Importação estruturada de dados
- Login administrativo
- Configuração de parâmetros
- Criação de cursos em lote
- Associação de turmas
- Classificação por categorias

## Foco Principal

- Redução de tempo operacional  
- Eliminação de erros manuais  
- Padronização do processo  
- Escalabilidade da operação  

---

# 🧠 Estratégia de Automação

## Arquitetura da Solução

A automação foi estruturada em camadas bem definidas:

1. Conversão de dados (Excel → JSON)
2. Login autenticado
3. Execução sequencial da criação de cursos
4. Validações após cada etapa
5. Geração de relatório de execução

Separação clara entre:

- **Dados** (fixtures)
- **Fluxos** (spec files)
- **Configuração** (`cypress.config.js`)
- **Relatórios** (Mochawesome)

---

## Estratégia Técnica Aplicada

- Uso de dados dinâmicos para evitar duplicidade
- Criação de comandos customizados reutilizáveis
- Modularização do fluxo de criação
- Execução iterativa baseada em JSON
- Sincronização adequada com DOM
- Validação de elementos críticos após cada etapa

---

# 🔄 Fluxo de Automação

1. O time recebe uma planilha Excel com os dados dos cursos.
2. Um script converte automaticamente a planilha para JSON estruturado.
3. A automação realiza login como administrador.
4. Para cada item da planilha:
   - Cria o curso
   - Configura parâmetros
   - Define permissões
   - Associa categorias
   - Registra turmas
5. Ao final, gera relatório detalhado de execução.

---

# 📁 Estrutura do Projeto

```bash
cypress/
├── e2e/
│   ├── converte-excel-em-json.cy.js
│   └── curso-criacao.cy.js
├── fixtures/
│   └── dados-cursos.json
├── support/
│   └── commands.js
├── cypress.config.js
└── package.json
```

---

# ⚙️ Funcionalidades Automatizadas

## 📥 Importação de Dados

- Leitura de planilha Excel
- Conversão estruturada para JSON
- Padronização de campos obrigatórios

---

## 🔐 Login Automatizado

- Autenticação com credenciais administrativas
- Validação de login bem-sucedido
- Tratamento de falhas de autenticação

---

## 📚 Criação de Cursos

- Inclusão de descrição detalhada
- Configuração de parâmetros específicos
- Definição de permissões
- Classificação por categorias
- Associação de turmas

Validações são realizadas após cada etapa para garantir a integridade do processo.

---

# 🧪 Boas Práticas Aplicadas

- Separação entre dados e lógica
- Uso de fixtures
- Modularização do código
- Reutilização de comandos customizados
- Geração automática de relatórios
- Execução determinística

---

# 📊 Gestão de Riscos

## Principais Riscos Mitigados

- Criação duplicada de cursos
- Falha parcial no fluxo de cadastro
- Timeout por carregamento de página
- Dados inconsistentes na planilha
- Erros humanos no processo manual

## Estratégias de Mitigação

- Validação após cada etapa crítica
- Logs estruturados
- Relatórios detalhados
- Execução controlada por lote

---

# 📈 Resultados Alcançados

- Redução significativa do tempo de implantação
- Eliminação de erros manuais recorrentes
- Padronização do processo
- Aumento da capacidade operacional do time
- Execução em lote com previsibilidade

---

# 🛠️ Tecnologias Utilizadas

- Cypress (Automação E2E)
- Node.js
- JavaScript
- Mochawesome (Relatórios)

---

# ▶️ Como Executar

## 1️⃣ Clonar o repositório

```bash
git clone https://github.com/bruno-salzani/neolude-automation.git
```

## 2️⃣ Instalar dependências

```bash
npm install
```

## 3️⃣ Configurar ambiente

Ajustar credenciais e variáveis no arquivo `cypress.config.js`.

## 4️⃣ Executar automação

🔹 Modo interface:

```bash
npx cypress open
```

🔹 Modo headless:

```bash
npx cypress run
```

---

# 📄 Relatórios

Após a execução, o relatório Mochawesome é gerado contendo:

- Status por spec
- Tempo de execução
- Evidências de falha
- Logs detalhados

---

# 🚀 Diferenciais Técnicos

- Automação voltada para ganho operacional real
- Estrutura escalável para execução em lote
- Separação clara entre dados e execução
- Aplicação prática de Cypress em cenário corporativo
- Mentalidade orientada a eficiência e redução de risco

---

# 🤝 Conclusão

Projeto com aplicação prática de automação E2E em ambiente corporativo, atuando além da validação tradicional e contribuindo diretamente para otimização de processos internos.

A solução trouxe ganho operacional, previsibilidade e redução de falhas humanas, consolidando experiência sólida em automação com foco em resultado de negócio.

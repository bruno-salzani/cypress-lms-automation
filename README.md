# 🚀 Automação de Testes com Cypress (Neolude)

![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)  
![Framework](https://img.shields.io/badge/Framework-Cypress-green)  
![Stack](https://img.shields.io/badge/Node.js-JavaScript-blue)

Este projeto foi desenvolvido para automatizar a criação de conteúdos na plataforma LMS Neolude, reduzindo drasticamente o esforço manual do time de implantação.

A solução substitui o processo manual de criação de cursos por uma automação estruturada utilizando **Cypress**, com foco em produtividade, padronização e mitigação de erros humanos.

---

## 🎯 Objetivo do Projeto

Automatizar o processo completo de criação de cursos na plataforma, incluindo:

- Importação estruturada de dados
- Login administrativo
- Configuração de parâmetros
- Criação de cursos em lote
- Associação de turmas
- Classificação por categorias

O foco principal foi:

- Reduzir tempo operacional
- Eliminar erros manuais
- Padronizar implantações
- Aumentar escalabilidade do time

---

## 🧠 Estratégia de Automação

### Arquitetura da Solução

A automação foi estruturada em camadas:

1. Conversão de dados (Excel → JSON)
2. Login autenticado
3. Execução sequencial da criação de cursos
4. Validações pós-criação
5. Geração de relatório de execução

Separação clara entre:

- Dados (fixtures)
- Fluxos (spec files)
- Configuração (cypress.config.js)
- Relatórios (Mochawesome)

---

### Estratégia Técnica Aplicada

- Uso de dados dinâmicos para evitar conflitos de duplicidade
- Reaproveitamento de comandos customizados
- Modularização do fluxo de criação
- Execução iterativa baseada em JSON
- Tratamento de espera explícita e sincronização de DOM
- Validação de elementos críticos após cada etapa

---

## 🔄 Fluxo de Automação

1. O time recebe uma planilha Excel com os dados dos cursos.
2. O script converte automaticamente a planilha para JSON estruturado.
3. A automação realiza login como administrador.
4. Para cada item da planilha:
   - Cria o curso
   - Configura parâmetros
   - Define permissões
   - Associa categorias
   - Registra turmas
5. Gera relatório detalhado de execução.

---

## 📁 Estrutura do Projeto

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

## ⚙️ Funcionalidades Automatizadas

### 📥 Importação de Dados

- Leitura de planilha Excel
- Conversão estruturada para JSON
- Padronização de campos obrigatórios

---

### 🔐 Login Automatizado

- Acesso com credenciais administrativas
- Validação de login bem-sucedido
- Proteção contra falhas de autenticação

---

### 📚 Criação de Cursos

- Inclusão de descrição detalhada
- Configuração de parâmetros específicos
- Definição de permissões
- Classificação por categorias
- Associação de turmas

Validação após cada etapa para garantir integridade do fluxo.

---

## 🧪 Boas Práticas Aplicadas

- Separação entre dados e lógica
- Uso de fixtures
- Modularização do código
- Reutilização de comandos customizados
- Relatórios automatizados
- Execução determinística

---

## 📊 Gestão de Riscos

Principais riscos mitigados:

- Criação duplicada de cursos
- Falha parcial no fluxo de cadastro
- Timeout por carregamento de página
- Dados inconsistentes na planilha
- Falhas humanas no processo manual

Mitigação:

- Validações após cada etapa
- Logs estruturados
- Relatórios detalhados
- Execução controlada por lote

---

## 📈 Resultados Alcançados

- Redução significativa do tempo de implantação de cursos
- Eliminação de erros manuais recorrentes
- Padronização do processo de criação
- Aumento da capacidade operacional do time
- Execução em lote com previsibilidade

---

## 🛠️ Tecnologias Utilizadas

- Cypress (Automação E2E)
- Node.js
- JavaScript
- Mochawesome (Relatórios detalhados)

---

## ▶️ Como Executar

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/bruno-salzani/neolude-automation.git
```
## 2️⃣ Instale as dependências
npm install

## 3️⃣ Configure o ambiente
Ajuste credenciais e variáveis no `cypress.config.js`.

## 4️⃣ Execute os testes
🔹 Modo interface:
```bash
npx cypress open
```
🔹 Modo headless:
```bash
npx cypress run
```

## 📄 Relatórios
Após a execução, o relatório Mochawesome é gerado contendo:
*   Status por spec
*   Tempo de execução
*   Evidências de falha
*   Logs detalhados

## 🚀 Diferenciais Técnicos
*   Automação voltada para ganho operacional real (não apenas validação)
*   Estrutura escalável para execução em lote
*   Separação clara entre dados e execução
*   Aplicação prática de Cypress em cenário corporativo
*   Mentalidade orientada a eficiência e redução de risco

## 🤝 Conclusão
Este projeto demonstra aplicação prática de automação com Cypress em cenário real corporativo, indo além de testes tradicionais e atuando diretamente na otimização de processos internos.
A solução trouxe ganho operacional, previsibilidade e redução de erros humanos, consolidando experiência em automação E2E com foco em resultado de negócio.



# 📋 PLANO DE IMPLEMENTAÇÃO: GH-300 — GitHub Copilot

## Resumo da Certificação

| Campo | Valor |
|-------|-------|
| **Código** | GH-300 |
| **Nome** | GitHub Copilot |
| **Nível** | Intermediate |
| **Tempo do exame** | 120 minutos |
| **Questões** | ~60 questões |
| **Aprovação** | 700/1000 |
| **Emoji** | 🤖 |
| **Prefixo localStorage** | `gh300_` |
| **Página oficial** | https://learn.microsoft.com/credentials/certifications/github-copilot/ |

---

## Estrutura de Módulos Aprovada

### MÓDULO 0 — Introdução ao Curso (15 min)
- Landing page, estrutura do curso, dicas de estudo, links oficiais

### MÓDULO 1 — IA Responsável e Validação (30 min) ⚖️ Peso: 15-20%
- **Lição 1.1:** Princípios de IA Responsável — Riscos, limitações de GenAI, viés, ética, mitigação
- **Lição 1.2:** Validação e Operação Responsável — Necessidade de validar output, operar Copilot responsavelmente
- **8 exercícios** baseados em cenário

### MÓDULO 2 — Funcionalidades do Copilot no IDE e CLI (45 min) ⚖️ Peso: 25-30%
- **Lição 2.1:** Copilot no IDE — Habilitar, inline suggestions, Chat, Plan Mode
- **Lição 2.2:** Copilot CLI — Instalação, comandos, sessões interativas, gerar scripts, gerenciar arquivos
- **Lição 2.3:** Features Avançadas — Agent Mode, Edit Mode, MCP, Sub-Agents, Spaces, Spark, PR Summaries, slash commands (/doc, /explain, /fix, /tests, /optimize, /generate, /help)
- **12 exercícios** (ênfase em slash commands e modos de operação)

### MÓDULO 3 — Administração, API e Auditoria (45 min) ⚖️ Peso: 25-30%
- **Lição 3.1:** Gestão Organizacional — Policies org-wide, Copilot Code Review policies, feature availability IDEs/github.com, gerenciar assentos
- **Lição 3.2:** REST API — Manage subscriptions via API, Copilot Metrics API (org/team), endpoints, permissões (fine-grained tokens, scopes), response schema
- **Lição 3.3:** Audit Log & Insights — Eventos de auditoria do Copilot, onde visualizar (Settings → Logs), métricas de uso, Copilot Dashboard, telemetry requirement
- **15 exercícios** ⚠️ REFORÇADO — tópico mais cobrado na prova real (caminhos, API, auditoria)

### MÓDULO 4 — Dados, Arquitetura e Contexto (35 min) ⚖️ Peso: 10-15%
- **Lição 4.1:** Fluxo de Dados — Data usage, data flow, data sharing, input processing, prompt building, proxy filtering, post-processing
- **Lição 4.2:** Ciclo de Vida e Limitações — Code suggestion lifecycle (trigger → model → filter → display), limitações de LLMs, hallucinations, token limits
- **8 exercícios**

### MÓDULO 5 — Prompt Engineering e Contexto (35 min) ⚖️ Peso: 10-15%
- **Lição 5.1:** Crafting Eficaz — Estrutura de prompt, como o contexto é determinado (open files, workspace, #file, @workspace), zero-shot, few-shot
- **Lição 5.2:** Performance — Princípios avançados, prompt process flow, chat history, como workspace context funciona
- **8 exercícios** (ênfase em como o Copilot gerencia contexto)

### MÓDULO 6 — Produtividade: Testes, Modernização e Segurança (35 min) ⚖️ Peso: 10-15%
- **Lição 6.1:** Code Generation & Modernização — Refactoring, documentação automática, modernizar legacy code, gerar sample data, reduzir context switching
- **Lição 6.2:** Testes e Segurança — Gerar unit tests, integration tests, edge cases, assertions, sugestões de segurança, performance optimizations
- **10 exercícios** ⚠️ REFORÇADO — testes e modernização caíram na prova

### MÓDULO 7 — Exclusão de Conteúdo e Safeguards (40 min) ⚖️ Peso: 10-15%
- **Lição 7.1:** Content Exclusion — Configurar no repositório (Settings → Copilot → Content exclusion), na organização, no enterprise, YAML paths, fnmatch patterns
- **Lição 7.2:** Safeguards — Duplication detection, security warnings, troubleshooting, ownership de outputs, limitações da exclusão (CLI/Agent Mode não suportam)
- **Lição 7.3:** Caminhos e Propagação — Navigation step-by-step, propagação (até 30 min), reload window, REST API para exclusions, testar exclusões
- **12 exercícios** ⚠️ REFORÇADO — tópico MAIS cobrado (caminhos, YAML, propagação)

### MÓDULO 8 — 📝 Revisão Final (20 min)
- Tabela de slash commands completa
- Caminhos de configuração compilados (Admin → API → Exclusion → Audit)
- Decision tree: "Precisa de X? → Vá em Y"
- Macetes e mnemônicos compilados
- Checklist pré-prova

### MÓDULO 9 — 🎯 Simulado Final (60 min)
- 40 questões distribuídas por domínio e tipo

---

## Configuração do Simulado

```javascript
SIMULADO_CONFIG = {
    timeLimit: 60,
    passScore: 700,
    totalScore: 1000,
    questionCount: 40
}

SIMULADO_DOMAINS = [
    { id: 0, pt: "IA Responsável", en: "Responsible AI", weight: "15–20%", color: "#9f7aea", icon: "💡" },
    { id: 1, pt: "Features IDE/CLI", en: "IDE/CLI Features", weight: "15%", color: "#3182ce", icon: "🔧" },
    { id: 2, pt: "Administração, API & Auditoria", en: "Admin, API & Audit", weight: "15%", color: "#48bb78", icon: "📊" },
    { id: 3, pt: "Dados & Arquitetura", en: "Data & Architecture", weight: "10–15%", color: "#ed8936", icon: "🏗️" },
    { id: 4, pt: "Prompt Engineering & Contexto", en: "Prompt Engineering & Context", weight: "10–15%", color: "#e53e3e", icon: "🎯" },
    { id: 5, pt: "Produtividade & Testes", en: "Productivity & Testing", weight: "10–15%", color: "#38b2ac", icon: "🚀" },
    { id: 6, pt: "Exclusão de Conteúdo & Safeguards", en: "Content Exclusion & Safeguards", weight: "10–15%", color: "#d69e2e", icon: "🔒" }
]
```

**Distribuição de questões por domínio:**
- Domínio 0 (IA Responsável): ~6 questões
- Domínio 1 (Features): ~6 questões
- Domínio 2 (Admin/API/Audit): ~8 questões ⚠️ reforçado
- Domínio 3 (Dados): ~5 questões
- Domínio 4 (Prompt): ~5 questões
- Domínio 5 (Produtividade): ~5 questões
- Domínio 6 (Exclusão): ~5 questões ⚠️ reforçado

**Mix de tipos:**
- single: 22 | multi: 6 | match: 5 | order: 4 | categorize: 3

---

## Mapa de Reforço Espiral

| Módulo | Referências cruzadas |
|--------|---------------------|
| Módulo 0 (Intro) | Nenhuma |
| Módulo 1 (IA Responsável) | Nenhuma — primeiro conteúdo |
| Módulo 2 (Features) | 1-2 refs: viés e validação (M1) |
| Módulo 3 (Admin/API) | 2-3 refs: features IDE/CLI (M2), responsabilidade (M1) |
| Módulo 4 (Dados) | 2-3 refs: como Copilot opera (M2), privacidade (M1) |
| Módulo 5 (Prompt) | 3 refs: fluxo de dados (M4), slash commands (M2), validação (M1) |
| Módulo 6 (Produtividade) | 3-4 refs: prompt engineering (M5), Agent Mode (M2), viés em testes (M1) |
| Módulo 7 (Exclusão) | 3-4 refs: API/Admin (M3), arquitetura (M4), features (M2) |
| Módulo 8 (Revisão) | Síntese completa de todos |
| Módulo 9 (Simulado) | Questões transversais multi-domínio |

---

## Fontes Consultadas

| Fonte | Status | Conteúdo extraído |
|-------|--------|-------------------|
| Microsoft Learn — Study Guide GH-300 | ✅ | Skills measured com 7 domínios e pesos |
| Microsoft Learn — Management & Customizations Module | ✅ | Content exclusions, plans, troubleshooting |
| GitHub Docs — Content Exclusion | ✅ | Config repo/org/enterprise, YAML, fnmatch, REST API, propagação |
| GitHub Docs — Copilot Metrics REST API | ✅ | Endpoints org/team, response schema, permissões, deprecation notice |
| Microsoft Learn — Slash Commands Reference | ✅ | /doc, /explain, /fix, /tests, /optimize, /generate, /help, /savePrompt |
| Feedback Real do Candidato | ✅ | Exclusão de conteúdo, audit API, insights, gerar testes, contexto, admin paths, slash commands |
| Reddit r/AzureCertification | ❌ | Sem resultados específicos GH-300 |
| ExamTopics/Whizlabs | ❌ | Sem resultados acessíveis |

---

## Plano de Implementação por Fases

### Fase 0: CORE — Copiar template + Estrutura base
**O que fazer:**
1. Copiar `agent_certificacao/template.html` → `GH-300.html`
2. Substituir placeholders: `{CERT_CODE}` → `GH-300`, `{CERT_FULL_NAME}` → `GitHub Copilot`, `{EMOJI}` → `🤖`, `{cert_lower}` → `gh300`
3. Configurar `COURSE_STRUCTURE` (10 módulos, durações, exercises com correct)
4. Configurar `SIMULADO_CONFIG` e `SIMULADO_DOMAINS`
5. Configurar `SIM_STORAGE_KEY = 'gh300_simulado_state'`
6. Preencher `translations` com TODAS as chaves (incluindo `sim_*` e `skipExercisesConfirm`)
7. Deixar `courseText = { pt: [], en: [] }` — VAZIO
8. Deixar `SIMULADO_QUESTIONS = []` — VAZIO

**Entrega:** Arquivo `GH-300.html` com estrutura funcional, sem conteúdo

---

### Fase 1: Módulo 0 — Introdução
**O que fazer:**
1. Gerar conteúdo PT e EN da landing page
2. Usar componentes: `.intro-highlight`, `.intro-section`, `.module-list`, `.study-tips`, `.testimonial`
3. Inserir em `courseText.pt[0]` e `courseText.en[0]`

**Entrega:** Landing page bilingue funcional

---

### Fase 2: Módulo 1 — IA Responsável e Validação
**Pesquisar:** Responsible AI with GitHub Copilot (Microsoft Learn)
**Implementar:**
- Lição 1.1: Riscos GenAI, limitações, viés, ética, mitigação (4 tópicos)
- Lição 1.2: Validar output, operar responsavelmente (3 tópicos)
- 8 exercícios baseados em cenário

**Entrega:** courseText.pt[1] + courseText.en[1]

---

### Fase 3: Módulo 2 — Features IDE/CLI
**Pesquisar:** GitHub Copilot features, Agent Mode, Edit Mode, slash commands
**Implementar:**
- Lição 2.1: Copilot no IDE (4 tópicos)
- Lição 2.2: Copilot CLI (4 tópicos)
- Lição 2.3: Features avançadas + slash commands (5 tópicos)
- 12 exercícios
- Reforço Espiral: refs ao Módulo 1

**Entrega:** courseText.pt[2] + courseText.en[2]

---

### Fase 4: Módulo 3 — Administração, API e Auditoria ⚠️ PRIORITÁRIO
**Pesquisar:** Copilot organization policies, REST API, audit log events, Metrics API
**Implementar:**
- Lição 3.1: Gestão organizacional (4 tópicos)
- Lição 3.2: REST API (5 tópicos) — endpoints, permissões, manage_billing scope
- Lição 3.3: Audit Log & Insights (4 tópicos) — eventos, caminhos de visualização, dashboard
- 15 exercícios (muitos sobre "onde visualizar" e "qual endpoint usar")
- Reforço Espiral: refs aos Módulos 1-2

**Entrega:** courseText.pt[3] + courseText.en[3]

---

### Fase 5: Módulo 4 — Dados e Arquitetura
**Pesquisar:** Copilot data handling, prompt building, proxy filtering
**Implementar:**
- Lição 4.1: Fluxo de dados (4 tópicos)
- Lição 4.2: Ciclo de vida e limitações (3 tópicos)
- 8 exercícios
- Reforço Espiral: refs aos Módulos 1-2

**Entrega:** courseText.pt[4] + courseText.en[4]

---

### Fase 6: Módulo 5 — Prompt Engineering e Contexto
**Pesquisar:** Copilot context determination, @workspace, #file, chat history
**Implementar:**
- Lição 5.1: Crafting eficaz (4 tópicos)
- Lição 5.2: Performance (3 tópicos)
- 8 exercícios (ênfase em como o contexto é gerenciado)
- Reforço Espiral: refs aos Módulos 2, 4

**Entrega:** courseText.pt[5] + courseText.en[5]

---

### Fase 7: Módulo 6 — Produtividade, Testes e Modernização ⚠️ REFORÇADO
**Pesquisar:** Testing with Copilot, modernize legacy code, refactoring
**Implementar:**
- Lição 6.1: Code generation e modernização (4 tópicos)
- Lição 6.2: Testes e segurança (4 tópicos) — /tests, unit tests, edge cases
- 10 exercícios (cenários de "como gerar teste", "como modernizar")
- Reforço Espiral: refs aos Módulos 1, 2, 5

**Entrega:** courseText.pt[6] + courseText.en[6]

---

### Fase 8: Módulo 7 — Exclusão de Conteúdo e Safeguards ⚠️ MAIS COBRADO
**Pesquisar:** Content exclusion docs (GitHub), propagation, REST API exclusion management
**Implementar:**
- Lição 7.1: Content exclusion config (5 tópicos) — repo, org, enterprise, YAML, fnmatch
- Lição 7.2: Safeguards (3 tópicos) — duplication detection, security warnings
- Lição 7.3: Caminhos e propagação (4 tópicos) — navegação step-by-step, 30 min delay, reload, testar
- 12 exercícios (muitos sobre "qual caminho seguir" e "o que acontece quando")
- Reforço Espiral: refs aos Módulos 2, 3, 4

**Entrega:** courseText.pt[7] + courseText.en[7]

---

### Fase 9: Módulo 8 — Revisão Final
**O que fazer:**
1. Reler TODOS os módulos implementados
2. Compilar: tabela de slash commands, tabela de caminhos admin, decision tree, macetes, checklist
3. Gerar courseText.pt[8] + courseText.en[8]

**Entrega:** Cheat-sheet completo

---

### Fase 10: Módulo 9 — Simulado Final
**O que fazer:**
1. Gerar SIMULADO_QUESTIONS (40 questões) distribuídas por domínio e tipo
2. Gerar courseText.pt[9] e courseText.en[9] (título + content vazio)
3. Validar questionCount = 40

**⚠️ Pode precisar 2 respostas (20 + 20 questões)**

**Entrega:** SIMULADO_QUESTIONS completo

---

### Fase 11: Validação Final
**Checklist:**
- [ ] 10 módulos no COURSE_STRUCTURE, courseText.pt e courseText.en
- [ ] Exercícios: M1=8, M2=12, M3=15, M4=8, M5=8, M6=10, M7=12
- [ ] COURSE_STRUCTURE.exercises.length = courseText exercises.length (cada módulo)
- [ ] CSS e JS copiados integralmente do template
- [ ] Todos os placeholders substituídos
- [ ] SIMULADO_CONFIG.questionCount = 40
- [ ] SIMULADO_QUESTIONS tem match, order, categorize (mín 1 de cada)
- [ ] SIM_STORAGE_KEY = 'gh300_simulado_state'
- [ ] skipExercisesConfirm definido em PT e EN
- [ ] Reforço Espiral aplicado: Módulos 2+ têm 20-30% exercícios intercalados
- [ ] courseText.pt e courseText.en têm estrutura espelhada
- [ ] Arquivo abre corretamente no navegador

---

## Notas de Prioridade (Feedback Real)

> **⚠️ TÓPICOS QUENTES — Confirmados pelo candidato:**
> 1. **Exclusão de conteúdo** — Muitas perguntas sobre como configurar, caminhos (Settings → Copilot → Content exclusion)
> 2. **API e Auditoria** — REST API, audit log events, onde ver insights
> 3. **Gerar testes** — Como usar Copilot para unit tests, /tests
> 4. **Gerenciamento de contexto** — Como o Copilot determina contexto, workspace
> 5. **Evitar viés** — Princípios de IA responsável
> 6. **Modernizar aplicação** — Legacy code modernization
> 7. **Slash commands (/)** — Saber cada comando e quando usar
> 8. **Caminhos de navegação** — "Onde configuro X?"

Esses tópicos receberão **exercícios extras** e **blocos `.exam-confirmed`** nos módulos correspondentes.

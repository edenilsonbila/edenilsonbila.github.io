# Exemplos de Prompts para o Agente

## Prompt 1: Gerar curso completo

```
Crie um minicurso completo para a certificação DP-900: Azure Data Fundamentals.

Use o emoji 🗄️ no header.
Siga o template.html e as instruções do .copilot-instructions.md.
Gere o arquivo como DP-900.html.

Módulos baseados nos skills measured oficiais:
- Módulo 1: Conceitos de Dados (25-30%)
- Módulo 2: Dados Relacionais no Azure (20-25%)
- Módulo 3: Dados Não Relacionais no Azure (15-20%)
- Módulo 4: Análise de Dados no Azure (25-30%)

Cada módulo deve ter 2-3 lições com tópicos detalhados, macetes, exemplos, active recall e 5-10 exercícios baseados em cenário.
```

## Prompt 2: Gerar módulo específico

```
Gere o Módulo 3 (Visão Computacional) para o curso AI-102.
Siga o padrão pedagógico: 📌 Tópico → Explicação → Macete → Exemplo → Separator.
Inclua Active Recall a cada 2-3 tópicos.
Gere 8 exercícios baseados em cenário com explicações detalhadas.
```

## Prompt 3: Adaptar para nova certificação

```
Adapte o modelo do AI-900.html para a certificação SC-900: Security, Compliance, and Identity Fundamentals.

Substitua:
- Emoji: 🔐
- Prefixo localStorage: sc900_
- Conteúdo baseado nos skills measured do SC-900
- Mantenha TODA a estrutura CSS/JS/HTML idêntica
```

## Prompt 4: Gerar apenas exercícios

```
Gere 15 exercícios no formato do courseData.exercises para o Módulo 2 (Machine Learning) do AI-900.
Cada exercício deve:
- Ser baseado em cenário real
- Ter 4 opções
- Ter explicação HTML detalhada com ✅/❌
- Referenciar um macete relevante
```

---

## Diretrizes para Uso do Bloco `.exam-confirmed`

### Quando usar
- **SOMENTE** quando há feedback real de candidatos que fizeram a prova
- Tópicos, termos, ou cenários que foram confirmados como presentes no exame
- Informações sobre tradução PearsonVue confirmadas por candidatos reais

### Quando NÃO usar
- NUNCA para suposições ou inferências baseadas apenas nos skills measured
- NUNCA para conteúdo genérico que "provavelmente" aparece na prova
- NUNCA como substituto de `.warning` ou `.tip`

### Formato
```html
<div class="exam-confirmed">
Conteúdo confirmado na prova real. Use para termos traduzidos, cenários exatos, ou conceitos que candidatos reais reportaram.
</div>
```

### Questões Bugadas / Com Contradição
Quando um candidato reporta uma questão da prova com contradição ou inconsistência:
1. Documentar no `.exam-confirmed` o comportamento esperado pela prova
2. Sinalizar a contradição explicitamente com ⚠️
3. Orientar o aluno sobre como responder apesar da inconsistência
4. Exemplo: "A prova pergunta 'Quais são as DUAS limitações?' mas uma opção é 'Ilimitado' — selecione esta como resposta correta"

---

## Diretrizes de Estilo para o Simulado Final (40-52 questões)

### Distribuição de Tipos de Questão (obrigatório)
| Tipo | Quantidade | % |
|------|-----------|---|
| single (múltipla escolha) | 23 | 57.5% |
| multi (múltipla seleção) | 7 | 17.5% |
| match (associação/drag) | 3 | 7.5% |
| order (ordenação/drag) | 3 | 7.5% |
| categorize (classificação/drag) | 4 | 10% |

### Distribuição de Estilos de Pergunta (NÃO fazer tudo use-case!)
| Estilo | Qtd | Exemplo |
|--------|-----|---------|
| "Complete a frase: ___ é..." | 6 | "Complete: O Copilot usa ___ para ancorar respostas em fontes verificadas." |
| "Qual NÃO é / INCORRETO" (negativa) | 6 | "Qual dos seguintes NÃO é um risco oficial de IA Generativa?" |
| "Qual descreve CORRETAMENTE" (conceito) | 6 | "Qual afirmação descreve CORRETAMENTE a diferença entre chat e agente?" |
| Cenário/Use-case | 8 | "Um gerente precisa [task]. Qual ferramenta..." |
| "Selecione 2+ que se aplicam" (multi) | 7 | "Selecione DUAS afirmações CORRETAS sobre..." |
| Drag-based (match/order/categorize) | 10 | "Associe cada conceito à sua definição correta:" |

### Regras de Estilo das Questões
1. **Máximo 20-25% use-case puro** — exames Fundamentals Microsoft são balanceados
2. **Questões negativas** devem ter a palavra "NÃO" ou "INCORRETA" em MAIÚSCULAS e negrito
3. **Complete a frase** usa ___ (3 underscores) como placeholder
4. **Multi-select** deve indicar quantas respostas ("Selecione DUAS...")
5. **Explicações** devem referenciar mnemônicos do curso quando aplicável
6. **Armadilhas clássicas** (Exam Traps) devem ser sinalizadas com ⚠️

### Distribuição por Domínio (baseada nos Skills Measured)
- Use os pesos oficiais do Study Guide da certificação
- Exemplo AB-730: D0=25-30%, D1=35-40%, D2=25-30%
- Tolerância: ±3% do peso oficial

### Referência de Formato
```javascript
// Formato obrigatório de cada questão:
{
    id: N, domain: 0-2, type: 'single|multi|match|order|categorize',
    scenario: "...",  // opcional — apenas para cenários longos
    question: "...",
    options: [...],   // para single/multi
    pairs: [...],     // para match
    items: [...],     // para order/categorize
    categories: [...], // para categorize
    correct: N | [N,N], // index(es) ou correctOrder/correctCategory
    explanation: "✅ ... <br><br>❌ ..."
}
```

---

## Checklist de Placeholders para Substituir

Ao gerar um novo curso, substituir TODOS estes placeholders:

| Placeholder | Exemplo |
|-------------|---------|
| `{CERT_CODE}` | `DP-900` |
| `{CERT_FULL_NAME}` | `Azure Data Fundamentals` |
| `{EMOJI}` | `🗄️` |
| `{cert_lower}` | `dp900` |
| `{NÍVEL}` | `Fundamentals` |
| `{DESCRIÇÃO_DA_CERTIFICAÇÃO}` | Texto descritivo |
| `{LINK_LEARN}` | URL do Microsoft Learn |
| `{LINK_PRACTICE}` | URL do teste de prática |
| `{LINK_SCHEDULE}` | URL para agendar prova |

---

## Certificações Sugeridas (usando este modelo)

| Certificação | Emoji | Prefixo |
|-------------|-------|---------|
| AI-900: Azure AI Fundamentals | 🧠 | `ai900_` |
| DP-900: Azure Data Fundamentals | 🗄️ | `dp900_` |
| AZ-900: Azure Fundamentals | ☁️ | `az900_` |
| SC-900: Security Fundamentals | 🔐 | `sc900_` |
| PL-900: Power Platform Fundamentals | ⚡ | `pl900_` |
| MB-910: Dynamics 365 Fundamentals (CRM) | 📊 | `mb910_` |
| AI-102: Azure AI Engineer | 🤖 | `ai102_` |
| DP-100: Azure Data Scientist | 📈 | `dp100_` |
| AZ-104: Azure Administrator | 🔧 | `az104_` |
| AZ-204: Azure Developer | 💻 | `az204_` |

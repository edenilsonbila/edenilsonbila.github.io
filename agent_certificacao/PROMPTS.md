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

# 09 — Métricas de UX

> *"O que não é medido não é gerenciado."* — Peter Drucker

---

## 🎯 Objetivos de Aprendizagem

- Entender por que medir UX é fundamental
- Conhecer o framework HEART e como aplicá-lo
- Calcular e interpretar o SUS (System Usability Scale)
- Compreender NPS e CSAT no contexto de UX
- Identificar métricas comportamentais e de produto

---

## 1. Por Que Medir UX?

Sem métricas, UX é apenas opinião. Métricas permitem:
- Justificar investimentos em design para a liderança
- Identificar prioridades de melhoria com dados
- Acompanhar o impacto de mudanças ao longo do tempo
- Comparar com benchmarks da indústria

### A Armadilha das Métricas de Vaidade

| Métrica de Vaidade ❌ | Métrica Acionável ✅ |
|----------------------|---------------------|
| Número de downloads | Taxa de retenção D7 (volta após 7 dias?) |
| Pageviews | Taxa de conclusão de tarefas-chave |
| Likes e shares | NPS e satisfação real |
| Tempo no site | Eficiência na tarefa (menos tempo = melhor?) |

---

## 2. Framework HEART (Google)

O Google desenvolveu o framework **HEART** para ajudar a escolher métricas de UX que realmente importam.

### As 5 Dimensões

| Dimensão | Significado | Perguntas-chave |
|----------|-------------|-----------------|
| **H**appiness | Satisfação e atitudes do usuário | Os usuários gostam de usar o produto? |
| **E**ngagement | Nível de envolvimento | Com que frequência e profundidade usam? |
| **A**doption | Novos usuários que adotam | Quantos experimentam novos recursos? |
| **R**etention | Usuários que continuam usando | Eles voltam? |
| **T**ask Success | Taxa de conclusão de tarefas | Conseguem fazer o que querem? |

### Processo GSM (Goals — Signals — Metrics)

Para cada dimensão HEART:
1. **Goal:** O que você quer alcançar?
2. **Signal:** Como o comportamento do usuário reflete esse goal?
3. **Metric:** Como quantificar esse signal?

**Exemplo para um app de banco:**

| Dimensão | Goal | Signal | Metric |
|----------|------|--------|--------|
| Happiness | Usuários satisfeitos | Resposta a pesquisa pós-uso | SUS ≥ 80 |
| Engagement | Uso frequente de features | Login diário | DAU/MAU ≥ 40% |
| Adoption | Novos usuários ativam PIX | Primeira transação PIX | % novos users que fazem PIX em 7 dias |
| Retention | Usuários voltam todo mês | Login mensal | Retenção M1 ≥ 70% |
| Task Success | Transferência bem-sucedida | Transferência concluída | Taxa de conclusão ≥ 95% |

---

## 3. System Usability Scale (SUS)

O **SUS** é o questionário de satisfação mais usado no mundo. Criado por John Brooke em 1986, consiste em 10 perguntas com escala Likert de 5 pontos.

### O Questionário

Responda de 1 (Discordo totalmente) a 5 (Concordo totalmente):

| # | Item |
|---|------|
| 1 | Eu gostaria de usar este sistema com frequência |
| 2 | Achei o sistema desnecessariamente complexo |
| 3 | Achei o sistema fácil de usar |
| 4 | Precisaria de apoio técnico para usar este sistema |
| 5 | Achei que as funções do sistema estavam bem integradas |
| 6 | Achei que havia muita inconsistência neste sistema |
| 7 | Imagino que a maioria das pessoas aprenderia a usar este sistema rapidamente |
| 8 | Achei o sistema muito complicado de usar |
| 9 | Me senti confiante usando este sistema |
| 10 | Precisei aprender muitas coisas antes de conseguir usar este sistema |

### Como Calcular

1. Para itens ímpares (1, 3, 5, 7, 9): `pontuação = valor - 1`
2. Para itens pares (2, 4, 6, 8, 10): `pontuação = 5 - valor`
3. Some os 10 valores ajustados
4. Multiplique por 2.5

**Resultado:** 0 a 100

### Interpretação do SUS

| Pontuação | Grau | Classificação | Aceitabilidade |
|-----------|------|---------------|----------------|
| ≥ 90 | A+ | Excelente | Aceitável |
| 80–89 | A/B | Bom | Aceitável |
| 70–79 | C | OK | Marginal |
| 60–69 | D | Ruim | Marginal |
| < 60 | F | Péssimo | Inaceitável |

**Benchmark da indústria:** média global ≈ 68 pontos

---

## 4. Net Promoter Score (NPS)

**Uma pergunta:** "De 0 a 10, qual a probabilidade de você recomendar [produto] para um amigo ou colega?"

### Segmentação

```
0–6:   Detratores   (insatisfeitos, podem prejudicar a marca)
7–8:   Passivos     (satisfeitos mas não entusiasmados)
9–10:  Promotores   (entusiastas, recomendam ativamente)

NPS = % Promotores - % Detratores
```

### Benchmarks de NPS por Setor (2024)

| Setor | NPS Médio |
|-------|-----------|
| Tech (SaaS) | 41 |
| Bancos digitais | 62 |
| E-commerce | 45 |
| Saúde | 27 |
| Telecom | -1 |

**Cuidado:** NPS mede lealdade, não usabilidade. Um produto pode ter NPS alto mas ter problemas sérios de UX.

---

## 5. CSAT — Customer Satisfaction Score

**Uma pergunta:** "Quão satisfeito você ficou com [experiência específica]?"

Escala de 1 a 5 (ou 1 a 10) após uma interação específica.

```
CSAT = (Respostas positivas / Total de respostas) × 100
```

**Quando usar:** após uma interação específica (atendimento, conclusão de tarefa, onboarding).

---

## 6. Métricas Comportamentais e de Produto

### Métricas de Eficiência

| Métrica | Como medir | O que indica |
|---------|------------|--------------|
| **Tempo na tarefa** | Cronometrar usuário | Eficiência do fluxo |
| **Número de cliques** | Analytics / teste | Caminhos desnecessários |
| **Taxa de erro** | Erros / total de tentativas | Clareza da interface |
| **Taxa de conclusão** | Tarefas concluídas / tentadas | Eficácia geral |

### Métricas de Negócio com Impacto de UX

| Métrica | Impacto de UX |
|---------|---------------|
| **Churn rate** | UX ruim aumenta churn |
| **Conversão** | UX bom aumenta conversão |
| **ARPU** (receita por usuário) | Features bem desenhadas aumentam uso |
| **CAC** (custo de aquisição) | Boca a boca de promotores reduz CAC |
| **LTV** (lifetime value) | Retenção via UX aumenta LTV |

### Core Web Vitals (Google)

Métricas técnicas de performance que afetam a experiência:

| Métrica | Significado | Meta |
|---------|-------------|------|
| **LCP** (Largest Contentful Paint) | Tempo para o maior elemento carregar | < 2.5s |
| **FID** (First Input Delay) | Tempo de resposta ao primeiro clique | < 100ms |
| **CLS** (Cumulative Layout Shift) | Estabilidade visual durante carregamento | < 0.1 |

---

## 7. Combinando Métricas — Um Dashboard de UX

Um bom dashboard de UX combina:

```
┌─────────────────────────────────────────────────────┐
│              DASHBOARD DE UX — App Banco            │
├─────────────────┬───────────────┬───────────────────┤
│  SATISFAÇÃO     │  COMPORTAMENTO│  NEGÓCIO          │
│                 │               │                   │
│  NPS: 72 ✅     │  Taxa de      │  Churn mensal:    │
│  (meta: 70)     │  conclusão    │  2.1% ✅           │
│                 │  PIX: 94% ✅  │  (meta: <3%)       │
│  SUS: 81 ✅     │               │                   │
│  (meta: 80)     │  Tempo médio  │  Conversão        │
│                 │  transferência│  onboarding:      │
│  CSAT suporte:  │  : 47s ⚠️    │  68% ⚠️           │
│  78% ⚠️        │  (meta: <40s) │  (meta: 75%)       │
└─────────────────┴───────────────┴───────────────────┘
```

---

## 🛠️ Práticas

### Prática 1 — Aplicar e Calcular o SUS (30 min)
1. Escolha um app que você usa com frequência
2. Aplique o questionário SUS para você mesmo
3. Aplique para 2 colegas que também usam o app
4. Calcule o SUS médio
5. Compare com o benchmark da indústria
6. Qual seria a recomendação de melhoria mais urgente?

### Prática 2 — Criar um Dashboard HEART (60 min)
Escolha um produto digital (real ou fictício).
1. Para cada dimensão HEART, defina: Goal, Signal e Metric
2. Defina as metas (targets) para cada métrica
3. Identifique onde você buscaria os dados (analytics, survey, observação)
4. Apresente para a turma

### Prática 3 — Análise de NPS Qualitativo (45 min)
Colete NPS de um serviço digital (pode ser a ferramenta da universidade — portais, sistemas etc.):
1. Colete ao menos 10 respostas (nota + comentário)
2. Categorize os promotores, passivos e detratores
3. Analise os comentários: quais são os temas mais frequentes?
4. Proponha 2 ações baseadas nos dados

---

## ✅ Checklist de Métricas de UX

- [ ] As métricas estão alinhadas com os objetivos do negócio e do usuário?
- [ ] Você tem pelo menos uma métrica de satisfação (SUS, NPS, CSAT)?
- [ ] Você tem pelo menos uma métrica comportamental (taxa de conclusão, tempo)?
- [ ] As metas (targets) estão definidas para cada métrica?
- [ ] As métricas são medidas regularmente (não apenas no lançamento)?
- [ ] Os dados são compartilhados com toda a equipe de produto?
- [ ] Você combina dados quantitativos com insights qualitativos?

---

## 📖 Referências

- RODDEN, Kerry et al. *Measuring the User Experience on a Large Scale: User-Centered Metrics for Web Applications*. Google, CHI 2010.
- BROOKE, John. *SUS: A Quick and Dirty Usability Scale*. 1996.
- Nielsen Norman Group — UX Metrics: [https://www.nngroup.com/articles/ux-metrics/](https://www.nngroup.com/articles/ux-metrics/)
- HEART Framework: [https://research.google/pubs/measuring-the-user-experience-on-a-large-scale/](https://research.google/pubs/measuring-the-user-experience-on-a-large-scale/)

---

[← Módulo anterior](../08-testes-usabilidade/README.md) | [Próximo módulo →](../10-etica-design/README.md)

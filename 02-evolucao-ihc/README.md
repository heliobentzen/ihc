# 02 — Evolução da IHC para o Design Centrado no Usuário

> *"Qualquer produto que precise de um manual para funcionar está quebrado."* — Elon Musk

---

## 🎯 Objetivos de Aprendizagem

- Compreender a história da Interação Humano-Computador
- Identificar as principais paradigmas e viradas conceituais
- Entender o que é Design Centrado no Usuário (DCU / UCD)
- Aplicar o processo iterativo de DCU em projetos reais

---

## 1. Linha do Tempo da IHC

### Era 1: Computação em Batch (1940–1960)
- Sem interação em tempo real
- Cartões perfurados e operações em lote
- Usuários = especialistas técnicos (só eles usavam computadores)

### Era 2: Linha de Comando (1960–1980)
- Terminal e teclado como única interface
- Curva de aprendizado enorme
- Primeiros estudos sobre **ergonomia cognitiva**
- **1963:** Ivan Sutherland cria o Sketchpad (1ª interface gráfica interativa)

### Era 3: Interface Gráfica — GUI (1980–1995)
- **1973:** Xerox PARC cria o Alto (ícones, janelas, mouse)
- **1984:** Apple Macintosh lança o modelo para o grande público
- **1985:** Microsoft Windows 1.0
- WIMP: **W**indows, **I**cons, **M**enus, **P**ointer
- Início dos estudos sistemáticos de usabilidade

### Era 4: Web e Multimídia (1990–2005)
- **1991:** Tim Berners-Lee cria a World Wide Web
- Explosão de informação — necessidade de arquitetura de informação
- **1994:** Jakob Nielsen publica as Heurísticas
- **1999:** Livro *The Inmates Are Running the Asylum* (Alan Cooper) — foco em personas

### Era 5: Móvel e Touch (2007–2015)
- **2007:** iPhone redefine o paradigma de interação
- Gestos multitouch substituem mouse e teclado
- Design responsivo torna-se necessidade
- **2013:** Google lança Material Design

### Era 6: Ubíqua e Conversacional (2015–hoje)
- Assistentes de voz (Siri, Alexa, Google Assistant)
- IoT — interfaces em geladeiras, carros, relógios
- Realidade Aumentada e Virtual
- IA generativa muda o design de interfaces (2022–)

---

## 2. Principais Paradigmas de Interação

| Paradigma | Período | Exemplo |
|-----------|---------|---------|
| Batch | 1940–60 | Cartões perfurados |
| Linha de comando | 1960–80 | Terminal Unix |
| WIMP / GUI | 1980–00 | Windows, macOS |
| Direto (touch) | 2007+ | iPhone, iPad |
| Voz | 2010+ | Alexa, Google Home |
| Realidade mista | 2015+ | HoloLens, Apple Vision Pro |
| Conversacional IA | 2022+ | ChatGPT, Copilot |

---

## 3. O Que é Design Centrado no Usuário (DCU)?

O DCU (ou **UCD — User-Centered Design**) é uma filosofia e um processo em que as necessidades, objetivos e limitações dos usuários finais são considerados em cada fase do processo de design.

### Princípios Fundamentais (ISO 9241-210)

1. **O design é baseado em compreensão explícita** dos usuários, tarefas e ambientes
2. **Os usuários são envolvidos** durante o design e o desenvolvimento
3. **O design é conduzido e refinado** por avaliações centradas no usuário
4. **O processo é iterativo**
5. **O design aborda toda a experiência** do usuário
6. **A equipe de design é multidisciplinar**

---

## 4. O Processo DCU — O Ciclo das 4 Fases

```
        ┌──────────────────────────────────────┐
        │                                      │
        ▼                                      │
  ┌──────────┐    ┌──────────┐    ┌──────────┐ │
  │ Entender │───►│ Especifi-│───►│ Projetar │ │
  │ contexto │    │  car     │    │          │ │
  └──────────┘    └──────────┘    └──────────┘ │
                                       │       │
                                       ▼       │
                                 ┌──────────┐  │
                                 │ Avaliar  │──┘
                                 └──────────┘
                                 (se não atender
                                  requisitos,
                                  iterar)
```

### Fase 1 — Entender o Contexto de Uso
- Quem são os usuários?
- Quais são as suas tarefas?
- Qual é o ambiente físico, social e tecnológico?

**Técnicas:** observação etnográfica, entrevistas contextuais, análise de tarefas

### Fase 2 — Especificar Requisitos
- Converter insights em requisitos de design
- Definir critérios de sucesso

**Entregáveis:** personas, cenários de uso, user stories

### Fase 3 — Produzir Soluções de Design
- Criar protótipos (baixa → alta fidelidade)
- Explorar múltiplas alternativas antes de convergir

**Entregáveis:** sketches, wireframes, protótipos interativos

### Fase 4 — Avaliar o Design
- Testar com usuários reais
- Avaliar heurísticas
- Medir contra critérios de sucesso

**Técnicas:** teste de usabilidade, avaliação heurística, eye-tracking

---

## 5. DCU vs. Outras Abordagens

| Abordagem | Foco | Problema |
|-----------|------|---------|
| **Tech-centered** | Viabilidade técnica | Ignora o usuário |
| **Business-centered** | ROI, velocidade | Sacrifica UX por métricas |
| **Designer-centered** | Estética, criatividade | Projeta para si, não para o usuário |
| **User-centered (DCU)** | Necessidades reais do usuário | Mais lento, mas mais eficaz a longo prazo |
| **Human-centered (HCD)** | Impacto humano amplo (inclui sociedade) | Escopo ainda mais amplo |

---

## 6. Estudos de Caso

### Caso 1: Healthcare.gov (2013) — Como NÃO fazer
- Site lançado sem testes adequados com usuários
- 500 milhões de dólares investidos
- No lançamento: travava, erros, confusão total
- **Lição:** Agilidade técnica sem DCU = desastre

### Caso 2: GOV.UK — Como fazer certo
- Governo britânico adotou explicitamente o DCU
- Princípio: "Start with user needs, not government needs"
- Reduziram 1.700 sites governamentais para 1
- Economia de £61.5 milhões/ano
- **Lição:** DCU escala. Desde sites pessoais até governo nacional.

### Caso 3: Nubank — Simplificação radical
- Incumbentes bancários tinham apps confusos, cheios de menus
- Nubank partiu do princípio: "O que o usuário realmente precisa fazer?"
- Interface minimalista, onboarding simples, linguagem humana
- De 0 a 80 milhões de clientes em ~10 anos
- **Lição:** Entender o usuário é vantagem competitiva

---

## 🛠️ Práticas

### Prática 1 — Arqueologia de Interface (30 min)
1. Encontre capturas de tela antigas de um produto digital (ex: Facebook 2004, Google 2000, site de banco dos anos 2000)
2. Compare com a versão atual
3. Liste 5 evoluções que refletem aprendizados sobre o usuário
4. Identifique qual paradigma de interação cada versão pertence

### Prática 2 — Mapa de Empatia Rápido (45 min)
Escolha um familiar não-técnico (avó, pai, tio...) e observe ele tentando usar um app de banco.
Preencha o mapa:
```
┌────────────────────────────────────────────────────┐
│                    PENSA E SENTE                   │
│         (medos, aspirações, preocupações)          │
├──────────────────┬─────────────────────────────────┤
│      VÊ          │            OUVE                  │
│  (ambiente,      │   (amigos, influenciadores,      │
│  mercado)        │    mídia)                        │
├──────────────────┴─────────────────────────────────┤
│                  FALA E FAZ                         │
│           (comportamento público)                   │
├────────────────────┬───────────────────────────────┤
│      DORES         │         GANHOS                 │
│  (frustrações,     │  (desejos, medidas de          │
│   obstáculos)      │   sucesso)                     │
└────────────────────┴───────────────────────────────┘
```

### Prática 3 — Mini Ciclo DCU (2 horas em grupo)
**Desafio:** Redesenhe o fluxo de cadastro de um app fictício de academia.

Etapas:
1. **Entender** (20 min): Entreviste 2 colegas sobre suas frustrações com apps de academia
2. **Especificar** (20 min): Crie 1 persona e liste os 5 requisitos mais importantes
3. **Projetar** (40 min): Faça um wireframe em papel com no máximo 4 telas
4. **Avaliar** (40 min): Peça para 2 colegas realizarem o cadastro no papel (teste de papel), anote as dificuldades

---

## ✅ Checklist — Seu Processo é Centrado no Usuário?

- [ ] Você entrevistou usuários reais antes de começar a projetar?
- [ ] Suas personas são baseadas em dados, não em suposições?
- [ ] Você iterou o design pelo menos 2 vezes com base em feedback?
- [ ] Usuários reais testaram o produto antes do lançamento?
- [ ] A equipe inclui perspectivas multidisciplinares?
- [ ] Os critérios de sucesso são definidos do ponto de vista do usuário?
- [ ] Você considera o contexto de uso (dispositivo, ambiente, estado emocional)?

---

## 📖 Referências

- ISO 9241-210:2019 — Ergonomics of human-system interaction
- NORMAN, Don. *The Design of Everyday Things*. Basic Books, 2013.
- COOPER, Alan. *The Inmates Are Running the Asylum*. Sams, 1999.
- GOV.UK Design Principles: [https://www.gov.uk/guidance/government-design-principles](https://www.gov.uk/guidance/government-design-principles)
- IDEO — Design Thinking: [https://designthinking.ideo.com](https://designthinking.ideo.com)

---

[← Módulo anterior](../01-fundamentos-ux-ui/README.md) | [Próximo módulo →](../03-product-discovery/README.md)

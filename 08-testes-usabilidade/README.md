# 08 — Testes de Usabilidade

> *"Teste com um usuário é 100% melhor que não testar com nenhum."* — Jakob Nielsen

---

## 🎯 Objetivos de Aprendizagem

- Compreender quando e por que realizar testes de usabilidade
- Planejar um teste de usabilidade completo
- Conduzir uma sessão de teste de usabilidade
- Analisar e sintetizar resultados de testes
- Distinguir testes moderados de não-moderados

---

## 1. O Que é um Teste de Usabilidade?

Um **teste de usabilidade** é uma técnica de avaliação em que representantes do público-alvo realizam tarefas reais usando o produto enquanto são observados por pesquisadores.

**Objetivo:** descobrir onde e por que o produto é difícil de usar — antes que isso afete usuários em produção.

### O Que um Teste NÃO é

| ❌ NÃO é | ✅ É |
|---------|------|
| Uma pesquisa de satisfação | Uma observação de comportamento |
| Um questionário | Uma sessão de tarefas reais |
| Um teste do usuário | Um teste do produto |
| Um focus group | Uma sessão 1:1 com tarefas específicas |
| Uma forma de mostrar que o design está correto | Uma forma de encontrar problemas |

---

## 2. Quantos Usuários São Necessários?

### A Curva de Nielsen

Jakob Nielsen descobriu que **5 usuários detectam ~85% dos problemas** de usabilidade. Isso porque os problemas se repetem depois do 5º usuário.

```
% de problemas
encontrados
    │
100%│                              ████████████
 85%│               ██████████████
 70%│          ████
 50%│     ████
    │  ██
    └─────────────────────────────────────────
       1    2    3    4    5    6    7    8
                              Número de usuários
```

**Recomendação prática:**
- **Exploratório (qualitativo):** 5 usuários por rodada
- **Estudo quantitativo:** mínimo 20–30 por grupo
- **A/B Test:** depende do tráfego e da métrica

---

## 3. Tipos de Testes de Usabilidade

### Por Moderação

| Tipo | Vantagens | Desvantagens |
|------|-----------|--------------|
| **Moderado (presencial)** | Profundo, pode aprofundar, observa linguagem corporal | Caro, lento, viés do facilitador |
| **Moderado (remoto)** | Mais participantes, geografias diversas | Sem linguagem corporal, problemas técnicos |
| **Não-moderado (remoto)** | Escala, rápido, barato, sem viés | Sem aprofundamento, qualidade variável |

### Por Objetivo

| Tipo | Objetivo | Quando usar |
|------|----------|-------------|
| **Exploratório** | Entender comportamentos e motivações | Início do projeto |
| **Formativo** | Identificar problemas durante o design | Ao longo do desenvolvimento |
| **Somativo** | Medir performance contra benchmarks | Antes do lançamento |
| **Comparativo** | Comparar A vs B | Decisões de design difíceis |
| **Benchmark** | Estabelecer linha de base | Antes de redesign |

---

## 4. Planejamento do Teste

### 4.1 Plano de Teste (Test Plan)

**Seções obrigatórias:**

```markdown
# Plano de Teste de Usabilidade

## Objetivo
O que queremos aprender com este teste?
Ex: "Identificar problemas no fluxo de checkout do app mobile"

## Questões de Pesquisa
1. Os usuários conseguem encontrar o botão de checkout?
2. A etapa de seleção de endereço é clara?
3. Os usuários compreendem as opções de frete?

## Participantes
- Perfil: mulheres, 25–45 anos, compram online 1x/mês ou mais
- Quantidade: 6 participantes
- Recrutamento: painel de usuários + rede interna

## Tarefas
[ver seção abaixo]

## Métricas
- Taxa de conclusão de tarefa
- Tempo por tarefa
- Número de erros
- SUS (System Usability Scale)

## Logística
- Data/hora: [...]
- Ferramenta: Maze / UserTesting / presencial
- Protótipo: [link]
```

### 4.2 Criando Boas Tarefas

**Características de boas tarefas:**
- **Realistas:** baseadas em cenários reais de uso
- **Inequívocas:** não sugerem como fazer, apenas o que fazer
- **Mensuráveis:** sucesso/fracasso claramente definíveis
- **Focadas:** uma coisa por vez

**Estrutura de tarefa com cenário:**
```
Contexto: "Você acabou de se mudar para uma nova cidade e quer 
          pedir uma pizza para o jantar."
          
Tarefa: "Usando o app, encontre uma pizzaria próxima, 
        escolha uma pizza de sua preferência e finalize o pedido."
        
Critério de sucesso: Usuário chega à tela de confirmação de pedido.
```

**Exemplos bons e ruins:**

| ❌ Ruim | ✅ Bom |
|---------|--------|
| "Clique no botão de 'Adicionar ao Carrinho'" | "Imagine que você quer comprar esta camiseta" |
| "Vá para a seção de Ajuda" | "Você recebeu uma cobrança indevida — o que você faria?" |
| "Como você se sentiria usando este app?" | "Tente pagar uma conta de luz usando o app" |

---

## 5. Conduzindo a Sessão

### Roteiro de Abertura (5 min)

```
"Obrigado por participar. Hoje vamos testar um produto,
não você. Não há respostas certas ou erradas.

Sua honestidade é o mais valioso para nós. Se algo 
parecer confuso ou difícil, é informação útil.

Enquanto realiza as tarefas, por favor fale em voz alta
o que está pensando — isso nos ajuda muito a entender.

Posso gravar esta sessão para análise interna? [aguarda resposta]

Tem alguma dúvida antes de começarmos?"
```

### Durante a Sessão — Regras do Facilitador

**Faça:**
- ✅ Observe em silêncio
- ✅ Anote comportamentos (não apenas falas)
- ✅ Faça perguntas abertas: "O que você esperava que acontecesse?"
- ✅ Aguarde pelo menos 10 segundos de silêncio antes de intervir
- ✅ Use "E daí?" para aprofundar

**Evite:**
- ❌ Ajudar o participante (mesmo que ele esteja perdido)
- ❌ Demonstrar aprovação/reprovação facial
- ❌ Perguntas que sugerem a resposta ("Você achou confuso, né?")
- ❌ Defender o design ("Ah, na verdade esse botão é para…")

### Lidando com Participante Travado

Quando o participante está completamente preso (>3 minutos):

> "Sem problemas, vamos seguir para a próxima tarefa. Sua dificuldade aqui já é informação valiosa."

---

## 6. Análise e Síntese

### 6.1 Rainbow Spreadsheet

Técnica para consolidar achados de múltiplas sessões:

```
┌──────────────────┬───────┬───────┬───────┬───────┬───────┐
│ Observação       │ P1    │ P2    │ P3    │ P4    │ P5    │
├──────────────────┼───────┼───────┼───────┼───────┼───────┤
│ Não encontrou    │ ❌    │ ❌    │       │ ❌    │       │
│ o botão Checkout │       │       │       │       │       │
├──────────────────┼───────┼───────┼───────┼───────┼───────┤
│ Confusão com     │       │ ❌    │ ❌    │ ❌    │ ❌    │
│ opções de frete  │       │       │       │       │       │
└──────────────────┴───────┴───────┴───────┴───────┴───────┘
```

### 6.2 Affinity Diagram

1. Escreva cada observação em um post-it
2. Agrupe os post-its por tema
3. Nomeie cada grupo
4. Identifique os temas com mais ocorrências

### 6.3 Priorizando os Problemas

| Problema | Frequência | Impacto | Prioridade |
|----------|-----------|---------|------------|
| Botão checkout invisível | 3/5 | Alto | 🔴 Alta |
| Confusão com frete | 4/5 | Médio | 🟠 Média-Alta |
| Typo na página | 1/5 | Baixo | 🟡 Baixa |

---

## 7. Ferramentas de Teste de Usabilidade

| Ferramenta | Tipo | Destaque |
|------------|------|----------|
| **Maze** | Não-moderado | Integração com Figma, analytics automático |
| **UserTesting** | Moderado + não-mod. | Painel grande, vídeo com highlights de IA |
| **Lookback** | Moderado remoto | Sessões ao vivo, multi-participante |
| **Hotjar** | Análise de sessão | Heatmaps, gravações de sessão real |
| **FullStory** | Análise de sessão | Session replay com busca avançada |
| **UsabilityHub** | Não-moderado | Testes rápidos (5 segundos, preferência) |
| **Optimal Workshop** | IA/Card sorting | Tree testing, card sorting |
| **Zoom** | Moderado remoto | Gravação, compartilhamento de tela |

---

## 🛠️ Práticas

### Prática 1 — Teste de Guerrilha (45 min)

1. Escolha um app de banco no seu celular
2. Elabore 3 tarefas (ex: "Consulte seu extrato dos últimos 7 dias")
3. Aborde 3 pessoas no campus (ou em casa) — explique que é um trabalho
4. Observe e anote os problemas sem ajudar
5. Compile os resultados em uma tabela de observações

### Prática 2 — Sessão Moderada Simulada (90 min)

Em trios (facilitador, usuário, observador):
1. **Facilitador** prepara roteiro de 3 tarefas para um app de e-commerce
2. **Usuário** realiza as tarefas fazendo think aloud
3. **Observador** anota comportamentos não-verbais
4. Rotação: cada um joga um papel diferente
5. Debriefing final: o que foi difícil de facilitar? O que surpreendeu?

### Prática 3 — Análise com Affinity Diagram (60 min)

Com base nos dados da Prática 1 ou 2:
1. Escreva cada observação em um post-it (físico ou Miro/FigJam)
2. Agrupe por tema
3. Identifique os 3 problemas mais críticos
4. Para cada problema, proponha uma solução e estime o impacto

---

## ✅ Checklist de Teste de Usabilidade

**Planejamento:**
- [ ] Objetivo do teste definido
- [ ] Questões de pesquisa listadas
- [ ] Perfil dos participantes definido
- [ ] Tarefas baseadas em cenários reais
- [ ] Critérios de sucesso definidos para cada tarefa
- [ ] Roteiro de moderação preparado

**Execução:**
- [ ] Participante assinou termo de consentimento
- [ ] Gravação iniciada (com permissão)
- [ ] Facilitador está em modo de observação (não de ajuda)
- [ ] Observador(es) presentes

**Análise:**
- [ ] Todos os achados documentados
- [ ] Problemas priorizados por frequência e impacto
- [ ] Recomendações concretas para cada problema

---

## 📖 Referências

- KRUG, Steve. *Rocket Surgery Made Easy*. New Riders, 2009.
- NIELSEN, Jakob. *Why You Only Need to Test with 5 Users*. Nielsen Norman Group, 2000.
- PORTIGAL, Steve. *Interviewing Users*. Rosenfeld Media, 2013.
- Maze Blog: [https://maze.co/blog/](https://maze.co/blog/)

---

[← Módulo anterior](../07-design-systems/README.md) | [Próximo módulo →](../09-metricas-ux/README.md)

# 03 — Product Discovery e Pesquisa com Usuários

> *"Se eu tivesse perguntado às pessoas o que elas queriam, elas teriam dito cavalos mais rápidos."* — (atribuído a Henry Ford, mas a lição vale: entenda o problema, não a solução)

---

## 🎯 Objetivos de Aprendizagem

- Entender o que é Product Discovery e por que ele existe
- Conhecer as principais técnicas de pesquisa com usuários
- Criar personas, mapas de empatia e jornadas do usuário
- Distinguir pesquisa qualitativa de quantitativa
- Planejar e conduzir uma entrevista com usuário

---

## 1. O Que é Product Discovery?

**Product Discovery** é o conjunto de atividades que ajudam uma equipe de produto a entender **qual problema resolver** antes de começar a construir a solução.

### O Duplo Diamante

```
   Problema           Solução
       │                 │
  ◄────┼────►       ◄────┼────►
 Diverge│Converge Diverge│Converge
       │                 │
  Descoberta       Definição        Desenvolvimento     Entrega
  (Pesquisa)      (Síntese)        (Prototipação)      (Teste)
```

**1º Diamante:** Descobrir o problema certo  
**2º Diamante:** Criar a solução certa para o problema

---

## 2. Por Que Fazer Discovery?

### O Cemitério de Produtos 💀

Segundo o CB Insights, as principais razões de startups falharem:
- **42%** → Não havia mercado/necessidade real para o produto
- **17%** → Produto sem modelo de negócio
- **14%** → Ignoraram feedback de clientes

**Discovery evita que você construa a coisa errada de forma perfeita.**

---

## 3. Pesquisa Qualitativa vs. Quantitativa

| Aspecto | Qualitativa | Quantitativa |
|---------|-------------|--------------|
| **Pergunta** | *Por que?* e *Como?* | *Quantos?* e *Com que frequência?* |
| **Dados** | Texto, áudio, vídeo, observações | Números, estatísticas |
| **Amostra** | Pequena (5–20 pessoas) | Grande (100+ pessoas) |
| **Técnicas** | Entrevistas, observação, guerrilha | Surveys, analytics, A/B test |
| **Resultado** | Insights profundos, contexto | Padrões, tendências, validação |
| **Quando usar** | Explorar o desconhecido | Validar hipóteses |

> **Regra de ouro:** Use qualitativa para descobrir o que perguntar. Use quantitativa para confirmar o que descobriu.

---

## 4. Principais Técnicas de Pesquisa

### 4.1 Entrevistas com Usuários

A técnica mais poderosa do arsenal do pesquisador. Conversa estruturada (ou semi-estruturada) para entender comportamentos, motivações e frustrações.

**Tipos:**
- **Estruturada:** roteiro fixo, boa para comparar respostas
- **Semi-estruturada:** roteiro guia, permite aprofundamento
- **Contextual:** ocorre no ambiente natural do usuário

**Dicas de ouro para entrevistas:**
1. Nunca pergunte sobre o futuro ("Você usaria?") — pergunte sobre o passado ("Quando foi a última vez que você…?")
2. Siga o "Método 5 Porquês": aprofunde cada resposta perguntando "Por quê?" repetidamente
3. Fique confortável com o silêncio — ele produz respostas mais honestas
4. Não venda sua ideia. Você está ali para aprender, não para convencer.
5. Grave (com permissão) e transcreva depois

**Roteiro modelo:**
```
ABERTURA (5 min)
- Apresentação e objetivo da entrevista
- Pedir permissão para gravar
- "Não há respostas certas ou erradas"

AQUECIMENTO (5 min)
- Conte-me um pouco sobre você e o que você faz no dia a dia
- Com que frequência você usa [categoria do produto]?

NÚCLEO (30–40 min)
- Me conta a última vez que você [fez a tarefa relevante]...
- O que foi mais difícil nesse processo?
- Como você resolve isso hoje? Me mostra?
- O que te frustra nessa solução atual?
- Se você tivesse uma varinha mágica, o que mudaria?

ENCERRAMENTO (5 min)
- Há algo que eu não perguntei mas que você acha relevante?
- Posso entrar em contato se tiver dúvidas?
```

### 4.2 Surveys e Questionários

Coleta de dados estruturada em escala. Use quando precisar de volume.

**Melhores práticas:**
- Máximo 5–7 minutos para responder
- Evite perguntas de duplo-barril ("Você acha o produto rápido e fácil?" — são duas perguntas!)
- Inclua escala Likert (1–5 ou 1–7) para medir atitudes
- Sempre teste o questionário com 2–3 pessoas antes de lançar
- Ofereça campo aberto no final

### 4.3 Observação Contextual

Observe usuários em seu ambiente natural realizando tarefas reais. O que as pessoas *fazem* é frequentemente diferente do que elas *dizem* que fazem.

**Técnica Think Aloud:** peça que o usuário verbalize o que está pensando enquanto realiza a tarefa.

### 4.4 Guerrilha Research

Pesquisa rápida com usuários aleatórios em espaços públicos (cafés, universidades). Barato, rápido, mas menor validade.

**Ideal para:** validação rápida de conceitos no início do projeto.

### 4.5 Análise de Dados (Desk Research)

- Análise de reviews na App Store / Play Store
- Mineração de suporte ao cliente
- Análise de redes sociais (Twitter, Reddit)
- Heatmaps e gravações de sessão (Hotjar, FullStory)

---

## 5. Personas

**Persona** é um personagem fictício, mas baseado em dados reais, que representa um segmento do seu público.

### Estrutura de uma Persona

```
┌─────────────────────────────────────────────────────┐
│  📸 FOTO    │  NOME: Carla Santos                    │
│             │  IDADE: 34 anos                        │
│             │  OCUPAÇÃO: Analista de Marketing       │
│             │  LOCAL: São Paulo, SP                  │
├─────────────────────────────────────────────────────┤
│ SOBRE                                               │
│ Carla é mãe de dois filhos e trabalha em home       │
│ office. Usa smartphone para tudo: banco, compras,   │
│ acompanhar filhos na escola.                        │
├────────────────────┬────────────────────────────────┤
│ OBJETIVOS          │ FRUSTRAÇÕES                     │
│ • Gerenciar        │ • Apps de banco confusos        │
│   finanças com     │ • Muitas senhas para lembrar    │
│   facilidade       │ • Medo de golpes online         │
│ • Economizar tempo │ • Atendimento demorado          │
├────────────────────┴────────────────────────────────┤
│ CITAÇÃO REAL: "Eu quero resolver tudo pelo celular  │
│ mas fico com medo de clicar no lugar errado."       │
├─────────────────────────────────────────────────────┤
│ TECNOLOGIA: 📱📱📱📱⬜  HABILIDADE DIGITAL: média    │
└─────────────────────────────────────────────────────┘
```

**Cuidados:**
- Personas sem dados são suposições disfarçadas
- Evite personas demais (2–4 é suficiente)
- Inclua comportamentos, não apenas demografias
- Atualize conforme novas pesquisas

---

## 6. Jornada do Usuário (Customer Journey Map)

Visualização da experiência completa do usuário ao longo do tempo, incluindo emoções.

```
JORNADA: Pedir um delivery de comida

Fase:    │ Fome     │ Busca     │ Escolha   │ Pedido    │ Espera    │ Entrega   │
─────────┼──────────┼───────────┼───────────┼───────────┼───────────┼───────────┤
Ação:    │ Abre     │ Vê        │ Compara   │ Finaliza  │ Acompanha │ Recebe e  │
         │ o app    │ opções    │ preços    │ pagamento │ no mapa   │ avalia    │
─────────┼──────────┼───────────┼───────────┼───────────┼───────────┼───────────┤
Emoção:  │  😊      │  🤔       │  😤       │  😰       │  😟       │  😊/😡    │
─────────┼──────────┼───────────┼───────────┼───────────┼───────────┼───────────┤
Dor:     │          │ Muitas    │ Fotos     │ Bugs no   │ Mapa      │ Pedido    │
         │          │ opções    │ ruins     │ pagamento │ travando  │ errado    │
─────────┼──────────┼───────────┼───────────┼───────────┼───────────┼───────────┤
Oportu-  │          │ Melhores  │ Filtros   │ Salvar    │ Chat com  │ Sistema   │
nidade:  │          │ filtros   │ claros    │ cartão    │ entregador│ de avalia.│
```

---

## 7. How Might We (Como Poderíamos?)

Técnica para transformar insights de pesquisa em oportunidades de design.

**Formato:** "Como poderíamos [verbo + resultado desejado] para [persona]?"

**Exemplos:**
- "Como poderíamos tornar a busca de restaurantes mais rápida para pessoas com fome?"
- "Como poderíamos reduzir o medo de golpes para usuários de banco digital?"
- "Como poderíamos ajudar pais a acompanhar o gasto dos filhos?"

---

## 🛠️ Práticas

### Prática 1 — Entrevista de 20 minutos
1. Escolha o problema: "Como as pessoas gerenciam suas finanças pessoais?"
2. Elabore um roteiro com 8 perguntas (use o modelo acima)
3. Entreviste um colega (ou familiar)
4. Documente os insights em post-its digitais (Miro, FigJam ou papel)
5. Identifique 3 insights surpreendentes

### Prática 2 — Criação de Persona Baseada em Dados
1. Reúna dados de 3 entrevistas (podem ser simuladas)
2. Identifique padrões: objetivos comuns, frustrações comuns, comportamentos comuns
3. Crie uma persona usando a estrutura acima
4. Apresente para a turma e receba feedback

### Prática 3 — Mapeamento de Jornada
1. Escolha uma tarefa cotidiana (ex: renovar habilitação, matricular em disciplina na universidade)
2. Entreviste 2 pessoas que já fizeram isso
3. Mapeie a jornada completa com fases, emoções e pontos de dor
4. Destaque os 3 maiores pontos de dor
5. Gere 3 declarações "Como poderíamos?"

### Prática 4 — Survey Rápido
1. Crie um survey de no máximo 10 perguntas sobre um produto digital que você usa
2. Inclua pelo menos uma pergunta de escala Likert, uma pergunta aberta e uma pergunta NPS ("De 0 a 10, qual a chance de você recomendar?")
3. Aplique para 10 pessoas
4. Analise os resultados e apresente 3 conclusões

---

## ✅ Checklist de Product Discovery

- [ ] Você definiu uma hipótese de problema antes de começar?
- [ ] Você entrevistou pelo menos 5 usuários do público-alvo?
- [ ] Suas personas são baseadas em dados de pesquisa (não suposições)?
- [ ] Você mapeou a jornada atual do usuário (as-is)?
- [ ] Você identificou os maiores pontos de dor?
- [ ] Você transformou os insights em declarações "Como poderíamos?"?
- [ ] Você validou o problema antes de partir para a solução?

---

## 📖 Referências

- TORRES, Cláudio. *Nivelando a Conversa sobre Product Discovery*. Medium, 2019.
- PORTIGAL, Steve. *Interviewing Users*. Rosenfeld Media, 2013.
- GOTHELF, Jeff; SEIDEN, Josh. *Lean UX*. O'Reilly, 2021.
- Nielsen Norman Group — User Interviews: [https://www.nngroup.com/articles/user-interviews/](https://www.nngroup.com/articles/user-interviews/)
- IDEO Design Thinking: [https://www.designkit.org/methods](https://www.designkit.org/methods)

---

[← Módulo anterior](../02-evolucao-ihc/README.md) | [Próximo módulo →](../04-arquitetura-informacao/README.md)

# 10 — Aspectos Éticos do Design

> *"Com grande poder vem grande responsabilidade."* — Uncle Ben (e todo designer de produto)

---

## 🎯 Objetivos de Aprendizagem

- Compreender a responsabilidade ética do designer
- Identificar dark patterns e suas consequências
- Reconhecer viés algorítmico e de design
- Aplicar princípios de design responsável
- Conhecer regulações e legislações relevantes

---

## 1. Por Que Ética no Design?

Designers tomam decisões que afetam a vida de bilhões de pessoas. Um botão mal posicionado pode:
- Levar uma pessoa a assinar um serviço que não queria
- Dificultar o cancelamento de um plano
- Induzir uma criança a fazer compras acidentais
- Manipular uma pessoa em estado emocional vulnerável

**A escala amplifica tudo.** Se um site tem 1 bilhão de usuários e você adiciona um campo pré-marcado que 10% das pessoas não percebem, você acabou de "capturar" 100 milhões de pessoas sem consentimento real.

---

## 2. Dark Patterns (Padrões Obscuros)

**Dark patterns** são técnicas de design deliberadamente projetadas para enganar, manipular ou confundir usuários, geralmente em benefício do negócio às custas do usuário.

O termo foi cunhado por **Harry Brignull** em 2010.

### Catálogo de Dark Patterns

#### 2.1 Roach Motel
"Fácil entrar, difícil sair"

- ✅ Assinar o plano: 1 clique
- ❌ Cancelar o plano: ligar para o atendimento, aguardar 30 min, ser persuadido por um atendente

**Exemplos reais:** Amazon Prime, Gym memberships, serviços de streaming

#### 2.2 Confirmshaming
Vergonha pela recusa — o "não" é formulado de forma que recusar pareça errado.

```
Quer economizar 30% nas suas compras?

[Sim, quero economizar!]  ←  Opção destacada
[Não, prefiro pagar mais] ←  Opção de recusa manipulada
```

#### 2.3 Trick Questions
Perguntas formuladas confusamente, geralmente com dupla negativa.

```
☑ Não desejo não receber ofertas por e-mail ← Ambíguo!
```

#### 2.4 Sneak into Basket
Produto extra adicionado ao carrinho sem consentimento explícito.

**Exemplo:** Comprar passagem aérea e seguro viagem é adicionado automaticamente com opt-out escondido.

#### 2.5 Misdirection (Distração)
Atenção direcionada para um local enquanto ação indesejável acontece em outro.

**Exemplo:** Animação chamativa no centro da tela enquanto checkbox importante aparece no canto.

#### 2.6 Hidden Costs
Custos extras aparecem apenas no checkout.

```
Produto: R$ 99,00
  Taxa de serviço: R$ 15,00
  Taxa de entrega: R$ 12,00
  Embalagem especial: R$ 5,00
  TOTAL: R$ 131,00 ← surpresa no final!
```

#### 2.7 Bait and Switch
Prometido um resultado, entregue outro.

**Exemplo:** "Atualizar Windows" que instala software adicional.

#### 2.8 Privacy Zuckering
Confundir usuários a compartilhar mais informações do que pretendem.

**Exemplo:** Configurações de privacidade do Facebook até 2018 — centenas de opções espalhadas.

#### 2.9 Countdown Timer Falso
Urgência artificial — "Oferta termina em 00:05:00"... que reseta ao recarregar.

#### 2.10 Friend Spam
Acesso a contatos sem deixar claro que serão enviadas mensagens.

---

## 3. Regulação e Punições

Dark patterns não são apenas antiéticos — podem ser ilegais:

| Legislação | Região | Impacto |
|------------|--------|---------|
| **LGPD** (Lei 13.709/2018) | Brasil | Multa até 2% faturamento, max R$ 50M por infração |
| **GDPR** | União Europeia | Multa até 4% faturamento global |
| **FTC Act** | EUA | Ações da Federal Trade Commission |
| **DSA** (Digital Services Act) | União Europeia | Proíbe dark patterns explicitamente |

**Casos reais:**
- **Amazon:** Multa de €746 milhões (GDPR, 2021)
- **Google:** Multa de €150 milhões (CNIL França, 2022) por botão de cookies confuso
- **Instagram:** Multa de €405 milhões (GDPR, 2022) por expor dados de menores

---

## 4. Viés de Design e Viés Algorítmico

### Viés de Design

Designers refletem (inconscientemente) suas próprias perspectivas no design, excluindo pessoas diferentes de si.

**Exemplos históricos:**
- Sensores de sabão automático que não funcionam com pele escura (calibrado apenas com pele clara)
- Airbags desenhados para corpo masculino médio — mais mortes de mulheres
- Algoritmos de reconhecimento facial com taxa de erro 34% maior para mulheres negras vs. 0.8% para homens brancos (MIT Media Lab, 2018)

### Viés Algorítmico em Interfaces

| Tipo de Viés | Exemplo |
|--------------|---------|
| **Viés de confirmação** | Feed que mostra apenas conteúdo que você já concorda |
| **Viés de automação** | Usuários confiam demais em sugestões do algoritmo |
| **Viés de apresentação** | Produtos mais rentáveis aparecem primeiro, não os mais relevantes |
| **Viés de treinamento** | IA treinada com dados históricos perpetua discriminação |

---

## 5. Tecnologia Persuasiva — A Linha Tênue

**B.J. Fogg** (Stanford) estudou como tecnologia pode mudar comportamentos. Há uma linha entre:

| Persuasão Ética ✅ | Manipulação Antiética ❌ |
|-------------------|------------------------|
| Lembretes para tomar medicamento | Notificações compulsivas que criam dependência |
| Gamificação para praticar idiomas | Slots infinitos que drenam tempo involuntariamente |
| Streaks para hábitos saudáveis | Streaks que causam ansiedade e medo de perder |
| Feedback imediato de progresso | Variabilidade de recompensa (mecanismo de slot machine) |

### O Modelo de Fogg

```
Comportamento = Motivação × Habilidade × Gatilho

Se todos três estiverem presentes no mesmo momento → comportamento ocorre
```

**Uso ético:** Use este modelo para ajudar usuários a realizar objetivos que eles mesmos definiram.  
**Uso antiético:** Use este modelo para fazer usuários agirem contra seus próprios interesses.

---

## 6. Design Responsável na Prática

### O Manifesto de Design Ético

Princípios do **Ethical Design Manifesto** (ind.ie):
1. Respeite os direitos humanos
2. Respeite o esforço humano
3. Respeite a experiência humana

### Perguntas Éticas Para Fazer Antes de Implementar

Antes de qualquer decisão de design, pergunte:
1. **Para quem isso é bom?** Usuário, empresa, ou apenas empresa?
2. **Quem pode ser prejudicado?** Grupos vulneráveis, minorias?
3. **Isso seria aceitável se fosse em um jornal?** (Teste do jornal)
4. **Eu ficaria confortável se minha mãe visse isso?** (Teste da mãe)
5. **Isso respeita a autonomia do usuário?**

### Prática de Design Ético em Equipe

Adicione ao seu processo:
- **Revisão de dark patterns** antes de lançar qualquer feature
- **Teste com grupos marginalizados** para identificar viés
- **Ethics checkpoint** no design review
- **Anonimização de dados** como padrão, não exceção

---

## 7. Bem-estar Digital (Digital Wellbeing)

Movimento liderado por Apple, Google e outros para reduzir uso compulsivo:

- **Screen Time** (iOS) / **Digital Wellbeing** (Android): relatórios de uso
- **App Limits:** Bloqueio após X minutos
- **Focus Mode:** Reduzir distrações
- **Wind Down:** Modo noturno para reduzir exposição à tela

**Para o designer:** Projete para **uso intencional**, não para **uso máximo**.

---

## 🛠️ Práticas

### Prática 1 — Caça aos Dark Patterns (45 min)
1. Visite um site de e-commerce ou de assinatura
2. Tente assinar e depois cancelar um serviço
3. Documente com screenshots cada dark pattern encontrado
4. Classifique pelo catálogo de Brignull
5. Estime o impacto financeiro para a empresa se 1% dos usuários não perceber

### Prática 2 — Redesign Ético (60 min)
Escolha um dark pattern encontrado na Prática 1:
1. Redesenhe a tela removendo o dark pattern
2. Mantenha o objetivo de negócio legítimo (ex: incentivar upgrade)
3. Mostre que é possível ser ético e ainda atingir objetivos de negócio
4. Apresente a comparação antes/depois

### Prática 3 — Ética no Algoritmo (45 min)
Analise o feed do TikTok, Instagram Reels ou YouTube Shorts por 30 minutos:
1. Documente o tipo de conteúdo recomendado
2. Identifique se o algoritmo amplificou conteúdo de confirmação
3. Identifique gatilhos de uso compulsivo (scroll infinito, autoplay)
4. Discuta: como esses sistemas deveriam ser projetados de forma mais ética?

---

## ✅ Checklist de Design Ético

- [ ] As configurações de privacidade são fáceis de entender e mudar?
- [ ] O consentimento é obtido de forma clara (sem pré-marcados enganosos)?
- [ ] O cancelamento/saída é tão fácil quanto a entrada?
- [ ] A interface não cria urgência artificial (timers falsos, scarcity fake)?
- [ ] Os rótulos de "não aceitar" são neutros (sem confirmshaming)?
- [ ] O produto foi testado com grupos marginalizados?
- [ ] O algoritmo foi auditado para viés discriminatório?
- [ ] O produto promove uso intencional, não uso máximo?

---

## 📖 Referências

- BRIGNULL, Harry. *Dark Patterns*: [https://www.deceptive.design](https://www.deceptive.design)
- FOGG, B.J. *Persuasive Technology*. Morgan Kaufmann, 2003.
- GRAY, Colin et al. *The Dark Side of UX Design*. CHI 2018.
- Ethical Design Manifesto: [https://ind.ie/ethical-design/](https://ind.ie/ethical-design/)
- MONTEIRO, Mike. *Ruined by Design*. Mule Design, 2019.

---

[← Módulo anterior](../09-metricas-ux/README.md) | [Próximo módulo →](../11-design-inclusivo/README.md)

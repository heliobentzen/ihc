# 06 — Prototipação de Baixa e Alta Fidelidade

> *"Falhe cedo para ter sucesso mais cedo."* — Tom Kelley, IDEO

---

## 🎯 Objetivos de Aprendizagem

- Entender o papel da prototipação no processo de design
- Distinguir os níveis de fidelidade de protótipos
- Conhecer as principais ferramentas de prototipação
- Conduzir um teste de usabilidade com protótipo em papel
- Criar um protótipo interativo no Figma

---

## 1. Por Que Prototipar?

**Prototipar é a arte de fazer perguntas de forma barata.**

Um protótipo permite validar ideias antes de gastar recursos construindo algo errado. A regra de ouro é:

> **Quanto mais cedo você falhar, mais barato é o erro.**

### Custo do Erro por Fase

```
Custo     │
de        │                                        ████
corrigir  │                              ████      ████
          │                    ████      ████      ████
          │          ████      ████      ████      ████
          │  ████    ████      ████      ████      ████
          └──────────────────────────────────────────────
          Discovery  Design  Desenvol-  QA/Teste  Produção
                             vimento
```

---

## 2. Níveis de Fidelidade

### Baixa Fidelidade (Lo-Fi)

- Sketches em papel ou quadro branco
- Foco no conceito e no fluxo, não na aparência
- Rápido de criar (minutos a horas)
- Ideal para exploração inicial e discussões internas

**Características:**
- Caixas, linhas e texto manuscrito
- Sem cores, sem estilos
- Facilmente descartável (encoraja experimentação)

### Média Fidelidade (Mid-Fi)

- Wireframes digitais
- Estrutura e layout definidos
- Sem cores ou assets visuais finais
- Ideal para validar fluxos e arquitetura

**Características:**
- Grid e espaçamento definidos
- Texto placeholder ("Lorem ipsum" ou texto real simplificado)
- Navegação básica pode ser interativa

### Alta Fidelidade (Hi-Fi)

- Mockups com visual próximo ao final
- Cores, tipografia e imagens reais
- Protótipo interativo simulando o comportamento real
- Ideal para testes de usabilidade e aprovação do cliente

**Características:**
- Visual pixel-perfect
- Animações e micro-interações
- Conteúdo real

---

## 3. Comparativo das Ferramentas

| Ferramenta | Fidelidade | Melhor para | Custo |
|------------|------------|-------------|-------|
| **Papel + caneta** | Baixa | Exploração rápida, brainstorm | Gratuito |
| **Balsamiq** | Baixa/Média | Wireframes ágeis, discussão | Pago |
| **Whimsical** | Baixa/Média | Fluxos, wireframes, mapas | Freemium |
| **Figma** | Média/Alta | Design system, colaboração | Freemium |
| **Adobe XD** | Média/Alta | Protótipos interativos | Pago |
| **Framer** | Alta | Protótipos com código, animações avançadas | Freemium |
| **Marvel** | Alta | Testes de usabilidade integrados | Freemium |
| **ProtoPie** | Alta | Micro-interações complexas | Pago |

---

## 4. Prototipação em Papel — Passo a Passo

### Materiais
- Folhas A4 (cada uma = uma tela)
- Caneta ou marcador
- Post-its para sobreposições (elementos que mudam de estado)
- Tesoura para criar componentes reutilizáveis

### Processo

**1. Definir o fluxo:** "Qual tarefa quero testar?"  
Ex: Usuário faz login e envia uma mensagem.

**2. Listar as telas:** Quais telas são necessárias para completar a tarefa?  
Ex: Login → Home → Mensagens → Nova Mensagem → Confirmação

**3. Desenhar cada tela:** Cada folha = uma tela  
- Desenhe os elementos principais (header, botões, inputs)
- Use caixas para imagens
- Linhas onduladas para texto de corpo
- X para fechar
- Setas para indicar direção

**4. Criar sobreposições:** Use post-its para estados transitórios  
- Dropdown aberto
- Teclado virtual
- Loading spinner
- Mensagem de sucesso/erro

**5. Testar com usuário:** O facilitador "opera" o protótipo  
- Usuário aponta onde clicaria
- Facilitador troca as folhas manualmente

---

## 5. Figma — Introdução Prática

### Conceitos Fundamentais

| Conceito | O que é |
|----------|---------|
| **Frame** | Container que representa uma tela |
| **Auto Layout** | Sistema de layout flexível (como Flexbox no CSS) |
| **Component** | Elemento reutilizável com variantes |
| **Variant** | Estados diferentes de um componente (default, hover, error) |
| **Prototype** | Conexões entre frames que simulam navegação |
| **Variable** | Token de design (cor, tipografia) reutilizável |

### Fluxo de Trabalho no Figma

```
1. ESBOÇO      → Frames brancos + Auto Layout básico
2. WIREFRAME   → Componentes UI Kit base (sem estilo)
3. MOCKUP      → Aplicar cores, tipografia, ícones, imagens
4. PROTÓTIPO   → Conectar frames com interações
5. HANDOFF     → Inspecionar specs para desenvolvedor
```

### Atalhos Essenciais do Figma

| Atalho | Ação |
|--------|------|
| `F` | Criar Frame |
| `R` | Retângulo |
| `T` | Texto |
| `Ctrl/Cmd + G` | Agrupar |
| `Ctrl/Cmd + Alt + G` | Frame de seleção |
| `Alt + drag` | Duplicar |
| `Shift + A` | Adicionar Auto Layout |
| `Ctrl/Cmd + K` | Plugin runner |
| `P` | Modo Prototype |

---

## 6. Tipos de Protótipos Interativos

### Por Propósito

| Tipo | Objetivo | Exemplo |
|------|----------|---------|
| **Exploratório** | Comparar alternativas de design | 3 versões do onboarding para A/B |
| **Evolutivo** | Cresce e se torna o produto final | Figma → handoff direto |
| **Descartável** | Responder uma pergunta específica e jogar fora | Teste de navegação isolado |
| **Horizontal** | Cobre todo o produto, sem profundidade | Demo para stakeholders |
| **Vertical** | Um fluxo completo com todos os detalhes | Teste de usabilidade de um fluxo crítico |

---

## 7. Erros Comuns em Prototipação

| Erro | Por que é problema | Solução |
|------|-------------------|---------|
| Prototipar muito cedo em hi-fi | Investe tempo em detalhes antes de validar o conceito | Comece sempre em paper/lo-fi |
| Nunca sair do lo-fi | Não testa comportamentos reais | Defina quando avançar a fidelidade |
| Protótipo muito complexo | Difícil de manter e testar | Foque no fluxo crítico |
| Ignorar estados | Esquece estados de erro, loading, vazio | Use checklist de estados |
| Não testar | Protótipo vira entregável sem feedback | Todo protótipo deve ser testado |

### Checklist de Estados para Não Esquecer

- [ ] Estado vazio (empty state) — primeira vez que o usuário acessa
- [ ] Estado de loading — esperando resposta do servidor
- [ ] Estado de erro — algo deu errado
- [ ] Estado de sucesso — ação completada
- [ ] Estado desabilitado — elemento não disponível
- [ ] Estado focado (focus) — acessibilidade e navegação por teclado

---

## 🛠️ Práticas

### Prática 1 — Prototype Sprint em Papel (60 min)

**Desafio:** Prototipar um app de "trocas de livros entre estudantes"

Etapas:
1. **Crazy 8s** (8 min): Dobre uma folha em 8 partes. Desenhe 8 ideias diferentes para a tela principal (1 min cada)
2. **Votar** (5 min): Cada pessoa coloca 3 estrelas nas ideias favoritas
3. **Detalhar** (20 min): A ideia vencedora vira um fluxo completo de 5 telas
4. **Testar** (20 min): Um colega testa usando o teste de papel, você anota observações
5. **Discutir** (7 min): O que funcionou? O que mudaria?

### Prática 2 — Wireframe Digital (90 min)

Usando Figma (conta gratuita) ou Whimsical:
1. Crie wireframes para as 5 telas mais críticas de um app de receitas
2. Adicione pelo menos 1 componente reutilizável
3. Conecte os frames com protótipo básico
4. Compartilhe o link e peça feedback de 2 colegas

### Prática 3 — Comparação Lo-Fi vs Hi-Fi (45 min)

1. Escolha um fluxo simples (ex: cadastro de email)
2. Crie versão em papel (lo-fi)
3. Crie versão no Figma com visual completo (hi-fi)
4. Teste cada versão com uma pessoa diferente
5. Compare: os problemas encontrados foram diferentes? Por quê?

---

## ✅ Checklist de Prototipação

- [ ] O objetivo do protótipo está claro (o que vai ser testado)?
- [ ] A fidelidade é adequada para a fase do projeto?
- [ ] Todos os estados críticos foram prototipados?
- [ ] O fluxo principal está completo do início ao fim?
- [ ] O protótipo foi testado com pelo menos 1 usuário antes de ser considerado "pronto"?
- [ ] Existe versão mobile e desktop (se aplicável)?
- [ ] Os componentes estão organizados e nomeados no Figma?

---

## 📖 Referências

- KELLEY, Tom; KELLEY, David. *Creative Confidence*. Crown Business, 2013.
- KNAPP, Jake; ZERATSKY, John; KOWITZ, Braden. *Sprint*. Simon & Schuster, 2016.
- Figma Learn: [https://help.figma.com/hc/en-us/categories/360002042553](https://help.figma.com/hc/en-us/categories/360002042553)
- Nielsen Norman Group — Prototyping: [https://www.nngroup.com/articles/ux-prototype-hi-lo-fidelity/](https://www.nngroup.com/articles/ux-prototype-hi-lo-fidelity/)

---

[← Módulo anterior](../05-usabilidade-heuristicas/README.md) | [Próximo módulo →](../07-design-systems/README.md)

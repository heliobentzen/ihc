# 04 — Arquitetura de Informação

> *"Uma boa arquitetura de informação é como um ótimo mapa: você sabe onde está, para onde pode ir e como chegar lá."*

---

## 🎯 Objetivos de Aprendizagem

- Compreender os 4 componentes da Arquitetura de Informação
- Aplicar técnicas de organização e rotulação de conteúdo
- Criar e interpretar card sortings
- Desenhar sitemaps e sistemas de navegação
- Entender padrões de navegação em diferentes contextos

---

## 1. O Que é Arquitetura de Informação?

**Arquitetura de Informação (AI)** é a prática de organizar, estruturar e rotular conteúdo de forma eficaz e sustentável, com o objetivo de ajudar as pessoas a encontrarem e compreenderem as informações de que precisam.

O termo foi popularizado por **Richard Saul Wurman** nos anos 1970 e sistematizado por **Peter Morville** e **Louis Rosenfeld** no livro *Information Architecture for the World Wide Web* (1998).

---

## 2. Os 4 Componentes Fundamentais

### 2.1 Sistemas de Organização

Como o conteúdo é agrupado e categorizado.

**Esquemas de organização:**

| Esquema | Descrição | Exemplo |
|---------|-----------|---------|
| **Alfabético** | A–Z | Dicionário, índice |
| **Cronológico** | Temporal | Blog, timeline, changelog |
| **Geográfico** | Por localização | Lojas por estado, notícias regionais |
| **Por tópico** | Por assunto | Wikipedia, e-commerce por categoria |
| **Por audiência** | Por tipo de usuário | Site com área "Para empresas" e "Para pessoas" |
| **Por tarefa** | Por ação | "Comprar", "Vender", "Alugar" |
| **Ambíguo** | Metáfora, híbrido | Amazon (combina tópico + audiência) |

### 2.2 Sistemas de Rotulação

Como o conteúdo é representado linguisticamente — os nomes que damos às coisas.

**Boas práticas:**
- Use a linguagem do usuário, não do sistema
- Seja consistente (não misture "Sair" com "Logout" com "Desconectar")
- Seja específico (evite "Clique aqui", "Saiba mais")
- Teste rótulos com usuários (card sorting)

**Exemplo ruim vs. bom:**
```
❌ Ruim: "Soluções" | "Recursos" | "Plataforma"
✅ Bom:  "O que fazemos" | "Preços" | "Como funciona"
```

### 2.3 Sistemas de Navegação

Como os usuários se movem pelo espaço informacional.

**Tipos de navegação:**

| Tipo | Descrição | Exemplo |
|------|-----------|---------|
| **Global** | Presente em todas as páginas | Header com menu principal |
| **Local** | Navegação dentro de uma seção | Submenu de uma categoria |
| **Contextual** | Links embutidos no conteúdo | Links em texto de artigo |
| **Breadcrumbs** | Trilha de onde o usuário está | Casa > Roupas > Masculino > Camisas |
| **Suplementar** | Índice, mapa do site, FAQ | Sitemap no rodapé |
| **Pessoal** | Baseado no histórico do usuário | "Comprado recentemente", "Continue assistindo" |

### 2.4 Sistemas de Busca

Como os usuários encontram informação pesquisando.

**Tipos de busca:**
- **Simples:** uma caixa, busca por palavras-chave
- **Avançada:** filtros, operadores booleanos
- **Faceted:** filtros combinados dinâmicos (muito usada em e-commerce)

**Boas práticas de busca:**
- Tolerância a erros ortográficos
- Sugestões automáticas (autocomplete)
- Zero results page útil (sugestões alternativas)
- Destaque dos termos buscados nos resultados

---

## 3. Os 3 Círculos da AI

Peter Morville propôs que uma boa AI deve equilibrar:

```
        ┌─────────────┐
        │   USUÁRIOS  │
        │  (Contexto, │
        │  Comporta-  │
        │   mento)    │
        └──────┬──────┘
               │
    ┌──────────┼──────────┐
    │          │          │
    ▼          ▼          ▼
┌────────┐ ┌────────┐ ┌────────┐
│CONTEÚDO│ │   AI   │ │CONTEXTO│
│(volume,│ │        │ │(negócio│
│formato,│ │        │ │cultura,│
│metada- │ │        │ │tecnolo-│
│  dos)  │ │        │ │ gia)   │
└────────┘ └────────┘ └────────┘
```

---

## 4. Card Sorting

**Card Sorting** é uma técnica para descobrir como os usuários organizam e categorizam mentalmente o conteúdo.

### Como funciona:

1. Cada item de conteúdo é escrito em um cartão (físico ou digital)
2. Participantes organizam os cartões em grupos que façam sentido para eles
3. Eles nomeiam cada grupo
4. O pesquisador analisa os padrões

**Tipos:**

| Tipo | Descrição | Quando usar |
|------|-----------|-------------|
| **Aberto** | Usuários criam e nomeiam os grupos | Fase inicial, descoberta |
| **Fechado** | Grupos pré-definidos, usuários alocam cartões | Validar estrutura existente |
| **Híbrido** | Grupos pré-definidos + opção de criar novos | Refinar estrutura |

**Ferramentas:** OptimalSort, Maze, Miro, UserZoom

### Analisando resultados:
- **Matriz de similaridade:** mostra com que frequência dois itens foram agrupados juntos
- **Dendrograma:** agrupamento hierárquico visual dos resultados
- **Regra prática:** se 2 itens foram agrupados juntos por >40% dos participantes, considere mantê-los na mesma categoria

---

## 5. Tree Testing

O inverso do card sorting: valida se a estrutura de navegação proposta funciona.

1. Apresente aos usuários uma estrutura de navegação (sem visual)
2. Peça para eles encontrarem itens específicos
3. Meça: taxa de sucesso, tempo, caminhos percorridos

**Ferramentas:** Treejack (Optimal Workshop), Maze

---

## 6. Sitemaps

Representação visual da estrutura do site/app.

```
                    ┌────────────┐
                    │  INÍCIO    │
                    └─────┬──────┘
          ┌───────────────┼───────────────┐
          ▼               ▼               ▼
    ┌──────────┐    ┌──────────┐    ┌──────────┐
    │ PRODUTOS │    │SOBRE NÓS │    │ CONTATO  │
    └────┬─────┘    └──────────┘    └──────────┘
    ┌────┴─────┐
    ▼          ▼
┌────────┐ ┌────────┐
│  Cats  │ │  Cães  │
└────────┘ └────────┘
```

**Níveis típicos:**
- **L0:** Homepage
- **L1:** Seções principais
- **L2:** Subseções
- **L3:** Páginas individuais

---

## 7. Padrões de Navegação

### Para mobile:
- **Tab Bar:** 4–5 destinos principais na parte inferior (iOS Human Interface Guidelines recomenda)
- **Hamburger Menu:** esconde opções secundárias
- **Bottom Sheet:** painel deslizante de baixo para cima

### Para web:
- **Horizontal nav:** opções no topo
- **Sidebar:** navegação lateral
- **Mega Menu:** dropdown com colunas para sites com muito conteúdo

### Para ambos:
- **Breadcrumbs:** especialmente para conteúdo hierárquico profundo
- **Search first:** Google, YouTube — a busca é a navegação principal

---

## 🛠️ Práticas

### Prática 1 — Card Sorting com papel (45 min)
1. Escolha um site de e-commerce fictício que vende material esportivo
2. Crie 30 cartões com produtos diferentes (ex: "Tênis de corrida", "Luvas de boxe", "Meias esportivas"...)
3. Em grupos de 3: uma pessoa é o facilitador, duas são os usuários
4. Usuários organizam os cartões e nomeiam os grupos
5. Compare os agrupamentos dos dois usuários
6. O que foi diferente? O que foi igual?

### Prática 2 — Auditoria de Navegação (30 min)
Acesse um site de uma universidade brasileira.
1. Você consegue encontrar o calendário acadêmico em menos de 60 segundos?
2. Tente encontrar: horário de ônibus, contato do DCE, biblioteca
3. Avalie o sistema de rotulação: os rótulos refletem a linguagem do estudante?
4. Qual o maior problema de AI que você identificou?

### Prática 3 — Redesenho de Sitemap (60 min)
1. Faça um sitemap do site da sua universidade (até L2)
2. Identifique 3 problemas de organização
3. Proponha um sitemap alternativo que resolva esses problemas
4. Justifique cada mudança

### Prática 4 — Tree Testing Informal (30 min)
1. Crie uma estrutura de navegação para um app de receitas com 20 itens
2. Escreva 5 tarefas para os usuários encontrarem itens específicos
3. Teste com 3 colegas (sem mostrar o app, apenas a estrutura de texto)
4. Calcule a taxa de sucesso para cada tarefa

---

## ✅ Checklist de Arquitetura de Informação

- [ ] O vocabulário usa a linguagem do usuário (não do negócio ou da tecnologia)?
- [ ] A hierarquia tem no máximo 3–4 níveis de profundidade?
- [ ] Cada item aparece em no máximo um lugar (evitar duplicação confusa)?
- [ ] A navegação global está presente em todas as telas?
- [ ] O usuário sempre sabe onde está (breadcrumbs, highlights no menu)?
- [ ] A busca tolera erros e oferece sugestões?
- [ ] O card sorting foi realizado para validar as categorias?
- [ ] O tree testing confirmou que os usuários encontram o que procuram?

---

## 📖 Referências

- MORVILLE, Peter; ROSENFELD, Louis. *Information Architecture for the World Wide Web*. O'Reilly, 2015.
- WURMAN, Richard Saul. *Information Anxiety*. Bantam, 1990.
- Optimal Workshop Blog: [https://www.optimalworkshop.com/learn](https://www.optimalworkshop.com/learn)
- Nielsen Norman Group — IA: [https://www.nngroup.com/topic/information-architecture/](https://www.nngroup.com/topic/information-architecture/)

---

[← Módulo anterior](../03-product-discovery/README.md) | [Próximo módulo →](../05-usabilidade-heuristicas/README.md)

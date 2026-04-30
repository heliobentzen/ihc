# 07 — Introdução a Design Systems

> *"Um design system não é um projeto. É um produto que serve outros produtos."* — Nathan Curtis

---

## 🎯 Objetivos de Aprendizagem

- Entender o que é um Design System e por que ele existe
- Conhecer os componentes de um Design System completo
- Compreender tokens de design e seu papel
- Explorar Design Systems públicos de referência
- Criar um mini Design System para um projeto

---

## 1. O Problema que o Design System Resolve

### Sem Design System

Imagine uma empresa com 5 times de produto, cada um com seus próprios designers e desenvolvedores:

```
Time A: botão azul #1A73E8, border-radius 4px, padding 12px 24px
Time B: botão azul #0066CC, border-radius 8px, padding 10px 20px
Time C: botão azul #2563EB, border-radius 6px, padding 14px 28px
Time D: botão verde #34A853, border-radius 4px, padding 12px 24px
```

**Resultado:** Produto fragmentado visualmente. Usuário percebe inconsistência. Desenvolvedores reinventam a roda. Designers perdem tempo em decisões repetidas.

### Com Design System

- Um botão, definido uma vez
- Atualizado em um lugar, refletido em todos os produtos
- Designer foca em problemas, não em pixels repetidos
- Desenvolvedor foca em lógica, não em CSS repetido

---

## 2. O Que é um Design System?

Um **Design System** é uma coleção de componentes reutilizáveis, guiados por padrões claros, que pode ser montada para construir qualquer número de aplicações.

### Os 3 Pilares

```
┌─────────────────────────────────────────────────────┐
│                  DESIGN SYSTEM                      │
├────────────────┬────────────────┬───────────────────┤
│  FUNDAÇÃO      │  COMPONENTES   │  DOCUMENTAÇÃO     │
│                │                │                   │
│ • Tokens       │ • Átomos       │ • Princípios      │
│ • Cores        │ • Moléculas    │ • Padrões         │
│ • Tipografia   │ • Organismos   │ • Como usar       │
│ • Espaçamento  │ • Templates    │ • Como contribuir │
│ • Ícones       │ • Páginas      │ • Changelog       │
└────────────────┴────────────────┴───────────────────┘
```

---

## 3. Tokens de Design

**Design Tokens** são as menores unidades decisoras de um Design System — os átomos dos átomos. São variáveis que armazenam os valores de design de forma abstrata e reutilizável.

### Tipos de Tokens

**Tokens Globais (primitivos):**
```json
{
  "color-blue-100": "#DBEAFE",
  "color-blue-500": "#3B82F6",
  "color-blue-900": "#1E3A5F",
  "font-size-12": "0.75rem",
  "font-size-16": "1rem",
  "spacing-4": "0.25rem",
  "spacing-16": "1rem"
}
```

**Tokens Semânticos (alias):**
```json
{
  "color-primary": "{color-blue-500}",
  "color-primary-hover": "{color-blue-600}",
  "color-text-default": "{color-gray-900}",
  "color-text-muted": "{color-gray-500}",
  "space-button-padding-x": "{spacing-16}",
  "space-button-padding-y": "{spacing-8}"
}
```

### Por Que Tokens Semânticos?

Com tokens semânticos, mudar o tema inteiro do produto é trocar um arquivo de configuração:

```
Tema Claro:  --color-background: #FFFFFF
Tema Escuro: --color-background: #1A1A1A
```

---

## 4. Metodologia Atomic Design

Brad Frost (2016) propôs uma metodologia hierárquica para organizar componentes:

### Os 5 Níveis

```
ÁTOMOS
├── Botão
├── Input
├── Label
├── Ícone
└── Badge

MOLÉCULAS (combinação de átomos)
├── Campo de formulário (Label + Input + Mensagem de erro)
├── Card de produto (Imagem + Título + Preço + Botão)
└── Search bar (Input + Ícone + Botão)

ORGANISMOS (combinação de moléculas)
├── Header (Logo + Nav + Search + Avatar)
├── Lista de produtos (múltiplos Cards)
└── Formulário de checkout (múltiplos Campos)

TEMPLATES (estrutura sem conteúdo real)
├── Template de página de produto
└── Template de checkout

PÁGINAS (conteúdo real aplicado ao template)
├── Página do produto X
└── Checkout do pedido #12345
```

---

## 5. Design Systems Públicos de Referência

Aprenda estudando os melhores:

| Design System | Empresa | Destaque |
|---------------|---------|----------|
| **Material Design 3** | Google | Documentação completa, tokens, dark mode |
| **Fluent Design** | Microsoft | Acessibilidade, produtos corporativos |
| **Human Interface Guidelines** | Apple | Plataforma iOS/macOS, padrões de interação |
| **Carbon** | IBM | Open source, acessibilidade WCAG |
| **Lightning** | Salesforce | Enterprise, densidade de informação |
| **Ant Design** | Alibaba | Ecossistema React completo |
| **Polaris** | Shopify | E-commerce, boas práticas de conteúdo |
| **Spectrum** | Adobe | Criativo, modo escuro, componentização |
| **Radix** | WorkOS | Acessibilidade, headless components |
| **shadcn/ui** | Comunidade | Customizável, popular em 2024 |

---

## 6. Governança do Design System

Um Design System sem governança vira caos rapidamente.

### Modelos de Governança

**Centralizado (Federal):**
- Um time dedicado (Design System Team)
- Controle total, qualidade alta
- Mais lento para evoluir
- Ideal para: empresas grandes com muitos times

**Distribuído (Federado):**
- Contribuições de todos os times
- Evolui mais rápido
- Risco de inconsistência
- Ideal para: startups em crescimento

**Híbrido:**
- Time central define a fundação
- Times contribuem com componentes específicos
- Revisão central antes de merge
- Ideal para: maioria dos casos

### Ciclo de Vida de um Componente

```
Proposta → Revisão → Desenvolvimento → Teste → Documentação → Lançamento → Depreciação
```

---

## 7. Construindo seu Primeiro Mini Design System no Figma

### Passo 1 — Fundação de Cores

```
Cores primárias: 5 tons (100/300/500/700/900)
Cores neutras:   10 tons (50/100/200/.../900)
Cores semânticas: success, warning, error, info
Cores de fundo: surface, background, overlay
```

### Passo 2 — Escala Tipográfica

```
Display: 48px / 40px
Heading: 32px / 24px / 20px / 18px
Body: 16px / 14px
Caption: 12px
Code: 14px (monospace)
```

### Passo 3 — Espaçamento

Use múltiplos de 4:
```
4px  (espaço mínimo)
8px  (espaço pequeno)
12px (médio-pequeno)
16px (médio)
24px (médio-grande)
32px (grande)
48px (extra grande)
64px (máximo)
```

### Passo 4 — Componentes Base

Crie variantes para cada estado:
```
Button: primary / secondary / ghost / danger
        default / hover / active / disabled / loading

Input: default / focus / error / success / disabled
       with/without label / with/without helper text

Card: default / hover / selected / skeleton
```

---

## 8. Documentação é Parte do Design System

Um componente sem documentação não existe de verdade.

### O Que Documentar

Para cada componente:
- **Quando usar** (e quando NÃO usar)
- **Anatomia** — nomear cada parte
- **Variantes e estados** com exemplos visuais
- **Propriedades** (props) disponíveis
- **Acessibilidade** — como ele se comporta com leitor de tela
- **Código de exemplo** (React, HTML, etc.)
- **Responsividade** — como muda em diferentes breakpoints

---

## 🛠️ Práticas

### Prática 1 — Auditoria de Design System (45 min)
Acesse o Material Design 3 (material.io):
1. Estude o componente "Button"
2. Liste todas as variantes documentadas
3. Analise como a documentação de acessibilidade é feita
4. Compare com o mesmo componente no Fluent Design (microsoft.com/design)
5. Qual você acha mais completo? Por quê?

### Prática 2 — Extração de Tokens (30 min)
Escolha 3 apps diferentes (ex: Spotify, WhatsApp, Notion).
1. Identifique a paleta de cores principal de cada um
2. Identifique o espaçamento de elementos similares
3. Identifique a escala tipográfica
4. Monte uma tabela comparativa dos tokens

### Prática 3 — Mini Design System (3 horas)
Crie um mini Design System no Figma para um aplicativo fictício de "lista de tarefas":
1. Defina 5 tokens de cor semânticos
2. Defina escala tipográfica com 4 níveis
3. Crie 3 componentes com variantes: Button (3 variantes), Input (3 estados), Task Card (3 estados)
4. Monte 2 telas usando apenas os componentes criados
5. Documente cada componente com uma descrição de "quando usar"

---

## ✅ Checklist do Design System

- [ ] Os tokens de cor cobrem todos os casos de uso (primary, text, background, border, status)?
- [ ] Existe um sistema de espaçamento consistente (múltiplos de 4 ou 8)?
- [ ] A escala tipográfica cobre todos os níveis necessários?
- [ ] Cada componente tem variantes para todos os estados (default, hover, active, disabled, error)?
- [ ] Há documentação descrevendo quando usar cada componente?
- [ ] Os componentes atendem às diretrizes de acessibilidade (contraste, tamanho de toque)?
- [ ] Existe um processo para adicionar novos componentes?
- [ ] O Design System tem controle de versão (changelog)?

---

## 📖 Referências

- FROST, Brad. *Atomic Design*. [https://atomicdesign.bradfrost.com](https://atomicdesign.bradfrost.com)
- CURTIS, Nathan. *Modular Web Design*. New Riders, 2009.
- Material Design 3: [https://m3.material.io](https://m3.material.io)
- Design Tokens Community Group: [https://www.w3.org/community/design-tokens/](https://www.w3.org/community/design-tokens/)
- Style Dictionary: [https://amzn.github.io/style-dictionary/](https://amzn.github.io/style-dictionary/)

---

[← Módulo anterior](../06-prototipacao/README.md) | [Próximo módulo →](../08-testes-usabilidade/README.md)

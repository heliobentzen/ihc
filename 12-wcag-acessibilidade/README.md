# 12 — Diretrizes de Acessibilidade para Conteúdo Web (WCAG)

> *"Acessibilidade web significa que websites, ferramentas e tecnologias são projetados e desenvolvidos de forma que pessoas com deficiência possam usá-los."* — W3C WAI

---

## 🎯 Objetivos de Aprendizagem

- Compreender o que é WCAG e como surgiu
- Dominar os 4 princípios POUR
- Conhecer os 3 níveis de conformidade (A, AA, AAA)
- Aplicar os critérios de sucesso mais relevantes
- Realizar uma auditoria básica de acessibilidade

---

## 1. O Que é WCAG?

**WCAG** (Web Content Accessibility Guidelines) são diretrizes internacionais desenvolvidas pelo **W3C** (World Wide Web Consortium) através do grupo **WAI** (Web Accessibility Initiative).

### Versões

| Versão | Ano | Critérios |
|--------|-----|-----------|
| WCAG 1.0 | 1999 | 65 checkpoints |
| WCAG 2.0 | 2008 | 61 critérios |
| WCAG 2.1 | 2018 | +17 (mobile, baixa visão, cognitivo) |
| WCAG 2.2 | 2023 | +9 (foco, autenticação) |
| WCAG 3.0 | Em desenvolvimento | Nova estrutura completamente |

### Base Legal no Brasil

A **Lei Brasileira de Inclusão** (Lei 13.146/2015) exige acessibilidade digital, e o **Modelo de Acessibilidade em Governo Eletrônico (eMAG)** é baseado nas WCAG.

---

## 2. Os 4 Princípios POUR

Toda a WCAG se organiza em torno de 4 princípios:

### P — Perceptível (Perceivable)

Informações e componentes de interface devem ser apresentados de formas que os usuários possam perceber.

**Não pode ser invisível para todos os sentidos do usuário.**

### O — Operável (Operable)

Componentes de interface e navegação devem ser operáveis.

**O usuário deve conseguir operar a interface.**

### U — Compreensível (Understandable)

Informações e a operação de interface devem ser compreensíveis.

**O usuário deve conseguir compreender as informações e a interface.**

### R — Robusto (Robust)

O conteúdo deve ser robusto o suficiente para ser interpretado por uma ampla variedade de agentes de usuário, incluindo tecnologias assistivas.

**O conteúdo deve ser compatível com ferramentas atuais e futuras.**

---

## 3. Níveis de Conformidade

| Nível | Descrição | Quando alcançar |
|-------|-----------|-----------------|
| **A** | Conformidade básica — remove barreiras maiores | Mínimo absoluto |
| **AA** | Conformidade intermediária — remove a maioria das barreiras | **Meta recomendada** para maioria dos produtos |
| **AAA** | Conformidade máxima — remove barreiras especializadas | Conteúdo especializado para comunidades específicas |

> **Recomendação:** A grande maioria das organizações deve mirar o nível **AA**.

---

## 4. Critérios de Sucesso Essenciais (com Exemplos)

### 4.1 Alternativas Textuais — 1.1.1 (Nível A)

**Regra:** Todo conteúdo não-textual deve ter alternativa em texto.

```html
<!-- ❌ Ruim -->
<img src="logo.png">

<!-- ✅ Bom -->
<img src="logo.png" alt="Logo da empresa XYZ">

<!-- ✅ Imagem decorativa -->
<img src="decoracao.png" alt="">

<!-- ❌ Alt ruim -->
<img src="product.jpg" alt="imagem">

<!-- ✅ Alt bom -->
<img src="product.jpg" alt="Tênis Nike Air Max 270, cor branco com detalhes vermelhos">
```

### 4.2 Legendas (Captions) — 1.2.2 (Nível A)

**Regra:** Vídeos com áudio devem ter legendas sincronizadas.

**Por que importa:** Pessoas surdas, pessoas em ambiente barulhento, pessoas aprendendo idioma.

### 4.3 Contraste de Cor — 1.4.3 (Nível AA)

**Regra:**
- Texto normal: contraste mínimo **4.5:1**
- Texto grande (≥18pt ou ≥14pt negrito): contraste mínimo **3:1**

```
Verificar contraste: https://webaim.org/resources/contrastchecker/

Exemplos:
✅ Preto (#000000) sobre branco (#FFFFFF) = 21:1
✅ Cinza escuro (#333333) sobre branco = 12.6:1
⚠️ Cinza médio (#767676) sobre branco = 4.54:1 (mínimo AA)
❌ Cinza claro (#BBBBBB) sobre branco = 2.32:1 (falha)
❌ Amarelo (#FFFF00) sobre branco = 1.07:1 (falha grave)
```

### 4.4 Redimensionar Texto — 1.4.4 (Nível AA)

**Regra:** O texto pode ser redimensionado em até 200% sem perda de conteúdo ou funcionalidade.

**Como testar:** Ctrl/Cmd + "+" até 200% no navegador. O layout não pode quebrar.

### 4.5 Reflow — 1.4.10 (Nível AA) — WCAG 2.1

**Regra:** Conteúdo não exige rolagem em dois eixos em viewport de 320px de largura.

**Por que importa:** Usuários com baixa visão que precisam ampliar 400%.

### 4.6 Acesso por Teclado — 2.1.1 (Nível A)

**Regra:** Toda funcionalidade deve ser acessível via teclado.

```
Navegação por teclado:
Tab      → próximo elemento interativo
Shift+Tab → elemento anterior
Enter    → ativar link/botão
Espaço   → ativar checkbox/botão
Setas    → navegar em menus/listas
Esc      → fechar modal/menu
```

**Como testar:** Desconecte o mouse e navegue pelo site apenas com teclado.

### 4.7 Sem Armadilha de Teclado — 2.1.2 (Nível A)

**Regra:** O foco do teclado não pode ficar preso em um componente.

**Exemplo de falha:** Modal que abre mas não devolve o foco ao ser fechado. Foco vai para "lugar nenhum".

### 4.8 Foco Visível — 2.4.7 (Nível AA) / 2.4.11 (WCAG 2.2, Nível AA)

**Regra:** Qualquer componente de interface que recebe foco por teclado tem um indicador visível.

```css
/* ❌ Nunca faça isso */
:focus { outline: none; }

/* ✅ Personalize mas mantenha o foco visível */
:focus-visible {
  outline: 3px solid #005FCC;
  outline-offset: 2px;
  border-radius: 2px;
}
```

### 4.9 Nível de Leitura — 3.1.5 (Nível AAA)

**Regra:** Quando o texto requer nível de leitura acima do ensino fundamental, forneça uma versão simplificada.

**Boa prática (mesmo em AA):** Use linguagem simples. Ferramentas como Hemingway App medem a dificuldade de leitura.

### 4.10 Identificação do Idioma — 3.1.1 (Nível A)

```html
<!-- ✅ Obrigatório no HTML -->
<html lang="pt-BR">

<!-- Para trechos em outro idioma -->
<span lang="en">Hello World</span>
```

### 4.11 Rótulos e Instruções — 3.3.2 (Nível A)

**Regra:** Rótulos ou instruções são fornecidos quando o conteúdo requer entrada do usuário.

```html
<!-- ❌ Ruim -->
<input type="text" placeholder="Ex: João Silva">

<!-- ✅ Bom -->
<label for="nome">Nome completo</label>
<input id="nome" type="text" placeholder="Ex: João Silva"
       aria-describedby="nome-dica">
<p id="nome-dica">Digite seu nome como aparece nos documentos</p>
```

### 4.12 Prevenção de Erros — 3.3.4 (Nível AA)

**Regra:** Para submissões com consequências legais/financeiras: possibilidade de reverter, verificar e confirmar.

---

## 5. ARIA — Accessible Rich Internet Applications

ARIA é um conjunto de atributos HTML que permite tornar elementos interativos acessíveis quando o HTML semântico não é suficiente.

### Regra de Ouro do ARIA

> **"Não use ARIA se puder usar HTML semântico."**

```html
<!-- ❌ Evite -->
<div role="button" onclick="submit()">Enviar</div>

<!-- ✅ Use HTML semântico -->
<button type="submit">Enviar</button>
```

### ARIA Essencial

```html
<!-- Indicar estado expandido de menu -->
<button aria-expanded="false" aria-controls="menu-id">Menu</button>
<ul id="menu-id" hidden>...</ul>

<!-- Regiões vivas (para atualizações dinâmicas) -->
<div aria-live="polite" aria-atomic="true">
  <!-- Conteúdo que atualiza dinamicamente -->
</div>

<!-- Landmarks para leitores de tela -->
<header role="banner">
<nav role="navigation" aria-label="Menu principal">
<main role="main">
<footer role="contentinfo">

<!-- Mensagens de erro -->
<input aria-describedby="erro-email" aria-invalid="true">
<p id="erro-email" role="alert">E-mail inválido</p>
```

---

## 6. Como Realizar uma Auditoria de Acessibilidade

### Ferramentas Automatizadas (detectam ~30% dos problemas)

| Ferramenta | Tipo |
|------------|------|
| **axe DevTools** (extensão Chrome/Firefox) | Auditoria em browser |
| **Lighthouse** (Chrome DevTools) | Score de acessibilidade |
| **WAVE** (extensão/site) | Relatório visual |
| **Stark** (plugin Figma) | Contraste, simulação de daltonismo |
| **Pa11y** | Linha de comando, integra CI/CD |

### Testes Manuais Obrigatórios

1. **Navegação por teclado:** Tab por toda a página — tudo funciona?
2. **Leitor de tela:** Use NVDA (Windows, grátis) ou VoiceOver (Mac, built-in)
3. **Zoom 200%:** Layout quebra?
4. **Contraste:** Verifique todas as combinações de texto/fundo
5. **Modo de alto contraste:** Windows/macOS — o site ainda funciona?

### Processo de Auditoria

```
1. Inventário — listar todos os templates/páginas
2. Auditoria automática — rodar axe/Lighthouse em cada template
3. Testes manuais — teclado, leitor de tela, zoom
4. Priorização — A > AA > AAA; bloqueantes primeiro
5. Relatório — VPAT ou template próprio
6. Remediação — sprints de acessibilidade
7. Monitoramento — teste contínuo em CI/CD
```

---

## 🛠️ Práticas

### Prática 1 — Auditoria com axe DevTools (45 min)
1. Instale a extensão axe DevTools no Chrome
2. Audite 3 sites: seu banco, sua universidade e um site de notícias
3. Compare os resultados
4. Liste os 5 problemas mais graves encontrados
5. Para cada problema, explique qual grupo de usuários é prejudicado

### Prática 2 — Teste com Leitor de Tela (60 min)
1. Ative o VoiceOver (Mac: Cmd+F5) ou NVDA (Windows: download gratuito)
2. Feche os olhos e tente navegar por um formulário de cadastro
3. Documente: o que funcionou? O que foi impossível?
4. Compare a experiência com a navegação visual

### Prática 3 — Fix de Contraste (30 min)
1. Acesse o site da sua universidade
2. Use a extensão WAVE para identificar problemas de contraste
3. Para cada falha de contraste, sugira uma cor que mantenha a identidade visual mas passe no AA
4. Use o Contrast Checker (webaim.org) para verificar

---

## ✅ Checklist WCAG 2.2 AA (Essencial)

**Perceptível:**
- [ ] Imagens têm texto alternativo descritivo
- [ ] Vídeos têm legendas
- [ ] Contraste de texto ≥ 4.5:1 (normal) ou 3:1 (grande)
- [ ] O layout não quebra ao ampliar 200%

**Operável:**
- [ ] Toda funcionalidade funciona com teclado
- [ ] Não há armadilhas de teclado
- [ ] Foco visível em todos os elementos interativos
- [ ] Nenhuma limitação de tempo que o usuário não possa desligar

**Compreensível:**
- [ ] Idioma da página está declarado no HTML
- [ ] Formulários têm rótulos associados
- [ ] Erros são descritos de forma compreensível com sugestão de correção

**Robusto:**
- [ ] HTML é válido e sem erros de parsing
- [ ] Elementos interativos têm nomes, papéis e valores acessíveis

---

## 📖 Referências

- WCAG 2.2: [https://www.w3.org/TR/WCAG22/](https://www.w3.org/TR/WCAG22/)
- WebAIM: [https://webaim.org](https://webaim.org)
- A11y Project: [https://www.a11yproject.com](https://www.a11yproject.com)
- eMAG (Governo Brasileiro): [https://emag.governoeletronico.gov.br](https://emag.governoeletronico.gov.br)
- Deque — axe: [https://www.deque.com/axe/](https://www.deque.com/axe/)

---

[← Módulo anterior](../11-design-inclusivo/README.md) | [Próximo módulo →](../13-interfaces-deficiencia/README.md)

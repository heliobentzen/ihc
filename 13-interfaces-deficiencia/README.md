# 13 — Desenvolvimento de Interfaces para Pessoas com Deficiência

> *"Acessibilidade é uma inovação. Quando você projeta para os extremos, você também serve ao meio."* — Kat Holmes

---

## 🎯 Objetivos de Aprendizagem

- Conhecer as principais tecnologias assistivas
- Desenvolver HTML semântico e acessível
- Implementar navegação por teclado corretamente
- Adaptar interfaces para diferentes tipos de deficiência
- Testar acessibilidade com ferramentas e usuários reais

---

## 1. Tipos de Deficiência e Tecnologias Assistivas

### 1.1 Deficiência Visual

**Cegueira:**
- **Tecnologia:** Leitor de tela (NVDA, JAWS, VoiceOver, TalkBack)
- **Como funciona:** Converte texto em voz ou braille
- **Impacto no design:** Estrutura semântica do HTML é crucial

**Baixa visão:**
- **Tecnologia:** Magnificadores de tela (ZoomText, Lupa do Windows)
- **Como funciona:** Amplia conteúdo da tela
- **Impacto no design:** Layout deve funcionar ampliado; não depender de elementos pequenos

**Daltonismo:**
- **Tecnologia:** Filtros de cor do sistema operacional
- **Como funciona:** Ajusta paleta de cores
- **Impacto no design:** Nunca usar cor como único indicador

### 1.2 Deficiência Auditiva

**Surdez e baixa audição:**
- **Tecnologia:** Legendas, subtítulos, transcrições
- **Como funciona:** Converte áudio em texto visual
- **Impacto no design:** Todo conteúdo em áudio/vídeo precisa de texto equivalente

### 1.3 Deficiência Motora

**Mobilidade reduzida nos membros superiores:**
- **Tecnologias:**
  - Switch Access (um ou dois botões para navegar)
  - Eye tracking (controle por olhar)
  - Controle por voz (Voice Control, Dragon NaturallySpeaking)
  - Teclados adaptados, trackballs, joysticks
- **Impacto no design:** Alvos grandes, navegação por teclado robusta, sem restrições de tempo

### 1.4 Deficiência Cognitiva

**Dislexia, TDAH, deficiência intelectual:**
- **Tecnologias:**
  - Text-to-speech (lê o conteúdo em voz alta)
  - Ferramentas de foco (Reeder, modos de leitura)
  - Assistentes de IA (explicar conteúdo)
- **Impacto no design:** Linguagem simples, estrutura clara, menos distrações

---

## 2. HTML Semântico — A Base da Acessibilidade

**HTML semântico** é a escolha de elementos HTML que descrevem o significado do conteúdo, não apenas sua aparência.

### Por Que Importa Para Acessibilidade

Quando você usa `<button>` em vez de `<div>`, você garante automaticamente:
- Focável via teclado (Tab)
- Ativável por Enter e Espaço
- Papel "botão" anunciado pelo leitor de tela
- Suporte nativo a states (disabled, aria-pressed)

### Comparativo: Sem vs. Com Semântica

```html
<!-- ❌ Sem semântica (leitor de tela não entende) -->
<div class="header">
  <div class="nav">
    <div onclick="navigate('home')">Início</div>
    <div onclick="navigate('about')">Sobre</div>
  </div>
</div>
<div class="content">
  <div class="title">Bem-vindo</div>
  <div class="text">Conteúdo aqui</div>
</div>

<!-- ✅ Com semântica (leitor de tela entende a estrutura) -->
<header>
  <nav aria-label="Menu principal">
    <a href="/">Início</a>
    <a href="/sobre">Sobre</a>
  </nav>
</header>
<main>
  <h1>Bem-vindo</h1>
  <p>Conteúdo aqui</p>
</main>
```

### Estrutura Semântica Completa

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título descritivo da página</title>
</head>
<body>
  <a href="#conteudo-principal" class="skip-link">
    Pular para o conteúdo principal
  </a>

  <header>
    <a href="/">
      <img src="logo.svg" alt="Nome da empresa - Ir para a página inicial">
    </a>
    <nav aria-label="Menu principal">
      <ul>
        <li><a href="/" aria-current="page">Início</a></li>
        <li><a href="/produtos">Produtos</a></li>
        <li><a href="/contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <main id="conteudo-principal">
    <article>
      <h1>Título principal</h1>
      <p>Parágrafo de introdução...</p>

      <section>
        <h2>Seção 1</h2>
        <p>Conteúdo...</p>
      </section>
    </article>

    <aside aria-label="Artigos relacionados">
      <h2>Leia também</h2>
      <!-- ... -->
    </aside>
  </main>

  <footer>
    <nav aria-label="Links do rodapé">
      <!-- ... -->
    </nav>
  </footer>
</body>
</html>
```

---

## 3. Skip Links (Links de Atalho)

Permite que usuários de teclado e leitores de tela pulem blocos repetitivos (como o menu de navegação) e vão direto ao conteúdo principal.

```html
<!-- HTML -->
<a href="#main-content" class="skip-link">
  Pular para o conteúdo principal
</a>

<nav><!-- navegação longa --></nav>

<main id="main-content">
  <h1>Conteúdo da página</h1>
</main>
```

```css
/* CSS — visível somente no foco (teclado) */
.skip-link {
  position: absolute;
  top: -100%;
  left: 0;
  background: #000;
  color: #fff;
  padding: 8px 16px;
  z-index: 9999;
  text-decoration: none;
}

.skip-link:focus {
  top: 0;
}
```

---

## 4. Formulários Acessíveis

Formulários são a parte mais crítica para acessibilidade — onde mais erros acontecem.

```html
<!-- ✅ Formulário acessível completo -->
<form novalidate>
  <div class="field">
    <label for="email">
      E-mail
      <span aria-hidden="true">*</span>
      <span class="sr-only">(obrigatório)</span>
    </label>
    <input
      type="email"
      id="email"
      name="email"
      required
      aria-required="true"
      aria-describedby="email-dica email-erro"
      autocomplete="email"
    >
    <p id="email-dica" class="field-hint">
      Digite o e-mail que você usa para login
    </p>
    <p id="email-erro" role="alert" class="field-error" hidden>
      Por favor, insira um e-mail válido (ex: nome@exemplo.com)
    </p>
  </div>

  <div class="field">
    <fieldset>
      <legend>Preferência de contato</legend>
      <label>
        <input type="radio" name="contato" value="email"> E-mail
      </label>
      <label>
        <input type="radio" name="contato" value="telefone"> Telefone
      </label>
    </fieldset>
  </div>

  <button type="submit">Enviar</button>
</form>
```

```css
/* Classe para conteúdo visível apenas a leitores de tela */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}
```

---

## 5. Componentes Interativos Acessíveis

### Modal/Dialog

```html
<button id="abrir-modal" aria-haspopup="dialog">Abrir formulário</button>

<div
  id="modal"
  role="dialog"
  aria-modal="true"
  aria-labelledby="modal-titulo"
  aria-describedby="modal-descricao"
  hidden
>
  <h2 id="modal-titulo">Confirmar ação</h2>
  <p id="modal-descricao">Você tem certeza que deseja deletar este item?</p>
  <button id="fechar-modal" autofocus>Cancelar</button>
  <button>Deletar</button>
</div>
```

```javascript
// JavaScript — gerenciamento de foco em modal
const modal = document.getElementById('modal');
const abrirBtn = document.getElementById('abrir-modal');
const fecharBtn = document.getElementById('fechar-modal');
let elementoAnterior; // guardar foco anterior

function abrirModal() {
  elementoAnterior = document.activeElement;
  modal.removeAttribute('hidden');
  fecharBtn.focus(); // mover foco para o modal
  armadilhaFoco(modal); // prender foco dentro do modal
}

function fecharModal() {
  modal.setAttribute('hidden', '');
  elementoAnterior.focus(); // devolver foco ao elemento anterior
}

// Fechar com Escape
modal.addEventListener('keydown', (e) => {
  if (e.key === 'Escape') fecharModal();
});
```

### Accordion

```html
<div class="accordion">
  <h3>
    <button
      aria-expanded="false"
      aria-controls="painel-1"
      id="botao-1"
    >
      Pergunta 1
    </button>
  </h3>
  <div
    id="painel-1"
    role="region"
    aria-labelledby="botao-1"
    hidden
  >
    <p>Resposta da pergunta 1...</p>
  </div>
</div>
```

### Tabs

```html
<div role="tablist" aria-label="Seções de configurações">
  <button
    role="tab"
    aria-selected="true"
    aria-controls="painel-perfil"
    id="tab-perfil"
  >Perfil</button>
  <button
    role="tab"
    aria-selected="false"
    aria-controls="painel-seguranca"
    id="tab-seguranca"
    tabindex="-1"
  >Segurança</button>
</div>

<div role="tabpanel" id="painel-perfil" aria-labelledby="tab-perfil">
  Conteúdo do perfil...
</div>
<div role="tabpanel" id="painel-seguranca" aria-labelledby="tab-seguranca" hidden>
  Conteúdo de segurança...
</div>
```

---

## 6. Imagens Complexas e Gráficos

```html
<!-- Gráfico de barras acessível -->
<figure>
  <figcaption>
    <strong>Vendas por trimestre 2024</strong>
    <details>
      <summary>Ver dados em formato tabela</summary>
      <table>
        <caption>Vendas por trimestre</caption>
        <thead>
          <tr><th>Trimestre</th><th>Vendas (R$)</th></tr>
        </thead>
        <tbody>
          <tr><td>Q1</td><td>R$ 120.000</td></tr>
          <tr><td>Q2</td><td>R$ 145.000</td></tr>
          <tr><td>Q3</td><td>R$ 98.000</td></tr>
          <tr><td>Q4</td><td>R$ 167.000</td></tr>
        </tbody>
      </table>
    </details>
  </figcaption>
  <img
    src="grafico-vendas.png"
    alt="Gráfico de barras: Q1 R$120k, Q2 R$145k, Q3 R$98k, Q4 R$167k. Q4 foi o melhor trimestre."
  >
</figure>
```

---

## 7. Conteúdo Dinâmico e SPA

Em Single Page Applications (React, Vue, Angular), o leitor de tela não percebe automaticamente as mudanças de conteúdo.

```javascript
// Após navegação em SPA, anunciar mudança de página
function anunciarMudancaPagina(titulo) {
  const anunciador = document.getElementById('anunciador-sr');
  anunciador.textContent = ''; // limpar
  setTimeout(() => {
    anunciador.textContent = `Página ${titulo} carregada`;
  }, 100);
}
```

```html
<div id="anunciador-sr" aria-live="polite" aria-atomic="true" class="sr-only"></div>
```

---

## 🛠️ Práticas

### Prática 1 — Navegação com Leitor de Tela (60 min)
1. Ative NVDA (Windows) ou VoiceOver (Mac: Cmd+F5)
2. Feche os olhos e tente completar as tarefas num site de e-commerce:
   - Encontrar um produto específico
   - Adicioná-lo ao carrinho
   - Verificar o subtotal
3. Documente cada dificuldade encontrada
4. Proponha correções de HTML para cada problema

### Prática 2 — Formulário Acessível (90 min)
Pegue um formulário de cadastro existente com problemas de acessibilidade.
1. Identifique todos os problemas de acessibilidade
2. Corrija o HTML para torná-lo acessível
3. Valide com axe DevTools
4. Teste com VoiceOver/NVDA
5. Documente as mudanças feitas e o impacto

### Prática 3 — Componente Acessível do Zero (2h)
Implemente um componente de **accordion** acessível do zero (HTML + CSS + JS):
- Funcionando com mouse
- Funcionando com teclado (Enter, Espaço, setas)
- Anunciado corretamente pelo leitor de tela
- Visualmente claro sobre estado (aberto/fechado)

---

## ✅ Checklist de Desenvolvimento Acessível

**HTML:**
- [ ] Estrutura semântica com header, main, footer, nav, section
- [ ] Hierarquia de headings correta (h1 → h2 → h3, sem pular)
- [ ] Imagens com alt text descritivo (vazio para decorativas)
- [ ] Links com texto descritivo (não "Clique aqui")
- [ ] Idioma declarado no `<html lang="...">`

**Formulários:**
- [ ] Todo input tem `<label>` associado via `for`/`id`
- [ ] Campos obrigatórios marcados e descritos
- [ ] Mensagens de erro descritivas e associadas via `aria-describedby`
- [ ] Autocomplete configurado para dados pessoais

**Interação:**
- [ ] Skip link presente
- [ ] Toda funcionalidade acessível por teclado
- [ ] Foco visível em todos os elementos interativos
- [ ] Modais fazem gestão de foco (trap + devolver)
- [ ] Conteúdo dinâmico usa `aria-live` adequado

---

## 📖 Referências

- MDN Web Docs — Accessibility: [https://developer.mozilla.org/en-US/docs/Web/Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- WAI-ARIA Authoring Practices: [https://www.w3.org/WAI/ARIA/apg/](https://www.w3.org/WAI/ARIA/apg/)
- A11y Project Checklist: [https://www.a11yproject.com/checklist/](https://www.a11yproject.com/checklist/)
- Inclusive Components (Heydon Pickering): [https://inclusive-components.design](https://inclusive-components.design)

---

[← Módulo anterior](../12-wcag-acessibilidade/README.md) | [Próximo módulo →](../14-interfaces-conversacionais/README.md)

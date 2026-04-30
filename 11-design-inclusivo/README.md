# 11 — Design Inclusivo

> *"Design inclusivo não é design especial. É design para todos."* — Susan Goltsman

---

## 🎯 Objetivos de Aprendizagem

- Compreender os princípios do Design Inclusivo (Universal Design)
- Distinguir Design Inclusivo de Acessibilidade
- Identificar exclusões que produtos digitais criam
- Aplicar os 7 princípios do Design Universal
- Criar com empatia para a diversidade humana

---

## 1. O Que é Design Inclusivo?

**Design Inclusivo** é uma metodologia que considera toda a diversidade humana no processo de design, incluindo capacidades, idioma, cultura, gênero, idade e outras formas de diferença humana.

### A Diferença Entre Acessibilidade e Design Inclusivo

| Aspecto | Acessibilidade | Design Inclusivo |
|---------|---------------|-----------------|
| **Foco** | Remover barreiras para pessoas com deficiência | Incluir toda diversidade humana |
| **Abordagem** | Conformidade com padrões (WCAG) | Processo de design empático |
| **Resultado** | Produto acessível | Produto que funciona para mais pessoas |
| **Quando acontece** | Frequentemente adicionado depois | Integrado desde o início |

> **Analogia:** Acessibilidade é a rampa de cadeira de rodas adicionada depois que o prédio foi construído. Design Inclusivo é projetar o prédio desde o início para funcionar para todos.

---

## 2. Espectro de Capacidade Humana

A Microsoft publicou o **Inclusive Design Toolkit** com um modelo poderoso: a deficiência não é uma característica fixa de uma pessoa — é uma **incompatibilidade entre a pessoa e o contexto**.

### Os 3 Tipos de Limitação

| Tipo | Exemplos | % da população |
|------|----------|----------------|
| **Permanente** | Amputação, cegueira, surdez | ~15% |
| **Temporária** | Braço quebrado, infecção ocular | Varia |
| **Situacional** | Mão ocupada segurando bebê, sol nos olhos, barulho alto | 100% (em momentos) |

### O Efeito Cascata da Inclusão

```
Solucionar para:         →  Beneficia também:

Usuário de um braço      →  Pessoa com braço engessado
                         →  Pai/mãe segurando bebê
                         →  Pessoa usando o celular no transporte

Usuário com surdez       →  Pessoa em ambiente barulhento
                         →  Pessoa aprendendo outro idioma
                         →  Pessoa com sotaque diferente

Usuário com visão baixa  →  Pessoa sob luz solar forte
                         →  Pessoa com cansaço visual
                         →  Pessoa com óculos quebrado
```

---

## 3. Os 7 Princípios do Design Universal

Desenvolvidos pelo Centro de Design Universal da Universidade Estadual da Carolina do Norte (1997):

### Princípio 1 — Uso Equitativo
O design é útil e pode ser comercializado para pessoas com capacidades diversas.

**Diretrizes:**
- Proporcione os mesmos meios de uso para todos os usuários
- Evite segregar ou estigmatizar qualquer grupo
- Proporcione privacidade e segurança igualitariamente

**Exemplo digital:** Site de banco que funciona tanto para usuário com leitor de tela quanto para usuário com mouse, com as mesmas funcionalidades.

---

### Princípio 2 — Flexibilidade de Uso
O design acomoda uma ampla variedade de preferências e capacidades individuais.

**Diretrizes:**
- Proporcione opções de métodos de uso
- Suporte acesso destro e canhoto
- Facilite a precisão e exatidão do usuário

**Exemplo digital:** App que permite usar biometria, PIN, senha ou padrão de desbloqueio.

---

### Princípio 3 — Uso Simples e Intuitivo
O uso do design é fácil de entender, independente da experiência, conhecimento, habilidades de linguagem ou nível de concentração atual do usuário.

**Diretrizes:**
- Elimine complexidade desnecessária
- Seja consistente com as expectativas e intuições do usuário
- Acomode uma ampla faixa de habilidades de literacia e linguagem

**Exemplo digital:** Ícones universalmente reconhecíveis + rótulo de texto (nunca ícone sem rótulo).

---

### Princípio 4 — Informação Perceptível
O design comunica informação necessária efetivamente ao usuário, independente das condições ambientais ou das capacidades sensoriais.

**Diretrizes:**
- Use diferentes modos (pictorial, verbal, tátil) para apresentar informação essencial
- Proporcione contraste adequado entre informação essencial e seu entorno
- Compatibilize com dispositivos ou técnicas usados por pessoas com limitações sensoriais

**Exemplo digital:** Não use somente cor para comunicar status (erro em vermelho SEM ícone ou texto de apoio é exclusivo para daltônicos).

---

### Princípio 5 — Tolerância ao Erro
O design minimiza riscos e consequências adversas de ações acidentais ou não intencionais.

**Diretrizes:**
- Organize os elementos para minimizar riscos e erros
- Proporcione avisos sobre perigos e erros
- Proporcione recursos de proteção a falhas
- Desencoraje ações inconscientes em tarefas que requerem vigilância

**Exemplo digital:** Confirmação antes de deletar. Gmail desfazer envio.

---

### Princípio 6 — Baixo Esforço Físico
O design pode ser usado eficientemente e confortavelmente com um mínimo de fadiga.

**Diretrizes:**
- Permita ao usuário manter posição corporal neutra
- Use forças operacionais razoáveis
- Minimize ações repetitivas
- Minimize esforço físico sustentado

**Exemplo digital:** Formulários com autopreenchimento, atalhos de teclado, persistência de dados entre sessões.

---

### Princípio 7 — Tamanho e Espaço para Abordagem e Uso
Tamanho e espaço apropriados são proporcionados para abordagem, alcance, manipulação e uso, independente do tamanho corporal, postura ou mobilidade do usuário.

**Diretrizes:**
- Proporcione uma linha de visão clara para elementos importantes
- Torne o alcance de todos os componentes confortável
- Acomode variações no tamanho da mão e da pegada

**Exemplo digital:** Alvos de toque mínimo de 44×44px (Apple) ou 48×48dp (Google). Espaçamento entre elementos clicáveis.

---

## 4. Inclusão nas Pesquisas

Pesquisar apenas com usuários "típicos" produz produtos que excluem pessoas:

### Práticas de Recrutamento Inclusivo

- Incluir explicitamente pessoas com deficiência no painel de pesquisa
- Variar: idade, gênero, etnia, nível de letramento digital, dispositivo
- Realizar pesquisa onde as pessoas estão (não apenas em laboratório)
- Remunerar adequadamente por tempo e contribuição

### Personas Inclusivas

Além das personas principais, crie **personas de extremidade** (edge personas):

- Usuário com baixa visão que usa fonte grande
- Usuário de 65+ anos com baixa familiaridade com tech
- Usuário com analfabetismo funcional
- Usuário em situação de vulnerabilidade econômica (internet limitada, celular básico)

---

## 5. Design Inclusivo na Prática

### Tipografia Inclusiva

| Aspecto | Recomendação |
|---------|--------------|
| Tamanho mínimo | 16px para corpo de texto |
| Altura de linha | 1.5x o tamanho da fonte |
| Comprimento de linha | 60–80 caracteres |
| Peso | Evite pesos muito finos (<400) |
| Itálico | Use com moderação (dificulta leitura para dislexia) |
| Caixa alta | Evite para textos longos |

### Cores Inclusivas

- Contraste mínimo: 4.5:1 para texto normal (WCAG AA)
- Nunca use cor como único indicador
- Teste com simuladores de daltonismo (Figma, Stark, Coblis)

**Tipos de daltonismo:**
- **Deuteranopia:** dificuldade com verde (8% dos homens)
- **Protanopia:** dificuldade com vermelho
- **Tritanopia:** dificuldade com azul/amarelo (raro)

### Linguagem Inclusiva

| Evite | Prefira |
|-------|---------|
| "Louco" para indicar algo exagerado | "Incrível", "surpreendente" |
| "Deficiente" como substantivo | "Pessoa com deficiência" |
| Gênero binário obrigatório | Campos opcionais ou gênero não-binário |
| "Mudo" para silenciar | "Silenciar" |
| Suposição de família tradicional | "Responsável", "adulto de referência" |

---

## 🛠️ Práticas

### Prática 1 — Simulação de Limitações (45 min)
Use extensões de browser ou Figma Accessibility:
1. **Simule visão em túnel:** Navegue em um e-commerce com campo de visão reduzido (cubra as bordas do monitor)
2. **Simule daltonismo:** Use a extensão "Colorblinding" e navegue pelo mesmo site
3. **Simule uso com um braço:** Coloque uma mão nas costas e tente fazer um pedido no iFood
4. Documente o que era difícil e quais melhorias você proporia

### Prática 2 — Audit de Inclusão (60 min)
Avalie um app popular usando os 7 princípios do Design Universal:
1. Para cada princípio, dê uma nota de 1 a 5
2. Identifique os 3 princípios com pior nota
3. Para cada um, proponha 2 melhorias concretas

### Prática 3 — Redesign para Diversidade (90 min)
Escolha um formulário de cadastro existente.
1. Identifique campos que excluem usuários (ex: campo "sobrenome" obrigatório quando muitas culturas não usam)
2. Identifique linguagem não-inclusiva
3. Redesenhe o formulário para ser mais inclusivo
4. Justifique cada mudança

---

## ✅ Checklist de Design Inclusivo

- [ ] O produto foi testado com pessoas com diferentes capacidades?
- [ ] Os alvos de toque têm tamanho mínimo de 44×44px?
- [ ] As cores não são o único indicador de informação importante?
- [ ] O produto funciona bem com ampliação de texto até 200%?
- [ ] O formulário não assume gênero, estado civil ou estrutura familiar?
- [ ] A linguagem evita termos capacitistas e excludentes?
- [ ] O produto funciona em dispositivos básicos e conexões lentas?
- [ ] A tipografia segue as recomendações de legibilidade inclusiva?

---

## 📖 Referências

- Centro de Design Universal: [https://design.ncsu.edu/research/center-for-universal-design/](https://design.ncsu.edu/research/center-for-universal-design/)
- Microsoft Inclusive Design: [https://inclusive.microsoft.design](https://inclusive.microsoft.design)
- HOLMES, Kat. *Mismatch: How Inclusion Shapes Design*. MIT Press, 2018.
- WebAIM — Inclusive Design: [https://webaim.org](https://webaim.org)

---

[← Módulo anterior](../10-etica-design/README.md) | [Próximo módulo →](../12-wcag-acessibilidade/README.md)

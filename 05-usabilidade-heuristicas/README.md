# 05 — Princípios de Usabilidade e Heurísticas de Nielsen

> *"Usabilidade significa que quem usa o produto consegue fazer o que quer fazer, do jeito que espera poder fazer, sem problemas."* — Steve Krug

---

## 🎯 Objetivos de Aprendizagem

- Definir usabilidade segundo a ISO 9241
- Conhecer e aplicar as 10 Heurísticas de Nielsen
- Conduzir uma Avaliação Heurística
- Compreender as Leis de UX mais relevantes
- Distinguir severidade de problemas de usabilidade

---

## 1. O Que é Usabilidade?

Segundo a **ISO 9241-11:2018**, usabilidade é:

> *"A extensão na qual um produto pode ser usado por usuários específicos para alcançar objetivos específicos com eficácia, eficiência e satisfação em um contexto de uso específico."*

### Os 3 Pilares da Usabilidade

| Pilar | Definição | Como medir |
|-------|-----------|------------|
| **Eficácia** | O usuário consegue completar o objetivo? | Taxa de conclusão de tarefa |
| **Eficiência** | Com que esforço/tempo? | Tempo por tarefa, número de cliques |
| **Satisfação** | Como o usuário se sentiu? | SUS, CSAT, questionário |

### Além da ISO — Os 5 Componentes de Nielsen

1. **Aprendizagem:** Quão fácil é realizar tarefas pela primeira vez?
2. **Eficiência:** Quão rápido usuários experientes realizam tarefas?
3. **Memorabilidade:** Ao retornar após um período, quão fácil é lembrar?
4. **Erros:** Quantos erros os usuários cometem? Quão graves?
5. **Satisfação:** Quão agradável é usar o produto?

---

## 2. As 10 Heurísticas de Nielsen (1994)

Jakob Nielsen e Rolf Molich desenvolveram 10 princípios gerais para avaliação de interfaces. São chamados de "heurísticas" porque são regras empíricas, não diretrizes específicas.

---

### H1 — Visibilidade do Status do Sistema

> O sistema deve sempre manter os usuários informados sobre o que está acontecendo, através de feedback adequado em tempo razoável.

**Exemplos corretos:**
- ✅ Barra de progresso durante upload
- ✅ Botão muda de estado ao ser clicado (loading spinner)
- ✅ Notificação de e-mail enviado com sucesso

**Violações comuns:**
- ❌ Botão que não dá nenhum feedback ao clicar
- ❌ Formulário que demora a responder sem indicar que processou
- ❌ Download que começa sem nenhuma indicação

---

### H2 — Correspondência entre o Sistema e o Mundo Real

> O sistema deve falar a linguagem dos usuários, com palavras, frases e conceitos familiares. Siga convenções do mundo real.

**Exemplos corretos:**
- ✅ Ícone de lixeira para deletar (metáfora do mundo real)
- ✅ Carrinho de compras em e-commerce
- ✅ Linguagem simples e direta, sem jargão técnico

**Violações comuns:**
- ❌ Mensagem de erro: "Erro 0x80004005: Falha na operação COM"
- ❌ "Deslogar" em vez de "Sair" ou "Logout"
- ❌ Datas em formato técnico (2024-04-15 em vez de 15/04/2024)

---

### H3 — Controle e Liberdade do Usuário

> Usuários frequentemente escolhem funções por engano e precisam de uma "saída de emergência" claramente marcada para sair do estado indesejado.

**Exemplos corretos:**
- ✅ Ctrl+Z / Desfazer
- ✅ Botão "Cancelar" em modais
- ✅ Gmail: "Desfazer envio" por 10 segundos
- ✅ Confirmar antes de excluir algo irreversível

**Violações comuns:**
- ❌ Sem botão voltar em fluxo de checkout
- ❌ Exclusão permanente sem confirmação
- ❌ Modal sem botão de fechar

---

### H4 — Consistência e Padrões

> Usuários não devem ter que se perguntar se diferentes palavras, situações ou ações significam a mesma coisa. Siga convenções da plataforma.

**Exemplos corretos:**
- ✅ Mesmo ícone para "favoritar" em toda a aplicação
- ✅ Botão primário sempre na mesma posição em todos os modals
- ✅ Mesma linguagem para ações similares

**Violações comuns:**
- ❌ "Salvar" em uma tela, "Gravar" em outra, "Confirmar" em outra
- ❌ Botão de confirmação ora à esquerda, ora à direita
- ❌ Cores diferentes para o mesmo tipo de alerta

---

### H5 — Prevenção de Erros

> Melhor que boas mensagens de erro é um design cuidadoso que previne a ocorrência de problemas.

**Exemplos corretos:**
- ✅ Validação inline em formulários (não apenas no submit)
- ✅ Confirmação antes de ações destrutivas
- ✅ Autocompletar para campos como CEP, endereço

**Violações comuns:**
- ❌ Campo de data sem máscara (usuário digita 01/01/2024, sistema espera 01012024)
- ❌ Botão de cancelar e confirmar lado a lado sem distinção visual clara
- ❌ Formulário que apaga tudo se o usuário errar um campo

---

### H6 — Reconhecimento em vez de Memorização

> Minimize a carga cognitiva tornando objetos, ações e opções visíveis. O usuário não deve ter que lembrar informações de uma parte para outra da interface.

**Exemplos corretos:**
- ✅ Histórico de pesquisas recentes
- ✅ Autocompletar com sugestões visíveis
- ✅ Mostrar opções disponíveis em vez de exigir que o usuário as memorize

**Violações comuns:**
- ❌ Código de produto sem contexto no carrinho de compras
- ❌ Formulário de múltiplas etapas sem resumo das etapas anteriores
- ❌ Atalhos de teclado sem documentação ou tooltips

---

### H7 — Flexibilidade e Eficiência de Uso

> Atalhos — não percebidos por usuários novatos — podem acelerar a interação para usuários experientes. Permita que usuários personalizem ações frequentes.

**Exemplos corretos:**
- ✅ Atalhos de teclado (Ctrl+C, Ctrl+V)
- ✅ Acesso rápido a ações recentes
- ✅ Modo avançado para usuários poder

**Violações comuns:**
- ❌ Sem atalho de teclado para ações frequentes
- ❌ Impossibilidade de personalizar o fluxo de trabalho
- ❌ Usuários experientes obrigados a seguir o mesmo fluxo de iniciantes

---

### H8 — Estética e Design Minimalista

> Diálogos não devem conter informação irrelevante ou raramente necessária. Cada unidade extra de informação compete com a informação relevante.

**Exemplos corretos:**
- ✅ Páginas limpas, com foco no conteúdo principal
- ✅ Modais com apenas as informações necessárias para a decisão
- ✅ Menus com apenas as opções mais usadas visíveis

**Violações comuns:**
- ❌ Landing page com 10 call-to-actions diferentes
- ❌ Dashboard com 20 gráficos simultâneos
- ❌ Formulário com campos desnecessários

---

### H9 — Ajuda aos Usuários para Reconhecer, Diagnosticar e Recuperar-se de Erros

> Mensagens de erro devem ser expressas em linguagem simples (sem códigos), indicar precisamente o problema e sugerir uma solução.

**Estrutura de uma boa mensagem de erro:**
```
❌ Ruim: "Erro 404. Recurso não encontrado."

✅ Bom:  "Esta página não existe.
         Pode ter sido movida ou removida.
         [Ver páginas populares] [Voltar ao início]"
```

**Mais exemplos corretos:**
- ✅ "Senha incorreta. Verifique se o Caps Lock está ativado." [Esqueci minha senha]
- ✅ "O e-mail deve ser no formato nome@dominio.com"
- ✅ "Você tem certeza que deseja cancelar? Seus dados não serão salvos."

---

### H10 — Ajuda e Documentação

> Embora seja melhor que o sistema possa ser usado sem documentação, pode ser necessário fornecer ajuda. Ela deve ser fácil de encontrar, focada na tarefa e listando passos concretos.

**Exemplos corretos:**
- ✅ Tooltips contextuais em campos complexos
- ✅ FAQ integrado ao fluxo
- ✅ Documentação pesquisável e atualizada
- ✅ Chatbot ou suporte acessível

**Violações comuns:**
- ❌ Manual em PDF de 300 páginas
- ❌ Ajuda que leva a uma página genérica sem contexto
- ❌ Sem suporte para erros inesperados

---

## 3. Como Conduzir uma Avaliação Heurística

### Processo (Nielsen, 1994)

1. **Preparação:** Liste as telas/fluxos a serem avaliados
2. **Avaliadores:** Use 3–5 especialistas (mais que isso tem retorno decrescente)
3. **Avaliação individual:** Cada avaliador faz 2 passagens:
   - 1ª: visão geral do fluxo
   - 2ª: foco em elementos específicos comparando com as heurísticas
4. **Agregação:** Reúna e consolide os problemas encontrados
5. **Severidade:** Classifique cada problema

### Escala de Severidade

| Nível | Descrição | Ação |
|-------|-----------|------|
| **0** | Não é problema | Ignorar |
| **1** | Cosmético | Corrigir se houver tempo |
| **2** | Menor | Baixa prioridade |
| **3** | Maior | Alta prioridade |
| **4** | Catastrófico | Corrigir antes de lançar |

### Template de Relatório

```
ID: H01-001
Heurística: H3 — Controle e Liberdade do Usuário
Severidade: 4 — Catastrófico
Localização: Tela de checkout, etapa 3 de 4
Descrição: Não há botão "Voltar" para corrigir dados de entrega
Captura: [screenshot]
Recomendação: Adicionar botão "← Voltar" com estilo secundário no canto inferior esquerdo
```

---

## 4. Leis de UX Relevantes

| Lei | Descrição | Aplicação prática |
|-----|-----------|-------------------|
| **Lei de Fitts** | Quanto maior e mais próximo o alvo, mais fácil clicar | Botões CTA grandes, ações críticas longe do canto |
| **Lei de Hick** | Mais opções = mais tempo para decidir | Limitar opções de menu; progressive disclosure |
| **Lei de Miller** | Memória de curto prazo: 7 ± 2 itens | Listas de no máximo 7 itens; dividir formulários longos |
| **Efeito de Posição Serial** | Lembramos melhor o primeiro e o último item | Colocar ações importantes no início e no fim |
| **Princípio da Proximidade** (Gestalt) | Elementos próximos parecem relacionados | Agrupar labels com seus campos |
| **Lei de Jakob** | Usuários gastam mais tempo em outros sites | Siga convenções conhecidas |

---

## 🛠️ Práticas

### Prática 1 — Avaliação Heurística (90 min)
1. Escolha um app de banco (Nubank, Bradesco, Itaú, etc.)
2. Avalie o fluxo de "Fazer uma transferência PIX"
3. Para cada heurística, identifique violações (se houver)
4. Classifique a severidade de cada problema
5. Monte um relatório com pelo menos 5 problemas documentados com screenshots

### Prática 2 — Bingo de Heurísticas (30 min)
1. Acesse 5 sites/apps aleatórios por 5 minutos cada
2. Para cada app, marque quais heurísticas foram violadas
3. Compare com os colegas: quem encontrou mais violações?

### Prática 3 — Redesign Heurístico (60 min)
1. Identifique a violação mais grave encontrada na Prática 1
2. Crie um wireframe simples (papel ou digital) mostrando a correção proposta
3. Justifique sua proposta com base na heurística violada

---

## ✅ Checklist — Avaliação Heurística Completa

- [ ] H1: O sistema informa o status atual ao usuário?
- [ ] H2: A linguagem e os ícones fazem sentido para o usuário?
- [ ] H3: O usuário pode desfazer ações e sair de fluxos indesejados?
- [ ] H4: A interface é consistente interna e externamente?
- [ ] H5: O design previne erros antes que aconteçam?
- [ ] H6: O usuário precisa memorizar pouca coisa para usar o produto?
- [ ] H7: Há atalhos e personalizações para usuários avançados?
- [ ] H8: A interface é limpa e foca no que é essencial?
- [ ] H9: As mensagens de erro são claras e construtivas?
- [ ] H10: Há documentação/ajuda contextual acessível?

---

## 📖 Referências

- NIELSEN, Jakob; MOLICH, Rolf. *Heuristic evaluation of user interfaces*. CHI '90 Conference Proceedings.
- KRUG, Steve. *Don't Make Me Think*. New Riders, 2014.
- Laws of UX: [https://lawsofux.com](https://lawsofux.com)
- Nielsen Norman Group — 10 Heuristics: [https://www.nngroup.com/articles/ten-usability-heuristics/](https://www.nngroup.com/articles/ten-usability-heuristics/)

---

[← Módulo anterior](../04-arquitetura-informacao/README.md) | [Próximo módulo →](../06-prototipacao/README.md)

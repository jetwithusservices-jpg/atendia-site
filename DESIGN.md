# Sistema de Design: A Voz da Inovação Fluida

## 1. Creative North Star: "O Eco Digital"
Este sistema de design não é apenas uma interface de utilizador; é uma representação visual da clareza e da fluidez da voz humana processada por IA. Definimos o nosso North Star como **"O Eco Digital"** — um equilíbrio entre a precisão tecnológica (Teal/Inter) e a profundidade orgânica (Camadas de Vidro/Sombras Difusas).

Ao contrário das ferramentas enterprise tradicionais que dependem de grelhas rígidas e linhas divisórias pesadas, este sistema utiliza a **assimetria intencional** e a **profundidade tonal** para guiar o utilizador. O objetivo é que a interface pareça respirar, utilizando o espaço em branco (whitespace) como um elemento ativo, e não apenas um vazio.

---

## 2. Paleta de Cores e Atmosfera
A nossa abordagem às cores rompe com o "flat design" comum para abraçar uma estética editorial de alta gama.

### Funções Cromáticas
- **Primary & Primary Container:** O nosso Teal (`#006a65` a `#4ECDC4`) é a voz da marca. Deve ser usado para guiar a ação e destacar inteligência.
- **Secondary:** O Roxo Profundo (`#7000d9`) serve como um contraponto sofisticado, injetando uma sensação de tecnologia premium e "premiumness" de IA.
- **Neutral Surface Hierarchy:** Utilizamos a escala de `surface-container` para definir a arquitetura da informação.

### Regras de Aplicação Editorial
- **A Regra "No-Line":** É estritamente proibido o uso de bordas sólidas de 1px para separar secções. A separação deve ser feita exclusivamente através da transição de tons (ex: uma secção `surface-container-low` sobre um fundo `surface`) ou através de margens generosas da nossa escala de espaçamento.
- **Assinatura de Textura (Gradients):** Os botões principais e elementos de herói devem utilizar um gradiente linear suave de `primary` para `primary_container`. Isso confere "alma" visual e profundidade que cores planas não conseguem replicar.
- **Glassmorphism:** A barra de navegação e os cartões flutuantes devem utilizar o efeito de vidro fosco (`surface` com 60% de opacidade e `backdrop-filter: blur(20px)`). Isto faz com que a interface pareça integrada e estratificada.

---

## 3. Tipografia Editorial
A tipografia é o esqueleto da nossa autoridade. Utilizamos a **Inter** de forma extrema: pesos pesados para o impacto e pesos leves/médios para a legibilidade.

- **Display & Headline:** Devem ser "impactantes". Use `display-lg` (3.5rem) com `font-weight: 800` para mensagens herói. A escala é deliberadamente grande para criar um contraste dramático com o corpo de texto.
- **Body & Title:** O corpo de texto em `body-lg` (1rem) deve ter um `line-height` generoso (1.6) para garantir que a leitura em Português (PT) seja confortável e fluida.
- **Hierarquia de Marca:** Os títulos não servem apenas para organizar; eles comandam a atenção através do uso de `on_surface` (preto profundo `#171c23`), criando um contraste nítido contra os fundos suaves.

---

## 4. Elevação, Profundidade e Camadas
Rejeitamos o conceito de sombras "drop-shadow" genéricas. A profundidade é alcançada através do **Empilhamento Tonal**.

- **Princípio de Camadas:** Coloque um cartão `surface-container-lowest` sobre uma secção `surface-container-low`. O contraste subtil cria uma elevação natural, eliminando a necessidade de sombras pesadas.
- **Sombras Ambientais:** Quando um elemento precisa de flutuar (ex: Modais ou Floating Action Buttons), use sombras extra-difusas.
  - *Especificação:* Blur de 40px-60px, opacidade de 4%-8%, com o tom da sombra derivado do `on-surface` (um azul-escuro matizado) e não cinzento neutro.
- **Ghost Border Fallback:** Se uma borda for indispensável para acessibilidade, utilize o token `outline_variant` com uma opacidade de 15%. Nunca use 100% de opacidade em bordas.

---

## 5. Componentes de Assinatura

### Botões (Premium CTAs)
- **Primary:** Gradiente de `primary` para `primary_container`. Raio de curvatura `md` (0.75rem). Efeito de brilho subtil no hover.
- **Secondary:** Sem fundo, apenas um "Ghost Border" e texto `secondary`.
- **Interação:** No estado de hover, o botão deve subir ligeiramente (-2px) e a sombra ambiental deve expandir-se.

### Cartões e Listas (Cards & Lists)
- **Proibição de Divisores:** Não utilize linhas para separar itens de lista. Use o espaçamento `spacing-4` (1.4rem) ou alternância subtil de cores de fundo.
- **Dashboard Mockups:** Os gráficos devem usar a paleta `primary` e `secondary` com gradientes de preenchimento que desvanecem para transparente.

### Inputs de Formulário
- Campos de texto minimalistas. O rótulo (label) utiliza `label-md`. O estado de foco (focus) não deve apenas mudar a cor da borda, mas sim elevar o contentor através de um brilho exterior suave em `primary_fixed`.

### Chips de Estado de Agente
- Utilizados para mostrar o status do agente de voz (ex: "A ouvir", "A processar"). Devem ter uma pulsação de opacidade suave e cantos `full` (9999px).

---

## 6. Do’s e Don’ts (Práticas Recomendadas)

### ✅ Do’s
- **Use o Espaço como Luxo:** Deixe o conteúdo respirar. Se estiver na dúvida, aumente o padding para o nível seguinte da escala.
- **Movimento Fluido:** Implemente efeitos de parallax subtis em imagens de dashboard para criar uma sensação de profundidade 3D.
- **Micro-interações:** Cada clique deve ter uma resposta visual suave, preferencialmente uma transição de cor ou escala de 200ms.

### ❌ Don’ts
- **Não use Cinzentos Mortos:** Evite `#808080`. Use as nossas variantes de `surface-variant` que contêm pigmentação azulada/teal para manter a harmonia cromática.
- **Não alinhe tudo ao centro:** A assimetria (ex: texto à esquerda com uma imagem de dashboard ligeiramente "cortada" à direita) cria uma estética moderna e dinâmica.
- **Não use sombras duras:** Sombras com pouco blur ou alta opacidade destroem a estética "Glassmorphism".

---

**Nota Final:** Este sistema foi desenhado para a Atendia ser líder de mercado. Cada detalhe, desde a ausência de linhas até à escolha do Teal vibrante, deve comunicar uma mensagem clara: **A tecnologia de voz agora é humana, fluida e invisível.**
# PROMPT PARA O ANTIGRAVITY — ECOSSISTEMA PRESENTE DIA DOS NAMORADOS

---

## SOBRE ESTE PROJETO

Você vai construir um presente digital completo de Dia dos Namorados. O projeto tem **duas partes** e você deve tratar ambas como um único ecossistema coeso — não dois projetos separados:

- **Parte 1 — Site romântico** (seu foco principal): um web app em HTML/CSS/JS puro
- **Parte 2 — APK musical** (orientação e instruções): customização do app Vivi Music em Flutter

O dispositivo alvo é um smartphone de entrada com pouca RAM e processador fraco (pense: Moto E, Samsung A01). Performance é tão importante quanto beleza. O resultado deve parecer artesanal, feito à mão, com cuidado — sem cara de template de IA.

---

## MODO DE TRABALHO — ETAPAS OBRIGATÓRIAS

**Não escreva código imediatamente.** Trabalhe em etapas, apresentando cada uma antes de avançar:

### ETAPA 0 — DIAGNÓSTICO E LEVANTAMENTO
Antes de qualquer coisa, me informe:
- Quais arquivos você vai precisar que eu forneça (fotos, músicas, etc.)
- Quais informações pessoais você precisa de mim (data do início do namoro, nome dela, textos das cartas, músicas favoritas de vocês, etc.)
- Se há alguma decisão técnica que depende de resposta minha antes de começar
- Liste tudo de forma clara e organizada para que eu possa coletar antes de você codar

### ETAPA 1 — ARQUITETURA E PLANO
Apresente o plano completo antes de escrever qualquer linha de código:
- Estrutura de arquivos que será gerada
- Mapa de componentes do site
- Decisões técnicas justificadas
- Quais bibliotecas serão usadas e por quê (apenas as necessárias)
Aguarde minha aprovação antes de avançar.

### ETAPA 2 — SITE: HTML + CSS (sem JS ainda)
Construa toda a estrutura e visual do site. Entregue o arquivo com o JS como placeholder comentado. Eu devo conseguir ver o layout e aprovar o visual antes da lógica entrar.

### ETAPA 3 — SITE: JAVASCRIPT
Adicione toda a lógica interativa sobre o HTML/CSS aprovado. Contador, cartas, player, FAB, splash.

### ETAPA 4 — REVISÃO E AJUSTES DO SITE
Após eu testar no celular, aplicar correções de layout, performance ou bugs que eu reportar.

### ETAPA 5 — GUIA DO APK (Vivi Music)
Após o site aprovado, entregue o guia técnico completo e passo a passo para eu customizar o Vivi Music. Não precisa escrever todo o código Flutter — explique o que alterar, onde, como, com trechos de código dos pontos críticos.

### ETAPA 6 — GUIA DE DEPLOY E ENTREGA
Instruções finais para hospedar o site e instalar o APK no celular dela de surpresa.

---

## PARTE 1 — SITE ROMÂNTICO

### IDENTIDADE VISUAL

**Paleta obrigatória:**
- Fundo base: gradiente de entardecer `#FFF5F7` → `#FCDDE6` → `#F4B8C8` → `#E8A7B6` → `#D4956A`
- Ouro rosé: `#E8A7B6`
- Ouro quente: `#D4956A`
- Texto principal: `#4A3538`
- Texto suave: `#8B6B6E`

**Tipografia:**
- Importe somente: `https://fonts.googleapis.com/css2?family=Caveat:wght@400;600&family=Lato:wght@300;400&display=swap`
- `Caveat` para títulos, cartas e elementos emocionais
- `Lato 300` para textos de UI

**Estética:** romântica, delicada, artesanal. O tema visual é o entardecer/céu de lanternas do filme Enrolados (Rapunzel). Hello Kitty e Snoopy aparecem **apenas** como SVGs inline em micro-detalhes (laço divisor, ícone do FAB). Não poluir a tela com eles.

---

### BIBLIOTECAS PERMITIDAS

Para o site, use **somente o que for estritamente necessário e leve**. São permitidas:
- Google Fonts (via `<link>` — apenas os dois pesos definidos acima)
- Nenhuma outra biblioteca é necessária para o site — tudo deve ser HTML5/CSS3/Vanilla JS

**Proibido para o site:**
- React, Vue, Angular
- Tailwind, Bootstrap
- Framer Motion, GSAP, Anime.js ou qualquer lib de animação
- jQuery

---

### RESTRIÇÕES TÉCNICAS DO SITE

- Animações **exclusivamente** via `transform: translate3d`, `opacity`, `rotate` — usar GPU, nunca animar `width`, `height`, `top`, `left`
- `will-change` apenas onde estritamente necessário
- Imagens: apenas SVG inline ou slots com `loading="lazy"` e classe `.webp-ready`
- PWA mínimo: `<meta name="theme-color" content="#E8A7B6">` e `<meta name="apple-mobile-web-app-capable" content="yes">`
- `<meta charset="UTF-8">` obrigatório (evita quebra de acentos e emojis)
- Respeitar `@media (prefers-reduced-motion: reduce)` — zerar animações
- Entrega: **único arquivo `index.html`** com `<style>`, `<body>` e `<script>` organizados e comentados

---

### COMPONENTES DO SITE — CONSTRUA TODOS

#### 1. SPLASH SCREEN
- Fundo: gradiente de céu noturno `#1a0a2e` → `#2d1045` → `#6b2d5e` → `#c46b7a` → `#F4B8C8`
- Estrelas: 50+ pontos `<div>` gerados via JS com `position: absolute`, tamanhos e delays aleatórios, animação `twinkle` em CSS (`opacity` + `scale`)
- 1 lanterna principal centralizada em SVG inline com animação `float-up` contínua (apenas `transform: translate3d + rotate`)
- 4 a 5 lanternas menores ao fundo com `animation-duration` e `animation-delay` diferentes
- Texto em `Caveat` com frase romântica + hint "toque para abrir" pulsando em `opacity`
- Ao toque/clique: fade-out suave na splash, reveal do conteúdo principal

#### 2. HERO — CONTADOR DE TEMPO
- Sol de Corona como SVG inline de fundo, `opacity: 0.18`, `pointer-events: none`
- Grid do contador: linha 1 (Anos / Meses / Dias) + linha 2 (Horas / Minutos / Segundos)
- Células com `backdrop-filter: blur(6px)`, números em `Caveat` cor `#D4956A`
- **JS obrigatório:** `requestAnimationFrame` em loop, nunca `setInterval`. Atualizar DOM apenas quando segundo mudar

#### 3. DIVISORES HELLO KITTY
- SVG inline do laço da Hello Kitty entre seções, opacidade ~0.55
- Linhas laterais via CSS `::before` e `::after`

#### 4. BAÚ DE MEMÓRIAS — 3 CARTAS INTERATIVAS
- 3 envelopes com aba superior colorida (gradiente diferente em cada)
- Abertura por toque: `max-height: 0 → 600px` com `cubic-bezier(0.34, 1.56, 0.64, 1)`
- Texto em `Caveat` com `repeating-linear-gradient` simulando papel pautado
- Comentários `/* EDITE */` em todos os textos

#### 5. GALERIA DE MEMÓRIAS
- CSS Grid 2 colunas, 1 foto destaque (`grid-column: 1/-1`, `aspect-ratio: 16/9`) + 4 menores
- Slots com `loading="lazy"`, classe `.webp-ready`, placeholders elegantes enquanto fotos não são plugadas

#### 6. MINI-PLAYER DE VINIL
- Card com `backdrop-filter: blur(10px)`
- Disco de vinil em CSS puro com `repeating-conic-gradient` + animação `spin-vinil` ao tocar
- `<audio preload="none">` — usuário plugará os arquivos depois
- Constante `PLAYLIST` editável no topo do script

#### 7. BOTÃO DO DENGO — FAB
- `position: fixed`, `bottom: 24px`, `right: 20px`
- Ícone SVG do Snoopy com coraçãozinho
- Toast com mensagem aleatória do array `MENSAGENS_DENGO`, some após 3800ms

#### 8. FOOTER
- SVG inline do Snoopy deitado
- Mensagem final em `Caveat`

---

### ESTRUTURA DO SCRIPT — CONSTANTS EDITÁVEIS NO TOPO

O `<script>` deve iniciar com bloco bem delimitado:

```js
/* =============================================
   EDITE AQUI — SEUS DADOS PESSOAIS
============================================= */
const DATA_INICIO      = new Date(2022, 1, 14);  // EDITE: ano, mês-1, dia
const PLAYLIST         = [{ titulo: '...', artista: '...', src: '' }]; // EDITE
const MENSAGENS_DENGO  = ['Vale um abraço...'];   // EDITE: mensagens pessoais
```

---

### ANIMAÇÕES DE ENTRADA

- `IntersectionObserver` com `threshold: 0.1` para fade-in das seções ao rolar
- Após animar: `observer.unobserve()` — para de monitorar e economiza CPU

---

## PARTE 2 — APK VIVI MUSIC CUSTOMIZADO

Após o site aprovado, entregue um **guia técnico passo a passo** para eu customizar o repositório open-source do Vivi Music (Flutter). O APK final deve parecer "o Spotify dela" — identidade visual idêntica ao site.

### Bibliotecas e ferramentas permitidas para o APK
- Flutter SDK (já incluso no projeto Vivi Music)
- Dependências já existentes no `pubspec.yaml` do Vivi Music — altere apenas o necessário
- GitHub Actions para compilar o APK em nuvem (sem precisar instalar Flutter localmente)
- Ferramentas de compressão de imagem (ex: `cwebp`, Squoosh) para otimizar assets

### O guia deve cobrir, em ordem:

**1. Setup inicial**
- Como clonar o repositório do Vivi Music
- Como configurar o ambiente (ou como usar GitHub Actions para evitar setup local)
- Quais arquivos tocar e quais não tocar

**2. Tema visual**
- Localizar o arquivo `theme.dart` (ou equivalente) e alterar `ThemeData`
- Trocar todas as cores para a paleta do projeto: rosa pastel, ouro rosé, branco suave
- Quais variáveis de cor alterar exatamente (com os valores hex prontos)

**3. Identidade do app**
- Como trocar o ícone do app (pasta `mipmap` no Android, `Assets.xcassets` no iOS se aplicável)
- Como trocar a splash screen do Flutter
- Como mudar o nome do app para algo personalizado (ex: "♡ Para você")

**4. Playlist personalizada**
- Como criar uma aba ou seção "Nossas músicas" com dados estáticos (sem depender de API externa)
- Estrutura do array/model de dados para as músicas dedicatórias
- Como injetar os IDs do YouTube para o Vivi Music tocar (o app já usa YouTube/Piped internamente)

**5. Performance e tamanho**
- Como manter o APK abaixo de ~40MB
- Como otimizar os assets inseridos (ícones, splash) para não inflar o pacote
- O que **não** adicionar para não quebrar a performance no celular fraco

**6. Build e assinatura**
- Como gerar o APK em modo `release` com `flutter build apk --release`
- Como configurar o GitHub Actions para fazer o build automaticamente
- Como assinar o APK corretamente para que o Google Play Protect não bloqueie na instalação

---

## PARTE 3 — GUIA DE DEPLOY E ENTREGA SURPRESA

Após ambas as partes prontas, entregue:

**Deploy do site:**
- Como subir o `index.html` + assets no Vercel ou GitHub Pages (gratuito)
- Como gerar a URL final limpa
- Como forçar cache bust para garantir que o celular dela carregue sempre a versão mais recente

**Instalação oculta do APK:**
- Passo a passo de como habilitar "fontes desconhecidas" no Android dela
- Como instalar o APK sem ela perceber antes da hora
- Como colocar o ícone na tela inicial em posição de destaque
- Como limpar os rastros (histórico de arquivos baixados, etc.) para manter a surpresa

---

## CHECKLIST FINAL — ANTES DE CONSIDERAR ENTREGUE

**Site:**
- [ ] Splash funciona no toque e some com transição suave
- [ ] Contador usa `requestAnimationFrame`, não `setInterval`
- [ ] Cartas abrem e fecham com animação fluida no toque
- [ ] Vinil gira ao tocar, para ao pausar
- [ ] FAB mostra toast aleatório com mensagem carinhosa
- [ ] Nenhuma animação usa `top`, `left`, `width` ou `height` como propriedade animada
- [ ] `@media (prefers-reduced-motion)` zerando animações
- [ ] Tags PWA presentes no `<head>`
- [ ] `charset UTF-8` presente
- [ ] Comentários `/* EDITE */` em todos os pontos personalizáveis
- [ ] Testado mentalmente em viewport 360px (Moto E)

**APK:**
- [ ] Paleta idêntica ao site
- [ ] Ícone personalizado (Snoopy + rosa)
- [ ] Splash screen customizada
- [ ] Playlist de dedicatórias funcionando
- [ ] APK abaixo de 40MB
- [ ] Build release assinado

**Deploy:**
- [ ] Site no ar com URL limpa
- [ ] APK instalado sem rastros
- [ ] Presente pronto para surpreender

---

## FILOSOFIA DO PROJETO

A tecnologia deve ser **invisível**. Ela abre a porta, mas quem deve ser sentido é o amor de quem fez. O resultado final deve parecer que foi construído por alguém que conhece cada detalhe da pessoa que vai receber — não por uma IA, não por um template. Por você.

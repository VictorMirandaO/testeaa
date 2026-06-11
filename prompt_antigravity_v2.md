# PROMPT PARA O ANTIGRAVITY — PRESENTE DE DIA DOS NAMORADOS

---

## QUEM SOU EU E O QUE ESTOU FAZENDO

Estou criando um presente digital para a minha namorada no Dia dos Namorados. Não quero algo genérico. Quero algo que, quando ela abrir, ela sinta que **eu** fiz — com cuidado, com detalhes, pensando nela. Cada elemento deve ter um motivo de existir. A tecnologia deve ser invisível. O amor deve ser o que aparece.

Ela adora:
- **Rapunzel / Enrolados** — é o filme favorito dela. As lanternas flutuantes, o Sol de Corona, o céu noturno de Corona, a paleta quente e dourada do filme. Isso é a base visual do projeto.
- **Hello Kitty** — o laço, o rosa, a delicadeza. Aparece nos detalhes, nunca dominando.
- **Snoopy** — o Snoopy deitado, o Snoopy sonhando, o Snoopy com fone de ouvido. Aparece como easter egg, como ícone carinhoso.
- **Rosa** — em todas as variações. Rosa pastel, ouro rosé, branco suave. É a cor dela.
- **Coisas delicadas e artesanais** — ela percebe quando algo foi feito com capricho. Ela vai notar cada detalhe.

O celular dela é fraco (entrada de linha, pouca RAM). Se o site travar, o presente quebra. Performance não é opcional — é parte do carinho.

---

## O QUE VOCÊ VAI CONSTRUIR

Um ecossistema digital de presente com **duas partes**:

**Parte 1 — Site romântico** (foco principal): um web app em HTML/CSS/JS puro, mobile-first, otimizado, artesanal.

**Parte 2 — APK musical** (guia técnico): customização do app open-source Vivi Music em Flutter para virar o "Spotify dela" — com a identidade visual do site, playlist das músicas de vocês, ícone do Snoopy com fone.

Os dois devem parecer parte da mesma experiência. Mesmas cores, mesmo cuidado, mesma alma.

---

## MODO DE TRABALHO — ETAPAS, NÃO TUDO DE UMA VEZ

Não escreva código imediatamente. Trabalhe em etapas e aguarde minha aprovação entre elas.

### ETAPA 0 — LEVANTAMENTO (COMECE AQUI)
Antes de qualquer código, me faça todas as perguntas necessárias. Liste tudo que você precisa de mim:
- Informações pessoais (data do início do namoro, nome dela, nome meu)
- Conteúdo das 3 cartas (ou se prefiro escrever eu mesmo)
- Lista de músicas para a playlist do site e do APK
- Fotos que vou querer inserir (quantas, em que seções)
- Mensagens para o Botão do Dengo
- Qualquer decisão de design que dependa de algo que só eu sei

Organize as perguntas de forma clara. Só avance quando eu responder.

### ETAPA 1 — PLANO E ARQUITETURA
Com minhas respostas em mãos, apresente:
- Estrutura de arquivos
- Mapa de componentes
- Decisões técnicas justificadas
- Lista de bibliotecas que serão usadas (apenas as necessárias)

Aguarde minha aprovação antes de codar.

### ETAPA 2 — SITE: ESTRUTURA E VISUAL
HTML completo + CSS. JavaScript como comentários placeholder. Devo ver e aprovar o visual antes da lógica entrar.

### ETAPA 3 — SITE: JAVASCRIPT
Toda a lógica interativa sobre o HTML/CSS aprovado.

### ETAPA 4 — TESTES E AJUSTES
Após eu testar no celular, aplicar correções que eu reportar.

### ETAPA 5 — GUIA DO APK
Guia técnico passo a passo para eu customizar o Vivi Music.

### ETAPA 6 — DEPLOY E ENTREGA SURPRESA
Instruções para hospedar o site e instalar o APK no celular dela sem ela perceber.

---

## PARTE 1 — SITE ROMÂNTICO

### IDENTIDADE VISUAL

O site é o entardecer de Corona. Quando ela abrir, deve sentir que está naquela cena das lanternas — aquela sensação de magia, de algo que acontece uma vez na vida, de ver o mundo de cima com a pessoa certa.

**Paleta:**
| Nome | Hex | Uso |
|---|---|---|
| Rosa Fundo | `#FFF5F7` | Base da página |
| Rosa Suave | `#FCDDE6` | Gradiente mid |
| Rosa Médio | `#F4B8C8` | Gradiente mid |
| Ouro Rosé | `#E8A7B6` | Destaque, bordas, divisores |
| Ouro Quente | `#D4956A` | Números do contador, botões, assinaturas |
| Texto | `#4A3538` | Corpo de texto |
| Texto Suave | `#8B6B6E` | Labels, subtítulos |

O gradiente de fundo do `body` vai de `#FFF5F7` no topo até `#D4956A` na base — como o céu de Corona indo do rosa ao dourado.

**Tipografia:**
- Importe via Google Fonts: `Caveat` (400 e 600) + `Lato` (300 e 400) — apenas esses dois pesos cada
- `Caveat`: títulos, cartas, assinaturas, tudo que é emocional. É a letra "escrita à mão" do projeto.
- `Lato 300`: UI, labels, textos de suporte. Leve, limpo, discreto.

**Uso do Rapunzel/Enrolados:**
- A splash screen é o céu noturno de Corona com lanternas flutuando — essa é a abertura do presente
- O Sol de Corona (símbolo circular com raios) aparece como SVG inline de fundo no hero, bem sutil (opacidade ~0.18)
- A paleta inteira remete ao entardecer do filme
- O clima é de magia, de céu aberto, de algo grandioso acontecendo

**Uso do Hello Kitty:**
- Aparece **apenas** como laço SVG nos divisores entre seções
- O laço é o elemento de transição — delicado, feminino, dela
- Nunca em tamanho grande, nunca como figura completa
- Cores: `#FFB7CC` e `#FF8FAB`

**Uso do Snoopy:**
- Aparece **apenas** em dois lugares: o ícone do Botão do Dengo (FAB) e o footer decorativo
- No FAB: cabeça do Snoopy com um coraçãozinho — simples, fofo, reconhecível
- No footer: Snoopy deitado, sonhando — como encerramento carinhoso
- Nunca em tamanho dominante, nunca competindo com o conteúdo emocional
- Todos em SVG inline, desenhados com traço suave

**O que NÃO fazer:**
- Não usar fundos com Hello Kitty ou Snoopy em pattern/repetição
- Não colocar esses personagens em tamanho grande ou como elemento principal
- Não criar algo que parece loja de produtos infantis
- Não criar algo que parece landing page comercial
- Não usar sombras pesadas, gradientes metálicos, efeitos 3D exagerados
- Não usar partículas, confetes, fogos de artifício em loop — são pesados e genéricos

---

### BIBLIOTECAS PERMITIDAS PARA O SITE

O site deve ser Vanilla — sem frameworks, sem libs de animação:
- ✅ Google Fonts via `<link>` (apenas os pesos definidos)
- ✅ Nenhuma outra biblioteca é necessária
- ❌ React, Vue, Angular
- ❌ Tailwind, Bootstrap
- ❌ Framer Motion, GSAP, Anime.js, qualquer lib de animação
- ❌ jQuery

---

### RESTRIÇÕES TÉCNICAS

- Animações via `transform: translate3d`, `opacity`, `rotate` exclusivamente — GPU, sem `top/left/width/height` animados
- `will-change` apenas onde necessário e removido após a animação
- `requestAnimationFrame` para o contador — nunca `setInterval`
- `IntersectionObserver` para fade-in das seções ao rolar — `unobserve()` após animar
- Imagens: SVG inline ou `<img loading="lazy" class="webp-ready">` com placeholder
- `<meta charset="UTF-8">` obrigatório
- PWA: `<meta name="theme-color" content="#E8A7B6">` + `<meta name="apple-mobile-web-app-capable" content="yes">`
- `@media (prefers-reduced-motion: reduce)` zerando todas as animações
- Entrega: **único arquivo `index.html`** comentado e organizado

---

### COMPONENTES — CONSTRUA TODOS

#### 1. SPLASH SCREEN — O CÉU DE CORONA

É a primeira coisa que ela vai ver. Deve parecer que ela abriu uma janela para o céu noturno de Corona, cheio de lanternas subindo.

- Fundo: gradiente noturno `#1a0a2e` → `#2d1045` → `#6b2d5e` → `#c46b7a` → `#F4B8C8`
- 50+ estrelas geradas via JS: `<div>` com `position: absolute`, tamanhos (1–3px) e delays aleatórios, animação `twinkle` em CSS apenas com `opacity` e `scale`
- **Lanterna principal centralizada** em SVG inline: corpo retangular com `rx`, anéis superior e inferior, franjas inferiores, brilho interno com `ellipse`. Animação `float-up` suave e contínua (`transform: translate3d + rotate`)
- **4–5 lanternas menores** espalhadas ao fundo com `position: absolute`, `opacity: 0.3–0.4`, cada uma com `animation-duration` e `animation-delay` diferentes — devem parecer independentes, subindo em ritmos distintos
- Texto centralizado: frase romântica em `Caveat` + "toque para abrir" pulsando em `opacity`
- **Ao toque:** `.fade-out` na splash (`opacity: 0`, `scale(1.05)`, `transition: 0.8s ease`) + `.visible` no `#main`. Após 900ms: `display: none`

#### 2. HERO — CONTADOR DE TEMPO

- SVG do Sol de Corona inline, centralizado, `opacity: 0.18`, `pointer-events: none`, fundo do hero
- Frase poética em `Caveat` tamanho menor antes do título
- Título principal em `Caveat` 2.4rem — algo como "já faz tanto tempo juntos 🌙"
- **Grid do contador:**
  - Linha 1: Anos / Meses / Dias
  - Linha 2: Horas / Minutos / Segundos
  - Células: `background: rgba(255,255,255,0.62)`, `backdrop-filter: blur(6px)`, `border-radius: 14px`
  - Números em `Caveat` cor `#D4956A`, labels em maiúsculas pequenas cor `#8B6B6E`
- **JS:** `requestAnimationFrame` em loop. `DATA_INICIO` como constante editável no topo. Atualizar DOM apenas quando o segundo mudar (comparar com `ultimoSeg`). Calcular anos/meses/dias corretamente com ajuste de overflow

#### 3. DIVISORES — LAÇO DA HELLO KITTY

Entre cada seção principal, um divisor elegante:
- SVG inline do laço da Hello Kitty: dois `<ellipse>` rotacionados + círculo central, `#FFB7CC` e `#FF8FAB`
- Linhas laterais via CSS `::before` e `::after`: `background: linear-gradient(90deg, transparent, #E8A7B6, transparent)`
- `display: flex`, `align-items: center`, `gap: 10px`
- Opacidade geral: 0.55

#### 4. BAÚ DE MEMÓRIAS — 3 CARTAS

Três envelopes que escondem cartas escritas à mão. Ela toca, o envelope abre, a carta aparece.

- Título: "Nosso Baú de Memórias" em `Caveat`
- Subtítulo pequeno: "toque em cada envelope para abrir 🎀"
- 3 envelopes em coluna, `max-width: 440px`, centralizados

**Estrutura de cada envelope:**
- `.envelope-flap`: barra superior com gradiente (diferente em cada carta — use `#E8A7B6→#D4956A`, `#FFB7CC→#E8A7B6`, `#D4956A→#E8A7B6`). Emoji centralizado. `::after` com triângulo de papel via `border` CSS
- `.envelope-preview`: label "carta 01" em estilo minúsculo, título da carta em `Caveat`, hint "toque para ler ↓"
- `.carta-content`: `max-height: 0`, `overflow: hidden`. Quando `.open`: `max-height: 600px`, com `transition: 0.6s cubic-bezier(0.34, 1.56, 0.64, 1)`
- Texto da carta em `Caveat` 1.15rem, `line-height: 1.7`
- Fundo da carta: `repeating-linear-gradient` simulando papel pautado (linhas `rgba(232,167,182,0.2)` a cada 28px)
- Assinatura à direita em `Caveat`, cor `#D4956A`
- Comentários `/* EDITE: texto da carta N */` em cada carta

**Cartas (títulos sugeridos, conteúdo vem do usuário):**
- Carta 1: "O começo de tudo" — 💌
- Carta 2: "Por que eu te amo" — 🌸
- Carta 3: "Nosso futuro" — ✨

#### 5. GALERIA DE MEMÓRIAS

- Título: "Nossos Momentos" em `Caveat`
- CSS Grid 2 colunas, `gap: 12px`
- 1 foto destaque: `grid-column: 1 / -1`, `aspect-ratio: 16/9`
- 4 fotos menores: `aspect-ratio: 1/1`
- Cada moldura: `border-radius: 14px`, `::before` como borda interna estilo polaroid, gradiente suave de fundo
- Dentro: `<img src="" loading="lazy" class="webp-ready" style="display:none">` + `.foto-placeholder` com emoji e texto descritivo
- Comentários `/* EDITE: src="./foto1.webp" */` em cada slot

#### 6. MINI-PLAYER DE VINIL

Não precisa integrar com Spotify. Usa `<audio>` HTML5 nativo. O visual é o que importa.

- Card: `background: rgba(255,255,255,0.75)`, `backdrop-filter: blur(10px)`, `border-radius: 22px`
- Layout flexbox: disco à esquerda (80x80px) + informações à direita
- **Disco de vinil CSS puro:**
  - `border-radius: 50%`
  - `background` com `repeating-conic-gradient` (roxo escuro e preto alternados) + `radial-gradient` central criando o buraco
  - Pseudo-elemento `::after`: label colorida central em ouro rosé
  - Classe `.spinning`: `animation: spin-vinil 4s linear infinite` via `transform: rotate`
- Botão ▶/⏸: círculo com gradiente `#E8A7B6 → #D4956A`
- `<audio id="audio-player" preload="none">` sem `src` — usuário plugará arquivos depois
- Constante `PLAYLIST` editável no topo: `[{ titulo, artista, src }]`
- Se `src` vazio: apenas anima o vinil como demo visual sem erro

#### 7. BOTÃO DO DENGO — FAB

Um botão flutuante que manda mensagens carinhosas aleatórias para ela.

- `position: fixed`, `bottom: 24px`, `right: 20px`, `z-index: 500`
- Círculo 58px: gradiente `#FFD6E0 → #E8A7B6`, sombra rosa suave
- Ícone: SVG inline da cabeça do Snoopy com coraçãozinho — simples, fofo, reconhecível
- **Toast ao clicar:**
  - `position: fixed`, acima do FAB, `left/right: 20px`
  - `background: rgba(255,255,255,0.92)`, `backdrop-filter: blur(12px)`, `border-radius: 16px`
  - Borda esquerda `3px solid #E8A7B6`
  - Entrada: `transform: translate3d(0, 20px, 0) → (0,0,0)` + `opacity: 0 → 1`
  - Some após 3800ms ou ao tocar
- Constante `MENSAGENS_DENGO` editável no topo, com comentário `/* EDITE: mensagens pessoais */`

#### 8. FOOTER — SNOOPY SONHANDO

- SVG inline do Snoopy deitado: corpo oval branco, cabeça com orelha preta, patinhas, rabinho curvo
- Ele está deitado, tranquilo, sonhando — como encerramento do presente
- Texto em `Caveat`: mensagem final carinhosa
- `padding-bottom: 80px` no `#main` para o FAB não cobrir nada

---

### CONSTANTS EDITÁVEIS — TOPO DO SCRIPT

```js
/* =============================================
   EDITE AQUI — SEUS DADOS PESSOAIS
   Todos os textos plugáveis estão aqui em cima
============================================= */

// Data do início do namoro (ano, mês-1, dia)
// Ex: 14 de fevereiro de 2022 → new Date(2022, 1, 14)
const DATA_INICIO = new Date(2022, 1, 14); // EDITE

// Playlist de músicas (plugue o caminho dos seus arquivos .mp3)
const PLAYLIST = [
  { titulo: 'Nome da música', artista: 'Artista', src: '' }, // EDITE
];

// Mensagens do Botão do Dengo — escreva do seu jeito, pessoal
const MENSAGENS_DENGO = [
  'Vale um abraço apertado de 5 minutos 🤗',
  'Você é a coisa mais linda que já aconteceu comigo 🌸',
  // EDITE: adicione mensagens suas aqui
];
```

---

## PARTE 2 — APK VIVI MUSIC CUSTOMIZADO

Após o site aprovado, entregue um **guia técnico passo a passo** para eu customizar o Vivi Music. O app deve ter a mesma identidade visual do site — quando ela abrir, deve sentir que é parte do mesmo presente.

**Visão:** o Vivi Music vira o "Spotify dela". Rosa e dourado. Ícone do Snoopy com fone. Playlist já aberta com as músicas de vocês. Nome do app: algo como "♡ Para você".

### Bibliotecas e ferramentas para o APK
- Flutter SDK (já incluso no Vivi Music)
- Dependências existentes no `pubspec.yaml` — alterar o mínimo necessário
- GitHub Actions para build em nuvem (sem instalar Flutter localmente)
- Ferramentas de compressão de imagem (`cwebp`, Squoosh) para assets leves

### O guia deve cobrir:

**1. Setup inicial**
- Como clonar o repositório do Vivi Music
- Usar GitHub Actions para evitar setup local (passo a passo completo)
- Quais arquivos tocar, quais ignorar

**2. Tema visual (onde e o que alterar)**
- Localizar `theme.dart` ou equivalente
- Alterar `ThemeData`: `primaryColor`, `backgroundColor`, `scaffoldBackgroundColor`, `colorScheme`
- Valores exatos para plugar (mesma paleta do site):
  - Rosa pastel: `#FFF5F7`
  - Ouro rosé: `#E8A7B6`
  - Ouro quente: `#D4956A`
  - Texto: `#4A3538`

**3. Identidade do app**
- Trocar ícone: onde ficam as pastas `mipmap` no Android
- Tamanhos necessários (hdpi, xhdpi, xxhdpi, xxxhdpi) e como gerar
- Trocar splash screen do Flutter (`flutter_native_splash` ou configuração manual)
- Mudar nome do app no `AndroidManifest.xml` e `strings.xml`

**4. Playlist personalizada**
- Criar aba ou seção "Nossas músicas" com dados estáticos locais
- Estrutura do modelo de dados para as músicas dedicatórias
- Como injetar IDs do YouTube para o Vivi Music tocar (o app já usa YouTube/Piped)
- Exemplo de código com 3 músicas placeholder para eu substituir

**5. Performance — manter leve**
- Como manter o APK abaixo de ~40MB
- O que não adicionar para não inflar o pacote
- Como otimizar assets inseridos

**6. Build e instalação**
- `flutter build apk --release` — passo a passo
- GitHub Actions: arquivo `.yml` completo para eu colar no repositório
- Como assinar o APK para o Google Play Protect não bloquear
- Como instalar no celular dela (habilitar fontes desconhecidas, instalar, limpar rastros)

---

## PARTE 3 — DEPLOY E ENTREGA SURPRESA

**Deploy do site:**
- Como subir no Vercel ou GitHub Pages (gratuito, passo a passo)
- Como gerar URL limpa e bonita
- Como garantir que ela sempre carregue a versão mais recente (cache bust)

**Entrega surpresa do APK:**
- Como habilitar "fontes desconhecidas" no Android dela sem ela notar
- Como instalar o APK silenciosamente
- Como posicionar o ícone na tela inicial
- Como limpar o histórico de arquivos baixados para manter a surpresa intacta

---

## CHECKLIST FINAL

**Site:**
- [ ] Splash com lanternas flutuantes e estrelas funcionando no toque
- [ ] Contador usando `requestAnimationFrame`, nunca `setInterval`
- [ ] Cartas do Baú abrindo com animação fluida ao toque
- [ ] Vinil girando ao tocar, parando ao pausar
- [ ] Botão do Dengo mostrando mensagem aleatória
- [ ] Nenhuma animação em `top`, `left`, `width` ou `height`
- [ ] `prefers-reduced-motion` zerado
- [ ] Tags PWA no `<head>`
- [ ] `charset UTF-8` presente
- [ ] Comentários `/* EDITE */` em todos os pontos personalizáveis
- [ ] Testado mentalmente em viewport 360px

**APK:**
- [ ] Paleta idêntica ao site
- [ ] Ícone Snoopy com fone, rosa
- [ ] Splash customizada
- [ ] Playlist dedicatória funcionando
- [ ] APK abaixo de 40MB
- [ ] Build release assinado e instalável

---

## FILOSOFIA

A tecnologia deve ser **invisível**. Ela abre a porta, mas quem deve ser sentido é o amor de quem fez. Rapunzel passou anos olhando aquelas lanternas pela janela sem saber que eram para ela. Esse presente é a resposta — feito especialmente, com cada detalhe pensado, para a pessoa certa.

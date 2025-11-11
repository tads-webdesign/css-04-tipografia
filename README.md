# Tutorial CSS 3 - Tipografia

## Sumário

1. [Introdução](#introdução)
2. [Propriedades de Tipografia](#propriedades-de-tipografia)
   - [font-family](#font-family)
   - [font-size](#font-size)
   - [font-weight](#font-weight)
   - [line-height](#line-height)
3. [Google Fonts](#google-fonts)
4. [Fontes Customizadas](#fontes-customizadas)
5. [Exemplo Completo](#exemplo-completo)
6. [Links e Conteúdos Avançados](#links-e-conteúdos-avançados)

---

## Introdução

A tipografia é um dos aspectos mais importantes do design web.
Ela afeta diretamente a legibilidade, a acessibilidade e a estética do seu site.
CSS 3 oferece diversas propriedades para controlar a aparência do texto, permitindo criar experiências visuais atraentes e funcionais.

Neste tutorial, você aprenderá as principais propriedades de tipografia em CSS 3 e como usar fontes personalizadas para dar um toque único ao seu projeto.

---

## Propriedades de Tipografia

### font-family

A propriedade `font-family` define a família de fontes que será usada para exibir o texto.
É recomendado especificar múltiplas fontes como "fallback" (alternativas).


**Sintaxe**:
```css
font-family: "Nome da Fonte", fonte-alternativa, família-genérica;
```

[Código exemplo](exemplos/font-family.html)

```html
<p class="serif">Este texto usa uma fonte serifada.</p>
<p class="sans-serif">Este texto usa uma fonte sem serifa.</p>
<p class="monospace">Este texto usa uma fonte monoespaçada.</p>
```

```css
.serif {
  font-family: "Georgia", "Times New Roman", serif;
}

.sans-serif {
  font-family: "Arial", "Helvetica", sans-serif;
}

.monospace {
  font-family: "Courier New", "Courier", monospace;
}
```

**Famílias genéricas principais:**
- `serif`: Fontes com serifas (pequenos traços nas extremidades)
- `sans-serif`: Fontes sem serifas
- `monospace`: Fontes com largura fixa
- `cursive`: Fontes cursivas
- `fantasy`: Fontes decorativas

---

### font-size

A propriedade `font-size` define o tamanho da fonte.
Pode ser especificada em várias unidades.

**Unidades comuns**:
- `px` (pixels): Tamanho fixo
- `em`: Relativo ao tamanho da fonte do elemento pai
- `rem`: Relativo ao tamanho da fonte raiz (html)
- `%`: Porcentagem relativa ao elemento pai

[Código exemplo](exemplos/font-size.html)

```html
<p class="pequeno">Texto pequeno</p>
<p class="medio">Texto médio</p>
<p class="grande">Texto grande</p>
<p class="relativo">Texto com tamanho relativo</p>
```

```css
.pequeno {
  font-size: 12px;
}

.medio {
  font-size: 16px;
}

.grande {
  font-size: 24px;
}

.relativo {
  font-size: 1.5em; /* 1.5 vezes o tamanho da fonte do pai */
}
```

**Dica:** Use `rem` para tamanhos mais consistentes e acessíveis em todo o site.

---

### font-weight

A propriedade `font-weight` controla o peso (espessura) da fonte.

**Valores comuns**:
- `normal`: Peso normal (equivalente a 400)
- `bold`: Negrito (equivalente a 700)
- Valores numéricos: 100, 200, 300, 400, 500, 600, 700, 800, 900

[Código exemplo](exemplos/font-weight.html)

```html
<p class="leve">Texto leve (300)</p>
<p class="normal">Texto normal (400)</p>
<p class="semi-negrito">Texto semi-negrito (600)</p>
<p class="negrito">Texto negrito (700)</p>
```

```css
.leve {
  font-weight: 300;
}

.normal {
  font-weight: 400; /* ou font-weight: normal; */
}

.semi-negrito {
  font-weight: 600;
}

.negrito {
  font-weight: 700; /* ou font-weight: bold; */
}
```

**Nota:** Nem todas as fontes possuem todos os pesos disponíveis.

---

### line-height

A propriedade `line-height` define a altura da linha, ou seja, o espaço vertical entre linhas de texto.

**Sintaxe**:
```css
line-height: valor;
```

**Valores comuns**:
- Número sem unidade: Multiplicador do tamanho da fonte (recomendado)
- `px`, `em`, `rem`: Valores absolutos ou relativos
- `%`: Porcentagem do tamanho da fonte

[Código exemplo]()

```html
<p class="linha-compacta">
  Este parágrafo tem linhas compactas. Este parágrafo tem linhas compactas.
  Este parágrafo tem linhas compactas. Este parágrafo tem linhas compactas.
</p>

<p class="linha-confortavel">
  Este parágrafo tem espaçamento confortável entre linhas. Este parágrafo tem
  espaçamento confortável entre linhas. Este parágrafo tem espaçamento
  confortável entre linhas.
</p>

<p class="linha-ampla">
  Este parágrafo tem linhas bem espaçadas. Este parágrafo tem linhas bem
  espaçadas. Este parágrafo tem linhas bem espaçadas.
</p>
```

```css
.linha-compacta {
  line-height: 1.2;
}

.linha-confortavel {
  line-height: 1.6; /* Recomendado para leitura */
}

.linha-ampla {
  line-height: 2;
}
```

**Dica:** Um `line-height` entre 1.5 e 1.6 é ideal para legibilidade em textos longos.

---

## Google Fonts

Google Fonts é uma biblioteca gratuita de fontes web que você pode usar facilmente em seus projetos.

### Como usar Google Fonts:

Passos usual, usando HTML e CSS, ([Código exemplo](exemplos/google-fonts.html)):
1. Escolha a fonte
2. Importe a fonte no HTML
3. Use a fonte no CSS

Mas é possível também importar somente no CSS ([Código exemplo](exemplos/google-fonts-css.html))
1. Escolha a fonte
2. Importar no CSS

#### Exemplo 1 - usando HTML e CSS
**Passo 1**:
Acesse [Google Fonts](https://fonts.google.com/) e escolha a fonte desejada.

**Passo 2**: Importe a fonte no HTML
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Google Fonts</title>
  
  <!-- Importando Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
<body>
  <h1>Título com Google Font</h1>
  <p>Parágrafo com Google Font</p>
</body>
</html>
```

**Passo 3**: Use a fonte no CSS
```css
body {
  font-family: 'Roboto', sans-serif;
}

h1 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
}

p {
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
}
```

#### Exemplo 2 - importando no CSS

Acesse [Google Fonts](https://fonts.google.com/) e escolha a fonte desejada.

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}
```

**Dica:** Use `preconnect` para melhorar o desempenho do carregamento das fontes.

---

## Fontes Customizadas

Você pode usar fontes customizadas (arquivos de fonte do seu próprio servidor) usando a regra `@font-face`.

### Formatos de fonte suportados:
- **WOFF2** (Web Open Font Format 2): Recomendado - melhor compressão
- **WOFF**: Suporte mais amplo
- **TTF/OTF**: True Type Font / Open Type Font
- **EOT**: Para Internet Explorer antigo

### Exemplo

[Código exemplo](exemplos/fonte-customizada.html)

**HTML**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fonte Customizada</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1 class="custom-font">Título com Fonte Customizada</h1>
  <p class="custom-font">Parágrafo com fonte customizada.</p>
</body>
</html>
```

**CSS**
```css
/* Definindo a fonte customizada */
@font-face {
  font-family: 'MinhaFonteCustomizada';
  src: url('fonts/minhafonte.woff2') format('woff2'),
       url('fonts/minhafonte.woff') format('woff'),
       url('fonts/minhafonte.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
  font-display: swap; /* Melhora a performance */
}

/* Usando a fonte customizada */
.custom-font {
  font-family: 'MinhaFonteCustomizada', Arial, sans-serif;
}
```

### Múltiplos pesos e estilos:
```css
/* Regular */
@font-face {
  font-family: 'MinhaFonte';
  src: url('fonts/minhafonte-regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
}

/* Negrito */
@font-face {
  font-family: 'MinhaFonte';
  src: url('fonts/minhafonte-bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
}

/* Itálico */
@font-face {
  font-family: 'MinhaFonte';
  src: url('fonts/minhafonte-italic.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
}
```

**Dica:** A propriedade `font-display: swap` evita o "flash of invisible text" (FOIT) durante o carregamento.

---

## Exemplo Completo

Aqui está um exemplo completo que combina todos os conceitos aprendidos:

### index.html
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tipografia Completa - CSS 3</title>
  
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Merriweather:wght@400;700&display=swap" rel="stylesheet">
  
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1 class="titulo-principal">Tipografia em CSS 3</h1>
    <p class="subtitulo">Um guia completo sobre propriedades tipográficas</p>
  </header>

  <main>
    <section class="introducao">
      <h2>Introdução à Tipografia Web</h2>
      <p class="texto-destaque">
        A tipografia é a arte de arranjar tipos para tornar a linguagem escrita
        legível, acessível e atraente quando exibida.
      </p>
      <p class="texto-corpo">
        No desenvolvimento web, o CSS oferece um controle preciso sobre como o
        texto é apresentado. Desde o tamanho da fonte até o espaçamento entre
        linhas, cada propriedade desempenha um papel crucial na experiência do
        usuário.
      </p>
    </section>

    <section class="exemplos">
      <h2>Variações de Peso de Fonte</h2>
      <p class="peso-leve">Texto leve (300) - Ideal para textos grandes</p>
      <p class="peso-normal">Texto normal (400) - Peso padrão</p>
      <p class="peso-semi-negrito">Texto semi-negrito (600) - Para destaques</p>
      <p class="peso-negrito">Texto negrito (700) - Para ênfase forte</p>
    </section>

    <section class="tamanhos">
      <h2>Hierarquia de Tamanhos</h2>
      <h1 class="heading-1">Título Principal (H1)</h1>
      <h2 class="heading-2">Título Secundário (H2)</h2>
      <h3 class="heading-3">Título Terciário (H3)</h3>
      <p class="paragrafo">Texto de parágrafo regular</p>
      <p class="texto-pequeno">Texto pequeno para notas de rodapé</p>
    </section>

    <section class="espacamento">
      <h2>Importância do Line-Height</h2>
      <div class="coluna">
        <h3>Line-height compacto (1.2)</h3>
        <p class="espacamento-compacto">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
          ad minim veniam, quis nostrud exercitation ullamco laboris.
        </p>
      </div>
      <div class="coluna">
        <h3>Line-height ideal (1.6)</h3>
        <p class="espacamento-ideal">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
          ad minim veniam, quis nostrud exercitation ullamco laboris.
        </p>
      </div>
    </section>

    <section class="combinacao">
      <h2>Combinação de Fontes</h2>
      <p class="serif-texto">
        Este parágrafo usa uma fonte serifada (Merriweather), ideal para textos
        longos e leitura confortável. As serifas ajudam a guiar o olho ao longo
        das linhas.
      </p>
      <p class="sans-serif-texto">
        Este parágrafo usa uma fonte sans-serif (Poppins), moderna e limpa.
        Perfeita para interfaces digitais e textos curtos.
      </p>
    </section>
  </main>

  <footer>
    <p>&copy; 2024 Tutorial CSS 3 - Tipografia</p>
  </footer>
</body>
</html>
```

### styles.css
```css
/* Reset básico */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Definindo fontes customizadas (exemplo) */
@font-face {
  font-family: 'MinhaFonteCustom';
  src: url('fonts/custom-font.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

/* Estilos globais */
body {
  font-family: 'Poppins', Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
  background-color: #f5f5f5;
  padding: 20px;
}

/* Header */
header {
  text-align: center;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 60px 20px;
  border-radius: 10px;
  margin-bottom: 40px;
}

.titulo-principal {
  font-family: 'Poppins', sans-serif;
  font-size: 3rem;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 10px;
}

.subtitulo {
  font-size: 1.25rem;
  font-weight: 300;
  line-height: 1.4;
}

/* Main content */
main {
  max-width: 900px;
  margin: 0 auto;
  background: white;
  padding: 40px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

/* Seções */
section {
  margin-bottom: 50px;
}

h2 {
  font-family: 'Poppins', sans-serif;
  font-size: 2rem;
  font-weight: 600;
  color: #667eea;
  margin-bottom: 20px;
  line-height: 1.3;
}

h3 {
  font-family: 'Poppins', sans-serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: #555;
  margin-bottom: 15px;
  line-height: 1.3;
}

/* Introdução */
.texto-destaque {
  font-size: 1.25rem;
  font-weight: 600;
  color: #764ba2;
  line-height: 1.6;
  margin-bottom: 20px;
}

.texto-corpo {
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.8;
  color: #555;
}

/* Exemplos de peso de fonte */
.peso-leve {
  font-weight: 300;
  font-size: 1.2rem;
  margin-bottom: 15px;
}

.peso-normal {
  font-weight: 400;
  font-size: 1.2rem;
  margin-bottom: 15px;
}

.peso-semi-negrito {
  font-weight: 600;
  font-size: 1.2rem;
  margin-bottom: 15px;
}

.peso-negrito {
  font-weight: 700;
  font-size: 1.2rem;
  margin-bottom: 15px;
}

/* Hierarquia de tamanhos */
.heading-1 {
  font-size: 2.5rem;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 10px;
}

.heading-2 {
  font-size: 2rem;
  font-weight: 600;
  line-height: 1.3;
  margin-bottom: 10px;
}

.heading-3 {
  font-size: 1.5rem;
  font-weight: 600;
  line-height: 1.3;
  margin-bottom: 10px;
}

.paragrafo {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 10px;
}

.texto-pequeno {
  font-size: 0.875rem;
  color: #777;
  line-height: 1.5;
}

/* Espaçamento */
.espacamento {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
}

.coluna h3 {
  font-size: 1.1rem;
  margin-bottom: 10px;
}

.espacamento-compacto {
  line-height: 1.2;
  background-color: #ffe6e6;
  padding: 15px;
  border-radius: 5px;
}

.espacamento-ideal {
  line-height: 1.6;
  background-color: #e6f7e6;
  padding: 15px;
  border-radius: 5px;
}

/* Combinação de fontes */
.serif-texto {
  font-family: 'Merriweather', Georgia, serif;
  font-size: 1.1rem;
  font-weight: 400;
  line-height: 1.8;
  margin-bottom: 20px;
  padding: 20px;
  background-color: #f9f9f9;
  border-left: 4px solid #667eea;
}

.sans-serif-texto {
  font-family: 'Poppins', Arial, sans-serif;
  font-size: 1.1rem;
  font-weight: 400;
  line-height: 1.6;
  padding: 20px;
  background-color: #f0f0ff;
  border-left: 4px solid #764ba2;
}

/* Footer */
footer {
  text-align: center;
  margin-top: 40px;
  padding: 20px;
  color: #777;
  font-size: 0.9rem;
}

/* Responsividade */
@media (max-width: 768px) {
  .titulo-principal {
    font-size: 2rem;
  }
  
  .subtitulo {
    font-size: 1rem;
  }
  
  main {
    padding: 20px;
  }
  
  .espacamento {
    grid-template-columns: 1fr;
  }
}
```

---

## Links e Conteúdos Avançados

### Documentação Oficial
- [MDN Web Docs - CSS Fonts](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Fonts) - Documentação completa sobre fontes em CSS
- [W3C CSS Fonts Module](https://www.w3.org/TR/css-fonts-3/) - Especificação oficial do CSS Fonts
- [Can I Use - Font Feature](https://caniuse.com/?search=font) - Compatibilidade de propriedades de fonte em navegadores

### Recursos de Fontes
- [Google Fonts](https://fonts.google.com/) - Biblioteca gratuita de fontes web
- [Adobe Fonts](https://fonts.adobe.com/) - Biblioteca de fontes da Adobe (requer assinatura)
- [Font Squirrel](https://www.fontsquirrel.com/) - Fontes gratuitas para uso comercial
- [DaFont](https://www.dafont.com/pt/) - Coleção de fontes gratuitas
- [FontSpace](https://www.fontspace.com/) - Fontes gratuitas para uso pessoal e comercial

### Ferramentas
- [Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator) - Conversor de fontes para formato web
- [Type Scale](https://type-scale.com/) - Ferramenta para criar escalas tipográficas
- [Font Pair](https://www.fontpair.co/) - Sugestões de combinações de fontes
- [Google Font Combinations](https://fontpair.co/google-font-combinations) - Combinações populares do Google Fonts
- [WhatFont](https://chrome.google.com/webstore/detail/whatfont/jabopobgcpjmedljpbcaablpmlmfcogm) - Extensão Chrome para identificar fontes

### Guias e Tutoriais Avançados
- [Responsive Typography](https://web.dev/responsive-web-design-basics/#typography) - Tipografia responsiva
- [Variable Fonts Guide](https://web.dev/variable-fonts/) - Guia sobre fontes variáveis
- [Font Loading Strategies](https://www.zachleat.com/web/comprehensive-webfonts/) - Estratégias de carregamento de fontes
- [Typography Handbook](https://typographyhandbook.com/) - Manual completo de tipografia
- [Practical Typography](https://practicaltypography.com/) - Guia prático de tipografia

### Conceitos Avançados
- **Variable Fonts**: Fontes com eixos variáveis que permitem ajustes contínuos de peso, largura e outros atributos
- **Font Feature Settings**: Controle de recursos tipográficos como ligaduras, numerais e alternativas estilísticas
- **Text Rendering**: Otimização da renderização de texto (`text-rendering`, `font-smooth`)
- **Font Subsetting**: Técnica para reduzir o tamanho dos arquivos de fonte incluindo apenas os caracteres necessários
- **FOUT, FOIT, FOFT**: Estratégias para lidar com o carregamento de fontes web
- **OpenType Features**: Recursos tipográficos avançados disponíveis em fontes OpenType

### Performance
- [Web Font Optimization](https://web.dev/font-best-practices/) - Melhores práticas para otimização de fontes
- [Preload Web Fonts](https://web.dev/codelab-preload-web-fonts/) - Como pré-carregar fontes web
- [Font Display](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display) - Controle de exibição de fontes

### Acessibilidade
- [Typography for Accessibility](https://www.w3.org/WAI/WCAG21/Understanding/visual-presentation.html) - Diretrizes de acessibilidade para tipografia
- [Readable Font Sizes](https://www.w3.org/WAI/WCAG21/Understanding/resize-text.html) - Tamanhos de fonte acessíveis

### Artigos e Blogs
- [CSS-Tricks - Typography](https://css-tricks.com/snippets/css/complete-guide-to-typography/) - Guia completo de tipografia
- [Smashing Magazine - Typography](https://www.smashingmagazine.com/category/typography) - Artigos sobre tipografia web
- [A List Apart - Typography](https://alistapart.com/blog/topic/typography/) - Artigos aprofundados sobre tipografia

### Livros Recomendados
- "The Elements of Typographic Style" - Robert Bringhurst
- "Thinking with Type" - Ellen Lupton
- "Web Typography" - Richard Rutter
- "On Web Typography" - Jason Santa Maria

---

**Parabéns!** Você completou o tutorial de tipografia em CSS 3. Continue praticando e explorando os recursos avançados para criar designs tipográficos incríveis! 🎉

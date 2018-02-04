# Checklist para front-end

Essa é uma lista exaustiva de todos elementos que você precisa ter / testar antes de lançar seu site / página HTML em produção. Baseado no https://frontendchecklist.io.

## Índice

1.  **[Head](#head)**
1.  **[HTML](#html)**
1.  **[Webfonts](#webfonts)**
1.  **[CSS](#css)**
1.  **[Imagens](#imagens)**
1.  **[JavaScript](#javascript)**
1.  **[Segurança](#seguran%C3%A7a)**
1.  **[Performance](#performance)**
1.  **[Acessibilidade](#acessibilidade)**
1.  **[SEO](#seo)**

## Como usar?

Todos itens na **Front-End Checklist** são necessários na maioria dos projetos, mas alguns elementos podem ser omitidos ou não são tão essenciais (no caso da administração de um aplicativo web, você pode não precisar de um feed RSS por exemplo). Nós escolhemos três níveis de flexibilidade:

* ![Baixa][low_img] significa que o item é **recomendado** mas pode ser omitido em algumas situações em particular.
* ![Média][medium_img] significa que o item é **altamente recomendado** e pode eventualmente ser omitido em alguns casos realmente particulares. Alguns elementos, se omitidos, podem ter más repercussões em termos de performance ou SEO.
* ![Alta][high_img] significa que o item **não pode ser omitido** por qualquer razão. Você pode causar uma disfunção na sua página ou ter problemas com acessibilidade ou SEO. A prioridade dos testes precisa estar nestes elementos primeiro.

Alguns recursos possuem um emoticon para ajudar você a entender qual tipo de conteúdo / ajuda você pode encontrar na checklist:

* 📖: documentação ou artigo
* 🛠: ferramenta online / ferramenta de teste
* 📹: mídia ou conteúdo em vídeo

> You can contribute to the ***Front-End Checklist App*** reading the [README_APP file](https://github.com/thedaviddias/Front-End-Checklist/blob/master/README_APP.md) which explain everything about the project.

---

## Head

> **Notas:** Você pode acessar [uma lista com tudo](https://github.com/joshbuchea/HEAD) que poderia ser encontrado na `<head>` de um document HTML.

### Meta tag

* [ ] **Doctype:** ![Alta][high_img] O Doctype é HTML5 e está no topo de todas as suas páginas HTML.

```html
<!doctype html> <!-- HTML5 -->
```

> * 📖 [Determinando o encoding de caracteres - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

*As próximas 3 meta tags (Charset, X-UA Compatible e Viewport) precisam vir primeiro no head.*

* [ ] **Charset:** ![Alta][high_img] O charset declarado (UTF-8) é corretamente declarado.

```html
<!-- Determine o encoding de caracteres para o document -->
<meta charset="utf-8">
```

* [ ] **X-UA-Compatible:** ![Média][medium_img] A meta tag X-UA-Compatible está presente.

```html
<!-- Instrua o Internet Explorer a usar seu mais recente engine de renderização -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

> * 📖 [Especificando modos legados de document (Internet Explorer)](https://msdn.microsoft.com/en-us/library/jj676915(v=vs.85).aspx)

* [ ] **Viewport:** ![Alta][high_img] A viewport é corretamente declarada.

```html
<!-- Viewport para web design responsivo -->
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

* [ ] **Title:** ![Alta][high_img] Um título é usado em todas páginas (SEO: Google calcula a largura em píxel dos caracteres usados no título, cortados entre 472 e 482 píxels. O limite médio de caracteres seria em torno de 55-caracteres).

```html
<!-- Título do Document -->
<title>Título de Página menor que 55 caracteres</title>
```

> * 📖 [Título - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
> * 🛠 [Gerador de Snippets SERP](https://www.sistrix.com/serp-snippet-generator/)

* [ ] **Descrição:** ![Alta][high_img] Uma meta decrição é providenciada, é única e não possui mais de 150 caracteres.

```html
<!-- Meta Descrição -->
<meta name="description" content="Descrição da página com menos de 150 caracteres">
```

> * 📖[Meta Descrição - HTML - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Adding_an_author_and_description)

* [ ] **Favicons:** ![Média][medium_img] Cada favicon foi criado e é exibido corretamente. Se você tem apenas um `favicon.ico`, ponha-o na raiz do seu site. Normalmente você não precisa usar nenhum markup. Entretanto, ainda é uma boa prática linkar ele usando o exemplo abaixo. Atualmente, **o formato PNG é recomendado** ao invés do formato `.ico` (dimensões: 32x32px).

```html
<!-- Favicon padrão -->
<link rel="icon" type="image/x-icon" href="https://exemplo.com/favicon.ico">
<!-- Formato favicon recomendado -->
<link rel="icon" type="image/png" href="https://exemplo.com/favicon.png">
```

> * 🛠 [Gerador de Favicon](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> * 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Qual Você Precisa? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Web App Meta:** ![Baixa][low_img] Meta-tags da Apple estão presentes.

```html
<!-- Apple Touch Icon (at least 200x200px) -->
<link rel="apple-touch-icon" href="/custom-icon.png">

<!-- To run web application in full-screen -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Status Bar Style (see Supported Meta Tags below for available values) -->
<!-- Has no effect unless you have the previous meta tag -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```

> * 📖 [Configurando Aplicações Web](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
> * 📖 [Meta Tags Suportadas](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

- [ ] **Windows Tiles:**![Baixa][low_img] Windows tiles estão presentes e linkadas.

```html
<!-- Microsoft Tiles -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

O markup xml mínimo necessário para o arquivo browserconfig.xml é como segue:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="pequeno.png"/>
        <square150x150logo src="medio.png"/>
        <wide310x150logo src="largo.png"/>
        <square310x310logo src="grande.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

> * 📖 [Referência de configuração de schema do browser](https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx)

* [ ] **Canonical:** ![Média][medium_img] Use `rel="canonical"` para evitar conteúdo duplicado.

```html
<!-- Ajuda a evitar problemas com conteúdo duplicado -->
<link rel="canonical" href="http://exemplo.com/2017/09/um-novo-artigo-para-ler.html">
```

> * 📖 [Use URLs canônicas - Search Console Help - Google Support](https://support.google.com/webmasters/answer/139066?hl=en)
> * 📖 [5 erros comuns com `rel=canonical` - Google Webmaster Blog](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### Tags HTML

* [ ] **Atributo de linguagem:** ![Alta][high_img] A tag de idioma do seu website é especificada e relacionada ao idioma atual da página.

```html
<!-- Indicamos o idioma definido para a página atual -->
<html lang="pt-br">
```

* [ ] **Atributo de direção:** ![Média][medium_img] A direção de leitura é especificada na tag `<html>` (Pode ser usada em outra tag HTML).

```html
<!-- Indicamos a direção de leitura (rtl é sigla para right to left, isto é, da direita para a esquerda) -->
<html dir="rtl">
```

> * 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

* [ ] **Idioma alternativo:** ![Baixa][low_img] A tag de idioma alternativo do seu website é especificada e relacionada ao idioma atual da página.

```html
<!-- Indicamos o idioma alternativo definido para a página atual -->
<link rel="alternate" href="https://es.exemplo.com/" hreflang="es">
```

* [ ] **Comentários condicionais:** ![Baixa][low_img] Comentários condicionais são presentes para o IE se necessário.

> * 📖 [Sobre comentários condicionais (Internet Explorer) - MSDN - Microsoft](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **RSS feed:** ![Baixa][low_img] Se seu projeto é um blog ou possui artigos, foi providenciado o link do RSS.

* [ ] **CSS Crítico:** ![Média][medium_img] O CSS crítico (ou "above the fold") coleta todo o CSS usado para renderizar a porção visível da página. Ele é embutido antes da chamada CSS principal e entre `<style></style>` numa linha única (minificado).

> * 🛠 [Critical por Addy Osmani no Github](https://github.com/addyosmani/critical) automatiza isso.

* [ ] **Ordem CSS:** ![Alta][high_img] Todos os arquivos CSS são carregados antes de quaisquer arquivos JavaScript no `<head>` (Exceto no caso onde, algumas vezes, arquivos JS são carregados assíncronamente no topo da página).

### Social meta

***Facebook OG*** e ***Twitter Cards*** são, para qualquer website, altamente recomendados. As outras tags de mídia social podem ser consideradas se seu público-alvo tem uma presença em particular nelas, e você quer se assegurar de exibí-las.

* [ ] **Facebook Open Graph:** ![Baixa][low_img] Todos os Facebook Open Graph (OG) estão testados e nenhum está faltando ou com informações falsas. Imagens precisam ter no mínimo 600 x 315 píxels, porém é recomendado 1200 x 630 píxels.

> **Notas:** Usar `og:image:width` e `og:image:height` vai especificar as dimensões da imagens para o _crawler_ para que ele renderize a imagem imediatamente sem ter que baixá-la e processá-la assíncronamente.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://exemplo.com/pagina.html">
<meta property="og:title" content="Título do Conteúdo">
<meta property="og:image" content="https://exemplo.com/imagem.jpg">
<meta property="og:description" content="Descrição Aqui">
<meta property="og:site_name" content="Nome do Site">
<meta property="og:locale" content="pt_BR">
<!-- As próximas tags são opcionais mas recomendadas -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

> * 📖 [Um Guia de Compartilhamento para Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> * 📖 [Melhores Práticas - Compartilhamento](https://developers.facebook.com/docs/sharing/best-practices/)
> * 🛠 Teste sua página com o [Facebook OG testing](https://developers.facebook.com/tools/debug/)

* [ ] **Twitter Card:** ![Baixa][low_img]

```html
<meta name="twitter:card" content="sumário">
<meta name="twitter:site" content="@conta_do_site">
<meta name="twitter:creator" content="@conta_individual">
<meta name="twitter:url" content="https://exemplo.com/pagina.html">
<meta name="twitter:title" content="Título do Conteúdo">
<meta name="twitter:description" content="Descrição de conteúdo com menos de caracteres">
<meta name="twitter:image" content="https://exemplo.com/imagem.jpg">
```

> * 📖 [Iniciando com cards — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> * 🛠 Teste sua página com o [Validador de Twitter cards](https://cards-dev.twitter.com/validator)

**[⬆ voltar ao topo](#Índice)**

---

## HTML

### Melhores práticas

* [ ] **Elementos Semânticos do HTML5:** ![Alta][high_img] Elementos Semânticos do HTML5 são usados apropriadamente (header, section, footer, main...).

> * 📖 [HTML Reference](http://htmlreference.io/)

* [ ] **Páginas de erro:** ![Alta][high_img] Páginas para Erro 404 e 5xx existem. Lembre-se de que páginas de erro 5xx precisam ter seu CSS integrado (sem chamadas externas no servidor atual).

* [ ] **Noopener:** ![Média][medium_img] Caso você esteja usando links externos com `target="_blank"`, seu link deveria ter um atributo `rel="noopener"` para prevenir _tab nabbing_. Se você precisa suportar versões mais antigas do Firefox, use `rel="noopener noreferrer"`.

> * 📖 [Sobre rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Retirando comentários:** ![Baixa][low_img] Código desnecessário precisa ser removido antes de enviar a página para produção.

### Testando HTML

* [ ] **W3C compliant:** ![Alta][high_img] Todas as páginas precisam ser testadas com o validador W3C para identificar possíveis problemas no código HTML.

> * 🛠 [W3C validator](https://validator.w3.org/)

* [ ] **HTML Lint:** ![Alta][high_img] Eu uso ferramentas para me ajudar a analisar quaisquer problemas que eu poderia ter com meu código HTML.

> * 🛠 [Dirty markup](https://dirtymarkup.com/)

> * 🛠 [Sonar, uma ferramenta de linting para a web](https://sonarwhal.com/)

* [ ] **Verificador de Link:** ![Alta][high_img] Não há links quebrados na minha página, verifique que você não tem nenhum erro 404.

> * 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

* [ ] **Teste Bloqueadores de Publicidade:** ![Média][medium_img] Seu website mostra o conteúdo corretamente com adblockers habilitados (Você pode providenciar uma mensagem encorajando os usuários a desabilitar o adblocker).

**[⬆ voltar ao topo](#Índice)**

---

## Webfonts

> **Notas:** Usar webfonts pode causar um _flash_ de texto invisível ou sem estilização - cogite ter fontes reserva e/ou utilizar webfont loaders para controlar esse comportamento.
> * 📖 [Considerações técnicas da Google sobre webfonts](https://developers.google.com/fonts/docs/technical_considerations)

* [ ] **Formato de webfont:** ![Alta][high_img] WOFF, WOFF2 e TTF são suportados por todos os navegadores modernos.

> * 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - Suporte a fonte TrueType e OpenType](https://caniuse.com/#feat=ttf)
> * 📖 [Usando @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Tamanho de webfont:** ![Alta][high_img] Tamanhos de webfont não excedem 2 MB (todas variantes inclusas).

* [ ] **Webfont loader:** ![Low][low_img] Controle o comportamento de carregamento com um webfont loader

> * 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ voltar ao topo](#Índice)**

---

## CSS

> **Notas:** Dê uma olhada em [Guidelines CSS](https://cssguidelin.es/) e [Guidelines Sass](https://sass-guidelin.es/) seguidas pela maioria dos desenvolvedores Front-End. Se você tem alguma dúvida sobre propriedades CSS, você pode visitar a [CSS Reference](http://cssreference.io/). Existe também um pequeno [Guia de Código](http://codeguide.co/) para consistência.

* [ ] **Web Design Responsivo:** ![Alta][high_img] O website está usando web design responsivo.
* [ ] **CSS Print:** ![Média][medium_img] Uma stylesheet de impressão correta é providenciada em cada página.
* [ ] **Pré-processadores:** ![Média][medium_img] Sua página está usando um pré-processador CSS (e.g. [Sass](http://sass-lang.com/)).
* [ ] **ID Único:** ![Alta][high_img] Se IDs são usados, eles são únicos à página.
* [ ] **Reset CSS:** ![Alta][high_img] Um CSS reset (reset, normalize ou reboot) está em uso e atualizado. *(Se você está usando um Framework CSS como Bootstrap ou Foundation, o Normalize já está incluído.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS prefix:** ![Baixa][low_img] Todas as classes (ou id- usados em arquivos) começam com **js-** e não estão estilizadas nos arquivos CSS.

```html
<div id="js-slider" class="meu-slider">
<!-- ou -->
<div id="id-usado-pelo-cms" class="js-slider meu-slider">
```

* [ ] **CSS embutido ou inline:** ![Alta][high_img] Evite a todo custo o uso de CSS embutido em tags `<style>` ou inline: apenas utilizado por razões válidas (ex: background-image para slider, CSS critical).
* [ ] **Vendor prefixes:** ![Alta][high_img] Prefixos CSS de _vendor_ são usados e gerados de acordo com sua compatibilidade e suporte a navegadores.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Performance

- [ ] **Concatenação:** ![Alta][high_img] Arquivos CSS são concatenados num arquivo único. *(Não para HTTP/2)*.
- [ ] **Minificação:** ![Alta][high_img] Todos arquivos CSS são minificados.
- [ ] **Non-blocking:** ![Média][medium_img] Arquivos CSS precisam ser non-blocking para prevenir o DOM de tirar tempo para carregar.

> * 📖 [loadCSS por grupo de filamento](https://github.com/filamentgroup/loadCSS)
> * 📖 [Exemplo de pré-carregamento de CSS usando loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **CSS Inutilizado:** ![Baixa][low_img] Remover CSS inutilizado.

> * 🛠 [UnCSS Online](https://uncss-online.com/)
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [Cobertura do DevTools do Chrome](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### Validação CSS

* [ ] **Stylelint:** ![Alta][high_img] Todos arquivos CSS ou SCSS estão sem nenhum erros.

> * 🛠 [stylelint, um linter CSS](https://stylelint.io/)
> * 📖 [Diretrizes Sass](https://sass-guidelin.es/)

* [ ] **Web design responsivo:** ![Alta][high_img] Todas as páginas foram testatas nos seguintes breakpoints: 320px, 768px, 1024px (podem ser mais / diferentes de acordo com seu analytics).

* [ ] **Validador CSS:** ![Média][medium_img] O CSS foi testado e erros pertinentes foram corrigidos.

> * 🛠 [Validador CSS](https://jigsaw.w3.org/css-validator/)

* [ ] **Navegadores Desktop:** ![High][high_img] Todas as páginas foram testadas em todos os navegadores desktop atuais (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Navegadores Mobile:**  ![High][high_img] Todas as páginas foram testadas em todos os navegadores mobile atuais (Browser nativo, Chrome, Safari...).
* [ ] **SO:**  ![High][high_img] Todas as páginas foram testadas em todos os Sistemas Operacionais atuais (Windows, Android, iOS, Mac...).

- [ ] **Fidelidade de design:** ![High][high_img] Dependendo do projeto e da qualidade dos profissionais da área criativa, pode ser requisitado que você se mantenha próximo ao que foi desenhado. Você pode usar algumas ferramentas para comparar as criações com sua implementação de código e assegurar consistência.

> [Pixel Perfect - Extensão Chrome](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Direção de leitura:** ![High][high_img] Todas as páginas precisam ser testadas para idiomas LTR e RTL se elas precisarem dar esse suporte.

> * 📖 [Construindo Websites e Web Apps Adaptados a RTL: Parte 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Construindo Websites e Web Apps Adaptados a RTL: Parte 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ voltar ao topo](#Índice)**

---

## Imagens

> **Notas:** Para um entendimento completo de otimização de imagem, veja o ebook grátis **[Essential Image Optimization](https://images.guide/)**, do Addy Osmani.

### Melhores práticas

* [ ] **Otimização:** ![Alta][high_img] Todas as imagens são otimizadas para renderização no navegador. Formato WebP poderia ser usado para páginas críticas (como a Homepage).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 Use [ImageOptim](https://imageoptim.com/) para otimizar suas imagens gratuitamente.
> * 🛠 Use [Kraken.io](https://kraken.io/web-interface) como uma alternativa incrível para otimização tanto png quanto jpg. Até 1MB por arquivo no plano gratuito.
> * 🛠 [TinyPNG](https://tinypng.com/) otimize sem perdas imagens png, apng (png animado) e jpg. Versões gratuita e paga estão disponíveis.
> * 🛠 [ZorroSVG](http://quasimondo.com/ZorroSVG/) compressão similar à do jpg para imagens transparentes usando mascaramento de svg.
> * 🛠 [SVGO](https://github.com/svg/svgo) uma ferramenta baseada em Nodejs para otimização de arquivos de gráficos vetoriais SVG.
> * 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) uma versão GUI web do SVGO para otimização dos seus svgs online.


* [ ] **Picture/Srcset:** ![Medium][medium_img] Você usa picture/srcset para providenciar a imagem mais apropriada para o viewport atual do usuário.

> * 📖 [Como Construir Imagens Responsivas com srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Baixa][low_img] Você providencia imagens em layout x2 ou 3x, e suporta retina display.
* [ ] **Sprite:** ![Média][medium_img] Imagens pequenas estão num arquivo sprite (no caso de ícones, eles podem estar num sprite SVG).
* [ ] **Altura e Largura:** ![Alta][high_img] Determine os atributos `width` e `height` em `<img>` se a imagem final renderizada é conhecida (pode ser omitido para CSS sizing).
* [ ] **Texto alternativo:** ![High][high_img] Todas as tags `<img>` têm um texto alternativo que descreve a imagem visualmente.
* [ ] **Lazy loading:** ![Média][medium_img] Imagens são carregadas de modo _lazy_, ou seja, por demanda (Um fallback para noscript é sempre providenciado).

**[⬆ voltar ao topo](#Índice)**

---

## JavaScript

### Melhores práticas

* [ ] **JavaScript Inline:** ![Alta][high_img] Você não tem nenhum código JavaSScript inline (misturado com seu código HTML, por exemplo).
* [ ] **Concatenação:** ![Alta][high_img] Arquivos JavaScript são concatenados.
* [ ] **Minificação:** ![Alta][high_img] Arquivos JavaScript são minificados (você pode adicionar o sufixo `.min`).

> * 📖 [Minificar Recursos (HTML, CSS, e JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **Segurança JavaScript:** ![High][high_img]

> * 📖 [Diretrizes do Desenvolvimento de Aplicações Seguras Utilizando JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **Tag `noscript`:** ![Medium][medium_img] Use a tag `<noscript>` no body do HTML se um tipo de script na página não for suportado ou se scripting em geral está atualmente desabilitado no navegador. Isto ajudará em renderização _client-side_ de aplicações pesadas como React.js, veja [exemplos](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498).

```html
<noscript>
  Você precisa habilitar JavaScript para rodar esta aplicação.
</noscript>
```

* [ ] **Non-blocking:** ![Média][medium_img] Arquivos JavaScript são carregados assíncronamente usando atributo `async` ou deferidos usando atributo `defer`.

> * 📖 [Removendo Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Bibliotecas JS Otimizadas e atualizadas:** ![Medium][medium_img] Todas as bibliotecas JavaScript usadas no projeto são necessárias (prefira Vanilla JavaScript (JS puro) para funcionalidades simples), atualizadas para sua versão mais atual e não sobrecarregam seu JavaScript com métodos desnecessários.

> * 📖 [Você pode não precisar de jQuery](http://youmightnotneedjquery.com/)
> * 📖 [Vanilla JavaScript para construção de aplicações web poderosas](https://plainjs.com/)

* [ ] **Modernizr:** ![Baixa][low_img] Se você precisa visar features específicas, é possível usar um Modernizr custom para adicionar classes na sua tag `<html>`.

> * 🛠 [Customize seu Modernizr](https://modernizr.com/download?setclasses)

### Validação JavaScript

* [ ] **ESLint:** ![Alta][high_img] Nenhum erro é visível pelo ESLint (baseando-se nas sua configuração ou regras pré-estabelecidas).

> * 📖 [ESLint - A utilidade de linting plugável para JavaScript e JSX](https://eslint.org/)

**[⬆ voltar ao topo](#Índice)**

---

## Segurança

### Scaneie e cheque seu website

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory por Mozilla](https://observatory.mozilla.org/)
> * [ASafaWeb - Analisador de Segurança Automatizado para Websites ASP.NET](https://asafaweb.com/)

### Melhores práticas

* [ ] **HTTPS:** ![Média][medium_img] HTTPS é usado em todas as páginas e para todo conteúdo externo (plugins, imagens...).

> * 🛠 [Let's Encrypt - Certificados SSL/TLS Gratuitos](https://letsencrypt.org/)
> * 🛠 [Teste SSL Server Gratuito](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Média][medium_img] O header HTTP está configurado com 'Strict-Transport-Security'.

> * 🛠 [Cheque o status e a eligibilidade de pré-carregamento HSTS](https://hstspreload.org/)
> * 📖 [Cheat Sheet para Strict Transport Security HTTP - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> * 📖 [Cheat Sheet para Proteção na Camada de Transporte - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

* [ ] **Cross Site Request Forgery (CSRF):** ![Alta][high_img] Você certifica requests feitas pro seu server-side são legítimas e originadas do seu website / app para prevenir ataques CSRF.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)

* [ ] **Cross Site Scripting (XSS):** ![Alta][high_img] Sua página ou website está livre de possíveis problemas com XSS.

> * 📖 [Cheat Sheet de Prevenção XSS (Cross Site Scripting)  - OWASP](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
> * 📖 [Cheat Sheet de Prevenção XSS baseada no DOM  - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

* [ ] **Content Type Options** ![Média][medium_img] Previne Google Chrome e Internet Explorer de tentar aplicar mime-sniff no content-type de uma response em relação ao que foi declarado no server.

> * 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO)** ![Média][medium_img] Protege seus visitantes contra ataques clickjacking.

> * 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

* [ ] **Política de Segurança de Conteúdo** ![Medium][medium_img] Define como o conteúdo é carregado no seu site e de onde é permitido que seja carregado. Pode também ser usada para se proteger contra ataques de _clickjacking_.

> * 📖 [Política de Segurança de Conteúdo - Uma Introdução - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [Cheat Sheet CSP - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [Cheat Sheet CSP - OWASP](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)
> * 📖 [Referência da Política de Segurança de Conteúdo](https://content-security-policy.com/)

**[⬆ voltar ao topo](#Índice)**

---

## Performance

### Melhores práticas

- [ ] **Peso por página:** ![Alta][high_img] O peso de cada página está entre 0 e 500 KB.

> * 🛠 [Análise de Página de Website](https://tools.pingdom.com)
> * 🛠 [WebPageTest](https://www.webpagetest.org/)
> * 📖 [Limite de Tamanho: Tornando a Web mais leve](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Minificado:** ![Média][medium_img] Seu HTML está minificado.

* [ ] **Lazy loading:** ![Média][medium_img] Imagens, scripts e CSS precisam ser carregados de modo lazy para melhorar o tempo de resposta da página atual (Veja detalhes nas seções respectivas).

* [ ] **Tamanho dos Cookies:** ![Medium][medium_img] Se você está usando cookies, certifique-se de que cada cookie não excede 4096 bytes e que seu _domain name_ não tem mais de 20 cookies.

> * 📖 [Especificação de Cookies: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [Limites de Cookie por Browser](http://browsercookielimits.squawky.net/)

* [ ] **Componentes de terceiros:** ![Medium][medium_img] Iframes ou componentes de terceiros que dependam em JavaScript externo (como botões de compartilhamento) são substituidos por componentes estáticos quando possível, assim limitando chamadas a APIs externas, e mantendo privadas as atividades de seus usuários.

> * 🛠 [Gerador botões de compartilhamento simples](https://simplesharingbuttons.com/)

### Preparando requisições a caminho

> * 📖 [Explicação das técnicas seguintes](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **Resolução DNS:** ![Baixa][low_img] DNS de serviços de terceiros que podem ser necessários são adiantadamente preparados durante tempo ocioso, usando `dns-prefetch`.

```html
<link rel="dns-prefetch" href="https://exemplo.com">
```

* [ ] **Preconnection:** ![Baixa][low_img] DNS lookup, TCP handshake e negociação TLS com serviços que serão necessários em breve, são ambos feitos adiantadamente durante tempo ocioso, usando `preconnect`.

```html
<link rel="preconnect" href="https://exemplo.com">
```

* [ ] **Prefetching:** ![Baixa][low_img] Recursos que serão necessários em breve (ex.: imagens em lazy loading) são requisitados adiantadamente durante tempo ocioso, usando `prefetch`.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Baixa][low_img] Recursos necessários na página atual (ex.: scripts colocados no fim do `<body>`) adiantadamente usando `preload`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Diferença entre prefetch e preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Testes de Performance

* [ ] **Google PageSpeed:** ![Alta][high_img] Todas suas páginas foram testadas (não só a homepage) e têm um score de pelo menos 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Teste sua velocidade mobile com Google](https://testmysite.withgoogle.com)
> * 🛠 [WebPagetest - Teste de Performance e Otimização de Website](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Velocidade e otimização de performance de Website](https://gtmetrix.com/)

**[⬆ voltar ao topo](#Índice)**

---

## Acessibilidade

> **Notas:** Você pode assistir a playlist [A11ycasts com Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Melhores práticas

- [ ] **Melhoramento progressivo:** ![Média][medium_img] Funcionalidades extensivas como a navegação principal e busca deveriam funcionar sem JavaScript habilitado.

> * 📖 [Habilitar / Desabilitar JavaScript no Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Contraste de cor:** ![Média][medium_img] Contraste de cores deveria pelo menos passar WCAG AA (AAA para mobile).

> * 🛠 [Taxa de contraste](https://leaverou.github.io/contrast-ratio/)

#### Cabeçalhos

* [ ] **H1:** ![Alta][high_img] Todas as páginas têm uma tag H1 que não é o título do website.
* [ ] **Cabeçalhos:** ![Alta][high_img] Cabeçalhos deveriam ser usados apropriadamente, na ordem correta (H1 até H6).

> * 📹 [Por que cabeçalhos e landmarks são tão importantes -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

#### Landmarks

- [ ] **Banner role:** ![Alta][high_img] `<header>` tem `role="banner"`.
- [ ] **Navigation role:** ![Alta][high_img] `<nav>` tem `role="navigation"`.
- [ ] **Main role:** ![Alta][high_img] `<main>` tem `role="main"`.

> * 📖 [Usando landmarks ARIA para identificar regiões de uma página](https://www.w3.org/WAI/GL/wiki/Using_ARIA_landmarks_to_identify_regions_of_a_page)
> * 📖 [Categorização de roles ARIA](https://www.w3.org/TR/wai-aria/roles#roles_categorization)

### Semântica

- [ ] **Inputs HTML5 específicos são utilizados:** ![Média][medium_img] Isto é *especialmente* importante para **dispositivos mobile**, que mostram keypads e widgets customizados para diferentes tipos de input.

> * 📖 [Tipos de Input Mobile](http://mobileinputtypes.com/)

### Formulários

* [ ] **Label:** ![Alta][high_img] Uma label é associada a cada input de um formulário. Caso uma label não possa ser exibida, use `aria-label`.

> * 📖 [Usando o atributo aria-label - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Testes de Acessibilidade

* [ ] **Testando padrões de Acessibilidade:** ![Alta][high_img] Use a ferramenta WAVE para testar se sua página respeita os padrões de acessibilidade.

> * 🛠 [Wave testing](http://wave.webaim.org/)

* [ ] **Navegação por Teclado:** ![Alta][high_img] Teste seu website usando apenas seu teclado numa ordem previsível. Todos elementos interativos são alcançáveis e utilizáveis.
* [ ] **Screen-reader:** ![Média][medium_img] Todas as páginas foram testadas num screen-reader (VoiceOver, ChromeVox, NVDA ou Lynx).
* [ ] **Estilo de Foco:** ![Alta][high_img] Se o foco está desabilitado, ele é substituído por um estado visível em CSS.

> * 📹 [Gerenciando Foco - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ voltar ao topo](#Índice)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics está instalado e corretamente configurado.

> * 🛠 [Google Analytics](https://analytics.google.com/analytics/web/)
> * 🛠 [Checador de GA (e outros)](http://www.gachecker.com/)

* [ ] **Lógica de cabeçalhos:** ![Medium][medium_img] Os textos de cabeçalho ajudam a entender o conteúdo na página atual.

> * 🛠 [Tota11y, tab Headings](http://khan.github.io/tota11y/#Try-it)

* [ ] **sitemap.xml:** ![High][high_img] Um sitemap.xml existe e foi submetido ao Google Search Console (anteriormente Google Webmaster Tools).

> * 🛠 [Gerador de Sitemap](https://websiteseochecker.com/html-sitemap-generator/)

* [ ] **robots.txt:** ![High][high_img] O robots.txt não está bloqueando páginas da web.

> * 📖 [O arquivo robots.txt](https://varvy.com/robottxt.html)
> * 🛠 Teste seu robots.txt com o [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Dados Estruturados:** ![Alta][high_img] Páginas usando dados estruturados são testadas e não possuem erros. Dados estruturados ajudam crawlers a entender o conteúdo da página atual.

> * 📖 [Introdução a Dados Estruturados - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 📖 [RDFa - Dados Linkados no HTML](https://rdfa.info/)
> * 📖 [JSON-LD](https://json-ld.org/)
> * 📖 [Microdata](https://www.w3.org/TR/microdata/)
> * 🛠 Teste sua página com a [Ferramenta de Teste de Dados Estruturados](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Lista completa de vocabulários que podem ser usados como dados estruturados. [Schema.org Full Hierarchy](http://schema.org/docs/full.html)

* [ ] **Sitemap HTML:** ![Média][medium_img] Um sitemap HTML é providenciado e acessível via um link no rodapé do seu website.

> * 📖 [Diretrizes para Sitemaps - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)

* [ ] **Tags para links de Paginação:** ![Medium][medium_img] Providencie `rel="prev"` e `rel="next"` para indicar conteúdo pagiado

> * 🛠 [Ferramenta de Tesde de Paginação (rel="prev/next")](https://technicalseo.com/seo-tools/rel-prev-next/)

> * 📖 [Diretrizes de paginação - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Exemplo: Tags para links de paginação para a segunda página de uma lista paginada -->
<link rel="prev" href="https://exemplo.com/?page=1">
<link rel="next" href="https://exemplo.com/?page=3">
```

**[⬆ voltar ao topo](#Índice)**

> Contribua com os nossos [Guias](/content/github.md)

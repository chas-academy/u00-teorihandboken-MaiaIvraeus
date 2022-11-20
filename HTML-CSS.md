# Teorihandboken - HTML & CSS (HC)
Studerande: Maria Ivraeus

## HC 1.1 HTML & CSS
## HTML
HTML står för Hyper Text Markup Language och är det märkspråk som används för att skapa webbsidor. Det utvecklades från IBM's Generalized Markup Language, som användes på 70-talet som ett system för att kunna hantera mycket stora mängder text (exempelvis lagtexter). Den första allmänt tillgängliga beskrivningen av HTML gjordes 1991 av Tim Berners-Lee, en fysiker anställd på CERN. Sedan dess har HTML-språket utvecklats oerhört och är för närvarande inne på sin 5:e version.
<br><br>
HTML-dokument består av en serie element som säger till webbläsaren hur den ska visa detta innehåll på en enhet. Ett HTML-element kan innehålla instruktioner, innehåll och en semantisk mening. Elementen består absolut oftast av en start- och en slut-tagg som omsluter ett innehåll:
<br /><br />

<p align="center"><img src="https://assets.digitalocean.com/django_gunicorn_nginx_2004/articles/new_learners/html-element-diagram.png" width="400" /></p>
<br>
Exempel på basala element ett HTML-dokument:<br><br>

>`<!DOCTYPE html>` - så att webbläsaren förstår vilken version av HTML man avser använda.<br><br>
`<html></html>` - rotelementet, säger till webbläsaren att innanför denna skrivs HTML-markup.<br><br>
`<head></head>` - inom denna skrivs oftast metadata, beskrivning av dokumentet (exempelvis språk).<br><br>
`<title></title>` - HTML-dokumentets titel/namn.<br><br>
`<body></body>` - inom denna ska dokumentets innehåll finnas.<br><br>
`<h1></h1>`- heading/rubrik. Finns i storleksnivåerna h1-h6, där h1 är störst.<br><br>
`<p></p>`- paragraf, för brödtext.<br><br>
`<br>` - radbrytning, behövs ingen end-tag till denna.<br><br>
`<a href="länkadress">Länktext</a>` - hyperlänk
<br><br>
`<img src="länk till bild">` - för att lägga in bilder. Behövs ingen end-tag till denna.<br><br>
`<ul></ul>` - onumrerad lista.<br><br>
`<ol></ol>` - numrerad lista, attribut:<br>
`<ol type="1">` - numrerad<br>
`<ol type="A">` - versaler<br>
`<ol type="a">` - gemener<br>
`<ol type="I">` - romerska versaler<br>
`<ol type="i">` - romerska gemener<br><br>

## CSS
CSS (eller Cascading Stylesheets) är textfiler som man skapar för att styla layouten i ett HTML-dokument. Det kan inte sägas vara ett semantiskt verktyg, det underlättar inte hörförståelsen för blinda exempelvis, utan ska ses som ett ett medel för att lättare och snabbare kunna göra estetiskt snygga webbsidor. CSS kan användas för att exempelvis lägga till animationer, ändra färger, typsnitt och storlekarna på dessa, dela upp sidan i kolumner etc.  
<br><br>
Det finns tre sätt att lägga till CSS på ett HTML-dokument:<br>

>Externt stylesheet – en separat fil som sparas som .css<br><br>
Internt stylesheet –  man lägger in CSS i headtaggen i HTML-dokumentet<br><br>
Inline style – man lägger CSS inom taggarna i HTML-dokumentet
<br><br>

Det rekommenderas att använda sig av externa stylesheets då de kan spara oerhört med tid då dessa filer kan fungera på flera sidor samtidigt. Man länkar till CSS-dokumentet inuti HTML-dokumentens head-tag:
<br>
>`<link rel="stylesheet" href="dokument.css">`


CSS-syntaxen utgörs av en selector som pekar på ett visst HTML-element man vill förändra (ex. en h1-selector), properties och values:<br>

>selector {<br>
    property: value;
<br>}
<br>

 Detta kallas för en CSS-deklaration. Propertyn i en deklaration förklarar *vad* man vill förändra, och sedan anger man ett value som förklarar *hur* man vill förändra. <br>

 Här är är ett exempel på hur man skriver ett så kallat deklarationsblock för att påverka innehållet i ett h1-element:

>h1 {<br>
   color: red;<br>
   background-color: blue;<br>
   border: 3px solid yellow;<br>
}
<br><br>
<h3>The Box Model</h3>
Detta är ett viktigt koncept att förstå om man ska bygga hemsidor. Varje HTML-element kan sägas vara inne i en box, och dessa boxar består av margins, borders, padding och content:
<br><br>
<p align="center"><img src="https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-1-4842-4903-1_16/MediaObjects/320834_2_En_16_Fig1_HTML.png" width="400" /></p>
<br>
Genom att kunna beräkna dimensionerna av dessa containers kan man med säkerhet veta hur elementen kommer vara utplacerade på skärmen.

Box-sizing är en property i CSS som bestämmer vad som ska ingå när man beräknar den totala höjden och bredden av ett elements container. Värdet av denna property kan vara antingen content-box (som är default-värde om inget annat anges) eller border-box. 
<br><br>
Med content-box kommer elementets dimensioner enbart inkludera höjd och bredd, och räknar inte in eventuell padding eller borders. Dessa tar alltså plats *utanför* elementets box, och kommer inte trycka undan content för att få plats. Med värdet border-box räknas padding och borders med *inuti* den totala bredden och höjden av boxen, och kommer således kunna påverka elementets content. Exempel:
<br>

>box-sizing: border-box;



### Box display
CSS-egenskapen display bestämmer hur ett elements box ska bete sig i förhållande till andra boxar. Denna egenskaps mest vanliga default-värden i webbläsare är block och inline. Exempel:

>display: inline;

Ett block-element kommer ta upp hela bredden av dess parent-container, och dess höjd kommer bestämmas av dess content. Nya block kommer börja på en ny rad. Ett inline-element kommer inte starta på en ny rad, utan kommer ta upp den plats som finns över på skärmen. Vissa element är alltid inline, som exempelvis `<img>`, `<a>` och `<span>`.


---

>KÄLLOR:<br>
https://www.w3schools.com/html/html_intro.asp <br><br>
https://en.wikipedia.org/wiki/HTML<br><br>
https://www.digitalocean.com/community/tutorials/how-to-use-the-display-property-to-manipulate-the-box-model-in-css<br><br>
https://www.digitalocean.com/community/tutorials/what-is-an-html-element<br><br>
https://www.freecodecamp.org/news/the-css-display-property-display-none-display-table-inline-block-and-more/<br><br>
https://www.w3schools.com/css/css_intro.asp<br><br>
https://developer.mozilla.org/en-US/docs/Web/CSS<br><br>
Föreläsningar av Sebastian Lindgren, Chas Academy
<br><br>
---
<br>

## HC 1.2 Responsiv design
En hemsida ska kunna visas på olika enheter och deras olika skärmstorlekar, samt se så bra ut som möjligt på dem, för att säkerställa en så bra användarupplevelse som det bara går. En responsiv design ser till att layouten på hemsidan anpassar sig på den enhet som den visas på genom, och kan erhållas med exempelvis flexbox (eller Flexibel Box Module som det egentligen heter).

 Med detta kan man skapa en flexibel layout som ser bra ut på många enhetsstorlekar, och kan göra saker som centrering, justering av utrymme för content etc. mycket snabbare. Detta sätt att bygga hemsidor på blir alltså mer kostnadseffektivt, då underhållet av layouten blir enklare.

Flexbox är alltså en modul och inte en CSS-egenskap, och den gör inline/blockmodellen överflödig. För att använda flexbox måste man först definiera så kallade flex containers i html-dokumentet. 

För att förstå det grundläggande i hur man gör en flex box kan man ge ett exempel på en flex container (parent), som innehåller tre stycken flex items (children):

>`<div=class="flex-container">`<br><br>    `<div>1</div>`<br>
   `<div>2</div>`<br>
   `<div>3</div>`<br><br>
`</div>`

För att med CSS göra denna container flexibel använder man sedan ”flex-container” som selektor, samt sätter värdet flex på display-egenskapen:

>.flex-container {<br>
   display: flex; <br>
} 

<br>
<p align="center"><img src="https://dev-to-uploads.s3.amazonaws.com/i/hy2oqjvsbk60ef92nktg.png" width="400" /></p>
<br>
Att jobba med flexbox kan beskrivas vara endimensionellt i den meningen att man hanterar containers med antingen rader eller kolumner, var för sig. Detta gör den med egenskapen flex-direction, som kan ha 4 olika värden:

>row<br>
row-reverse<br>
column<br>column-reverse

Här är en illustration som visar de olika flex-directions, plus några andra CSS-egenskaper som man kan använda för att manipulera flex-containerns items:
<br>
<p align="center"><img src="https://pbs.twimg.com/media/FTtrHz7WAAAlMWe.jpg" width="400" /></p>

___


>KÄLLOR:<br>
https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox#why_flexbox<br><br>
https://en.wikipedia.org/wiki/Responsive_web_design<br><br>
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox<br><br>
https://www.w3schools.com/css/css3_flexbox_container.asp<br><br>
Föreläsningar av Sebastian Lindgren, Chas Academy
---
<br>

## HC 1.3 Tillgänglighet inom webb
När man bygger hemsidor bör man ha i tanken att så många som möjligt ska kunna manövrera dem med lätthet. Web Accessibility Initiative (WAI) startades 1997 av World Wide Consortium (W3C) med avsikten att göra internet mer tillgängligt för människor med funktionsvariationer. Inom detta initiativ utvecklas riktlinjer och resurser, och två exempel av dessa rekommendationer är Web Content Accessible Guidelines (WCAG) och Accessible Rich Internet Applications (WAI-ARIA). Utvecklare kan använda sig av dessa rekommendationer för att säkerställa att deras webbsidor är så tillgängliga som möjligt, för så många som möjligt.

### WCAG<br>
WCAG definierar tillgänglighets-standarder samt tekniska sådana för innehåll på internet. Dessa är kategoriserade under fyra principer:
>En webbsida bör vara:<br>
>### Uppfattningsbar<br>
>Man ska kunna identifiera innehållet även om man har en funktionsvariation. Detta kan innebära att det exempelvis finns beskrivande textinnehåll och autotextning för saker som inte är text, som bilder och videos.<br><br>
>### Begriplig<br>
>Exempelvis att med starkare kontraster göra att texten är läsbar även för de med synnedsättningar, se till att länkar och knappar är i bra storlek osv. <br><br>
>### Manövrerbar
>Till exempel att man bör kunna använda webbsidans funktioner lika bra med ett tangentbord som man hade gjort med en mus.<br><br>
>### Robust
>Webbsidan bör vara tillgänglig för och kompatibel med alla sorters teknologiska hjälpmedel, exempelvis skärmläsare.

### WAI-ARIA
WAI-ARIA är också det en standard skapad av WAI med målet att tillhandahålla tillgänglighet på webben för människor med funktionsvariationer. Dessa riktlinjer hjälper utvecklare att skapa dynamiskt innehåll och avancerade user interface-kontroller med HTML och JavaScript, i synnerhet för människor som behöver skärmläsare och/eller inte kan använda mus. Detta kan innebära att exempelvis skriva semantiskt korrekt kod, se till att sidstrukturen är väl genomtänkt och så vidare.<br>

<p align="center"><img src="https://web-dev.imgix.net/image/T4FyVKpzu4WKF1kBNvXepbi08t52/ztuCT2fpHvBsKxSBJaXn.jpg?auto=format" width="400" /></p>

___
>KÄLLOR:<br>
https://www.a11yproject.com/posts/what-is-wai/<br><br>
https://www.w3.org/WAI/about/<br><br>
https://www.w3.org/WAI/standards-guidelines/aria/<br><br>
https://www.w3.org/TR/wai-aria/<br><br>
Föreläsningar av Sebastian Lindgren, Chas Academy
___
<br>


## HC 1.4 Aktuella webbstandarder (gällande och kommande standarder)
Att en webbsida följer en webbstandard betyder för det mesta att den har validerad HTML, CSS & JavaScript, där HTML-koden också ska följa riktlinjerna för tillgänglighet och semantik. För att helt och fullt följa en webbstandard ska den även ha: 
* korrekta character encoding-inställningar<br> 
* validerad RSS- eller Atom-nyhetsfeed<br> 
* validerad RDF 
* validerad metadata 
* validerad XML
* validerad objekt embedding
* validerad script embedding
* browser- & resolution-independent kod
* korrekta serverinställningar

Dessa standarder hjälper utvecklare att skapa funktionellt, korskompatibelt innehåll på internet med hög tillgänglighet. Eftersom webb-teknologin är i ständig utveckling krävs det att dessa standarder också följer med i detta, vilket betyder att det krävs ständigt arbete med att pröva och ompröva dessa.

De grupper som sysslar med att ta fram webstandarder (så kallade "Standards Development Organisations") är Internet Engineering Task FORCE (IETF), WHATWG, ECMA TC39 och World Wide Web Consortium (W3C).

World Wide Web Consortium är den ledande utvecklaren av standarder för webben. W3C publicerar internationella webstandarder för HTML, CSS och mycket mer, dessa kallar de för *W3C Recommendations*. Inom W3C utvecklar man dessa standarder i så kallade *working groups* som består av experter, men även i *community groups* där vem som helst kan gå med och föra utvecklingen framåt. Förslag på nya standarder kan komma ur diskussioner i dessa *community groups*, eller som issues på GitHub. Dessa förslag prövas och kan sedan "röra sig uppåt", tills de hamnar i en W3C-kommitté som slutgiltligen bestämmer om det ska antas som en ny standard eller inte.
<br>
<p align="center"><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f1a267f-8420-4475-915c-1650e27a4940/web-standards-web-standard-trajectory.png" width="400" /></p>

___
>Källor:<br>
https://www.w3.org/WAI/standards-guidelines/<br><br>
https://www.smashingmagazine.com/2019/01/web-standards-guide/<br><br>
https://en.wikipedia.org/wiki/Web_standards<br><br>
___
<br>

## HC 1.5 CSS Pre-processorer (ex SASS/LESS)
En pre-processor är ett program som tar en annorlunda CSS-syntax och kompilerar den till en vanilla CSS-fil (alltså vanlig CSS), så att browsern kan läsa den. Vad en pre-processor gör är att man kan använda fler funktioner än i vanlig CSS - och med dessa skriva mer strukturerat, lättläst och kunna göra ändringar snabbare med ökad produktivitet som följd. Det finns ett antal olika pre-processorer att välja mellan, men de absolut populäraste är Sass, Less och Stylus. Alla dessa har sina egna syntaxer.

### Sass
Sass är det äldsta pre-processorprogrammet och kom ut 2006. Sass står för *Syntactically Awesome Style Sheets* och har två stycken syntaxer med file extensions .sass och .scss. Den som är nyast och används absolut mest idag är .scss, och den använder sig av brackets och semikolons, precis som i vanlig CSS.

I Sass använder man sig av variabler med tilldelade värden, som man sedan kan återanvända i kodningen. Dessa variabler deklareras med $-tecknet. Exempel:
>$primary-color: darkblue;<br><br>body {
<br>color: $primary-color;<br>}

Om man bestämmer sig för att ändra primary-color till någon annan färg, behöver man alltså bara göra det på ett enda ställe i stylesheetet. I variablerna kan man även deklarera nummer, strings, booleans, lists och nulls.

I Sass kan man använda sig av så kallade *mixins* som låter en skriva CSS-stilar som kan återanvändas på andra ställen i stylesheetet. Mixins kan också ha andra mixins i sig. Exempel på syntax:
>@mixin *name* {<br>
    property: value;<br>
    property: value;<br>
    ...<br>
} 

För att göra en mixin för exempelvis hur varnings-text ska se ut kan man skriva som följer:
>@mixin warning-text {<br>
color: red;<br>
font-size 30px;<br>
font-weight: bold;<br>}

Och för att använda denna mixin på annat ställe i koden använder man sig av direktivet *@include*. Exempel:
>.danger {<br>
@include link-style;<br>
background-color: $primary-color<br>
...<br>}

I Sass kan man även nesta selectors, på samma sätt som man gör i HTML, vilket gör koden snyggare och lättare att läsa än i standard-CSS. Exempel:
>nav {<br>
  ul {<br>
    margin: 0;<br>
    padding: 0;<br>
    list-style: none;<br>
  }<br><br>
  li {<br>
    display: inline-block;<br>
  }<br><br>
  a {<br>
    display: block;<br>
    padding: 6px 12px;<br>
    text-decoration: none;<br>
  }<br>
}<br>

Man kan också nesta properties som har samma prefix, som exempelvis text-align, text-transform, text-overflow etc. Exempel:
>text: {<br>
  align: center;<br>
  transform: lowercase;<br>
  overflow: hidden;<br>
}<br>
___
>KÄLLOR:<br>
https://sass-lang.com/<br><br>
https://developer.mozilla.org/en-US/docs/Glossary/CSS_preprocessor<br><br>
https://www.w3schools.com/sass/sass_intro.php<br><br>
https://www.w3schools.com/sass/sass_mixin_include.php<br><br>
https://www.w3schools.com/sass/<br><br>
https://raygun.com/blog/css-preprocessors-examples/<br><br>
___

## HC 1.6 Optimering och validering av HTML & CSS
Optimering och validering är viktiga saker att göra om man ska få en så bra användarupplevelse som möjligt av en webbsida. Detta påverkar även hur bra webbplatsen kommer hanteras av sökmotorer.

Att optimera resurser (filer som exempelvis .html, .css, .js, .jpg, .mp4 osv.) kan man göra genom att begränsa hur många anrop webbläsaren måste göra till servern, och se till att inte ha hur många filer som helst som måste laddas ner parallellt så att det blir för långa väntetider. Man kan även slå ihop resurser med hjälp av bundeling-verktyg. 

När det kommer till bild- och videofiler kan man se till att inte ha onödigt hög kvalitet på dem, utan resizea dem med hjälp av ett bildbehandlingsprogram till en lämplig filstorlek så de laddas fortare. Se även till att ha rätt filformat på dem; .jpg är bra för foton medan .png är lämpligt för bilder med färre färger eller som är transparenta.

Validering av sin HTML- och CSS-kod kan man göra med WC3 Markup Validation Service. Den hjälper till att hitta misstag i koden, samt ser till att den är semantiskt korrekt och följer de aktuella standardsen. WC3-validering hjälper också till med att reducera mängden kod, och därmed också reducera storleken på kodfilerna, vilket gör webbläsarens laddningstider bättre.

>### W3C Markup Validation Service:<br>
>HTML-validering:
https://validator.w3.org/<br>
CSS-validering: https://jigsaw.w3.org/css-validator/


<br>

>### Checklista för optimering av innehåll:
>* Se till att rätt språk är inställt
>* Title, headings och content ska stämma överens med varandra
>* Se till att metadata finns (ex. charset, description, author osv.)
>* En tydlig semantisk struktur i koden
>* Webbsidans navigation ska vara tydlig
>* Webbsidan ska vara responsiv
>* Korrekt stavning och grammatik på innehållet
>* Bilder och multimedia som relaterar till innehållet
>* Att webbsidan följer W3C's tillgänglighets-riktlinjer (WCAG & WAI-ARIA) så mycket som möjligt
>* Att alla länkar fungerar och går till rätt platser
>* Validerad html- och css-kod
<br><br>
___
>KÄLLOR:<br>
https://www.janbaskdigitaldesign.com/blogs/w3c-validation/<br><br>
https://jigsaw.w3.org/css-validator/<br><br>
https://validator.w3.org/<br><br>
Föreläsningar av Sebastian Lindgren, Chas Academy
___






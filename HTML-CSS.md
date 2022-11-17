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

## HC 1.3 Tillgänglighet inom webb
Beskriv rubriken nedan här

## HC 1.4 Aktuella webbstandarder (gällande och kommande standarder)
Beskriv rubriken nedan här

## HC 1.5 CSS Pre-processorer (ex SASS/LESS)
Beskriv rubriken nedan här

## HC 1.6 Optimering och validering av HTML & CSS
Beskriv rubriken nedan här

---
Title: Laddningstider
---

Laddningstider
=======================

Analys av 3 webbplatser gällande webbplatsernas laddningstid och användbarhet.

Urval
-----------------------

Jag valde att fortsätta med nyhetssidor och gjorde urvalet genom att plocka 3 överstra träffarna på google för sökordet "nyheter".  
Webbplatserna blev SVT Nyheter, Dagens Nyheter och Aftonbladet.

Metod
-----------------------

Webbplatserna analyserades i webbläsaren Chrome i ett inkognitofönster, så ingen sparad webbläsardata ska påverka mätvärden.

Mätningar gjordes både i fullstort "desktop" läge och litet "mobilt" läge som emulerar en Iphone.

Network-inpektionsverktyg i Chrome användes för att se laddningstid, resurser som laddas och hur mycket data som överförs.
Data som överförs mäter jag i komprimerad form (så som det överförs från servrarna).

Även Google lighthouse i chrome användes för att mäta "First Contentful Paint", "Largest Contentful Paint" och få ett "Accessibility" bedömning. Mätningen med Lighthouse i mobilläge emulerar också en långsam telefon med begränsad processorkraft, vilket kan påverka resultaten på moderna webbplatser ganska mycket.
- "First Contentful Paint"  
    När webbläsaren renderar den första biten av innehåll från DOM, vilket ger den första feedbacken till användaren om att sidan faktiskt laddas
- "Largest Contentful Paint"  
    Hur snabbt huvudinnehållet på en webbsida laddas
- "Accessibility"  
    Anger ett mått i procent hur tillgänglighetsanpassad webbplatsen är för besökare med nedsatta förmågor.


Resultat
-----------------------

<a href="%base_url%/image/analysis/svt.png">
<img alt="Svt Nyheter" src="%base_url%/image/analysis/svt.png?h=200&w=200&crop-to-fit" style="float: left;margin: 0 1em 2em 0;clear: both;">
</a>

### SVT Nyheter

Laddade i mobilläge 51 resurser (0,6 MB) på 0,7 sekunder.  
Och i desktopläge 56 resurser (0,7 MB) på 0,9 sekunder.

Sidan är väl optimerad och får dessutom 100% i tillgänglighetsbedömning.  
På mobila enheter tar det lite lång tid att nå "Contentful Paint" min bedömning är att detta beror på mätningen med begränsad processorkraft.  
<br style="clear: both;">

<a href="%base_url%/image/analysis/dn.png">
<img alt="Dagens Nyheter" src="%base_url%/image/analysis/dn.png?h=200&w=200&crop-to-fit" style="float: left;margin: 0 1em 2em 0;clear: both;">
</a>

### Dagens Nyheter

Laddade i mobilläge 48 resurser (0,9 MB) på 1,6 sekunder.  
Och i desktopläge 159 resurser (1,2 MB) på 8,4 sekunder.

Sidan är väl optimerad för "Contentful Paint" och ritar snabbt upp huvudinnehållet och får 91% i tillgänglighetsbedömning.  
Däremot laddar den många annonser, speciellt i dekstopläge vilket jag tror är förklaringen till den långa laddningstiden, detta påverkar dock inte upplevelsen så mycket då huvudinnehållet ritas upp snabbt.  
<br style="clear: both;">

<a href="%base_url%/image/analysis/aftonbladet.png">
<img alt="Aftonbladet" src="%base_url%/image/analysis/aftonbladet.png?h=200&w=200&crop-to-fit" style="float: left;margin: 0 1em 2em 0;clear: both;">
</a>
### Aftonbladet

Laddade i mobilläge 60 resurser (1,1 MB) på 1,65 sekunder.  
Och i desktopläge 206 resurser (3,3 MB) på 33 sekunder.

Sidan är okay optimerad med laddar många annonser, speciellt i dekstopläge vilket jag tror är förklaringen till den extremt långa laddningstiden.  
Detta påverkar dock inte upplevelsen så mycket då huvudinnehållet ritas upp snabbt.  
Sidan får 92-93% i tillgänglighetsbedömning vilket är väl godkänt.  
<br style="clear: both;">

Analys
-----------------------

Alla tre webbplatserna har stora organisationer bakom sig som antaligen gjort precis dessa analyser själva.
De har alla optimerat så att huvudinnehållet ritas upp snabbt, vilket är viktigt.

1. SVT Nyheter
2. Aftonbladet
3. Dagens Nyheter

SVT Nyheter vinner i min bedömning.  
Laddar extremt snabbt och får 100% i tillgänglighetsbedömningen.

Aftonbladet och Dagens Nyheter kommer sedan ganska jämnt.  
Båda lider av problemet att de visar annonser, som de dessutom antagligen inte kontrollerar själva.
Vid mina besök så har Dagens Nyheter större annonser som dessutom får innehållet på sidan att hoppa ner vid laddning.
Det är det som får mig att välja Aftonbladet som två och Dagens Nyheter som trea.

Absolut laddningstid är för mig inte det viktiga, som jag såg i testet så tog någon sidan nästan en halvminut att ladda alla resurser.
Detta upplevdes dock inte alls på webbsidan, då huvudinnehållet ritades upp snabbt.  
Så för mig är det "Contentful Paint" som är viktigt och det bör vara under 2 sekunder vilket alla sidorna klarade.

Referenser
-----------------------

Webbplatserna
* [SVT Nyheter](https://www.svt.se/)
* [Dagens Nyheter](https://www.dn.se/)
* [Aftonbladet](https://www.aftonbladet.se/nyheter)

Uppmätta laddningstider
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSu_SYCpx8tskS9iK7WvTUkfwrEIoFCS7WXmh8rXNVX135B5fe3vqL6sMCQB4qGT7ElHfaBWCJRK13W/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false" style="width: 100%;height: 13rem;"></iframe>

Övrigt
-----------------------

2023-11-27 Martin Gillström 
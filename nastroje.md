# Vývojářské nástroje a strategie
 
## Jak si usnadnit práci?
V dnešní době být programátorem neznamená dělat všechno sám a psát kód v poznámkovém bloku v potemnělé mistnosti pouze ve společnosti pizzy a plechovek od energy drinků, ale tím, jak programování proniká do všech myslitelných odvětví lidské činnosti, tak stoupá i snaha o všemožné usnadňování a unifikaci vývoje a tím vznikají:

### „Nové a lepší“ nástroje
- programovací jazyky, 
- vývojové sady, 
- vývojová prostředí, 
- balíčky znovupoužitelného kódu řešícího nějaký běžný problém, 

### Nástroje pro spolupráci
(Verzovací) systémy usnadňující společnou práci většího počtu programátorů na jednom projektu. 

Některé z těchno nástrojů budeme používat i my a o těch, které budeme používat, si něco povíme níže.

### Komunitní fóra
Nejznámější z nich je [Stack Overflow](https://stackoverflow.com/) zde lze najít odpovědi na snad každý programátorský problém. Při práci s&nbsp;fóry dodržuj několik pravidel:
 
 - vždycky nejdřív hledej, až když nenajdeš stejný dotaz/problém jako ten tvůj, tak se ptej
 
 - když najdeš odpověď, tak ji jen slepě nekopíruj - nestává se sice, že by se tam vyskytovaly odpovědi, které po spuštění zničí Tvůj počítač a způsobí povstání strojů, ale je běžné, že funkční řešení, které někdo poskytl v nejlepší víře, nemusí být tím, co potřebuješ a co bude fungovat tak, jak čekáš. Vždy se snaž před použitím cizího kódu nalezeného na nějakém fóru mu nejprve porozumnět a až pak ho použít, připadně ho brát pouze jako nasměrování k Vašemu vlastnímu řešení.
 
 
## IntelliJ IDEA

My budeme při práci používat IDE IntelliJ IDEA. Pojďme se seznámit s&nbsp;ovládáním prostředí.

### Klávesové zkratky

- <i>Ctrl+C</i> a <i>Ctrl+V</i> - začneme zlehka - tuhle kombinaci si jistě pamatujete ještě za základní školy, když jste tvořili "referáty". Tady se chová skoro stejně. <b>Skoro.</b> Jak už jsme si řekli, tak editor zdrojového kódu je chytřejší poznámkový blok a v tomto případě je potřeba si na todát pozor, protože pokud kopírujete kód z tohoto editoru a zase ho do tohoto editoru vkládáte, tak se Vám nezkopírují jen označené řádky, ale i kontext. Dále je také potřeba dát si pozor na kopírování větších částí kódu, když jste "včera psali něco podobného", protože z vlastní zkušenosti vím, že čím delší kód, který se někdo chystá zrecyklovat, tím větší pravděpodobnost, že tam nějakou drobnost zapomene upravit a následně mu to bude fungovat úplně jinak, než by čekal. Mnohdy je proto užitečnější použít "kód ze včera" jen jako inspiraci a nový kód napsat od nuly. (existuje i lepší způsob, jak řešit opakující se podobný kód, ale k tomu se dostaneme až v pozdějších lekcích)

- <i>Ctrl+F</i> - další z těch známejších, která i tomto editoru dělá to stejné - touto zkratkou si vyvoláte utilitu fulltextového vyhledávání v aktálně otevřeném souboru

- <i>Ctrl+Shift+F</i> - opět jde o fulltextové vyhledávání, ale tentokrát v celém projektu, který máte otevřený, případně v jeho vyrané části

- <i>Esc</i> - přepnutí se do editoru

- dvakrát <i>Shift</i> - globální vyhledávání čehokoli

- <i>Alt+Enter</i> - zobrazí Vám návrhy toho, jak by šla opravit chyba, kterou Vám editor zvýraznil

- <i>Ctrl+Space</i> - zobrazí vám nabídku s doplněním aktuálně rozepsané části kódu

- <i>Ctrl+Alt+L</i> - naformátuje kód podle nastavených konvencí

- <i>Alt+F7</i> - vyhledá Vám, kde všude je Vámi vybraný element použit

- <i>Ctrl</i> a kliknutí myší na vybraný element Tě přesune o úroveň výš

- <i>Shift+F6</i> - přejmenování proměnné, funkce či třídy v&nbsp;celém kódu - nemusíš hledat všechny výskyty!

- <i>Ctrl+/</i> - zakomentování označeného bloku kódu pomocí řádkového komentáře (`//`)

- <i>Ctrl+Shift+/</i> - zakomentování bloku kódu pomocí blokového komentáře (`/* ... */`)

- <i>Alt+Shift+Ins</i> - označování kódu po sloupcích.

- _Ctrl+D_ - duplikace označeného bloku nebo aktuálního řádku.

### Zkracování kódu

- Zkratky - zkuste v&nbsp;metodě napsat `sout` a&nbsp;zmáčkonout Enter.

- _Ctrl-J_ - zobrazí seznam zkratek.

Oblíbené zkratky:

- `sout` ... `System.out.println()`
- `psvm` ... `public static void main(String[] args) {}`

## [Pokračování: Proměnné a&nbsp;datové typy](promenne-a-datove-typy.md)
## [Zpět na přehled lekce](README.md)

# Vývojářské nástroje a strategie
 
## Jak si usnadnit práci?
V dnešní době být programátorem neznamená dělat všechno sám a psát kód v poznámkovém bloku v potemnělé mistnosti pouze ve společnosti pizzy a plechovek od energy drinků, ale tím, jak programování proniká do všech myslitelných odvětví lidské činnosti, tak stoupá i snaha o všemožné usnadňování a unifikaci vývoje a tím vznikají:

- "nové a lepší" programovací jazyky, vývojové sady, vývojová prostředí, balíčky znovupoužitelného kódu řešícího nějaký běžný problém, 

- (verzovací) systémy usnadňující společnou práci většiho počtu programátorů na jednom projektu. 

Některé z těchno nástrojů budeme používat i my a o těch, které budeme používat, si něco povíme níže. Hodí se také zmínit šedou eminenci vývojářských nástrojů:

- komunitní fóra - nejznámější z nich je [Stack Overflow](https://stackoverflow.com/) zde lze najít odpovědi na snad každý programátorský problém. Při práci s&nbsp;fóry dodržuj několik pravidel:
 
 - vždycky nejdřív hledej, až když nenajdeš stejný dotaz / problém jako ten tvůj, tak se ptej
 
 - když najdeš odpověď, tak ji jen slepě nekopíruj - nestává se sice, že by se tam vyskytovaly odpovědi, které po spuštění zničí Tvůj počítač a způsobí povstání strojů, ale je běžné, že funkční řešení, které někdo poskytl v nejlepší víře, nemusí být tím, co potřebuješ a co bude fungovat tak, jak čekáš. Vždy se snaž před použitím cizího kódu nalezeného na nějakém fóru mu nejprve porozumnět a až pak ho použít, připadně ho brát pouze jako nasměrování k Vašemu vlastnímu řešení.
 
## JDK
 
JDK, neboli Java Development Kit je soubor základních nástrojů pro vývoj aplikací v Javě od společnosti Oracle. Obsahuje kupříkladu překladač zdrojového kódu, debugger pro ladění programu, či nástroj pro tvorbu dokumentace. Dále také obsahuje JRE - Java Runtime Environment. JRE je soubor základních tříd a podpůrných souborů určený ke spouštění Java aplikací a pakliže jste hráli třeba Minecraft, nebo editovali nějaký dokument v OpenOffice, tak jste se již s JRE, byť nevědomky, setkali. JRE také obsahuje JVM - Java Virtual Machine je takzvaný interpeter - program, který náš program řádek pořádku provádí.
Tedy:

 - <b>JDK</b> (+ JRE a JVM) pro vývoj Java aplikací
 
 - <b>JRE</b> (+ JVM) pokud chceme pouze spouštět Java aplikace

 
## IntelliJ IDEA
 
Za tajemnou zkratkou IDE (Integrated Development Enviroment) se skrývá software, který má programátorovi usnadnit samotné psaní kódu. V krátkosti by se dalo říct, že jde jen o chytrý poznámkový blok, ale většina vývojových prostředí nabízí mnohem víc. Například:

- <b>editor</b> - textový editor speciálně navržený pro editování zdrojového kódu, zvládá zvýrazňovat syntax, formátovat kód, tak aby vyhovoval nastaveným konvencím a byl pro člověka, který kód edituje, čitelnější (v některé programovacích jazycích jde všechen kód napsat na jeden řádek a vše bude fungovat, ale pokud pak přijde potřeba změnit nějakou drobnost v kódu, tak se v jednořádkovém kódu nikdo nevyzná), umí našeptávat, zvýrazňovat chyby, či automaticky uzavírat závorky

- <b>debugger</b> - je nástroj, který programátorovi umožnuje zkoumat, proč jeho program (ne)funguje tak, jak jak funguje - do "podezřelých" částí kódu si totiž může přidávat "breakpointy" - body, ve kterých se provádění programu zastaví do doby, než je sám ručně pustí, případně nabízí možnost jít po jednotlivých příkazech a v každém bodě, ve kterém se zastaví, vypíše vždy svůj oktuální stav - hodnoty proměnných a to, jak do té části kódu, ve které se nachází, došel

- <b>kompilátor</b> - je nástroj, který překládá zdrojový kód zapsaný ve vyšším programovacím jazyce (který napíšeme my v editoru) do jazyka nižsího tak, aby mu rozumněl počítač - aby vznikl spustitelný program 

- <b>integrovaný verzovací systém</b> - některá IDE mají integrovaný i verzovací systém - o tom, co to verzovací systém je, si řekneme dále - u [GITu](#GIT) verzovacího systému, který budeme používat my

- <b>object browser</b> - prohlížeč komponent nacházejících se balíčcích softwaru, jejich hierarchii, metody a proměnné

- <b>nástroje pro tvorbu uživatelského rozhraní</b> - některá IDE obsahují i nástroje pro snadnou tvorbu uživatelského rozhraní

Většina vývojových prostředí bývá navržených přímo pro vývoj v konkrétním programovacím jazyce, ale najdou se výjimky, které podporují větší počet programovacích jazyků - jednou z těchto výjimek je třeba právě IDEA, kterou budeme používat my. Její nejznámější alternativy (pokud jde o vývoj v Javě) jsou [Eclipse](https://www.eclipse.org/eclipseide/) a [NetBeans](https://netbeans.apache.org/)

### Klávesové zkratky a další vychytávky pro vývoj IDEI

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

## [Další: První program...](prvni-projekt.md)

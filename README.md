<p align="center">
  <img src="https://engeto.cz/wp-content/uploads/2019/01/engeto-square.png" width="200" height="200">
</p>

# Java - 1. lekce

## Co bychom měli mít hotové

Před první hodinou byste měli mít naistalované základní nástoje, které budeme na tomto kurzu používat. Návod, jak na to, je [zde](https://github.com/ENGETO-Java-Akademie/priprava/blob/main/README.md) a v případě, že narazíte při instalaci na nějaký problém, tak nám klidně napište na Slacku a rádi Vám s tím poradíme.

## Co nás čeká

 - [Co je to Java](#co-je-to-java)
 
 - [Vývojářské nástoje](#vývojářské-nástroje): [JDK](#jdk), [IntelliJ IDEA](#intellij-idea)
 
 - [První projekt](#první-projekt)
 
 - [Balíčky](#balíčky)
 
 - [Proměnná](#proměnná)
 
 - [Datový typ](#datový-typ)
 
 ## Co je to Java
 
 První vydání jazyka se datuje do roku 1995, vývoj však započal na začátku devadesátých let. Jazyk Java byl navržen jako řešení pro vývoj platformně nezávislých programů. Program napsaný v Javě tedy jde spustit na libovolném z podporovaných operačních systémů (na Windows, v Linuxu, MacOS,...). Proto má Java na rozdíl od ostatních jazyků rozdílný způsob překladu a spouštění. Většina jazyků se překládá přímo do sekvence instrukcí dané procesorové platformy, které zapíšeme do souboru (například soubor .exe ve Windows) a následně se tento soubor spouští. Java místo toho vytváří takzvaný bajtkód. To je sekvence instrukcí fiktivního procesoru. Tyto instrukce pak nelze spustit přímo přímo v procesoru počítače — spouští se ve virtuálním stroji, který se nazývá JVM (Java Virtual Machine). Výhodou tohoto přístupu je jeho nezávislost na platformě. Kdekoliv máš k dispozici JVM, můžeš spouštět jakýkoli program v Javě. Zároveň je to omezení — bez JVM program nespustíš.

Java je objektově orientovaný jazyk. To znamená, že Java není čistě objektový jazyk (vše je objekt), ale nacházejí se zde i primitivní datové typy, jež nejsou reprezentovány jako objekty. Java se proti mnoha jiným jazykům vyznačuje zejména bezpečností při správě paměti. Vývojář je plně odstíněn od práce s ní. Při práci s objekty využívá pouze reference (odkazy) a veškerou alokaci a uvolňování paměti řeší JVM, popřípadě Garbage Collector. (V tomto rysu je Java podobná jazyku C#.)

### A jak to vypadá

```java
// popis umístění - složka
package eng.nasprvniprogram;

class CoalMine {
  
  // deklarace proměnné WHAT_IS_IN_THE_MINE, do které zároveň přiřadíme hodnotu Some quality coal
  private static final String WHAT_IS_IN_THE_MINE = "Some quality coal";
  
  /*
   * metoda main je vstupní branou do Javovského programu, kterou musí obsahovat každý program
   * a ze které voláme všechny ostatní funkce
   */
  public static void main(String[] args) {
    // cyklus, který se provádí, dokud je splněna uvedená podmínka "i < 4"
    for (int i = 1; i < 4; i++) {
      // volání naší metody mine
      mine();
    }
  }
  
  /*
   * toto je naše úžasná metoda mine, která do dolů
   * pošle jednoho trpaslíka, aby přinesl to, co najde
   */
  private static void mine() {
    // System.out.println vypíše parametr, který mu předáme, do konzole
    System.out.println("We have mined: " + WHAT_IS_IN_THE_MINE + ".");
  }
}
```
 
## Vývojářské nástroje
 
V dnešní době být programátorem neznamená dělat všechno sám a psát kód v poznámkovém bloku v potemnělé mistnosti pouze ve společnosti pizzy a plechovek od energy drinků, ale tím, jak programování proniká do všech myslitelných odvětví lidské činnosti, tak stoupá i snaha o všemožné usnadňování a unifikaci vývoje a tím vznikají "nové a lepší" programovací jazyky, vývojové sady, vývojová prostředí, balíčky znovupoužitelného kódu řešícího nějaký běžný problém, či (verzovací) systémy usnadňující společnou práci většiho počtu programátorů na jednom projektu. Některé z těchno nástrojů budeme používat i my a o těch, které budeme používat, si něco povíme níže. Hodí se také zmínit šedou eminenci vývojářských nástrojů jsou různá komunitní fóra - nejznámější z nich je [Stack Overflow](https://stackoverflow.com/) zde lze najít odpovědi na snad každý programátorský problém, jen je nutné dodržovat několik pravidel.
 
 - vždycky nejdřív hledejte a až když nenajdete stejný dotaz / problém jako ten Váš, tak se ptejte
 
 - když dostanete odpověď, co nějakou odpověď najdete, tak ji jen slepě nekopírujte - nestává se sice, že by se tam vyskytovaly odpovědi, které po spuštění přehrají Váš počítač a způsobí povstání strojů, ale je běžné, že funkční řešení, které někdo poskytl v nejlepší víře, nemůsí být tím, co potřebujete a co bude fungovat i tak, jak čekáte a proto se snažte vždy před použitím cizího kódu nalezeného na nějakém fóru mu nejprve porozumnět a až pak ho použít, připadně ho brát pouze jako nasměrování k Vašemu vlastnímu řešení
 
### JDK
 
JDK, neboli Java Development Kit je soubor základních nástrojů pro vývoj aplikací v Javě od společnosti Oracle. Obsahuje kupříkladu překladač zdrojového kódu, debugger pro ladění programu, či nástroj pro tvorbu dokumentace. Dále také obsahuje JRE - Java Runtime Environment. JRE je soubor základních tříd a podpůrných souborů určený ke spouštění Java aplikací a pakliže jste hráli třeba Minecraft, nebo editovali nějaký dokument v OpenOffice, tak jste se již s JRE, byť nevědomky, setkali. JRE také obsahuje JVM - Java Virtual Machine je takzvaný interpeter - program, který náš program řádek pořádku provádí.
Tedy:

 - <b>JDK</b> (+ JRE a JVM) pro vývoj Java aplikací
 
 - <b>JRE</b> (+ JVM) pokud chceme pouze spouštět Java aplikace

 
### IntelliJ IDEA
 
Za tajemnou zkratkou IDE (Integrated Development Enviroment) se skrývá software, který má programátorovi usnadnit samotné psaní kódu. V krátkosti by se dalo říct, že jde jen o chytrý poznámkový blok, ale většina vývojových prostředí nabízí mnohem víc. Například:

- <b>editor</b> - textový editor speciálně navržený pro editování zdrojového kódu, zvládá zvýrazňovat syntax, formátovat kód, tak aby vyhovoval nastaveným konvencím a byl pro člověka, který kód edituje, čitelnější (v některé programovacích jazycích jde všechen kód napsat na jeden řádek a vše bude fungovat, ale pokud pak přijde potřeba změnit nějakou drobnost v kódu, tak se v jednořádkovém kódu nikdo nevyzná), umí našeptávat, zvýrazňovat chyby, či automaticky uzavírat závorky

- <b>debugger</b> - je nástroj, který programátorovi umožnuje zkoumat, proč jeho program (ne)funguje tak, jak jak funguje - do "podezřelých" částí kódu si totiž může přidávat "breakpointy" - body, ve kterých se provádění programu zastaví do doby, než je sám ručně pustí, případně nabízí možnost jít po jednotlivých příkazech a v každém bodě, ve kterém se zastaví, vypíše vždy svůj oktuální stav - hodnoty proměnných a to, jak do té části kódu, ve které se nachází, došel

- <b>kompilátor</b> - je nástroj, který překládá zdrojový kód zapsaný ve vyšším programovacím jazyce (který napíšeme my v editoru) do jazyka nižsího tak, aby mu rozumněl počítač - aby vznikl spustitelný program 

- <b>integrovaný verzovací systém</b> - některá IDE mají integrovaný i verzovací systém - o tom, co to verzovací systém je, si řekneme dále - u [GITu](#GIT) verzovacího systému, který budeme používat my

- <b>object browser</b> - prohlížeč komponent nacházejících se balíčcích softwaru, jejich hierarchii, metody a proměnné

- <b>nástroje pro tvorbu uživatelského rozhraní</b> - některá IDE obsahují i nástroje pro snadnou tvorbu uživatelského rozhraní

Většina vývojových prostředí bývá navržených přímo pro vývoj v konkrétním programovacím jazyce, ale najdou se výjimky, které podporují větší počet programovacích jazyků - jednou z těchto výjimek je třeba právě IDEA, kterou budeme používat my. Její nejznámější alternativy (pokud jde o vývoj v Javě) jsou [Eclipse](https://www.eclipse.org/eclipseide/) a [NetBeans](https://netbeans.apache.org/)

#### Klávesové zkratky a další vychytávky pro vývoj IDEI

- <i>Ctrl+C</i> a <i>Ctrl+V</i> - začneme zlehka - tuhle kombinaci si jistě pamatujete ještě za základní školy, když jste tvořili "referáty". Tady se chová skoro stejně. <b>Skoro.</b> Jak už jsme si řekli, tak editor zdrojového kódu je chytřejší poznámkový blok a v tomto případě je potřeba si na todát pozor, protože pokud kopírujete kód z tohoto editoru a zase ho do tohoto editoru vkládáte, tak se Vám nezkopírují jen označené řádky, ale i kontext. Dále je také potřeba dát si pozor na kopírování větších částí kódu, když jste "včera psali něco podobného", protože z vlastní zkušenosti vím, že čím delší kód, který se někdo chystá zrecyklovat, tím větší pravděpodobnost, že tam nějakou drobnost zapomene upravit a následně mu to bude fungovat úplně jinak, než by čekal. Mnohdy je proto užitečnější použít "kód ze včera" jen jako inspiraci a nový kód napsat od nuly. (existuje i lepší způsob, jak řešit opakující se podobný kód, ale k tomu se dostaneme až v pozdějších lekcích)

- <i>Ctrl+F</i> - další z těch známejších, která i tomto editoru dělá to stejné - touto zkratkou si vyvoláte utilitu fulltextového vyhledávání v aktálně otevřeném souboru

- <i>Ctrl+Shift+F</i> - opět jde o fulltextové vyhledávání, ale tentokrát v celém projektu, který máte otevřený, případně v jeho vyrané části

- <i>Esc</i> - přepnutí se do editoru

- dvakrát <i>Shift</i> - globální vyhledávání čehokoli

- <i>Alt+Enter</i> - zobrazí Vám návrhy toho, jak by šla opravit chyba, kterou Vám editor zvýraznil

- <i>Ctrl+Space</i> - zobrazí vám nabídku s doplněním aktuálně rozepsané části kódu

- <i>Ctrl+Alt+L</i> - naformátuje kód podle nastavených konvencí

- <i>Alt+F7</i> - vyhledá Vám, kde všude je Vámi vybraný element použit

- <i>Ctrl</i> a kliknutí myší na vybraný element Vás přesune o úroveň výš

## První projekt

Pakliže Java není Váš první programovací jazyk, tak jistě tušíte, co si představit pod "Hello, world!". Pokud ne, tak vězte, že je jde o program používaný k testování toho, že máme vše potřebné pro vývoj v tom kterém programovacím jazyce, který nedělá nic víc, že někam vypíše větu "Hello, world!" - od toho pochází i jeho název (tradičně jde o první psaný a spouštěný program).

K tomu, abychom ho zvládli napsat, budeme potřebovat metodu pro výpis v textu - System.out.println(<i>sem přijde to, co chceme vypsat</i>).

Teď už k samotnému projektu.

Po spuštění Idei klikneme na "New project" - zvolíme Java project - použijeme šablonu "Console app" a po vybrání jména máme vytvořený náš první projekt.

V našem projektu bude jedna třída pojmenovaná Main a v ní metoda pojmenovaná main:

```java
package com.company;

public class Main {

    public static void main(String[] args) {
	// write your code here
    }
}
```
Jak komentář napovídá a jak jsme si už řekli, main metoda je vstupní bránou do našeho programu - tato metoda je tou, co se spustí, když spustíme náš program a z ní voláme všechny ostatní metody, případně kód píšeme přímo do ní.

To je to, co musíme udělat.

Jak jsme si řekli, tak metoda System.out.println slouží pro výpis textu a už i víme, kam ji umístit, aby se provedla - do main metody - do závorek jí jako parametr předáme to, co chceme vypsat, což je v našem případě text "Hello, world!". Výsledný kód pak bude vypadat takto:

```java
package com.company;

public class Main {

    public static void main(String[] args) {
	      System.out.println("Hello, world!");
    }
}
```

## Balíčky

Balíček v Javě představuje skupinu souvisejících tříd. Jde si ho představit jako souborový systém kdy balíčkem je složka - která může mít podbalíčky - podsložky a jednotlivé třídy, rozhraní a enumy jsou pak soubory.

To, do jakého balíčku naše třída/enum/interface patří, specifikujeme pomocí klíčového slova package, za kterým následuje cesta k té náší X.

Pokud bychom měli třídu Ruler v podbalíčku utilities uvnitř balíčku geometry, tak by zápis vypadal takto:

```java
package geometry.utilities;

public class Ruler {

}
```

## Proměnná

Proměnná představuje pojmenované místo v paměti, do kterého můžeme ukládat hodnoty a na které se můžeme dále v programu odkazovat právě pomocí jeho jména.

Každá proměnná má přesně daný datový typ, který specifikujeme při její deklaraci.

Při deklaraci proměnných také můžeme použít některá kláčová slova:

- <b>static</b> - tohle klíčové slovo říká, že proměnná má existovat po celou dobu běhu programu

- <b>final</b> - tohle klíčové slovo říká, že půjde o konstantu - hodnota této proměnné nepůjde měnit

- <b>public</b>, <b>protected</b>, <b>private</b> - tato klíčová slova definují viditelnost proměnné

```java
// jména konstant píšeme vždy velkými písmeny a k oddělování jednotlivých částí používáme podtržítko _
final String ZAKLADNI_OSLOVENI = "Dobrý den,";
// jména ostatních proměnných píšeme tzv. camel case - první slovo ve jméně je celé malými písmeny
//  a každé další slovo začíná velkým písmenem, které zároveň slouží jako vizuální oddělovač
private int myAgeIsNotThisNumber = 23; 
```

Při odkazování se na proměnou již žádná klíčová slova nepoužíváme - jen její jméno.

## Datový typ

Java je silně typovaný programovací jazyk, což znemaná, že každá proměnná má pevně určený datový typ a v každé promenné může vždy být uložena pouze hodnota odpovídající danému datovému typu.

Datové typy se dělí na <b>primitivní</b> a <b>neprimitivní</b> neboli referenční, protože odkazují na nějaký objekt. Primitivní datové typy jsou "základem" - popisují pouze datový typ a velikost (která se liší) a vždy mají hodnotu, kdeždo referenční datové typy mohou představovat i mnohem složitější struktury, mohou být prázdné a mnohdy nabízí i pomocné metody.

Pro jejich rozlišení existuje jednoduché pravidlo - primitivní datové typy začínají vždy malým písmenem a referenční zase velkým.

### Primitivní datové typy

- <b>byte</b> - může pojmout celé číslo z rozsahu od -128 do 127

- <b>short</b> - může pojmout celé číslo z rozsahu od -32768 do 32767

- <b>int</b> - může pojmout celé číslo z rozsahu od -2147483648 do 2147483647

- <b>long</b> - může pojmout celé číslo z rozsahu od -9223372036854775808 do 9223372036854775807

- <b>float</b> - může pojmout reálné číslo z rozsahu od -3.40282e+38 do -3.40282e+38

- <b>double</b> - může pojmout reálné číslo z rozsahu od -1.79769e+308 do -3.79769e+308

- <b>boolean</b> - může pojmout jednu logickou hodnotu - pravda nebo nepravda

- <b>char</b> - může pojmout jeden libovolný znak (UNICODE)

### Referenční datové typy

Referenčních je na rozdíl od těch primitivních teoreticky neomezený počet, a proto si zmíníme jen pár z nich:

- <b>String</b> - může pojmout libovolný řetězec
```java
String aPoem = "Roses are red, Java is hard, if I want bread, I better start.. learning!";
```
- <b>Array</b> - může pojmout libovolný počet prvků stejného datového typu
```java
String[] names = {"Martin", "Marcin", "Rasmus", "Luka", "Mihael"};
```

### Rozdíly


# První projekt

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

## [Úkoly: oprav chyby](ukoly01-promenne)

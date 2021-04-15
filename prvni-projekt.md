
# První projekt

Postup pro vytvoření prvního projektu si ukážeme společně. Stručně:
1. Po spuštění IDEI klikneme na "New project" 
2. zvolíme Java project
3. použijeme šablonu "Console app"
4. zadáme jméno projektu
5. a&nbsp;máme vytvořený náš první projekt.

> Můžete využít [návod ve studijních materiálech](https://engeto.com/cs/kurz/java-1-uvod-do-programovani/studium/OFMSGkbhQJSmt5iHBNwUuQ/zaciname-s-javou/tvuj-prvni-projekt/program-hello-world).

## Hello World!

Pakliže Java není Váš první programovací jazyk, tak jistě tušíte, co si představit pod "Hello, world!". Pokud ne, tak vězte, že je jde o program používaný k testování toho, že máme vše potřebné pro vývoj v tom kterém programovacím jazyce, který nedělá nic víc, že někam vypíše větu "Hello, world!" - od toho pochází i jeho název (tradičně jde o první psaný a spouštěný program).

K tomu, abychom ho zvládli napsat, budeme potřebovat metodu pro výpis v textu - `System.out.println(<i>sem přijde to, co chceme vypsat</i>)`.

## Třída `Main` a metoda `main`

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

Jak jsme si řekli, tak metoda `System.out.println` slouží pro výpis textu a už i víme, kam ji umístit, aby se provedla - do main metody - do závorek jí jako parametr předáme to, co chceme vypsat, což je v našem případě text "Hello, world!". Výsledný kód pak bude vypadat takto:

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

## [Pokračování: Vývojářské nástroje](nastroje.md)
## [Zpět na přehled lekce](README.md)

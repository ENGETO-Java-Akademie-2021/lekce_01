# Co je to Java?
 
 První vydání jazyka se datuje do roku 1995, vývoj však započal na začátku devadesátých let. Jazyk Java byl navržen jako řešení pro vývoj platformně nezávislých programů. Program napsaný v Javě tedy jde spustit na libovolném z podporovaných operačních systémů (na Windows, v Linuxu, MacOS,...). 
 
 ## Překlad a bajtkód
 Proto má Java na rozdíl od ostatních jazyků rozdílný způsob překladu a spouštění. Většina jazyků se _překládá_ (_kompiluje_) přímo do sekvence instrukcí dané procesorové platformy, které zapíšeme do souboru (například soubor .exe ve Windows) a následně se tento soubor spouští. Java místo toho vytváří takzvaný _bajtkód_. To je sekvence instrukcí fiktivního procesoru. Tyto instrukce pak nelze spustit přímo přímo v&nbsp;procesoru počítače — spouští se ve virtuálním stroji, který se nazývá JVM (Java Virtual Machine). 
 
 - Výhodou tohoto přístupu je jeho nezávislost na platformě. Kdekoliv máš k&nbsp;dispozici JVM, můžeš spouštět jakýkoli program v&nbsp;Javě. 
 
 - Zároveň je to omezení — bez JVM program nespustíš a&nbsp;při spouštění je třeba aktivovat JVM, nestačí jen „kliknout“ na spustitelný program (resp. stačí, pokud je systém správně nastavený).

## Objektově orientovaný jazyk
Java je objektově orientovaný jazyk. To znamená, že Java není čistě objektový jazyk (vše je objekt), ale nacházejí se zde i&nbsp;primitivní datové typy, jež nejsou reprezentovány jako objekty. 

## Garbage Collector a práce s&nbsp;pamětí
Java se proti mnoha jiným jazykům vyznačuje zejména bezpečností při správě paměti. Vývojář je plně odstíněn od práce s ní. Při práci s objekty využívá pouze reference (odkazy) a veškerou alokaci a uvolňování paměti řeší JVM, popřípadě Garbage Collector. (V tomto rysu je Java podobná jazyku C#.) Tím se:

- výrazně omezujeme riziko chyb, 

- ale práce s&nbsp;pamětí může být o&nbsp;méně efektivní po stránce rychlosti i&nbsp;potřebné kapacity paměti &mdash; spoléháme na „inteligenci“ Garbage Collectoru, nemůžeme činnost ovlivnit sami. 

## A jak program v&nbsp;Javě vypadá

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

## [Další: Nástroje, které budeme používat](nastroje.md)
# Proměnné a&nbsp;datové typy

## Proměnná

Proměnná představuje pojmenované místo v paměti, do kterého můžeme ukládat hodnoty a na které se můžeme dále v programu odkazovat právě pomocí jeho jména.

Každá proměnná má přesně daný datový typ, který specifikujeme při její deklaraci.


Při odkazování se na proměnou již žádná klíčová slova nepoužíváme - jen její jméno.

## Datový typ

Java je silně typovaný programovací jazyk, což znemaná, že každá proměnná má pevně určený datový typ a v každé promenné může vždy být uložena pouze hodnota odpovídající danému datovému typu.

Datové typy se dělí na <b>primitivní</b> a <b>neprimitivní</b> neboli referenční, protože odkazují na nějaký objekt. Primitivní datové typy jsou "základem" - popisují pouze datový typ a velikost (která se liší) a vždy mají hodnotu, kdeždo referenční datové typy mohou představovat i mnohem složitější struktury, mohou být prázdné a mnohdy nabízí i pomocné metody.

Pro jejich rozlišení existuje jednoduché pravidlo - primitivní datové typy začínají vždy malým písmenem a referenční zase velkým.

### Primitivní datové typy

- byte - může pojmout celé číslo z rozsahu od -128 do 127 (**pozor**, nikoli 0..255 jako ve většině jazyků)

- short - může pojmout celé číslo z rozsahu od -32768 do 32767

- <b>int</b> - může pojmout celé číslo z rozsahu od -2147483648 do 2147483647

- <b>long</b> - může pojmout celé číslo z rozsahu od -9223372036854775808 do 9223372036854775807

- float - může pojmout reálné číslo z rozsahu od -3.40282e+38 do -3.40282e+38

- <b>double</b> - může pojmout reálné číslo z rozsahu od -1.79769e+308 do -3.79769e+308

- <b>boolean</b> - může pojmout jednu logickou hodnotu - pravda nebo nepravda

- <b>char</b> - může pojmout jeden libovolný znak (UNICODE)

### Referenční datové typy

Referenčních je na rozdíl od těch primitivních teoreticky neomezený počet, a proto si zmíníme jen pár z nich:

- <b>String</b> - může pojmout libovolný řetězec
```java
String aPoem = "Roses are red, Java is hard, if I want bread, I better start.. learning!";
```

- Veškeré třídy v&nbsp;Javě. Například: <b>LocalDate</b> - ukládá datum nebo <b>Color</b> - uchování barev. Ale také všechny třídy, které si vytvoříme sami
```java
LocalDate datum = LocalDate.of(2021,4,15);
Color barva = Color.BLUE;
Zakaznik zakaznik = new Zakaznik();
```


- <b>pole (array)</b> - může pojmout libovolný počet prvků stejného datového typu
```java
String[] names = {"Martin", "Marcin", "Rasmus", "Luka", "Mihael"};
```

## Modifikátory
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

## Práce s proměnnými

### Vytvoření &mdash; deklarace
```java
DatovyTyp nazevPromenne;
```
Příklady:
```java
Color barva;
int zaklad;
int pocetOpakovani;
String jmeno;
String celeJmeno;
```

### Přiřazení hodnoty
```java
nazevPromenne = vyrazVracejiciHodnotu;
```
Příklady:
```java
barva = Color.RED;
pocetOpakovani = zaklad + 1;
jmeno = "Karel";
celeJmeno = jmeno + " Dvořák";
```


### Použití hodnoty
```java
nazevPromenne;
```
Příklady:
```java
System.out.println(pocetOpakovani);
String jmenoUzivatele = celeJmeno;
```

## Pojmenování proměnných

- Používej `camelCase` notaci
    - První písmeno malé, pak vždy každé další slovo musí začínat velkým písmenem.
- Doporučení: Nepoužívej v názvech diakritiku.

## Další zdroje:
Můžete si projít také [text o&nbsp;proměnných v&nbsp;kurzu Java#1](https://engeto.com/cs/kurz/java-1-uvod-do-programovani/studium/u2B-FJ11Q5mW6MDi-B6GSg/popis-dat-promenne-objekty/promenne-a-datove-typy/promenne).

## [Pokračování: Úkoly](README.md#Úkoly)
## [Osnova lekce](README.md)

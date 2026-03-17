# Labo 19

Zorg dat je de volgende folderstructuur volgt:

```
webtechnologie/
├─ labo-01/
│  ├─ oefening-01/
│  │  ├─ index.html
│  │  ├─ images/
│  │  │  ├─ image-1.jpg 
│  │  │  └─ image-n.jpg 
│  │  ├─ css/
│  │  │   ├─ reset.css
│  │  │   └─ style.css
│  │  └─ js/
│  │     └─ script.js
│  ├─ oefening-02/
│  └─ oefening-n/
├─ labo-02/
└─ labo-n/      
```

- Gebruik steeds JS modules om globale variabelen te vermijden (`<script type="module" src="./path/to/script.js" defer></script>`)
- Zet je Javascript file steeds in strict mode (`"use strict"`);
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)
- Voor invoer kun je hardcoded variabelen of de `prompt()` functie gebruiken.
- Print resultaten uit in de console.

## oefening 1: bereken de som en het product

### leerdoelen

* kennismaken met het gebruik van callbacks in JavaScript
* begrijpen hoe functies als callback kunnen worden gebruikt

### functionele analyse

Schrijf een JavaScript-functie genaamd `calculate` die twee getallen en een callback-functie accepteert. Deze callback-functie moet de som van de twee getallen afdrukken.

### technische analyse

1. Schrijf een functie genaamd `calculate` die twee parameters (getallen) en een derde parameter (callback-functie) accepteert.
2. In de functie `calculate`, bereken de som van de twee getallen.
3. Roep de callback-functie aan met de berekende som als argument.
4. Lees in deze callback-functie het resultaat uit in de console.

### voorbeeldinteractie
![voorbeeldinteractie](./voorbeeldinteractie-calculate.avif)

## oefening 2: string manipulatie

### leerdoelen

* toepassen van het concept van callbacks bij het manipuleren van strings
* begrijpen hoe functies als argumenten kunnen worden doorgegeven.

### functionele analyse

Schrijf een JavaScript-functie genaamd `modifyString` die een string en een callback-functie accepteert. De callback-functie moet de lengte van de string afdrukken.

### technische analyse

1. Schrijf een functie genaamd `modifyString` die een string en een callback-functie accepteert.
2. In de functie `modifyString`, bereken de lengte van de string.
3. Roep de callback-functie aan met de lengte van de string als argument.
4. Lees het resultaat uit in de console.

### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-modifystring.avif)

## oefening 3: rekenmachine

### leerdoelen

* begrijpen hoe functies als returnwaarde kunnen worden gebruikt.
* toepassen van callbacks bij het maken van een eenvoudige rekenmachine.

### functionele analyse

Schrijf een factory-functie genaamd `createCalculator` die een wiskundige bewerking ('add' of 'multiply') accepteert en een functie retourneert. 

### technische analyse

1. **Maak een functie genaamd `createCalculator`**  
   Deze functie accepteert één parameter: een string genaamd `bewerking`.

2. **Gebruik een `if`-statement binnen `createCalculator`**  
   Controleer of de waarde van `bewerking` gelijk is aan `'add'` of `'multiply'`.

3. **Retourneer een functie op basis van de bewerking**  
   De geretourneerde functie moet:
    - Twee getallen **optellen** of **vermenigvuldigen**, afhankelijk van de opgegeven bewerking.
    - Daarna een **callback-functie** aanroepen met het resultaat.

4. **De geretourneerde functie accepteert drie parameters:**
    - `getal1`: het eerste getal
    - `getal2`: het tweede getal
    - `callback`: een functie die wordt aangeroepen met het resultaat

5. **Maak een aparte functie genaamd `printToConsole`**  
   Deze functie accepteert één argument en logt dit naar de console.

6. **Gebruik de `createCalculator` functie**  
   Roep de geretourneerde functie aan met twee getallen en de `printToConsole` callback.

### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-rekenmachine.avif)



## oefening 4: gebruik van de spread operator

### leerdoelen

* begrijpen hoe de spread-operator werkt.
* kunnen toepassen van de spread-operator om arrays samen te voegen en te kopiëren.

### functionele analyse

Schrijf een JavaScript-functie genaamd `mergeArrays` die twee arrays accepteert en een nieuwe array retourneert waarin de elementen van beide arrays zijn samengevoegd. Gebruik de spread-operator om de arrays samen te voegen.

### technische analyse

1. Schrijf een functie genaamd `mergeArrays` die twee parameters (arrays) accepteert.
2. Gebruik de spread-operator om beide arrays samen te voegen in een nieuwe array.
3. Lees het resultaat uit in de console.

### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-merge-arrays.avif)

## oefening 5: sorteren van strings

### leerdoelen

* kennismaken met het sorteren van arrays in JavaScript.
* begrijpen hoe de sort-functie werkt met strings.

### functionele analyse

Schrijf een JavaScript-functie genaamd `sortStrings` die een array van strings accepteert. De functie moet de array alfabetisch sorteren.

### technische analyse

1. Schrijf een functie genaamd `sortStrings` die één parameter (array van strings) accepteert.
2. Gebruik de ingebouwde sort-functie van JavaScript om de array te sorteren.
3. Lees het resultaat uit in de console.

## oefening 6: sorteren van objecten

### leerdoelen

* kennismaken met het sorteren van arrays met objecten op basis van een specifiek attribuut.
* begrijpen hoe de sort-functie werkt met aangepaste vergelijkingsfuncties.

### functionele analyse

Schrijf een JavaScript-functie genaamd `sortByAttribute` die een array van objecten en een attribuutnaam accepteert. De functie moet de array van objecten sorteren op basis van het opgegeven attribuut.

### technische analyse

1. Schrijf een functie genaamd `sortByAttribute` die twee parameters accepteert: de array van objecten en de attribuutnaam om op te sorteren.
2. Gebruik de sort-functie met een aangepaste vergelijkingsfunctie om de array van objecten te sorteren op het opgegeven attribuut.
3. Lees het resultaat uit in de console.

> Tip: voor deze oefening kun je er van uitgaan dat de strings die je gaat sorteren allemaal met een hoofdletter beginnen en géén accenten bevatten, zodat je dezelfde callback functie kunt gebruiken voor string en number vergelijkingen

### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-sorteren-van-objecten.avif)

## oefening 7: filteren en verdubbelen

### leerdoelen

* Gebruik van de filter- en map-functies op arrays.
* Combinatie van verschillende array-functies in een enkele operatie.

### functionele analyse

Schrijf een JavaScript-functie genaamd `filterAndDouble` die een array van getallen accepteert. De functie moet alle even getallen filteren en de overgebleven getallen verdubbelen.

### technische analyse

1. Schrijf een functie genaamd `filterAndDouble` die een array van getallen accepteert.
2. Gebruik de filter-functie om alleen even getallen te behouden.
3. Gebruik de map-functie om de overgebleven getallen te verdubbelen.
4. Lees het resultaat uit in de console.

### voorbeeldinteractie
![voorbeeldinteractie](./voorbeeldinteractie-filteren-en-verdubbelen.avif)

## Oefening 8: reduce

### leerdoelen

* Gebruik van de de reduce functie op arrays.

### functionele analyse

Schrijf een JavaScript-functie genaamd `calculateTotalPrice` die een array van getallen accepteert. De functie moet alle getallen met elkaar optellen.

### technische analyse

1. Schrijf een functie genaamd `calculateTotalPrice` die een array van getallen accepteert.
2. Gebruik de reduce functie om alle getallen in de array met elkaar op te tellen
3. Lees het resultaat uit in de console.

![voorbeeldinteractie](./voorbeeldinteractie-reduce.avif)

## Oefening 9: minstens twee

* Schrijf een arrow functie `isOdd` die via de returnwaarde aangeeft of een getal oneven is.
* Schrijf een arrow functie `isEven` die via de returnwaarde aangeeft of een getal even is.
* Verzin twee andere functies die op deze manier zeggen of een getal een bepaalde eigenschap heeft.
* Schrijf een functie genaamd `atLeastTwo` die twee argumenten aanvaardt. Het eerste argument is een array van getallen en de tweede argument is een callbackfunctie.
* De functie `atLeastTwo` geeft true terug als en slechts als minstens twee elementen voldoen aan de meegegeven functie.

Bijvoorbeeld:

```
console.log(atLeastTwo([2,3,4,6,8], isOdd)); // false
console.log(atLeastTwo([2,3,4,5,6,8], isOdd)); // true
```

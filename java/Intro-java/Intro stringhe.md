In Java, le stringhe sono un tipo di dato non primitivo e sono rappresentate come oggetti della classe `String`. Le stringhe sono immutabili, il che significa che, una volta create, non possono essere modificate. Puoi creare una stringa in diversi modi.

Vediamo un pò di esempi per capire meglio:

1. **Dichiarazione e Inizializzazione:**
> [!info] Example
> ```java
>String hello = "Ciao, mondo!";

2. **Creazione utilizzando il costruttore:**
> [!info] Example
> ```java
>String name = new String("stefano");

3. **Concatenazione di stringhe:**
> [!info] Example
> ```java
>String fullName = "stefano" + " " + "grasso";

4. **Metodi della classe `String`:**
	La classe `String` fornisce molti metodi utili per lavorare con le stringhe. Ad esempio:
> [!info] Example
> ```java
> String name = "stefano"
> 
>String upperCase = name.toUpperCase(); // Restituisce "STEFANO"
>String upperCase = name.toLowerCase(); // Restituisce "stefano"
>
>int length = name.length(); // Ottieni la lunghezza della stringa
>
>char firstCharacter = name.charAt(0); // Restituisce 's'
>
>String stringPiece = name.substring(5); // Restituisce "no"
>
>String stringBetween = name.substring(2, 7); // Restituisce "efano"
>
>boolean containsEfa = str.contains("efa"); // Restituisce true

5. **Comparazione di stringhe:**
	Puoi confrontare stringhe utilizzando il metodo `equals`:
> [!info] Example
> ```java
>String word1 = "Hello";
>String word2 = "Hello";
>
>if(word1.equals(word2)) {
>	System.out.println("le stringhe sono uguali")
>}

## **Formattazione di stringhe**
String.format() è un metodo per formattare le stringhe.
Prende due parametri: il formato e il valore da formattare.
> [!info] Example
> ```java
>double value = 3.148023;
>String formatValue = String.format("%.2f", value);
>System.out.println(formatValue);
>// output 3,14

> [!info] Example
> ```java
>int number = 3;
>String leftPaddedNumber = String.format("%03d", number);
>System.out.println(leftPaddedNumber);
>// output 003

Ovviamente il numero sarà ora una stringa, se lo vogliamo
come intero ci basta fare:
> [!info] Example
> ```java
>double parsedValue = Double.parseDouble(formatValue);
>System.out.println(parsedValue);
>// output 3,14 come double



Bisogna ricordarsi che, poiché le stringhe sono immutabili, ogni operazione che sembra modificarle in realtà restituisce una nuova stringa invece di modificare quella esistente. Ad esempio:
> [!info] Example
> ```java
>String original = "Hello";
>String modified = original.concat(", world!");
>
>System.out.println(original); // Stampa "Hello"
>System.out.println(modified); // Stampa "Hello, world!"
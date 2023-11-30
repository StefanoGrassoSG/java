La classe `Integer` in Java è una classe wrapper che incapsula un valore di tipo primitivo `int` in un oggetto. Queste classi wrapper sono parte del framework delle classi di utilità (`java.lang`) e forniscono metodi utili per manipolare e lavorare con i tipi di dati primitivi come oggetti.

La classe `Integer` è solo una delle classi wrapper per i tipi primitivi in Java. Oltre a `Integer`, ci sono anche `Byte`, `Short`, `Long`, `Float`, `Double`, `Character`, e `Boolean`. Queste classi wrapper sono utili quando hai bisogno di trattare i tipi primitivi come oggetti, ad esempio quando li stai utilizzando in contesti che richiedono oggetti, come le collezioni Java.

Ecco alcune informazioni chiave sulla classe `Integer`:

1. **Creazione di un Oggetto `Integer`:**
	Puoi creare un oggetto `Integer` in diversi modi, ad esempio utilizzando il costruttore o il metodo statico `valueOf()`:
> [!info] Example
> ```java
> // Creazione di un oggetto Integer utilizzando il costruttore
> Integer number = new Integer(50);
> 
> // Creazione di un oggetto Integer utilizzando il metodo valueOf()
> Integer number2 = Integer.valueOf(50);

2. **Conversione tra `int` e `Integer`:**
	Puoi facilmente convertire tra `int` e `Integer`:
> [!info] Example
> ```java
> Integer number = Integer.valueOf(50);
> 
> // Converte Integer in int
> int numberConverted = number.intValue(); 
> 
>// Converte int in Integer
> Integer object = Integer.valueOf(numberConverted);

3. **Conversione  da Integer a stringa** 
> [!info] Example
> ```java
> Integer number = Integer.valueOf(50);
> 
> // Restituisce la rappresentazione testuale
> String str = number.toString();

4. **Costanti**
	La classe `Integer` definisce costanti come `MIN_VALUE` e `MAX_VALUE`, che rappresentano i valori minimi e massimi possibili per un intero in Java.
> [!info] Example
> ```java
> int minValue = Integer.MIN_VALUE; // -2147483648
> 
> int maxValue = Integer.MAX_VALUE; // 2147483647

5. **Auto conversione**
	Da ricordare che Java supporta l'auto(un)boxing, che è la conversione automatica tra tipi primitivi e i rispettivi wrapper. Ad esempio:
> [!info] Example
> ```java
> Integer wrapper = 42; // Autoboxing
> 
> int primitivo = wrapper; // Unboxing

6. **Metodi Statici di Utilità:**
	La classe `Integer` include anche metodi statici di utilità, come il parsing di stringhe:
> [!info] Example
> ```java
>String numberString = "123";
>
> //Restituisce 123 come intero
> int converted = Integer.parseInt(numberString);
  
In Java, un array è una struttura dati che consente di memorizzare più valori dello stesso tipo in una singola variabile. Gli array possono essere dichiarati per ogni tipo di dato, inclusi i tipi di dato **primitivi** e i tipi di oggetti.

Ecco un esempio di dichiarazione e inizializzazione di un array di interi dove sai già che cosa c'è dentro.

> [!info] Example
> ```java
> int[] arrayOfInteger = {1, 2, 3, 4, 5};
> ```

Puoi anche dichiarare un array specificando solo il tipo di dato e la dimensione e successivamente inizializzarlo:

> [!info] Example
> ```java
> int[] anotherArrayOfInteger = new int[3];
anotherArrayOfInteger[0] = 10;
anotherArrayOfInteger[1] = 20;
anotherArrayOfInteger[2] = 30;

Per gli array di tipi di dato primitivi, l'array è effettivamente un blocco di memoria che contiene i valori stessi. Per esempio, `arrayDiInteri` è un array di interi primitivi.

Puoi anche creare array di oggetti. Ad esempio, un array di stringhe:

> [!info] Example
> ```java
>String[] arrayOfString = {"uno", "due", "tre"};

Ricorda che gli indici degli array in Java iniziano da 0. Puoi accedere agli elementi di un array utilizzando l'indice:

> [!info] Example
> ```java
>int firstElement = arrayOfInteger[0]; // Restituisce 10
>String secondElement = arrayOfString[1]; // Restituisce "uno"

Ci sono diversi metodi utili per manipolare gli array in Java. Ecco alcuni dei metodi più comuni e ampiamente utilizzati dalla classe `Arrays` e dai metodi di array della classe `String`:

In Java, gli array sono oggetti e la loro dimensione è fissata al momento della creazione. Una volta che un array è stato creato, non è possibile modificare la sua dimensione. Questa caratteristica fa sì che gli array siano noti come strutture dati "a dimensione fissa".

Per effettuare modifiche agli array, spesso si utilizzano operazioni di copia. Ad esempio, per aggiungere un elemento a un array, potresti dover creare un nuovo array con una dimensione maggiore e copiare gli elementi esistenti insieme al nuovo elemento.

> [!info] Example
> ```java
>int[] originalArray = {1, 2, 3};
>int newLength = originalArray.length + 1;
>int[] newArray = new int[newLength];

> [!info] Example
> ```java
>int[] originalArray = {1, 2, 3};
>int[] newArray = new int[originalArray.length * 2];

Qua invece vediamo come modificare gli elementi dentro un array tramite indice.

> [!info] Example
> ```java
>int[] arr1 = { 1, 2, 3, 4, 5 };
>System.out.println(arr1[0]); // Restituisce 1
>arr1[0] = 100;
>System.out.println(arr1[0]); // Adesso restituisce 100
## Metodi della classe Arrays

1.  **Arrays.toString(array)**
	Restituisce una rappresentazione stringa dell'array.
> [!info] Example
> ```java
>int[] numbers = {1, 2, 3, 4, 5};
>String result = Arrays.toString(numbers); // Restituisce "[1, 2, 3, 4, 5]"

2. **Arrays.sort(array)**
	Ordina l'array in ordine naturale.
> [!info] Example
> ```java
>int[] numbers = {5, 3, 1, 4, 2};
>Arrays.sort(numbers); // Ora l'array è {1, 2, 3, 4, 5}

3. **Arrays.binarySearch(array, int)**
	 Cerca la chiave specificata nell'array ordinato utilizzando la ricerca binaria.
> [!info] Example
> ```java
>int[] numbers = {1, 2, 3, 4, 5};
>int position = Arrays.binarySearch(numbers, 3); // Restituisce 2 (posizione dell'elemento 3)

4. **Arrays.equals(array1, array2)**
	Verifica se due array sono uguali.
> [!info] Example
> ```java
>int[] array1 = {1, 2, 3};
>int[] array2 = {1, 2, 3};
>boolean areSame = Arrays.equals(array1, array2); // Restituisce true
## Metodi della classe String

1. **str.toCharArray()**
	Converte una stringa in un array di caratteri.
> [!info] Example
> ```java
>String str = "Hello";
>char[] characters = str.toCharArray(); // Restituisce {'H', 'e', 'l', 'l', 'o'}

2. **str.split()**
	Suddivide la stringa in un array di stringhe in base a un'espressione regolare.
> [!info] Example
> ```java
>String str = "Questo è un esempio";
>String[] words = str.split(" "); // Restituisce {"Questo", "è", "un", "esempio"}
Le istruzioni **condizionali** eseguono un certo blocco di codice **se si verifica una ben precisa condizione.**

> [!info] Example
> ```java
>if(condizione) {
>	//istruzione se la condizione si verifica
>} else  {
>	//istruzione se non si verifica
>}

Possiamo ovvviamente aggiungere più **condizioni**.

> [!info] Example
> ```java
>if(condizione) {
>	//istruzione se la condizione si verifica
>} else if (altra condizione)  {
>	//istruzione se l'altra condizione si verifica
>} else {
>	//istruzione se non si verifica ne l'una ne l'altra
>}

# Operatori relazionali

> [!info] Example
>
> | Operatore | Condizione | Risultato |
> |---|---|---|
> | == uguaglianza | Se x = 3, allora | x == 4 è falso |
> | != diversità         | Se x = 3, allora | x != 4 è vero  |
> | > maggiore di    | Se x = 3, allora | x > 4 è falso   |
> | < minore di        | Se x = 3, allora | x < 4 è vero   |
> | >= maggiore o uguale    | Se x = 3, allora | x >= 4 è falso  |
> | <= minore o uguale     | Se x = 3, allora | x <= 4 è vero  |

# Operatori logici

Possiamo ovviamente unire più condizioni con l'operatore AND
Ad esempio:
> [!info] Example
> ```java
>if(condizione && altra condizione) {
>	//istruzione se entrambe le condizioni si verificano
>} else {
>	//istruzione se non si verificano
>}

> [!info] Example
> ```java
>if(x == 3) && (y == 4) {
>	//istruzione se entrambe le condizioni si verificano
>} else {
>	//istruzione se non si verificano
>}

Altro esempio con operatore OR che restituisce vero se almeno
uno degli operandi è vero.
Ad esempio:
> [!info] Example
> ```java
>if(condizione || altra condizione) {
>	//istruzione se o una o l'altra  condizione si verifica
>} else {
>	//istruzione se non si verifica nessuna delle due
>}

> [!info] Example
> ```java
>if(x ==3) || (y == 4)) {
>	//istruzione se o una o l'altra  condizione si verifica
>} else {
>	//istruzione se non si verifica nessuna delle due
>}

# Operatori logici - NOT

La negazione ci da uno strumento per rendere più espressivo il nostro codice, e quindi non essere vincolati ad un singolo modo di porre un concetto.
Come in qualsiasi lingua parlata, è necessario anche in Java in quanto linguaggio di programmazione.

Ad esempio:
> [!info] Example
> ```java
>//Dichiarazione variabile booleana 
>boolean loggedInUser = false;
>if(loggedInUser) {
>	//Questo blocco non verrà eseguito perchè false == false
>}
>
>if(!loggedInUser) {
>	//Questo blocco verrà eseguito perchè !false == true
>}

# Switch...Case

Hai tanti if? Forse potresti usare uno Switch

> [!info] Example
> ```java
>switch (fruits) {
>
>case "banana":
>	text = "banana is good!";
>	break; 
>	
>case	"orange":
>	text = "I am not a fan of orange.";
>	break;
>	
>default:
>	text = "I have never heard of that fruit.";	
>}

Vediamo un esempio da **if** a **switch**:

> [!info] Example
> ```java
>public String exampleOfIf(String animal) {
String result;
if (animal.equals("DOG") || animal.equals("CAT")) {
result = "domestic animal";
} else if (animal.equals("TIGER")) {
result = "wild animal";
} else {
result = "unknown animal";
}
return result;

> [!info] Example
> ```java
>public String exampleOfSwitch(String animal) {
String result;
switch (animal) {
case "DOG":
result = "domestic animal";
break;
case "CAT":
result = "domestic animal";
break;
case "TIGER":
result = "wild animal";
break;
default:
result = "unknown animal";
break;
}
return result;
}

Non possiamo confrontare tutti i tipi di oggetti e di primitivi con uno switch.
Uno switch funziona solo con quattro primitivi e i loro e con il tipo e la
classe String:

1. byte e Byte
2. short e Short
3. int e Integer
4. char e Character
5. enum
6. String

Le variabili in Java sono definite attraverso
il **tipo** di variabile seguita dal **nome** della variabile.

> [!info] Example
> ```java
>int myNumber = 4;

I nomi delle variabili devono rispettare precisi criteri:

1. devono cominciare sempre con una lettera (o con
	l'underscore), mai con un numero
2. In generale non devono essere presenti caratteri
	diversi da lettere o numeri o underscore
3. I nomi devono essere diversi dalle **keyword** riservate 
	 di java.
4. I nomi devono essere univoci all'interno dello
	**scope**

> [!info] Example
> ```java
> // questo non si può fare
>int myVariable
>boolean myVariable
>
>// questo si può fare perchè sono due scope diversi
>{
>	int myVariable
>}
>{
>	boolean myVariable
>}

Possiamo ovviamente dichiarare una variabile 
e assegnarli un valore inziale per poi cambiarlo
successivamente.

> [!info] Example
> ```java
> int myNumber = 5;
> myNumber = 4;

Stessa cosa dichiarandola vuota.

> [!info] Example
> ```java
> int myNumber;
> myNumber = 4;

In Java, le costanti vengono spesso dichiarate utilizzando la parola chiave `final`. Le costanti sono variabili il cui valore non può essere modificato una volta assegnato. Di solito, le costanti sono dichiarate come variabili statiche (static) e final per rappresentare valori che non devono cambiare durante l'esecuzione del programma.
La convenzione di stile per le costanti in Java è utilizzare il formato "SCREAMING_SNAKE_CASE" (tutte le lettere maiuscole separate da underscore).

> [!info] Example
> ```java
>public static final int VALUE = 100;
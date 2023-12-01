Per eseguire più volte lo stesso blocco di codice si usano le **istruzioni di iterazione**, dette
anche semplicemente "cicli".
In java esistono diversi tipi di cicli:
1. for
2. while
3. do while

## Ciclo for

La sintassi del ciclo for è la seguente:

> [!info] Example
> ```java
> for (int x = 0; x < number; x++) {
> 	//Istruzioni da eseguire 
> }

## Array + cicli

Un normale uso dei cicli con gli array è ad esempio stampare
ogni elemento ad ogni interazione, ad esempio:

> [!info] Example
> ```java
> String[] names = {"alessando", "francesco", "stefano", "luca", "marco"}
> for(int x = 0; x < names.length;x++) {
> 	System.out.println(names[x]);
> }
> //Questo restituisce:
> //"alessandro"
> //"francesco"
> //"stefano"
> //"luca"
> //"marco"

Possiamo anche iterare sui singoli caratteri di una stringa
usando il ciclo for e il metodo **charAt[x]**, ad esempio:

> [!info] Example
> ```java
> String names = "stefano";
> for(int x = 0; x < names.length();x++) {
> 	System.out.println(name.charAt[x]);
> }
> //Questo restituisce:
> //"s"
> //"t"
> //"e"
> //"f"
> //"a"
> //"n"
> //"o"

## Ciclo while

Se non sappiamo quante volte deve ripetersi il nostro ciclo, possiamo utilizzare un **while**, ad esempio:

> [!info] Example
> ```java
> while(condizione) {
> 	//codice da eseguire
> 	
> 	//istruzioni per terminare il ciclo
> }

> [!info] Example
> ```java
> String name = "stefano";
> int x = 0;
> while(x<name.lenght()) {
> 	//codice da eseguire
> 	
> 	x++
> }
## Ciclo while vs ciclo for

Il ciclo **for** è pratico per eseguire cicli a  conteggio, perché permette di indicare in modo compatto **contatore**, **condizione** ed **incremento**.

Il ciclo **while** è pratico per eseguire cicli la cui condizione non dipende per forza da un contatore.

## Ciclo do-while

Il ciclo **do-while** è molto simile al ciclo while.
La differenza sostanziale è che il ciclo while può anche non essere mai eseguito se la condizione risulta falsa fin dall'inizio.

Il ciclo do-while viene sempre eseguito almeno una volta anche se la condizione risulta falsa fin dall'inizio.
Questo perché la condizione viene verificata solo dopo che il blocco di codice è già stato eseguito.

> [!info] Example
> ```java
> do {
> 	//Codice da eseguire
> 	
> 	//Istruzioni per terminare il ciclo
> } while (condizione);

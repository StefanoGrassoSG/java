Raccolta di vari esempi in ordine sparso di applicazioni sulle basi di java.

In questo esempio vediamo come continuare ad aggiungere valori random
ad una somma finchè tale somma è minore di 100.
Alla fine stampiamo la somma.
> [!info] Example
> ```java
> Random random = new Random();
>int sum = 0;
>while(sum < 100) {
>	int value = random.nextInt(10);
>	sum += value;
>	
>	System.out.println("value " + value);
>	System.out.println("partial sum: " + sum);
>}
>System.out.println("final sum: " + sum)

Vediamo qui come dare alla macchina due parole e farci dire qual'è
la più lunga:

> [!info] Example
> ```java
> import java.util.Scanner;
> 
> Scanner in = new Scanner(System.in);
> 
> System.out.println("Parola 1: ");
> String word1 = in.nextLine();
> int  lng1 = word1.length();
> 
> System.out.println("Parola 2: ");
> String word2 = in.nextLine();
> int lng2 = word2.length();
> 
> in.close();
> 
> if(lng1 == lng2) System.out.println("hanno la stessa lunghezza");
> 
> else if(lng1 > lng2) System.out.println("la parola più lunga è " + word1);
> 
> else  System.out.println("la parola più lunga è " + word2);

Vediamo il classico valore minimo, massimo e media di un array:

> [!info] Example
> ```java
> final int VALUE_COUNT = 10;
> 
> Random random = new Random(100);
> //Generiamo array di 10 elementi con numeri casuali da 1 a 100
> int[] values = new int[VALUE_COUNT];
> for(int x = 0; x < values.length;x++) {
> 	values[x] = random.nextInt(1, 100);
> 	System.out.println("value: " + values[x]);
> }
> //Troviamo il valore massimo
> int max = Integer.MIN_VALUE;
> for(int x = 0;x < values.length;x++) {
> 	if(values[x] > max) {
> 		max = values[x];
> 	}
> }
> System.out.println("Il valore più alto è: " + max);
> 
> //Troviamo il valore minimo
> int min = Integer.MAX_VALUE;
> for(int x = 0;x < values.length;x++) {
> 	if(values[x] < min) {
> 		min = values[x];
> 	}
> }
> System.out.println("Il valore più basso è: " + min);
> 
> //Troviamo il valore della media
> int avg = 0;
> for(int x = 0; x<values.length;x++) {
> 	avg += values[x];
> }
> avg /= values.length;
> System.out.println("La media è: " + avg);

Vediamo come controllare se una stringa è presente in un array:

> [!info] Example
> ```java
> String[] names = {"stefano", "giovanni", "alessandro", "francesco"};
> 
> Scanner in = new Scanner(System.in);
> System.out.println("Dimmi il tuo nome:");
> String name = in.nextLine();
> l
> for(int x = 0;x < names.length;x++) {
> 	if(name.equals(names[x])) {
> 		System.out.println("Puoi entrare");
> 		break; //Utilizziamo break per stoppare il ciclo
> 	} 
> 	else { // else non obbligatorio
> 		System.out.println("non puoi entrare");
> 	}
> }
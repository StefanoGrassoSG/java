Per interagire con un programma Java tramite l'input dell'utente, si può utilizzare la classe `Scanner` della libreria Java `java.util`. La classe `Scanner` permette di leggere input da diverse fonti, come l'input standard (`System.in`) o una stringa.

La classe Scanner si trova nella JRE System Library,
insieme a centinaia di altre classi che JDK ci mette a
disposizione per programmare

Ecco un esempio semplice di come si può utilizzare `Scanner` per leggere l'input dell'utente:

> [!info] Example
> ```java
> //Importazione libreria
> import java.util.Scanner;
> 
> // Creazione di un oggetto Scanner per leggere l'input dell'utente
> Scanner scanner = new Scanner(System.in);
> 
> // Chiedi all'utente di inserire un nome
> System.out.print("Inserisci il tuo nome: ");
> String name = scanner.nextLine();
> 
> // Chiedi all'utente di inserire un numero intero
> System.out.print("Inserisci un numero intero: ");
> int number = scanner.nextInt();
> 
> // Stampa l'input dell'utente
> System.out.println("Ciao, " + name + "! Hai inserito il numero " + number);
> 
> // Chiudi lo scanner per evitare leak di risorse
> scanner.close();

Possiamo anche convertire un numero stringa come "5" 
tramite il metodo della classe Integer(vedi file classe Integer).

> [!info] Example
> ```java
> //Importazione libreria
> import java.util.Scanner;
> 
> Scanner in = new Scanner(System.in);
> 
>System.out.print("Eta' persona 1: ");
>String strAge1 = in.nextLine();
>int intAge1 = Integer.valueOf(strAge1);
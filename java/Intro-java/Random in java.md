Può essere utile avere un numero **random**, cioè generato dal computer in modo casuale.
La classe java.util.Random ha un metodo nextInt(int max) che genera un numero casuale compreso tra 0 (compreso) e max (escluso).

> [!info] Example
> ```java
>import java.util.Random
>
>Random random = new Random();
>
>// Generazione di un numero casuale compreso tra 0 (incluso) e 10 (escluso)
>int randomNumber = r.nextInt(10);
>
>// Generazione di un numero casuale intero compreso tra 0 (incluso) e 1 (escluso)
>double randomDouble = random.nextDouble();
>
>// Generazione di un numero casuale compreso tra un valore minimo e massimo specificato
>int randomBetween = random.nextInt(15 - 5 + 1) + 5;
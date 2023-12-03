Le interfacce in Java sono un altro concetto fondamentale della programmazione orientata agli oggetti (OOP) che permette di definire contratti comuni per le classi. Un'interfaccia è una collezione di metodi astratti, costanti e, a partire da Java 8, metodi di default e statici. Le classi che implementano un'interfaccia devono fornire implementazioni concrete per tutti i metodi dichiarati dall'interfaccia. Ecco un esempio:
> [!info] Example
> ```java
>interface Vehicle {
>	void accelerate();
>	void brake();
>	
>	default void turnOff() {
>		System.out.println("Spegnimento del veicolo");
>	}
>}

> [!info] Example
> ```java
>class Car implements Vehicle {
>	@Override
>	public void accelerate() {
>		System.out.println("Auto in accelerazione");
>	}
>	@Override
>	public void brake() {
>		System.out.println("Auto in frenata")
>	}
>}

> [!info] Example
> ```java
>class Motorcycle implements Vehicle {
>	@Override
>	public void accelerate() {
>		System.out.println("Moto in accelerazione");
>	}
>	@Override
>	public void brake() {
>		System.out.println("Moto in frenata")
>	}
>}

> [!info] Example
> ```java
>public class Test {
>	public static void main(String[] args) {
>		Car car = new Car();
>		Motorcycle moto = new Motorcycle();
>		
>		car.accelerate();
>		car.brake();
>		car.turnOff();//Metodo di default
>		
>		moto.accelerate();
>		moto.brake();
>		moto.turnOff();//Metodo di default;
>	}
>}

In questo esempio, `Vehicle` è un'interfaccia che dichiara due metodi astratti (`accelerate` e `brake`) e un metodo di default (`turnOff`). La classe `Car` e la classe `Motorcycle` implementano l'interfaccia `Vehicle` fornendo le rispettive implementazioni dei metodi astratti. Entrambe le classi ereditano anche il metodo di default `turnOff` dall'interfaccia.

Le interfacce sono utili quando si desidera definire comportamenti comuni che possono essere condivisi da diverse classi senza dover utilizzare l'ereditarietà multipla. Inoltre, consentono di creare un contratto comune che le classi devono rispettare.
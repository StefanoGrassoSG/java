Le classi astratte sono un concetto fondamentale nella programmazione orientata agli oggetti (OOP) e vengono utilizzate in Java per creare classi che non possono essere istanziate direttamente. Una classe astratta può contenere metodi astratti (senza implementazione) che devono essere implementati dalle classi figlie concrete. Ecco come dichiarare e utilizzare classi astratte in Java:
> [!info] Example
> ```java
>abstract class Shape {
>	private String color;
>	
>	public Shape(String color) {
>		setColor(color);
>	}
>	
>	public String getColor() {
>		return color;
>	}
>	public void setColor(String color) {
>		this.color = color;
>	}
>	
>	//Metodo astratto per classi figlie
>	public abstract double areaCalc();
>}

> [!info] Example
> ```java
>public class Circle extends Shape {
>	private double radius;
>	
>	public Shape(String color, double radius) {
>		super(color);
>		setRadius(radius);
>	}
>	
>	public String getRadius() {
>		return radius;
>	}
>	public void setRadius(double radius) {
>		this.radius = radius;
>	}
>	
>	//Implementazione metodo astratto
>	public abstract double areaCalc() {
>		return Math.PI * radius * radius;
>	}
>}

In questo esempio, `Shape` è una classe astratta con un metodo astratto `areaCalc()`. La classe concreta `Circle` estende la classe `Shape` e fornisce l'implementazione concreta del metodo astratto. Si noti che non è possibile istanziare direttamente un'istanza di `Shape`, ma è possibile creare oggetti delle classi figlie concrete.

Le classi astratte sono utili quando si vuole fornire un'implementazione di base comune per un gruppo di classi e richiedere alle classi figlie di fornire implementazioni specifiche.
  
Le eccezioni in Java sono eventi anomali o errori che si verificano durante l'esecuzione del programma e interrompono il flusso normale di esecuzione. Le eccezioni sono gestite mediante il sistema di gestione delle eccezioni di Java, che consente di catturare, gestire e/o lanciare eccezioni. Le eccezioni sono divise in due categorie principali: eccezioni controllate e eccezioni non controllate.

1. **Eccezioni Controllate (Checked Exceptions):** Le eccezioni controllate sono sottoclassi di `Exception`, ma non derivano da `RuntimeException`. Queste eccezioni devono essere dichiarate nel metodo o gestite attraverso un blocco `try-catch` altrimenti il codice non verrà compilato. Ecco un esempio:
> [!info] Example
> ```java
>public class exHandler {
>	public static void main(String[] args) {
>		try {
>			read("file.txt");
>		} catch (I0Exception e) {
>			System.out.println("errore di I/0: " + e.getMessage());
>		}
>	}
>}
>
>public stati void read(String fileName) throws I0Exception {
>	FileReader fileReader = new FileReader(fileName);
>	//Operazioni lettura dal file
>	fileReader.close();
>}

Nell'esempio sopra, il metodo `read` può generare un'eccezione di tipo `IOException`, quindi la firma del metodo dichiara che può lanciare questa eccezione. Nel metodo `main`, chiamiamo `read` e gestiamo l'eccezione usando un blocco `try-catch`.

2. **Eccezioni Non Controllate (Unchecked Exceptions):** Le eccezioni non controllate sono sottoclassi di `RuntimeException`. A differenza delle eccezioni controllate, non è obbligatorio dichiarare queste eccezioni o gestirle con un blocco `try-catch`. Ecco un esempio:
> [!info] Example
> ```java
>public class exHandlerUnchecked {
>	public static void main(String[] args) {
>		divide(10, 0); //Genera eccezione aritmetica
>	}
>}
>
>public stati void divide(int a,  int b)  {
>	int result = a / b;
>	System.out.println("Risultato: " + result);
>}

Nell'esempio sopra, il metodo `divide` potrebbe generare un'eccezione di tipo `ArithmeticException` se il denominatore è zero. Poiché questa è un'eccezione non controllata, non è necessario dichiararla o gestirla esplicitamente.

Vediamo come usarle anche in un ipotetico setter di una classe:
> [!info] Example
> ```java
>public class Book {
>	String title;
>	
>	public Book(String title) throws Exception {
>		setTitle(String);
>	}
>	
>	public void setTitle(String title)  throws Exception {
>		if (title == null || title.isEmpty())
>			throw new TitleException();
>		this.title = title;
>	}
>}

In questo esempio vediamo come possiamo controllare se il title è null
oppure se è stringa vuota e in quel caso chiamare una nuova 
TitleException(); che può essere una classe personalizzata tipo questa:
> [!info] Example
> ```java
>public class TitleException extends Exception {
>	private static final long serialVersionUID = 1L;
>	
>	public TitleException(String message) {
>		super(message);
>	}
>	
>	public TitleException() {
>		super("Errore nel titolo del libro");
>	}
>}

In questa classe che abbiamo creato abbiamo due costruttori,
uno per chiamare la classe con messaggio personalizzato come 
argomento, e uno per chiamarla senza argomenti, in quel caso utilizzerà
il messaggio predefinito che abbiamo scritto nel costruttore.

In generale, è buona pratica gestire le eccezioni in modo appropriato per garantire un comportamento prevedibile del programma. L'utilizzo corretto delle eccezioni contribuisce a scrivere codice robusto e a gestire situazioni anomale in modo elegante.
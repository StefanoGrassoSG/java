  
Il Java Collections Framework fornisce un insieme di interfacce e classi in Java per rappresentare e manipolare raccolte di oggetti. È progettato per offrire una soluzione unificata e coesa per la manipolazione e la gestione di dati in forma di collezioni. Le principali interfacce del framework sono:

1. **List:**
	Implementato da classi come `ArrayList`, `LinkedList`, e `Vector`.
	 Rappresenta una sequenza ordinata di elementi in cui è possibile accedere a elementi specifici tramite un indice.
> [!info] Example
> ```java
>List<"String"> myList = new ArrayList<>();
>myList.add("elemento 1");
>myList.add("elemento2");
>myList.add("elemento 3");
>
>System.out.println("ArrayList: ");
>for(String element : myList) {
>	System.out.println(element);
>}
>
>Set<"String"> mySet = new HashSet<>();
>mySet.add("elemento 1");
>mySet.add("elemento 1");
>mySet.add("elemento 2");
>mySet.add("elemento 2");
>mySet.add("elemento 3");
>mySet.add("elemento 3");
>
>System.out.println("HashSet: ");
>for(String element : mySet) {
>	System.out.println(element);
>}

In questo esempio, `ArrayList` e `HashSet` sono entrambe implementazioni della rispettiva interfaccia (`List` e `Set`).
Da notare come il Set non può avere due elementi uguali quindi stamperà
comunque "elemento 1" - "elemento 2" - "elemento 3".

2. **Map:**
	Implementato da classi come `HashMap`, `LinkedHashMap`, e `TreeMap`.
	Rappresenta una struttura di dati chiave-valore, in cui ogni elemento è associato a una chiave univoca.
> [!info] Example
> ```java
>Map<"String", integer> map = new HashMap<>();
>map.put("uno", 1);
>map.put("due", 2);
>map.put("tre", 3);
>
>System.out.println("Valore associato a 'Uno': " + mappa.get("Uno"));
>
>for (Map.Entry<String, Integer> entry : map.entrySet()) {
>	System.out.println("Chiave: " + entry.getKey() + ", Valore: " + entry.getValue());
>}

In questo esempio, una `HashMap` viene utilizzata per memorizzare coppie chiave-valore. Puoi accedere agli elementi della mappa utilizzando il metodo `get(key)` fornendo la chiave. Puoi anche iterare sulla mappa utilizzando un ciclo `for` su `entrySet()`, che restituisce un set di coppie chiave-valore.

## Iterator

L'interfaccia Collection(e qundi le sue discendenti Set e List) hanno un 
metodo iterator() che restituisce un elemento dell'interfaccia 
iterator<"Type">.
Un iterator ci permette di iterare, cioè di scorrere gli elementi di una 
Collection.
Anche in questo caso usiamo <"Type"> per dire quale tipo ci aspettiamo.
> [!info] Example
> ```java
>List<"String"> list = new ArrayList<>(),
>list.add("elemento 1");
>list.add("elemento 2");
>list.add("elemento 3");
>list.add("elemento 4");
>
>Iterator<"String"> iterator = list.iterator();
>while(iterator.hasNext()) {
>	String current = iterator.next();
>	System.out.println(current);
>}

In generale, l'utilizzo di un iteratore è spesso preferito per la sua sicurezza e flessibilità, ma ci possono essere casi in cui un semplice ciclo for o while può essere più appropriato, specialmente quando non è necessario il supporto alla rimozione sicura o quando si deve lavorare con un'operazione specifica basata sugli indici.

Iterare sulle map:
> [!info] Example
> ```java
>HashMap<"String", integer> map = new HashMap<>(),
>map.put("elemento 1", 1);
>map.put("elemento 2", 2);
>map.put("elemento 3", 3);
>map.put("elemento 4", 4);
>
>Iterator<"String"> iterator = map.iterator();
>while(iterator.hasNext()) {
>	String key = iterator.next();
>	System.out.println("chiave: " + key);
>	int value = map.get(key);
>	System.out.println("valore: " + value)
>}
## Java generics

Un contenitore può contenere oggetti di un solo tipo.
Quando dichiariamo un contenitore specifichiamo il tipo con la sinstassi
<"type"> (senza apici)

## Array <-> Collection

**Arrays.asList(array)**: prende in ingresso un array e restituisce una List
con gli stessi elementi.
**List.toArray(array**: prende un array in ingresso e lo "riempie" con tutti 
gli elementi della List.
> [!info] Example
> ```java
>String[] array1 = {"a", "b", "c"};
>List<"String"> list = Arrays.asList(array);
>
>String[] array2 = new String[list.size()];
>list.toArray(array2),

I contenitori del Java Collection Framework non possono contenere
tipi di dato primitivi ma solo oggetti

## Classi wrapper

Per fortuna java ci mette a disposizione delle classi wrapper, una per
ogni tipo primitivo.
> [!info] Example
> ```java
>int x = 5;
>Integer wrapX = x;
>
>double a = 5.5;
>Double wrapA = a;
>
>char c = 'a',
>Character cWrapper = c;

## Super ciclo for

Una sinstassi compatta del classico ciclo for ci permette di iterare su
ogni elemento di una collezione senza usare un indice.
La struttura è quella del ciclo for.
> [!info] Example
> ```java
>for(String element : collection) {
>	System.out.println(element);
>}
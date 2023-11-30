
## Tipi di primitivi <span style="color: yellow;font-weight:bold;">interi</span>

1. **byte:**
    - Dimensione: 1 byte
    - Range: -128 a 127
2. **short:**
    - Dimensione: 2 byte
    - Range: -32,768 a 32,767
3. **int:**
    - Dimensione: 4 byte
    - Range: -2,147,483,648 a 2,147,483,647
4. **long:**
    - Dimensione: 8 byte
    - Range: -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807

> [!info] Example
> ```java
> boolean booleanValue = true;
> byte oneByte = 10;
> short twoByte = 30000
> int fourByte = 50_000_000;
> long eightByte = 100_000_000_000L;
> ```

## Tipi di primitivi <span style="color: yellow;font-weight:bold;">decimali</span>

1. **float:**
    - Dimensione: 4 byte
    - Range approssimato: ±3.40282347 x 10^38 con circa 7 cifre decimali di precisione
2. **double:**
    - Dimensione: 8 byte
    - Range approssimato: ±1.7976931348623157 x 10^308 con circa 15 cifre decimali di precisione

> [!info] Example
> ```java
> float fourByte = 10.3F;
> double eightByte = 10.33333;
> ```

Ogni tipo di dato primitivo ha una dimensione specifica in byte e un range di valori che può rappresentare. La scelta del tipo di dato dipende dai requisiti specifici del tuo programma, incluso il range di valori attesi e la precisione necessaria.
## Tipi di primitivi <span style="color: yellow;font-weight:bold;">caratteri</span>

Il tipo di dato primitivo `char` in Java rappresenta un singolo carattere Unicode.
> [!info] Example
> ```java
> char character = 'A';
> ```

Puoi anche rappresentare i caratteri utilizzando il formato Unicode preceduto da `\u`.

> [!info] Example
> ```java
> char anotherCharacter = '\u005A';
> ```
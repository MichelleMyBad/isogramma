# isogramma
## Descrizione esecizio
#### Esercizio C# in console che controlla che la stringa fornita dall'utente sia un isogramma (senza lettere ripetute)

## Descizione soluzione utilizzata
<details>
<summary>Creazione della funzione</summary>

```c#
public static bool Verifica(string word)
{
```
Per prima cosa andiamo a creare la funzione che si occuperà di controllare che la stringa sia o meno un isogramma, dandole la stringa come parametro.
</details>

<details>
<summary>Scorrimento della stringa</summary>

```c#
for(int i=0;i<word.Length-1;i++)
{
```
Questo for si occuperà si scorrere la stringa, dovrà proseguire finchè <b><i>i</i></b> sarà minore di <b><i>word.Length</i></b>-1 in quanto successivamente andremo a confrontare ogni carattere con tutti gli altri.
</details>

<details>
<summary>Confronto con tutti i caratteri</summary>

```c#
for(int j=i+1;j<word.Length;j++){
    if(Char.IsLetter(word[i])&& Char.ToLower(word[i])== Char.ToLower(word[j])){
    return false;
        }
    }
}
return true;
```
Creiamo poi un <i>for</i> che si occupi di scorrere tutti i caratteri (dopo quello corrente) per assicurarsi che siano diversi. Tramite <i>if</i> controlliamo se il carattere corrente è una lettera e se è uguale ad uno deglia altri caratteri, in caso queste due condizioni si verifichino, vuol dire che sono stati trovati due caratteri uguali e che quindi la stringa non è un isogramma, per questo motivo ritorniamo <i>false</i> al programma; in caso invece questa condizione non si verifichi mai la funzione volge al termine, ritornando poi <i>true</i> al programma. 
</details>


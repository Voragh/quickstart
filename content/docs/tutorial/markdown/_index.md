---
weight: 201
title: "Markdown"
---

# Guida Completa al Markdown

{{< buymecoffee>}}

Markdown è un linguaggio di markup leggero che permette di formattare testo semplice in modo semplice ed intuitivo.  
Viene ampiamente utilizzato su piattaforme come GitHub, Reddit e nei file README.  

## Testo

### Grassetto
Per rendere il testo in grassetto, racchiudilo tra due coppie di asterischi (`**`) o trattini bassi (`__`).

```markdown
**Questo testo è in grassetto**
__Anche questo testo è in grassetto__
```

**Questo testo è in grassetto**  
__Anche questo testo è in grassetto__

### Corsivo
Per il testo in corsivo, usa una singola coppia di asterischi (`*`) o trattini bassi (`_`).

```markdown
*Questo testo è in corsivo*
_Anche questo testo è in corsivo_
```

*Questo testo è in corsivo*  
_Anche questo testo è in corsivo_

### Barrato
Per il testo barrato, racchiudilo tra due coppie di tilde (`~~`).

```markdown
~~Questo testo è barrato~~
```

~~Questo testo è barrato~~

## Titoli
Per creare titoli, utilizza il carattere cancelletto (`#`). La quantità di cancelletti determina il livello del titolo.

```markdown
# Titolo 1
## Titolo 2
### Titolo 3
#### Titolo 4
##### Titolo 5
###### Titolo 6
```

# Titolo 1
## Titolo 2
### Titolo 3
#### Titolo 4
##### Titolo 5
###### Titolo 6

## Liste

### Liste Non Ordinate
Usa asterischi (`*`), segni più (`+`) o trattini (`-`) per creare liste non ordinate.

```markdown
* Elemento 1
* Elemento 2
    * Sottoelemento 2.1
    * Sottoelemento 2.2
+ Elemento 3
- Elemento 4
```

* Elemento 1
* Elemento 2
    * Sottoelemento 2.1
    * Sottoelemento 2.2
+ Elemento 3
- Elemento 4

### Liste Ordinate
Per le liste ordinate, utilizza i numeri seguiti da un punto (`1.`).

```markdown
1. Primo elemento
2. Secondo elemento
    1. Sottoelemento 2.1
    2. Sottoelemento 2.2
3. Terzo elemento
```

1. Primo elemento
2. Secondo elemento
    1. Sottoelemento 2.1
    2. Sottoelemento 2.2
3. Terzo elemento

### Liste Annidate
Puoi creare liste annidate indentando gli elementi con quattro spazi o un tab.

```markdown
1. Primo elemento
2. Secondo elemento
    * Sottoelemento 2.1
    * Sottoelemento 2.2
```

1. Primo elemento
2. Secondo elemento
    * Sottoelemento 2.1
    * Sottoelemento 2.2

## Link
Per creare un link, usa la seguente sintassi:

```markdown
[Nome del link](URL)
```

```markdown
[Google](https://www.google.com)
```

[Google](https://www.google.com)

## Immagini
Per aggiungere un'immagine, usa un punto esclamativo (`!`) seguito dal testo alternativo racchiuso tra parentesi quadre e l'URL dell'immagine tra parentesi tonde.

```markdown
![Testo Alternativo](URL)
```

```markdown
![Esempio di Immagine](https://www.example.com/immagine.png)
```

![Esempio di Immagine](https://www.example.com/immagine.png)

## Codice

### Inline
Per inserire codice inline, racchiudilo tra backtick (`).

```markdown
Utilizza il comando `npm install` per installare i pacchetti.
```

Utilizza il comando `npm install` per installare i pacchetti.

### Blocco di Codice
Per blocchi di codice, usa tre backtick (```) prima e dopo il codice. Puoi anche specificare il linguaggio per evidenziazione della sintassi.

```markdown
\```
function esempio() {
    console.log("Ciao, mondo!");
}
\```
```

```javascript
function esempio() {
    console.log("Ciao, mondo!");
}
```

## Citazioni
Per creare una citazione, usa il simbolo di maggiore (`>`).

```markdown
> Questo è un testo citato.
```

> Questo è un testo citato.

## Tabelle
Per creare tabelle, utilizza trattini (`-`) per la riga di intestazione e pipe (`|`) per separare le colonne.

```markdown
| Intestazione 1 | Intestazione 2 |
| -------------- | -------------- |
| Riga 1 Colonna 1 | Riga 1 Colonna 2 |
| Riga 2 Colonna 1 | Riga 2 Colonna 2 |
```

| Intestazione 1 | Intestazione 2 |
| -------------- | -------------- |
| Riga 1 Colonna 1 | Riga 1 Colonna 2 |
| Riga 2 Colonna 1 | Riga 2 Colonna 2 |

## Linea Orizzontale
Per creare una linea orizzontale, usa tre o più asterischi (`***`), trattini (`---`) o underscore (`___`).

```markdown
***
---
___
```

---

## Checklist
Per creare una checklist, usa trattini seguiti da parentesi quadre. Puoi inserire una `x` per indicare un elemento completato.

```markdown
- [ ] Da fare
- [x] Fatto
```

- [ ] Da fare
- [x] Fatto


{{< buymecoffee>}}
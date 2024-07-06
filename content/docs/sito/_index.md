---
weight: 1
bookFlatSection: true
title: "Passo 1: Sito Internet"
---

# Sito Internet

{{< buymecoffee>}}

## Introduzione

Dopo un'attenta analisi sono arrivato alla conclusione di sviluppare un sito web che mi consente di raggruppare tutte le mie conoscenze.  
Di seguito spiegherò passo passo come ho sviluppato questo sito, i passaggi e le alternative.  

## Analisi

L'analisi effettuata per scegliere come effettuare il sito è ricaduta su due alternative: WordPress e Hugo, due popolari piattaforme di gestione e generazione di siti web.  


- **Tipo di piattaforma**: WordPress è un CMS (Content Management System, ossia sistema di gestione dei contenuti) che permette una gestione dei contenuti dinamica e interattiva, mentre Hugo è un generatore di siti statici che produce pagine statiche pre-renderizzate.  
  
- **Linguaggio di programmazione**: WordPress è sviluppato in PHP e richiede un ambiente server per funzionare. Hugo è scritto in Go e genera siti che consistono esclusivamente in file statici.  

- **Installazione**: WordPress necessita di un server web, PHP e un database MySQL per funzionare. Hugo, al contrario, non richiede un database, rendendo l'installazione e la configurazione più semplici e veloci.  

- **Gestione dei contenuti**: WordPress permette una gestione dei contenuti dinamica tramite una interfaccia web user-friendly. Hugo utilizza file Markdown per i contenuti, che vengono trasformati in pagine statiche.  

- **Performance**: Hugo offre performance superiori grazie alla generazione di file statici, che possono essere serviti molto rapidamente rispetto ai contenuti dinamici di WordPress, che dipendono dalle query al database.  

- **Sicurezza**: I siti generati con Hugo sono intrinsecamente più sicuri poiché non ci sono esecuzioni lato server o database. WordPress, essendo dinamico, è più vulnerabile agli attacchi e richiede aggiornamenti regolari per mantenere la sicurezza.  

- **Scalabilità**: I siti statici generati da Hugo sono altamente scalabili e possono essere facilmente distribuiti su CDN (Content Distribution Network ossia delle reti di distribuzione dei contenuti). WordPress può diventare lento e problematico quando il traffico e il numero di contenuti crescono significativamente.  

- **Temi e plugin**: WordPress ha un vasto ecosistema di temi e plugin che permettono di estendere le funzionalità del sito. Hugo offre temi e una certa quantità di plugin, ma la personalizzazione può richiedere più interventi manuali.  

- **SEO (Search Engine Optimization ossia “ottimizzazione per i motori di ricerca”)**: WordPress può essere ottimizzato per SEO tramite vari plugin. Hugo offre buone capacità SEO nativamente, e ulteriori ottimizzazioni possono essere configurate facilmente.  

- **Aggiornamenti**: WordPress richiede aggiornamenti frequenti per il core, i temi e i plugin. Hugo, essendo statico, richiede meno manutenzione; basta rigenerare il sito quando ci sono aggiornamenti.  

- **Curva di apprendimento**: WordPress è più facile da usare per i principianti grazie alla sua interfaccia grafica. Hugo, pur essendo potente, richiede un po' di conoscenza di programmazione e uso del terminale.  

- **Community e supporto**: WordPress ha una delle più grandi comunità open source con abbondante documentazione e supporto. Hugo ha una community in crescita e un buon supporto, soprattutto su GitHub.  

- **Esempi di utilizzo**: WordPress è ideale per blog, siti aziendali, e-commerce e qualsiasi sito che necessiti di interattività dinamica. Hugo è perfetto per blog, documentazioni, portfoli e qualsiasi sito che beneficia di contenuti statici.  

- **Costo**: Entrambe le piattaforme sono gratuite, ma i costi di hosting e plugin possono variare. WordPress può richiedere hosting più potente e plugin a pagamento, mentre Hugo può essere ospitato a basso costo su servizi di hosting statici.  

---


### Tabella Riassuntiva

| **Caratteristica**         | **WordPress**                       | **Hugo**                               |
|----------------------------|-------------------------------------|----------------------------------------|
| **Tipo di piattaforma**    | CMS (Content Management System)     | Generatore di siti statici             |
| **Linguaggio di programmazione** | PHP                                 | Go                                     |
| **Installazione**          | Richiede server web, PHP e database | No database, solo file statici         |
| **Gestione dei contenuti** | Dinamica, tramite interfaccia web   | Statico, tramite file Markdown         |
| **Performance**            | Dipende dal server e dal database   | Altissima, generazione di file statici |
| **Sicurezza**              | Vulnerabile a attacchi (richiede aggiornamenti frequenti) | Molto sicuro (nessuna esecuzione lato server) |
| **Scalabilità**            | Scalabilità limitata da server e database | Altamente scalabile                    |
| **Temi e plugin**          | Migliaia di temi e plugin disponibili | Temi disponibili, meno plugin (più customizzazioni manuali) |
| **SEO**                    | Ottimizzato tramite plugin          | Ottimizzato nativamente e tramite configurazioni |
| **Aggiornamenti**          | Richiede aggiornamenti regolari     | Meno frequenti, basta rigenerare il sito |
| **Curva di apprendimento** | Facile per principianti             | Più ripida, richiede conoscenze di base di programmazione e terminale |
| **Community e supporto**   | Ampia community e supporto esteso   | Comunità in crescita, supporto disponibile su forum e GitHub |
| **Esempi di utilizzo**     | Blog, siti aziendali, e-commerce    | Blog, documentazione, portfolio, siti statici |
| **Costo**                  | Gratuito (con hosting e plugin a pagamento) | Gratuito (con hosting statico a pagamento) |

---

{{< buymecoffee >}}

## Scelta

La scelta tra **WordPress** e **Hugo**, dipende dalle esigenze specifiche del progetto.  
Nel mio caso, ho preferito **Hugo** per diverse ragioni:

---

### Sicurezza

Hugo offre un livello di sicurezza superiore rispetto a WordPress.  
Essendo un generatore di siti statici, Hugo non richiede un database né l'esecuzione di script lato server, riducendo così i potenziali punti di attacco.  
Questo è particolarmente importante per chi, come me, vuole evitare problemi di sicurezza e manutenzione costante.  

---

### Linguaggio di programmazione

Uno dei motivi principali per cui ho scelto Hugo è il linguaggio di programmazione.  
Hugo è scritto in Go (Golang), un linguaggio che apprezzo molto per la sua efficienza e le sue performance.  
Go è utilizzato in progetti importanti come Docker e Kubernetes, il che dimostra la sua potenza e affidabilità.  
Al contrario, WordPress è basato su PHP, un linguaggio che considero obsoleto e che non mi piace utilizzare nonostante sia uno dei linguaggi più utilizzati sul web.  

---

### Tipo di sito

Il sito che volevo sviluppare è principalmente un gruppo di tutorial o un blog di documentazione.  
Hugo è perfetto per questo scopo perché consente di scrivere i contenuti in Markdown, un formato semplice e intuitivo che adoro.  
Questa scelta mi permette di mantenere il sito minimalista e facile da gestire.  

---

### Temi minimalisti

I temi disponibili per Hugo sono generalmente minimalisti, che è esattamente quello che cercavo.  
Non ho bisogno di interfacce complesse o di numerose funzionalità avanzate; voglio un sito pulito e funzionale, che Hugo è in grado di offrire perfettamente.  

---

### Costo

Utilizzando Hugo e GitHub Pages, i costi di hosting del mio sito sono pari a zero.  
Questa è una grande vantaggio rispetto a WordPress, che può richiedere spese aggiuntive per hosting e plugin.  
E visto che voglio investire solo i soldi guadagnati seguendo questo progetto, vuol dire che è ottimo per avere un sito web di partenza.  

---

### Scalabilità

Anche se il mio sito è attualmente un semplice blog di documentazione, c'è sempre la possibilità che cresca in futuro.  
In tal caso, posso sempre considerare di passare a WordPress se dovessi avere bisogno di funzionalità più avanzate.  
Tuttavia, per ora, Hugo soddisfa pienamente le mie esigenze.  

---

{{< buymecoffee >}}

## Primi Passi

---

### Passo 1: Installare Hugo

Per l'installazione potete seguire le indicazioni dettagliate sulla pagina ufficiale di [Hugo](https://gohugo.io/documentation/).  
Gli strumenti utilizzati sono:  
- **Terminale** o **Powershell**
- Editor di testo, nel mio caso **Visual Studio Code**  
- Git ed Github per tenere traccia del sito e poterlo pubblicare 

Verifichiamo che Hugo sia stato installato con successo, aprendo il **Terminale** su Linux o Mac, oppure aprendo la **Powershell** su Windows e scriviamo il comando:  

```sh
hugo version
```

Premiamo invio, e se ci ritorna la versione il tutto è stato installato correttamente.  

---

### Passo 2: Creare un nuovo sito Hugo

Creiamo una nuova cartella dove lo desideriamo per esempio sul **Desktop**  e ci spostiamo al suo interno tramite i comandi:  
```sh
hugo new site nome-sito
cd nome-sito
```

---

### Passo 3: Inizializzare un repository Git

Inizializza un repository Git nella cartella del progetto:

```sh
git init
```

Questo ci servirà per pubblicare su GitHub il nostro sito e avere uno storico delle versioni del sito.

---

### Passo 4: Aggiungere il tema

Sono andato sulla pagina ufficiale [Hugo Themes](https://themes.gohugo.io/) per scegliere il tema giusto per me.    
Nel mio caso ho scelto [Hugo Book Theme](https://themes.gohugo.io/themes/hugo-book/), e l'ho installato tramite il comando:

```sh
git submodule add https://github.com/alex-shpak/hugo-book themes/hugo-book
```

---

### Passo 5: Configurare il tema nel file di configurazione

Arrivati a questo punto bisogna configurare il tema, e per farlo basta aprire il file di configurazione **hugo.toml** e aggiungere o sostituire il seguente rigo:

```toml
theme = "hugo-book"
```
---

### Passo 6: Creare il primo contenuto

Crea una nuova pagina di esempio scrivendo sul Terminale o sulla Powershell:

```sh
hugo new docs/prima-pagina.md
```

Tutte le pagine verranno inserite all'interno della cartella: ***content/docs***.  

Le pagine devono essere scritte in [Markdown](/posts/my-first-post/).

---

### Passo 7: Eseguire il server di sviluppo

Avvia il server di sviluppo per vedere il sito in azione:

```bash
hugo server -D
```
Il sito sarà disponibile sull'URL [http://localhost:1313/](http://localhost:1313/)

{{< buymecoffee >}}

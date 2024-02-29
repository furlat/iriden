[[Abstractions]]
### validazione automatica

Sarebbe buono creare un dataset, probabilmente con Enrica, di validazione degli output strutturati. Penso che il task, per quanto semplice e stupido, di estrarre frasi, paragrafi, sentences, parole e matchare, e sostanzialmente utilizzare come ground truth le estrazioni con metodi tradizionali di NLP, tipo punct, o quelli compresi dentro NLTK, potrebbe essere interessante. 
Uno, possiamo testare su qualunque tipo di dato, quindi generare evaluation quanto si vuole. 

Due, abbiamo una qualche misura, un task che dal punto di vista semantico è banale, dal punto di vista sintattico è anche abbastanza semplice, tale che appunto siamo in gradocostruire un evaluation set e soprattutto un task che possiamo 
	A fare a diversi livelli di risoluzione e 
	B possiamo fare in maniera strutturata e nested, quindi anche valutare la capacità del modello di scrivere JSON nested a depth diverse. 

L'altra situazione in cui dovrebbe essere davvero banale, però magari per alcune cose meno semplice, è quella di utilizzare l'IBCST per passare Python e matchare, quindi ovviamente non possiamo farlo in maniera totale, ma matchare alcune strutture facili da estrarre con Python per poter creare dei target Pydantic su pacchetti generici che potrebbero essere utilizzati per validazione. 

Terzo, anche pensando al task dell'FDA di identificazione di dati duplicati, penso che ci sia tutta una serie di task di istruzione strutturata che possono essere composti da task di pairwise comparison o di pick K out of N. E quindi penso che queste possano essere altre maniere artificiali di creare dei task strutturati partendo da dati di cui già abbiamo delle sorte di etichette che possiamo utilizzare per poi invertirle. Grazie. 

dovremo probabilmente utilizzare open bugger quindi di nuovo libcst per creare forse dei task strutturati specifici invece rispetto all'identificazione di bug

## validazione finita

C'è probabilmente un altro migliaio di classi separate, probabilmente, non lo so, in 20 modelli Pydantic con 50 esempi labellizzati per ognuno che dovremmo fare a mano, non penso ci sia speranza. E quindi il comparison di questi mille modelli un po' più specifici, probabilmente, fatte a mano con quelli generati sopra potrebbero essere un buon benchmark. 

Sicuramente dovremmo includere anche le query di Polar per almeno riutilizzare quella parte dei dati di Daniel e includerlo nel caso scriviamo un paper sull'argomento. 

nel totale bisogna anche tenere in considerazione il costo di valutazione del modello di nuovo applicandolo appunto su tutte su un range così alto di sample potrebbe essere problematico potrebbe andare bene per per un paper inizialmente però dall'altra parte se pensiamo questo come un evaluation suite che può essere utilizzata da più persone vale la pena di avere una versione ristretta di qualità più alta per le tasche 

https://gorilla.cs.berkeley.edu/blogs/8_berkeley_function_calling_leaderboard.html

Questa leaderboard è legata ma è più function calling, c'è una parte di valutazione con l'API con AST, ma mi sembra abbastanza fatta maluccio, comunque bisogna guardare. 
``` 
In more details, BFCL includes 100 Java, 50 JavaScript, 70 REST API, 100 SQL and 1,680 Python on various simple, parallel, multiple, executable functions calling scenarios as well as function relevance detection.
```

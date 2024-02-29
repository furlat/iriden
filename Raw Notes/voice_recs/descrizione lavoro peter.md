La descrizione del lavoro è Junior Large Language Model Engineer. Le sue responsabilità saranno quelle di sviluppare sui sistemi locali di HK3 un inference server per Large Language Model che sia molto efficiente nel ripetere lo task con prompt prefissi comuni su batch di dati. 

L'architettura di neural network che utilizzeremo come language model è mixtral e i requisiti del server sono 1. Estrazione strutturata utilizzando Pydantic 2. efficient Batching con prefissi comuni, quindi ripetizione dello stesso task su migliaia di documenti diversi in maniera tale da riutilizzare la KV cache per quanto riguarda il system prompt e altri prefissi condivisi 3. Utilizzazione di un sistema di prefissi comuni 4. Speculative decoding, un esempio potrebbe essere prompt n-gram caching che permette di dare suggerimenti al modello con il testo già presente all'interno dell'input Il quinto requisito è la possibilità di utilizzare modelli quantizzati perché dovremmo essere in grado di utilizzare Mixtral con un budget di 2 GPU 4090 per ogni server, quindi un 48 giga totali di VRAM per server. Il nostro obiettivo e la valutazione sarà la velocità in termini di lettura e scrittura dell'inference server e nella di massima noi siamo interessati di sapere quanto tempo ci vuole per leggere e scrivere un milione di token con lo stesso task di estrazione strutturata. 


Nella proposta di lavoro, il ruolo per cui ci si candida è quello di Junior Large Language Model Engineer. In questa posizione, il candidato sarà responsabile dello sviluppo di un inference server per Large Language Model sui sistemi locali di HK3, con un focus particolare sull'efficienza nel ripetere task con prompt prefissi comuni su batch di dati.

L'architettura di neural network utilizzata come language model sarà Mixtral. Il server dovrà soddisfare i seguenti requisiti:

1. Estrazione strutturata utilizzando Pydantic.
2. Efficiente batching con prefissi comuni, in modo da ripetere lo stesso task su migliaia di documenti diversi e riutilizzare la KV cache per quanto riguarda il system prompt e altri prefissi condivisi.
3. Utilizzo di un sistema di prefissi comuni.
4. Speculative decoding, come ad esempio prompt n-gram caching, che permette di dare suggerimenti al modello con il testo già presente all'interno dell'input.
5. Possibilità di utilizzare modelli quantizzati, in quanto dovremmo essere in grado di utilizzare Mixtral con un budget di 2 GPU 4090 per ogni server, per un totale di 48 GB di VRAM per server.

L'obiettivo e la valutazione saranno la velocità in termini di lettura e scrittura dell'inference server. In particolare, siamo interessati a sapere quanto tempo ci vuole per leggere e scrivere un milione di token con lo stesso task di estrazione strutturata su circa mille documenti in parallelo.



mistral large

Nella proposta di lavoro, il ruolo per cui ci si candida è quello di Junior Large Language Model Engineer. In questa posizione, il candidato sarà responsabile dello sviluppo di un inference server per Large Language Model sui sistemi locali di HK3, con un focus particolare sull'efficienza nel ripetere task con prompt prefissi comuni su batch di dati.  
  
L'architettura di neural network utilizzata come language model sarà Mixtral. Il server dovrà soddisfare i seguenti requisiti:  
  
1. Estrazione strutturata utilizzando Pydantic.  
2. Efficiente batching, in modo da ripetere lo stesso task su migliaia di documenti diversi.   
3. Utilizzo di un sistema di prefissi comuni riutilizzare la KV cache per quanto riguarda il system prompt e altri prefissi condivisi.  
4. Speculative decoding, come ad esempio prompt n-gram caching, che permette di dare suggerimenti al modello con il testo già presente all'interno dell'input.  
5. Possibilità di utilizzare modelli quantizzati, in quanto dovremmo essere in grado di utilizzare Mixtral con un budget di 2 GPU 4090 per ogni server, per un totale di 48 GB di VRAM per server.  
6. Utilizzo di FastAPI per servire l'inference server ad altre macchine all'interno della VPN/LAN dei server.  
  
L'obiettivo e la valutazione saranno la velocità in termini di lettura e scrittura dell'inference server. In particolare, siamo interessati a sapere quanto tempo ci vuole per leggere e scrivere un milione di token con lo stesso task di estrazione strutturata su circa mille documenti in parallelo.  
  
English:  
  
In the job proposal, the role being applied for is that of a Junior Large Language Model Engineer. In this position, the candidate will be responsible for developing an inference server for a Large Language Model on HK3's local systems, with a particular focus on efficiency in repeating tasks with common prefixed prompts on data batches.  
  
The neural network architecture used as the language model will be Mixtral. The server must meet the following requirements:  
  
1. Structured extraction using Pydantic.  
2. Efficient batching in order to repeat the same task on thousands of different documents.  
3. Use of a common prefix system to reuse the KV cache regarding the system prompt and other shared prefixes.  
4. Speculative decoding, such as prompt n-gram caching, which allows the model to make suggestions with the text already present within the input.  
5. The ability to use quantized models, as we should be able to use Mixtral with a budget of 2 GPU 4090s per server, for a total of 48 GB of VRAM per server.  
6. Use of FastAPI to serve the inference server to other machines within the VPN/LAN of the servers.  
  
The goal and evaluation will be the speed in terms of reading and writing of the inference server. In particular, we are interested in knowing how much time it takes to read and write one million tokens with the same structured extraction task on about a thousand documents in parallel.
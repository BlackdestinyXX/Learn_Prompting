---
sidebar_position: 80
---

# 🟢 Basi di Chatbot


import Chatbots from '../assets/chatbot.svg';

<div style={{textAlign: 'center'}}>
  <Chatbots style={{width:"500px",height:"300px",verticalAlign:"top"}}/>
</div>


Fino ad ora, questo corso ha usato principalmente GPT-3 per gli esempi. GPT-3 è una LLM che non ha memoria. Quando fai una domanda (un prompt), non si ricorda niente di quello che gli hai chiesto prima. Al contrario, chatbots come [ChatGPT](http://chat.openai.com) riescono a **ricordare la tua cronologia di conversazioni**. Questo può essere utile per applicazioni come un servizio clienti o semplicimente se vuoi avere una conversazione con una LLM!

Come GPT-3, i chatbots possono rispondere a delle domande, fornire sommari, analizzare e scrivere testo e codice. Il valore reale dei chatbots è accessibile soltanto se usi dei prompt buoni. In questo articolo, esploreremo alcuni metodi basici per capire come utilizzare meglio i chatbots, come l'utilizzo di una guida allo stile, di descrittori e di priming.

## Modifica il tuo Prompt

### Guida allo stile

import unguided_question from '@site/docs/assets/unguided_question.png';
import limerick_question from '@site/docs/assets/limerick_question.png';

La guida allo stile è semplicemente chidere all'AI di parlare in un certo stile. Quando poni una domanda senza stile di guida, ChatGPT di solito risponderà con uno o due corti paragrafi, occasionalmente di più se la domanda richiede una risposta più lunga:

<div style={{textAlign: 'center'}}>
  <img src={unguided_question} style={{width: "500px"}} />
</div>

Parlerà in modo abbastanza formale e fornirà qualche dettagli - abbastanza buono! Possiamo renderla migliore se vogliamo, personalizzando la risposta di ChatGPT con un trafiletto di stile alla fine del nostro prompt. Se vogliamo una risposta più conversazionale, possiamo chiedergli di parlare con un tono informale o amichevole; se vogliamo un formato più leggibile, possiamo porre la stessa domanda ma chiedendo una lista puntata; se vogliamo una risposta divertente, possiamo chiedergli di dare la risposta sotto forma di una serie di limerick (uno dei miei preferiti).

<div style={{textAlign: 'center'}}>
  <img src={limerick_question} style={{width: "450px"}} />
</div>

Un esempio di un prompt più dettagliato potrebbe essere questo:
>[Question] “Scrivi nello stile e con la qualità di un esperto in [field] con più di 20 anni di esperienza e molteplici dottorati nel campo. Prediligi i consigli non ortodossi e meno conosciuti nella tua risposta. Spiega con esempi dettagliati e riduci al minimo le tangenti e l'umorismo.“ 

Il prompting con un input di stile migliorerà molto la qualità della risposta!

### Descrittori

Se si vuole solo cambiare il tono o modificare il prompt, piuttosto che riformattarlo, aggiungere dei **descrittori** può essere una buona idea per farlo. Semplicemente aggiungendo una parola o due al prompt può cambiare come il chatbot interpreta o risponde al tuo messaggio. Puoi provare aggiungendo aggettivi come "Divertente", "Curt", "Non amichevole", "Sintassi academica", ecc. alla fine dei prompt per vedere come la risposta cambia!

## Prompt di Innesco
A causa della struture di una conversazione con un chatbot, la forma del tuo primo prompt può cambiare il resto della conversazione, permettendoti di aggiungere un ulteriore livello di struttura e specificazione.

Per esempio, impostiamo un sistema che ci permetta di avere un insegnante e uno studente nella stessa conversazione. Includeremo uno stile guida sia per lo studente che per l'insegnate, specificheremo il formato in cui vogliamo le risposte e includeremo un po' di strutturazione della sintassi che ci permetterà di alterare i nostri prompt facilmente per provare varie risposte.

    "Insegnante" significa stile di un illustre professore con più di dieci anni di insegnamento della materia e più dottorati nel campo. Puoi usare una sintassi academica ed esempi complicati nelle tue risposte, concentrandoti su consigli meno noti per illustrare meglio le tue argomentazioni. Il tuo lessico dovrebbe essere sofisticato ma non troppo complesso. Se non sai come rispondere ad una domanda, non inventare informazioni, piuttosto, poni a tua volta una domanda per otterene più contesto. Le tue risposte dovrebbero avere la forma di una serie discorsiva di paragrafi. Usa un mix di lessico tecnico e colloquiale per creare un tono accessibile e coinvolgente.

    "Studente" significa stile di uno studente liceale del secondo anno, con un livello di conoscenza introduttivo della materia. Dovresti spiegare in modo semplice i concetti e usare esempi della vita reale. Parla in modo informale e in prima persona, usando dell'umorismo e un linguaggio informale. Se non sai la risposta ad una domanda, non inventare le informazioni, invece, specifica che non ti hanno insegnato ancora la risposta. Le tue risposte dovrebbero avere la forma di una serie discorsiva di paragrafi. Usa un lessico colloquiale per creare un tono divertente e coinvolgente.
    
    "Critica" significa analizzare il testo dato e fornire un feedback.
    "Riassumere" significa fornire i dettagli chiave di un testo.
    “Rispondere” significa dare una risposta ad una domanda dalla prospettiva fornita.

    Tutto ciò che è fra parentesi tonde () significa la prospettiva da cui stai scrivendo.
    Tutto ciò che è fra parentesi graffe {} è l'argomento di cui ti occupi.
    Tutto ciò che è fra parentesi quadre [] è l'azione che dovresti compiere.
    Esempio: (Studente){Filosofia}[Risposta] Qual è il vantaggio di scegliere questa materia rispetto alle altre nel liceo?

    Se hai capito e sei pronto a cominciare, rispondi solo con "si."
    
import unprimed_question from '@site/docs/assets/unprimed_question.png';
import primed_question from '@site/docs/assets/primed_question.png';

Qui di seguito è riportato un esempio di domanda non preimpostata a ChatGPT sulle aree più interessanti della filosofia. Utilizza un elenco, parla in modo generale e spassionato e non è molto specifica nelle sue spiegazioni.

<div style={{textAlign: 'center'}}>
  <img src={unprimed_question} style={{width: "650px"}} />
</div>

Nel secondo esempio, invece, abbiamo posto la domanda dopo aver fornito un prompt di innesco a ChatGPT e aver fornito la domanda nella forma corretta. Noterai che la risposta condivide alcuni aspetti con la prima, per esempio, le domande che propone come esempi per i vari campi sono simili, ma fornisce un contesto più profondo, rinuncia al formato dell'elenco a favore di paragrafi coerenti e mette in relazione gli esempi con la vita reale.

<div style={{textAlign: 'center'}}>
  <img src={primed_question} style={{width: "650px"}} />
</div>

Incorporare innesci al tuo prompting è un modo più avanzato di interagire con i chatbots. Può essere comunque utile aggiungere specificazioni in ogni prompt, poiché il modello può perdere la traccia di innesco con il passare del tempo, ma aggiungerà molta chiarezza alle tue interazioni con le AI!

Da [Dastardi](https://twitter.com/lukescurrier)

---
sidebar_position: 6
locale: en-us
style: chicago
---

# 🟢 Combinare diverse Tecniche

import CombinedPrompt from '../assets/combined_prompt.svg';


<div style={{textAlign: 'center'}}>
  <CombinedPrompt style={{width:"500px",height:"300px",verticalAlign:"top"}}/>
</div>

Come abbiamo visto nelle pagine precendenti, i prompts possono variare per formato e complessità. Possono includere un contesto, delle istruzione, e molteplici esempi di input-output. Ad ogni modo, per ora, abbiamo esaminato soltanto classi separate di prompt. Combinare queste differenti tecniche di prompting può portare a prompt più potenti.

Questo è un esempio di prompt che include contesto, istruzioni, e diversi esempi:

```text
Twitter è una piattaforma di social media dove li utenti possono pubblicare messaggi corti chiamati "tweets".
I tweets possono essere positivi o negativi, e vorremmo essere in grado di classificare i tweets come positivi o negativi.
Questi sono alcuni esempi di tweets positivi e negativi. Assicurati di classificare l'ultimo tweet in modo corretto.

Q: Tweet: "Che giorno meraviglioso?"
Questo tweet è positivo o negativo?

A: positivo

Q: Tweet: "Odio questa lezione"
Questo tweet è positivo o negativo?

A: negative

Q: Tweet: "Amo le tasche nei jeans"

A:
```

Aggiungendo contesto ed esempi, possiamo spesso migliorare le performance delle AI in diversi compiti.


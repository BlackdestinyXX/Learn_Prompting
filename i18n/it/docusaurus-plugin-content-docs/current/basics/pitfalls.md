---
sidebar_position: 90
---

# 🟢 Insidie dei LLM

import Pitfalls from '../assets/pitfalls.svg';

<div style={{textAlign: 'center'}}>
  <Pitfalls style={{width:"500px",height:"200px",verticalAlign:"top"}}/>
</div>


I LLM sono molto potenti, ma ancora lontane della perfezione. Ci sono molte insidie di cui bisogna essere consapevoli quando le si usa.

## Citare le fonti

La maggior parte dei LLM non possono **citare accuratamente le fonti**. Questo è perché non hanno accesso a Internet e non si ricordano esattamente da dovre proviene quell'informazione. Generano spesso fonti che sembrano affidabili, ma sono completamente inaccurate.

:::note
Strategie come i LLM con ricerca aumentata (LLM in grado di effettuare ricerche su Internet e su altre fonti) possono spesso risolvere questo problema.
:::

## Pregiudizio

I LLM sono spesso prevenuti nel generare risposte stereotipate. Anche con protezioni, possono dire ogni tanto cose sessiste/razziste/omofobe. Stai attendo quando usi LLM in applicazioni rivolte ai consumatori e stai anche attento quando le usi in ricerche (possono generare risultati stereotipati).

## Allucinazioni

I LLM generano spesso una falsità quando li viene posta una domanda di cui non conoscono la risposta. Delle volte dichiareranno di non sapere la risposta, ma la maggior parte delle volte daranno una risposta sbagliata.

## Matematica

I LLM non sono bravi in matematica la maggior parte delle volte. Hanno difficoltà a risolvere problemi di matematica semplici e spesso non riescono a risolvere problemi problemi di matematica più complessi. 

:::note
Questo problema può essere risolto usando uno [strumento aumentato LLM](https://learnprompting.org/docs/advanced_applications/mrkl).
:::

## Prompt Hacking

Li utenti possono spesso ingannare i LLM per farli generare il contenuto che vogliono. Leggi di più su questo argomento [qui](https://learnprompting.org/docs/category/-prompt-hacking).
---
sidebar_position: 90
---

# 📙 Riferimenti al vocabolario

Si prega di fare riferimento a questa pagina per un elenco di termini e concetti che useremo durante questo corso.

#### Large Language Models (LLMs), Pretrained Language Models (PLMs)(@branch2022evaluating), Language Models (LMs), e foundation models

Questi termini si riferiscono tutti più o meno alla stessa cosa: grandi IA (reti neurali), che di solito sono state addestrate
su un'enorme quantità di testo.

#### Masked Language Models (MLMs)

I MLM sono un tipo di modello NLP, che hanno un token speciale, di solito "[MASK]", che è
sostituito con una parola del vocabolario. Il modello quindi prevede la parola che
era mascherata. Ad esempio, se la frase è "Il cane sta [MASK] il gatto", il modello
predice "inseguendo" con alta probabilità.

#### Labels

Il concetto di etichette si comprende meglio con un esempio.

Supponiamo di voler classificare alcuni Tweet come cattivi o non cattivi. Se abbiamo un elenco di Tweet e
la loro *etichetta* corrispondente (cattiva o non cattiva), possiamo addestrare un modello da classificare
se i tweet sono cattivi o meno. Le etichette sono generalmente solo possibilità per il
compito di classificazione.

#### Label Space

Tutte le possibili etichette per un determinato compito ('cattivo' e 'non cattivo' per l'esempio precedente).

#### Sentiment Analysis 
 
L'analisi del sentimento è il compito di classificare il testo in sentimenti positivi, negativi o di altro tipo.

#### "Model" vs. "AI" vs. "LLM"

Questi termini sono usati in qualche modo in modo intercambiabile durante questo corso, ma
non significano sempre la stessa cosa. Gli LLM sono un tipo di AI, come specificato sopra, ma non tutti gli AI sono LLM.
Quando abbiamo menzionato i modelli in questo corso, ci riferiamo ai modelli AI. Pertanto, in questo corso,
puoi considerare intercambiabili i termini "modello" e "AI".

#### Machine Learning (ML)

Il ML è un campo di studio che si concentra su algoritmi che
può imparare dai dati. Il ML è un sottocampo di AI.

#### Verbalizer

Nel campo della classificazione, i verbalizzatori sono mappature dalle etichette alle parole in
il vocabolario di un modello linguistico(@schick2020exploiting). Ad esempio, considera
eseguendo la classificazione dei sentimenti con il seguente prompt:

```text
Tweet: "
Adoro le tasche calde"
Qual è il sentimento di questo tweet? Pronuncia "pos" o "neg".
```

Qui, il verbalizzatore è la mappatura dalle etichette concettuali di "positivo" e "negativo" ai token "pos" e "neg".

#### Reinforcement Learning from Human Feedback (RLHF)


Il RLHF è un metodo per mettere a punto gli LLM in base ai dati sulle preferenze umane.

<!-- %%RemarkAutoGlossary::list_all%% -->

# Pyspark_classification

Il DataFrame ha 31 colonne:
* __30 features:__  attributi dell'agobiopsia.
* __1 target:__  che è la colonna malignant, un valore di 1 indica un tumore maligno, al contrario un valore di 0 indica un tumore benigno.

La classe __MLlib__  richiede che le features si trovino tutte all'interno di un unico vettore su di una colonna, possiamo creare questa rappresentazione utilizzando la classe VectorAssemlber di MLlib:
* All'interno del parametro __inputCols__  sono specificate le colonne con gli input.
* All'interno del parametro __outputCol__  è specificato il nome della colonna che conterrà le features.
    
L'accuracy indica semplicemente la percentuale di classificazioni che il nostro modello ha eseguito correttamente.

__evaluation.accuracy --> Out[24]: 0.956989247311828__

La precision ci dice, tra le classificazioni eseguite per una data classe, quante sono effettivamente apparteneti a quella classe.

__evaluation.precisionByLabel -->Out[25]: [0.9629629629629629, 0.953125]__

Il recall ci dice quanti dei casi positivi il modello è riuscito a classificare correttamente.

__evaluation.recallByLabel -->Out[26]: [0.9719626168224299, 0.9384615384615385]__


il DataFrame alla fine conterrà due nuove colonne:
* __Prediction:__  (0=benigno, 1=maligno)
* __Probabily:__  probabilità di apparteneza alle due classi.


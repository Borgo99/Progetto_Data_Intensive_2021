# Progetto_Data_Intensive_2021

Progetto con l'obiettivo di prevedere i ritardi degli aerei con tecniche di machine learning.

Link Colab
https://colab.research.google.com/drive/1ZJkkxB_bK1pekR9My14vQMljX7EX54gg?usp=sharing

Il dataset è stato raccolto dal Bureau of Transportation Statistics of the USA. 
Il contenuto è diviso in due file .csv:
- Jan_2019_ontime.csv : Contiene tutti i voli nel mese di Gennaio 2019. (Pulendo il dataset si ricavano 583985 instanze)
- Jan_2020_ontime.csv : Contiene tutti i voli nel mese di Gennaio 2020.

Le colonne utilizzate in questa analisi sono le seguenti:
- DAY_OF_MONTH : Giorno del mese, è un intero da 1 a 31.
- DAY_OF_WEEK : Giorno della settimana, è un intero da 1 a 7.
- ORIGIN : Sigla aereoporto di origine, è una stringa di lunghezza fissa pari a 3; gli aereoporti di origine sono 346 in totale.
- DEST : Sigla areoporto di arrivo; è un parametro analogo a ORIGIN.
- DEP_TIME : Orario programmato di partenza; espresso nel formato hhmm.
- ARR_TIME : Orario programmato di arrivo; espresso nel formato hhmm.
- DEP_DEL15 : Indica se l'aereo è partito con 15 o più minuti di ritardo.
- DISTANCE : Indica la distanza tra l'aereoporto di partenza e quello di arrivo in miglia.
- ARR_DEL15 : È la variabile da predire, indica se l'aereo è atterrato con 15 o più minuti di ritardo.

Come primo passo verrà svolta un'analisi dividendo il mese di gennaio in due con il metodo hold-out e si cercherà quindi di predire gli aerei in ritardo negli ultimi giorni del mese. 
Per sfruttare la colonna DAY_OF_MONTH è più opportuno testare i modelli ottenuti utilizzando tutto il mese di Gennaio 2019 come training e tutto il mese di Gennaio 2020 come validation set. 
Infine, verrà svolta anche una previsione sul mese di Febbraio 2019 per confrontare il risultato ottenuto con quello ottenuto con la predizione di Gennaio 2020. 

# *The World in a Box* tutorial

---

## Indice

1. [Preparare i pulsanti](#preparare-i-pulsanti)
2. [Collegare i pulsanti a raspberry](#collegare-i-pulsanti-a-raspberry)
3. [Collegare il display a raspberry](#collegare-il-display-a-raspberry)
4. [Preparare i file video](#preparare-i-file-video)
5. [Portare i file video su raspberry](#portare-i-file-video-su-raspberry)
6. Test
    - [Panoramica del prodotto finito](#test-finale)
    - [Comportamento](#comportamento)

---

## Preparare i pulsanti...

https://user-images.githubusercontent.com/37317157/176022224-ad0473d8-b182-44cb-8a35-7c25a5100e3b.mp4



## Collegare i pulsanti a raspberry

https://user-images.githubusercontent.com/37317157/176022196-9fdb25dc-8c41-4ad6-8a02-37064ad747c1.mp4



## Collegare il display a raspberry

https://user-images.githubusercontent.com/37317157/176018566-add1cf07-c615-43d5-8f9a-ba0bbf038f9b.mp4



## Preparare i file video

Un file video sarà proiettato in seguito alla pressione di un pulsante. Per associare un file ad un determinato pulsante è necessario che il nome del file sia preceduto dal numero del pulsante, espresso nella forma `n_`, dove `n` è il numero del pulsante. Ad esempio se ho i seguenti file:

```
pippo.mp4
pluto.mp4
```

e voglio associare il primo al pulsante 1 e il secondo al pulsante 2, dovrò rinominare i file nel modo seguente:

```
1_pippo.mp4
2_pluto.mp4
```

A questo punto sarà il software ad effettuare l'associazione con i pulsanti. E' opportuno che la cartella `VIDEO`, che contiene i file dei video, non abbia più di un file che inizi con lo stesso prefisso nella forma `n_`. In sostanza, è preferibile che la cartella contenga esclusivamente i due file da proiettare.

https://user-images.githubusercontent.com/37317157/176018686-cdb41813-6708-4d67-9808-05444a7b6e7d.mp4



## Portare i file video su raspberry

https://user-images.githubusercontent.com/37317157/176018694-872df8c5-8982-401f-b026-1a8890d1971e.mp4



## Test finale

https://user-images.githubusercontent.com/37317157/176032932-030e7367-0e40-423b-b111-47d6fedbb9e7.mp4


## Comportamento

L'interfaccia per lo spettatore è la seguente: 2 pulsanti, ognuno dei quali attiva un video. Dopo aver premuto un pulsante, il video parte e, durante il *playback*, i pulsanti vengono disattivati. Al termine della riproduzione i pulsanti tornano attivi, in modo che lo spettatore successivo possa selezionare nuovamente un video da proiettare.

Flusso di comportamento dei pulsanti-spettatore: 

1.  premi un pulsante
1.  il video va in riproduzione e i pulsanti diventano **disattivi** per tutta la durata della riproduzione
2.  il *playback termina*, i pulsanti tornano **attivi**
3.  ricomincia dall'inizio

Un terzo pulsante, detto *di regia*, sulla base del tipo di azione,permette di:

- effettuare il **play/resume** di un filmato in esecuzione (pressione breve del pulsante)
- **spegnere/accendere** l'applicazione (pressione prolungata del pulsante)


https://user-images.githubusercontent.com/37317157/176033016-8ecd244e-8b42-4243-a83f-97786892f663.mp4


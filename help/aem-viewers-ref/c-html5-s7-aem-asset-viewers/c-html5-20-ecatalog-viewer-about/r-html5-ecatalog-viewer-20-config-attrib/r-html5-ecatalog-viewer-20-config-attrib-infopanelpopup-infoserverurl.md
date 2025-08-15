---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Il server informazioni URL modello viene usato per recuperare le coppie chiave/valore per la sostituzione della variabile nel pannello Info contenuto nel modello. Il modello specificato contiene in genere segnaposto macro che vengono sostituiti con i dati effettivi prima che il richiesta venga inviato al server. </p> <p><span class="codeph"> $1$</span> viene sostituito con il valore di rollover che ha attivato l'attivazione <span class="codeph"> di InfoPanelPopup</span> . </p> <p><span class="codeph"> $2$</span> viene sostituito con il numero di sequenza del fotogramma corrente nel set di immagini. </p> <p><span class="codeph"> $3$</span> viene sostituito con il primo elemento percorso specificato nel nome del set padre dell'elemento corrente. Corrisponde tipicamente all'ID del catalogo. </p> <p><span class="codeph"> $4$</span> viene sostituito con il seguente elemento nel percorso e corrisponde all'ID risorsa. L'effettiva sintassi del server di informazioni richiesta dipende dal server delle informazioni e differisce da server a server. Ad esempio, quello che segue è un tipico modello richiesta server di informazioni Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$ (informazioni in lingua inglese)</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Quando configurate la finestra a comparsa del pannello Info, il codice HTML e JavaScript codice passato al pannello Info vengono eseguiti sul computer del client. Accertatevi pertanto che il codice HTML e il codice JavaScript siano sicuri.

## Proprietà {#section-71356e3c13244e62b0582980d9d05328}

Facoltativo.

## Predefinito {#section-22e9af803f724434807d34e200eb7518}

Nessuno.

## Esempio {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`

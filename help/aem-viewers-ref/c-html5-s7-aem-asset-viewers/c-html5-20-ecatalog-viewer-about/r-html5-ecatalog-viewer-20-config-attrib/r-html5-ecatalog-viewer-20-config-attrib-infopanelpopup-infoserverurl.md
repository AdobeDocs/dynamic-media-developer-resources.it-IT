---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Il modello URL di Info server viene utilizzato per recuperare coppie chiave/valore per la sostituzione della variabile nel modello di contenuto del pannello informazioni. Il modello specificato in genere contiene i segnaposto macro che vengono sostituiti con i dati effettivi prima che la richiesta venga inviata al server. </p> <p><span class="codeph"> $1$</span> viene sostituito con il valore di rollover che ha attivato l'attivazione di  <span class="codeph"> </span> InfoPanelPopupactivation. </p> <p><span class="codeph"> $2$</span> viene sostituito con il numero di sequenza del fotogramma corrente nel set di immagini. </p> <p><span class="codeph"> $3$</span> viene sostituito con il primo elemento percorso specificato nel nome del set padre dell'elemento corrente. In genere corrisponde all’ID del catalogo. </p> <p><span class="codeph"> $4$</span> viene sostituito con l’elemento seguente nel percorso e corrisponde all’ID risorsa. La sintassi effettiva della richiesta del server di informazioni è dipendente dal server di informazioni e varia da server a server. Ad esempio, il seguente è un tipico modello di richiesta server di informazioni Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tieni presente che quando configuri Info Panel Popup, il codice HTML e il codice JavaScript passato al pannello Info viene eseguito sul computer del client. Assicurati pertanto che tali codici HTML e codice JavaScript siano protetti.

## Proprietà {#section-71356e3c13244e62b0582980d9d05328}

Facoltativo.

## Predefinito {#section-22e9af803f724434807d34e200eb7518}

Nessuno.

## Esempio {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`

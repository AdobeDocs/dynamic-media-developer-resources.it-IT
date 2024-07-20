---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Il modello URL del server informazioni viene utilizzato per recuperare coppie chiave/valore per la sostituzione della variabile nel modello di contenuto del pannello informazioni. In genere, il modello specificato contiene i portapacro che vengono sostituiti con i dati effettivi prima che la richiesta venga inviata al server. </p> <p><span class="codeph"> $1$</span> è stato sostituito con il valore di rollover che ha attivato l'attivazione di <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> è stato sostituito con il numero di sequenza del fotogramma corrente nel set di immagini. </p> <p><span class="codeph"> $3$</span> è sostituito con il primo elemento percorso specificato nel nome del set padre dell'elemento corrente. In genere corrisponde all’ID del catalogo. </p> <p><span class="codeph"> $4$</span> è stato sostituito con il seguente elemento nel percorso e corrisponde all'ID risorsa. La sintassi effettiva della richiesta del server di informazioni dipende dal server di informazioni e varia da server a server. Di seguito è riportato, ad esempio, un modello di richiesta per il server di informazioni di Dynamic Medie: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tenere presente che quando si configura Info Panel Popup, il codice HTML e il codice JavaScript passato al Pannello informazioni vengono eseguiti sul computer del client. Assicurati pertanto che tale codice HTML e il codice JavaScript siano protetti.

## Proprietà {#section-71356e3c13244e62b0582980d9d05328}

Facoltativo.

## Predefinito {#section-22e9af803f724434807d34e200eb7518}

Nessuno.

## Esempio {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]

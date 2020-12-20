---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Il modello URL del server informazioni viene utilizzato per recuperare le coppie chiave/valore per la sostituzione della variabile nel modello di contenuto del pannello Info. Il modello specificato in genere contiene i segnaposto delle macro che vengono sostituiti con i dati effettivi prima dell'invio della richiesta al server. </p> <p><span class="codeph"> $1$</span> viene sostituito con il valore di rollover che ha attivato l'attivazione di  <span class="codeph"> </span> InfoPanelPopupactivate. </p> <p><span class="codeph"> $2$</span> viene sostituito con il numero di sequenza del fotogramma corrente nel set di immagini. </p> <p><span class="codeph"> $3$</span> viene sostituito con il primo elemento percorso specificato nel nome del set padre dell'elemento corrente. In genere corrisponde all’ID del catalogo. </p> <p><span class="codeph"> $4$</span> viene sostituito con il seguente elemento nel percorso e corrisponde all’ID della risorsa. La sintassi di richiesta del server di informazioni effettiva dipende dal server di informazioni e varia da server a server. Ad esempio, di seguito è riportato un tipico modello di richiesta server Scene7 Info: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Quando configurate il Popup del pannello Info, il codice HTML e JavaScript passato al pannello Info viene eseguito sul computer client. Accertatevi pertanto che il codice HTML e il codice JavaScript siano protetti.

## Proprietà {#section-71356e3c13244e62b0582980d9d05328}

Facoltativo.

## Predefinito {#section-22e9af803f724434807d34e200eb7518}

Nessuno.

## Esempio {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`

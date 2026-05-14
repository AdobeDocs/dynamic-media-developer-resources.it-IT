---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
TQID: 'https://experienceleague.adobe.com/AFeptUljCobQmP2KN2Cx-F-gddObD-AgDJznC5oVdes'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 1%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Il modello URL del server informazioni viene utilizzato per recuperare coppie chiave/valore per la sostituzione della variabile nel modello di contenuto del pannello informazioni. In genere, il modello specificato contiene i portapacro che vengono sostituiti con i dati effettivi prima che la richiesta venga inviata al server. </p> <p><span class="codeph"> $1$</span> è stato sostituito con il valore di rollover che ha attivato l'attivazione di <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> è stato sostituito con il numero di sequenza del fotogramma corrente nel set di immagini. </p> <p><span class="codeph"> $3$</span> è sostituito con il primo elemento percorso specificato nel nome del set padre dell'elemento corrente. In genere corrisponde all’ID del catalogo. </p> <p><span class="codeph"> $4$</span> è stato sostituito con il seguente elemento nel percorso e corrisponde all'ID risorsa. La sintassi effettiva della richiesta del server di informazioni dipende dal server di informazioni e varia da server a server. Ad esempio, di seguito è riportato un tipico modello di richiesta del server di informazioni Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Quando si configura Info Panel Popup, il codice HTML e il codice JavaScript passato al Pannello informazioni vengono eseguiti sul computer del client. Di conseguenza, assicurati che tale codice HTML e il codice JavaScript siano protetti.

## Proprietà {#section-71356e3c13244e62b0582980d9d05328}

Facoltativo.

## Predefinito {#section-22e9af803f724434807d34e200eb7518}

Nessuno.

## Esempio {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`

---
description: Il visualizzatore di ricerca eCatalog supporta il rendering delle icone di mappa immagine sopra la vista principale.
solution: Experience Manager
title: Supporto mappa immagine
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Supporto mappa immagine{#image-map-support}

Il visualizzatore di ricerca eCatalog supporta il rendering delle icone di mappa immagine sopra la vista principale.

L&#39;aspetto delle icone delle mappe è controllato tramite CSS come descritto in [Effetto mappa immagine](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Le mappe immagine eseguono una delle tre azioni seguenti: reindirizzare a una pagina Web esterna, attivare la finestra a comparsa del pannello Info e i collegamenti ipertestuali interni.

## Reindirizza a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

L&#39;attributo `href` della mappa immagine ha un URL per la risorsa esterna, specificato in modo esplicito o racchiuso in una delle funzioni del modello di JavaScript supportate: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

Di seguito è riportato un esempio di reindirizzamento URL semplice:

`href=http://www.adobe.com`

In questo esempio, lo stesso URL viene racchiuso con la funzione `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tieni presente che quando aggiungi il codice JavaScript nell&#39;attributo `HREF` della mappa immagine, il codice viene eseguito sul computer del client. Di conseguenza, assicurati che il codice JavaScript sia sicuro.

## Attivazione popup pannello Info {#section-7aa036420af646d1ad8cdc388add0b57}

Per utilizzare i pannelli Info, per una mappa immagine è impostato l&#39;attributo `ROLLOVER_KEY`. Inoltre, impostare l&#39;attributo `href` contemporaneamente, altrimenti l&#39;elaborazione dell&#39;URL esterno interferisce con l&#39;attivazione a comparsa del pannello Info.

Verificare infine che la configurazione del visualizzatore includa i valori appropriati per `InfoPanelPopup.template` e, facoltativamente, `InfoPanelPopup.infoServerUrl` parametri.

>[!NOTE]
>
>Tenere presente che quando si configura Info Panel Popup, il codice HTML e il codice JavaScript passato al Pannello informazioni vengono eseguiti sul computer del client. Di conseguenza, assicurati che tale codice HTML e il codice JavaScript siano protetti.

## Collegamenti ipertestuali interni {#section-6afa4fb2fe564c429e0201f019a95849}

Facendo clic su una mappa immagine si esegue uno scambio di pagine interno al visualizzatore. Per utilizzare questa funzione, un attributo `href` nella mappa immagine ha il seguente formato speciale:

` href=target: *`idx`*`

dove `*`idx`*` è un indice in base zero della distribuzione del catalogo.

Di seguito è riportato un esempio di attributo `href` per una mappa immagine che punta alla distribuzione 3D nell&#39;eCatalog:

`href=target:2`

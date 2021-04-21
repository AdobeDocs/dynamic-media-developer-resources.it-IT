---
description: Il visualizzatore di ricerca per eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.
solution: Experience Manager
title: Supporto mappa immagine
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# Supporto mappa immagine{#image-map-support}

Il visualizzatore di ricerca per eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.

L&#39;aspetto delle icone della mappa viene controllato tramite CSS come descritto in [Effetto mappa immagine](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Le mappe immagine eseguono una delle tre azioni seguenti: reindirizzare a una pagina Web esterna, all’attivazione a comparsa del pannello Info e ai collegamenti ipertestuali interni.

## Reindirizzare a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attributo `href` della mappa immagine ha un URL per la risorsa esterna, specificato esplicitamente o racchiuso in una delle funzioni di modello JavaScript supportate: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

Di seguito è riportato un esempio di un semplice reindirizzamento URL:

`href=http://www.adobe.com`

In questo esempio, lo stesso URL viene racchiuso con la funzione `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tieni presente che quando aggiungi il codice JavaScript all’attributo `HREF` della mappa immagine, il codice viene eseguito sul computer del client. Assicurati pertanto che il codice JavaScript sia protetto.

## Attivazione popup pannello informazioni {#section-7aa036420af646d1ad8cdc388add0b57}

Per lavorare con i pannelli Info, per una mappa immagine è impostato l’attributo `ROLLOVER_KEY` . Inoltre, imposta l’attributo `href` contemporaneamente, altrimenti l’elaborazione dell’URL esterno interferisce con l’attivazione a comparsa del pannello Info.

Infine, assicurati che la configurazione del visualizzatore includa i valori appropriati per i parametri `InfoPanelPopup.template` e, facoltativamente, per i parametri `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Tieni presente che quando configuri Info Panel Popup, il codice HTML e il codice JavaScript passato al pannello Info viene eseguito sul computer del client. Assicurati pertanto che tali codici HTML e codice JavaScript siano protetti.

## Collegamenti ipertestuali interni {#section-6afa4fb2fe564c429e0201f019a95849}

Facendo clic su una mappa immagine viene eseguito uno scambio di pagina interno all’interno del visualizzatore. Per utilizzare questa funzione, un attributo `href` nella mappa immagine ha il seguente formato speciale:

` href=target: *`idx`*`

dove `*`idx`*` è un indice basato su zero dello spread del catalogo.

Di seguito è riportato un esempio di attributo `href` per una mappa immagine che punta alla diffusione 3D nell&#39;eCatalog:

`href=target:2`

---
description: Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.
seo-description: Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.
seo-title: Supporto per mappe immagine
solution: Experience Manager
title: Supporto per mappe immagine
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per mappe immagine{#image-map-support}

Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.

L’aspetto delle icone delle mappe è controllato tramite CSS come descritto nell’effetto [Mappa](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)immagine.

Le mappe immagine eseguono una delle tre azioni seguenti: reindirizzare a una pagina Web esterna, l’attivazione del pannello Info e i collegamenti ipertestuali interni.

## Reindirizza a una pagina Web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’ `href` attributo della mappa immagine ha un URL per la risorsa esterna, specificato esplicitamente o incluso in una delle funzioni di modello JavaScript supportate: `loadProduct()`, `loadProductCW()`, e `loadProductPW()`.

Esempio di semplice reindirizzamento URL:

`href=http://www.adobe.com`

In questo esempio, lo stesso URL viene racchiuso con la `loadProduct()` funzione:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. Accertatevi pertanto che il codice JavaScript sia protetto.

## Attivazione popup pannello Info {#section-7aa036420af646d1ad8cdc388add0b57}

Per utilizzare i pannelli Informazioni, una mappa immagine ha l’ `ROLLOVER_KEY` attributo impostato. Inoltre, impostate l’ `href` attributo allo stesso tempo, altrimenti l’elaborazione URL esterna interferisce con l’attivazione a comparsa del pannello Info.

Infine, accertatevi che la configurazione del visualizzatore includa i valori appropriati per `InfoPanelPopup.template` i parametri e, facoltativamente, per `InfoPanelPopup.infoServerUrl` .

>[!NOTE]
>
>Quando configurate il Popup del pannello Info, il codice HTML e JavaScript passato al pannello Info viene eseguito sul computer client. Accertatevi pertanto che il codice HTML e il codice JavaScript siano protetti.

## Collegamenti ipertestuali interni {#section-6afa4fb2fe564c429e0201f019a95849}

Facendo clic su una mappa immagine si esegue uno scambio di pagina interno all’interno del visualizzatore. Per utilizzare questa funzione, un `href` attributo nella mappa immagine ha il seguente formato speciale:

` href=target: *`idx`*`

dove ` *`idx`*` è un indice basato su zero del set di pagine affiancate del catalogo.

Di seguito è riportato un esempio di `href` attributo per una mappa immagine che punta al set di pagine affiancate 3D nell’eCatalog:

`href=target:2`

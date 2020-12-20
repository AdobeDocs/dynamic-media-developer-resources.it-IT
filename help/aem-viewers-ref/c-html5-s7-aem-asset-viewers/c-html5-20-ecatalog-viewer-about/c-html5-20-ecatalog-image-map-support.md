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
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Supporto mappa immagine{#image-map-support}

Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.

L&#39;aspetto delle icone delle mappe è controllato tramite CSS come descritto in [Effetto mappa immagine](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Le mappe immagine eseguono una delle tre azioni seguenti: reindirizzare a una pagina Web esterna, l’attivazione del pannello Info e i collegamenti ipertestuali interni.

## Reindirizza a una pagina Web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

L&#39;attributo `href` della mappa immagine ha un URL per la risorsa esterna, specificato esplicitamente o incluso in una delle funzioni supportate per i modelli JavaScript: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

Esempio di semplice reindirizzamento URL:

`href=http://www.adobe.com`

In questo esempio, lo stesso URL viene racchiuso con la funzione `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tenete presente che quando aggiungete il codice JavaScript all&#39;attributo `HREF` della mappa immagine, il codice viene eseguito nel computer client. Accertatevi pertanto che il codice JavaScript sia protetto.

## Attivazione popup pannello Info {#section-7aa036420af646d1ad8cdc388add0b57}

Per utilizzare i pannelli Informazioni, una mappa immagine ha l&#39;attributo `ROLLOVER_KEY` impostato. Inoltre, impostate l&#39;attributo `href` allo stesso tempo, altrimenti l&#39;elaborazione URL esterna interferisce con l&#39;attivazione a comparsa del pannello Info.

Infine, accertatevi che la configurazione del visualizzatore includa i valori appropriati per i parametri `InfoPanelPopup.template` e, facoltativamente, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Quando configurate il Popup del pannello Info, il codice HTML e JavaScript passato al pannello Info viene eseguito sul computer client. Accertatevi pertanto che il codice HTML e il codice JavaScript siano protetti.

## Collegamenti ipertestuali interni {#section-6afa4fb2fe564c429e0201f019a95849}

Facendo clic su una mappa immagine si esegue uno scambio di pagina interno all’interno del visualizzatore. Per utilizzare questa funzione, un attributo `href` nella mappa immagine ha il seguente formato speciale:

` href=target: *`idx`*`

dove ` *`idx`*` è un indice basato su zero dell&#39;estensione del catalogo.

Di seguito è riportato un esempio di attributo `href` per una mappa immagine che indirizza alle pagine affiancate 3D nell’eCatalog:

`href=target:2`

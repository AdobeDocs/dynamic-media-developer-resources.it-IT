---
title: Supporto mappa immagine
description: Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Supporto mappa immagine{#image-map-support}

Il visualizzatore di eCatalog supporta il rendering delle icone delle mappe immagine sopra la vista principale.

L’aspetto delle icone delle mappe è controllato tramite CSS come descritto in [Effetto mappa immagine](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Le mappe immagine eseguono una delle tre azioni seguenti: reindirizzare a una pagina Web esterna, all’attivazione a comparsa del pannello Info e ai collegamenti ipertestuali interni.

## Reindirizzamento a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

La `href` L&#39;attributo della mappa immagine ha un URL per la risorsa esterna, specificato esplicitamente o racchiuso in una delle funzioni di modello JavaScript supportate: `loadProduct()`, `loadProductCW()`e `loadProductPW()`.

Di seguito è riportato un esempio di un semplice reindirizzamento URL:

`href=http://www.adobe.com`

In questo esempio, lo stesso URL viene racchiuso con il tag `loadProduct()` funzione:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Quando aggiungi il codice JavaScript nel `HREF` attributo della mappa immagine, il codice viene eseguito sul computer del client. Assicurati pertanto che il codice JavaScript sia protetto.

## Attivazione a comparsa del pannello Info {#section-7aa036420af646d1ad8cdc388add0b57}

Per lavorare con i pannelli Info, una mappa immagine ha `ROLLOVER_KEY` set di attributi. Inoltre, imposta la `href` allo stesso tempo, in caso contrario l’elaborazione dell’URL esterno interferisce con l’attivazione a comparsa del pannello Info.

Infine, assicurati che la configurazione del visualizzatore includa i valori appropriati per `InfoPanelPopup.template` e, facoltativamente, `InfoPanelPopup.infoServerUrl` Parametri.

>[!NOTE]
>
>Quando si configura Info Panel Popup, il codice HTML e il codice JavaScript passato al pannello Info viene eseguito sul computer del client. Assicurati pertanto che il codice HTML e il codice JavaScript siano protetti.

## Collegamenti ipertestuali interni {#section-6afa4fb2fe564c429e0201f019a95849}

Quando si seleziona una mappa immagine, viene eseguito uno scambio di pagina interno all’interno del visualizzatore. Per utilizzare questa funzione, viene visualizzata una `href` l&#39;attributo nella mappa immagine ha il seguente formato speciale:

` href=target: *`idx`*`

Dove `*`idx`*` è un indice basato su zero dello spread del catalogo.

Di seguito è riportato un esempio di `href` attributo per una mappa immagine che punta alla diffusione 3D nell&#39;eCatalog:

`href=target:2`

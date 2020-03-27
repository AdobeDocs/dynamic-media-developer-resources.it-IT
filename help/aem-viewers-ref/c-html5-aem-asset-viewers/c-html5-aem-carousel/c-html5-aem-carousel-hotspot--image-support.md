---
description: 'null'
seo-description: 'null'
seo-title: Supporto per aree sensibili e mappe immagine
solution: Experience Manager
title: Supporto per aree sensibili e mappe immagine
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per aree sensibili e mappe immagine{#hotspot-and-image-maps-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi e delle aree delle mappe immagine sopra la vista principale. L’aspetto delle icone e delle aree sensibili è controllato tramite CSS come descritto nella sezione Personalizzazione di aree sensibili e mappe immagine.

Consultate [Punti attivi e mappe](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)immagine.

I punti attivi e le aree geografiche possono attivare una funzione di visualizzazione rapida sulla pagina Web host attivando un callback JavaScript o reindirizzando un utente a una pagina Web esterna.

## Punti di attivazione della Vista rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti attivi o mappe immagine devono essere creati utilizzando il tipo di azione &quot;Vista rapida&quot; in Contenuti multimediali dinamici, di AEM. Quando un utente attiva un punto di attivazione o una mappa immagine di questo tipo, il visualizzatore esegue il callback `quickViewActivate` JavaScript e vi passa i dati del punto di attivazione o della mappa immagine. È previsto che la pagina Web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione di Vista rapida.

## Reindirizza a una pagina Web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Punti attivi o mappe immagine creati per il tipo di azione &quot;Vista rapida&quot; in Contenuti multimediali dinamici di AEM reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante la creazione, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

---
title: Supporto di mappe immagine e punti attivi
description: Supporto di mappe immagine e punti attivi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Supporto di mappe immagine e punti attivi{#hotspot-and-image-maps-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi e delle aree della mappa immagine sopra la vista principale. L’aspetto delle icone e delle aree geografiche dei punti attivi è controllato tramite CSS come descritto nella sezione Personalizzazione di punti attivi e mappe immagine .

Consulta [Hotspot e mappe immagine](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Gli hotspot e le aree geografiche possono attivare una funzione Quickview sulla pagina web di hosting attivando un callback JavaScript o reindirizzando un utente a una pagina web esterna.

## Punti attivi della visualizzazione rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di hotspot o mappe immagine devono essere creati utilizzando il tipo di azione &quot;Quickview&quot; in Dynamic Media, di Adobe Experience Manager. Quando un utente attiva un punto attivo o una mappa immagine, il visualizzatore esegue il callback JavaScript `quickViewActivate` e trasmette i dati del punto attivo o della mappa immagine. È previsto che la pagina web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione Quickview.

## Reindirizzamento a una pagina web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspot o mappe immagine creati per il tipo di azione &quot;Quickview&quot; in Dynamic Media di Experience Manager reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL viene aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

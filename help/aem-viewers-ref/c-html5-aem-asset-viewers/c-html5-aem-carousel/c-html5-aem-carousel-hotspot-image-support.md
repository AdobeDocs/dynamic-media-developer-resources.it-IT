---
title: Supporto di punti attivi e mappe immagine
description: Supporto di punti attivi e mappe immagine
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Supporto di punti attivi e mappe immagine{#hotspot-and-image-maps-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi e delle aree della mappa immagine sopra la vista principale. L’aspetto delle icone e delle aree sensibili è controllato tramite CSS come descritto nella sezione Personalizzare punti attivi e mappe immagine.

Consulta [Punti attivi e mappe immagine](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

I punti attivi e le aree geografiche possono attivare una funzione Quickview sulla pagina web di hosting attivando un callback JavaScript o reindirizzare un utente a una pagina web esterna.

## Hotspot Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti attivi o mappe immagine devono essere creati utilizzando il tipo di azione &quot;Quickview&quot; in Dynamic Medie, di Adobe Experience Manager. Quando un utente attiva un punto attivo o una mappa immagine, il visualizzatore esegue `quickViewActivate` Callback JavaScript e trasmissione dei dati del punto attivo o della mappa immagine. La pagina Web di incorporamento deve essere in ascolto di questo callback. Quando attiva la pagina, apre la propria implementazione Quickview.

## Reindirizza a pagina web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

I punti attivi o le mappe immagine creati per il tipo di azione &quot;Quickview&quot; in Dynamic Medie di Experience Manager reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

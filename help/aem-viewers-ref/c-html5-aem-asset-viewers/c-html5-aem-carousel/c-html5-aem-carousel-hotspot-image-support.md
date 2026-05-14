---
title: Supporto di punti attivi e mappe immagine
description: Supporto di punti attivi e mappe immagine
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
TQID: 'https://experienceleague.adobe.com/lXiW-xoAeHFZic9fH-AN491yZfrPE1R0S53FBS1oMig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Supporto di punti attivi e mappe immagine{#hotspot-and-image-maps-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi e delle aree della mappa immagine sopra la vista principale. L’aspetto delle icone e delle aree sensibili è controllato tramite CSS come descritto nella sezione Personalizzare punti attivi e mappe immagine.

Consulta [Punti attivi e mappe immagine](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

I punti attivi e le aree geografiche possono attivare una funzione Quickview sulla pagina web di hosting attivando un callback di JavaScript o reindirizzare un utente a una pagina web esterna.

## Hotspot Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti attivi o mappe immagine devono essere creati utilizzando il tipo di azione &quot;Quickview&quot; in Dynamic Media, di Adobe Experience Manager. Quando un utente attiva un punto attivo o una mappa immagine, il visualizzatore esegue il callback di JavaScript `quickViewActivate` e vi trasmette i dati del punto attivo o della mappa immagine. La pagina Web di incorporamento deve essere in ascolto di questo callback. Quando attiva la pagina, apre la propria implementazione Quickview.

## Reindirizza a pagina web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

I punti attivi o le mappe immagine creati per il tipo di azione &quot;Quickview&quot; in Dynamic Media di Experience Manager reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

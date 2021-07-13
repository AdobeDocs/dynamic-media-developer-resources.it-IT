---
description: Supporto di mappe immagine e punti attivi
solution: Experience Manager
title: Supporto di mappe immagine e punti attivi
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Supporto di mappe immagine e punti attivi{#hotspot-and-image-maps-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi e delle aree della mappa immagine sopra la vista principale. L’aspetto delle icone e delle aree geografiche dei punti attivi è controllato tramite CSS come descritto nella sezione Personalizzazione di punti attivi e mappe immagine .

Consulta [Hotspot e mappe immagine](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Gli hotspot e le aree geografiche possono attivare una funzione di visualizzazione rapida sulla pagina web in hosting attivando un callback JavaScript o reindirizzando un utente a una pagina web esterna.

## Punti attivi nella visualizzazione rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti attivi o mappe immagine devono essere creati utilizzando il tipo di azione &quot;Visualizzazione rapida&quot; in Dynamic Media, di AEM. Quando un utente attiva un punto attivo o una mappa immagine, il visualizzatore esegue il callback JavaScript `quickViewActivate` e trasmette i dati del punto attivo o della mappa immagine. È previsto che la pagina web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione Visualizzazione rapida.

## Reindirizzamento a una pagina web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspot o mappe immagine creati per il tipo di azione &quot;Visualizzazione rapida&quot; in Dynamic Media di AEM reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL viene aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

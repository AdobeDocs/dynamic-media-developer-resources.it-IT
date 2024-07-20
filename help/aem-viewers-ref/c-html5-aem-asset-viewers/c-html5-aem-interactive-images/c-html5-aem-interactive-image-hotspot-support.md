---
title: Supporto hotspot
description: Supporto hotspot
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Supporto hotspot{#hotspot-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi sopra la vista principale. L’aspetto delle icone dei punti attivi viene controllato tramite CSS come descritto nella sezione Punti attivi.

Vedi [Punti attivi](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

I punti attivi possono attivare una funzione Quickview sulla pagina web di hosting attivando un callback di JavaScript o reindirizzare un utente a una pagina web esterna.

## Hotspot Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di hotspot devono essere creati utilizzando il tipo di azione &quot;Quickview&quot; in Dynamic Medie, di Adobe Experience Manager Assets - On-demand. Quando un utente attiva un punto attivo di questo tipo, il visualizzatore esegue il callback di JavaScript `quickViewActivate` e trasmette i dati del punto attivo a tale punto. La pagina Web di incorporamento deve essere in ascolto di questo callback. Quando attiva la pagina, apre la propria implementazione Quickview.

## Reindirizza a pagina web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Punti attivi creati per il tipo di azione &quot;Quick View&quot; (Visualizzazione rapida) in Dynamic Medie of Experience Manager Assets: on-demand reindirizza l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

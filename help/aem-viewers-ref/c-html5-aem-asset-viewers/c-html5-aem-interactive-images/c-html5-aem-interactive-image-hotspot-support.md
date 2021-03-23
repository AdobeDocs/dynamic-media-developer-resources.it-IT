---
description: Supporto per punti attivi
solution: Experience Manager
title: Supporto per punti attivi
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Supporto per punti attivi{#hotspot-support}

Il visualizzatore supporta il rendering delle icone dei punti attivi sopra la visualizzazione principale. L’aspetto delle icone dei punti attivi è controllato tramite CSS come descritto nella sezione Hotspot .

Vedere [Punti attivi](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Gli hotspot possono attivare una funzione di visualizzazione rapida sulla pagina web in hosting attivando un callback JavaScript o reindirizzando un utente a una pagina web esterna.

## Punti attivi della visualizzazione rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di hotspot devono essere creati utilizzando il tipo di azione &quot;Quick View&quot; in Dynamic Media, di AEM Assets - on demand. Quando un utente attiva un punto attivo di questo tipo, il visualizzatore esegue il callback JavaScript `quickViewActivate` e trasmette i dati del punto attivo ad esso. È previsto che la pagina web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione Visualizzazione rapida.

## Reindirizzare a una pagina Web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspot creati per il tipo di azione &quot;Visualizzazione rapida&quot; in Dynamic Media di AEM Assets - su richiesta reindirizzerà l’utente a un URL esterno. A seconda delle impostazioni effettuate durante l’authoring, l’URL viene aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

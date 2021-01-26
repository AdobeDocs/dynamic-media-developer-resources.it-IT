---
description: Supporto per i punti di attivazione
solution: Experience Manager
title: Supporto per i punti di attivazione
topic: Dynamic Media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# Supporto per punti di attivazione{#hotspot-support}

Il visualizzatore supporta il rendering delle icone dei punti di attivazione sopra la vista principale. L’aspetto delle icone dei punti di attivazione è controllato tramite CSS come descritto nella sezione Hotspot.

Vedere [Punti attivi](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

I punti attivi possono attivare una funzione di visualizzazione rapida sulla pagina Web host attivando un callback JavaScript o reindirizzando un utente a una pagina Web esterna.

## Punti di attivazione di Vista rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti di attivazione devono essere creati utilizzando il tipo di azione &quot;Vista rapida&quot; in Dynamic Media, di  AEM Assets - su richiesta. Quando un utente attiva un tale punto di attivazione, il visualizzatore esegue il callback JavaScript `quickViewActivate` e vi passa i dati del punto di attivazione. È previsto che la pagina Web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione di Vista rapida.

## Reindirizza alla pagina Web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Punti attivi creati per il tipo di azione &quot;Vista rapida&quot; in Dynamic Media di  AEM Assets - su richiesta reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante la creazione, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

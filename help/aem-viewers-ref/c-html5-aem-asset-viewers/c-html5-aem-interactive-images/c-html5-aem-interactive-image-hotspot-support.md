---
description: 'null'
seo-description: 'null'
seo-title: Supporto per i punti di attivazione
solution: Experience Manager
title: Supporto per i punti di attivazione
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per i punti di attivazione{#hotspot-support}

Il visualizzatore supporta il rendering delle icone dei punti di attivazione sopra la vista principale. L’aspetto delle icone dei punti di attivazione è controllato tramite CSS come descritto nella sezione Hotspot.

Vedere [Punti attivi](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

I punti attivi possono attivare una funzione di visualizzazione rapida sulla pagina Web host attivando un callback JavaScript o reindirizzando un utente a una pagina Web esterna.

## Punti di attivazione della Vista rapida {#section-cda48fc9730142d0bb3326bac7df3271}

Questi tipi di punti di attivazione devono essere creati utilizzando il tipo di azione &quot;Vista rapida&quot; in Contenuti multimediali dinamici, di Risorse AEM - su richiesta. Quando un utente attiva un tale punto di attivazione, il visualizzatore esegue il callback `quickViewActivate` JavaScript e vi passa i dati del punto di attivazione. È previsto che la pagina Web di incorporamento ascolti questo callback. Quando attiva la pagina, apre la propria implementazione di Vista rapida.

## Reindirizza a una pagina Web esterna {#section-ef820c71251e4215800bb99c0c9ebe16}

Punti attivi creati per il tipo di azione &quot;Vista rapida&quot; in Contenuti multimediali dinamici di Risorse AEM - su richiesta reindirizzano l’utente a un URL esterno. A seconda delle impostazioni effettuate durante la creazione, l’URL si apre in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

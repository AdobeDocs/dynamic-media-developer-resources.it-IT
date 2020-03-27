---
description: Il visualizzatore video interattivo supporta il rendering dei campioni interattivi in base ai dati interattivi passati al visualizzatore come parametro di configurazione.
seo-description: Il visualizzatore video interattivo supporta il rendering dei campioni interattivi in base ai dati interattivi passati al visualizzatore come parametro di configurazione.
seo-title: Supporto dei dati interattivi
solution: Experience Manager
title: Supporto dei dati interattivi
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Supporto dei dati interattivi{#interactive-data-support}

Il visualizzatore video interattivo supporta il rendering dei campioni interattivi in base ai dati interattivi passati al visualizzatore come parametro di configurazione.

Il campione correntemente visibile corrisponde all’area temporale del video a cui è associato. Toccando o facendo clic sul campione interattivo si attiva l’azione assegnata al campione al momento dell’authoring.

Un campione interattivo può attivare una visualizzazione rapida sulla pagina Web host attivando un callback JavaScript oppure reindirizzare l’utente a una pagina Web esterna.

## Informazioni sulla visualizzazione rapida {#section-7990e44f641042d2a38ba20c9413b3f8}

Questi tipi di campioni interattivi devono essere creati utilizzando il tipo di azione &quot;quickview&quot; in AEM Assets - on-demand. Quando un utente attiva un tale campione, il visualizzatore esegue il callback `quickViewActivate` JavaScript e vi passa i dati del campione. È previsto che la pagina Web in cui è stato incorporato ascolti questo callback e, quando viene attivata, la pagina apre la propria implementazione Visualizzazione rapida.

## Reindirizza a una pagina Web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

Campioni creati per il tipo di azione &quot;visualizzazione rapida&quot; in Risorse AEM - su richiesta reindirizzano l’utente a un URL esterno. A seconda delle impostazioni al momento dell’authoring, l’URL può essere aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

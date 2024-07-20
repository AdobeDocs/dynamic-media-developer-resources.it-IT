---
title: Supporto dati interattivi
description: Il Visualizzatore video interattivo supporta il rendering dei campioni interattivi basati sui dati interattivi passati al visualizzatore come parametro di configurazione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Supporto dati interattivi{#interactive-data-support}

Il Visualizzatore video interattivo supporta il rendering dei campioni interattivi basati sui dati interattivi passati al visualizzatore come parametro di configurazione.

Il campione attualmente visibile corrisponde all&#39;area temporale del video a cui è associato. Toccando o facendo clic sul campione interattivo si attiva l’azione ad esso assegnata al momento dell’authoring.

Il campione interattivo può attivare un Quickview sulla pagina web di hosting attivando un callback di JavaScript oppure può reindirizzare l’utente a una pagina web esterna.

## Informazioni su Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Questi tipi di campioni interattivi devono essere creati utilizzando il tipo di azione &quot;quickview&quot; in Adobe Experience Manager Assets - On-demand. Quando un utente attiva un campione di questo tipo, il visualizzatore esegue il callback di JavaScript `quickViewActivate` e gli trasmette i dati del campione. È previsto che la pagina web incorporante ascolti questo callback e, quando viene attivata, la pagina apre la propria implementazione Quickview.

## Reindirizza a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

Campioni creati per il tipo di azione &quot;quickview&quot; in Experience Manager Assets: l’utente viene reindirizzato su richiesta a un URL esterno. A seconda delle impostazioni al momento dell’authoring, l’URL può aprirsi in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

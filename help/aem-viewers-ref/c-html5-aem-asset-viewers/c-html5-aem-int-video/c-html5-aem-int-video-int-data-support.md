---
description: Il Visualizzatore video interattivo supporta il rendering di campioni interattivi in base ai dati interattivi trasmessi al visualizzatore come parametro di configurazione.
solution: Experience Manager
title: Supporto dei dati interattivi
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,Business Practitioner
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Supporto dei dati interattivi{#interactive-data-support}

Il Visualizzatore video interattivo supporta il rendering di campioni interattivi in base ai dati interattivi trasmessi al visualizzatore come parametro di configurazione.

Il campione attualmente visibile corrisponde all’area temporale del video a cui è associato. Tocca o fai clic sul campione interattivo per attivare l’azione assegnata al campione al momento dell’authoring.

Il campione interattivo può attivare una Visualizzazione rapida sulla pagina Web in hosting attivando un callback JavaScript oppure reindirizzare l’utente a una pagina Web esterna.

## Informazioni sulla visualizzazione rapida {#section-7990e44f641042d2a38ba20c9413b3f8}

Questi tipi di campioni interattivi devono essere creati utilizzando il tipo di azione &quot;quickview&quot; in AEM Assets - on-demand. Quando un utente attiva un campione di questo tipo, il visualizzatore esegue il callback JavaScript `quickViewActivate` e trasmette i dati del campione ad esso. È previsto che la pagina web di incorporamento ascolti questo callback e quando si attiva, la pagina apre la propria implementazione di Visualizzazione rapida.

## Reindirizzamento a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

Campioni creati per il tipo di azione &quot;quickview&quot; in AEM Assets - su richiesta reindirizzano l’utente a un URL esterno. A seconda delle impostazioni al momento dell’authoring, l’URL può essere aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

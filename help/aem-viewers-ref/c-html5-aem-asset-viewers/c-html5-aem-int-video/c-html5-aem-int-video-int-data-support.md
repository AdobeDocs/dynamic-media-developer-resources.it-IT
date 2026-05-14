---
title: Supporto dati interattivi
description: Il Visualizzatore video interattivo supporta il rendering dei campioni interattivi basati sui dati interattivi passati al visualizzatore come parametro di configurazione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
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

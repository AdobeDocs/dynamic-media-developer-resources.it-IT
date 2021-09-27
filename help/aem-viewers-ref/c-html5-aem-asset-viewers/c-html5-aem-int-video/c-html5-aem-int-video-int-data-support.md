---
title: Supporto dei dati interattivi
description: Il Visualizzatore video interattivo supporta il rendering di campioni interattivi in base ai dati interattivi trasmessi al visualizzatore come parametro di configurazione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Supporto dei dati interattivi{#interactive-data-support}

Il Visualizzatore video interattivo supporta il rendering di campioni interattivi in base ai dati interattivi trasmessi al visualizzatore come parametro di configurazione.

Il campione attualmente visibile corrisponde all’area temporale del video a cui è associato. Tocca o fai clic sul campione interattivo per attivare l’azione assegnata al campione al momento dell’authoring.

Il campione interattivo può attivare una visualizzazione rapida sulla pagina Web in hosting attivando un callback JavaScript oppure reindirizzare l’utente a una pagina Web esterna.

## Informazioni su Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Questi tipi di campioni interattivi devono essere creati utilizzando il tipo di azione &quot;quickview&quot; in Adobe Experience Manager Assets - Su richiesta. Quando un utente attiva un campione di questo tipo, il visualizzatore esegue il callback JavaScript `quickViewActivate` e trasmette i dati del campione ad esso. È previsto che la pagina web di incorporamento ascolti questo callback e quando si attiva, la pagina apre la propria implementazione Quickview.

## Reindirizzamento a una pagina web esterna {#section-32ebe3c3a7f74892a428c5d48801de4d}

Campioni creati per il tipo di azione &quot;quickview&quot; in Experience Manager Assets - su richiesta reindirizzano l’utente a un URL esterno. A seconda delle impostazioni al momento dell’authoring, l’URL può essere aperto in una nuova scheda del browser, nella stessa finestra o nella finestra del browser denominata.

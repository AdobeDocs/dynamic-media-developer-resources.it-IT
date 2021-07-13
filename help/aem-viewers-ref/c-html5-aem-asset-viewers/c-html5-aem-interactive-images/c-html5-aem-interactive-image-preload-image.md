---
description: L’immagine di precaricamento è un’immagine di anteprima della risorsa statica che si carica subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie SDK del visualizzatore, le informazioni sulla risorsa e sul predefinito. Lo scopo dell’immagine precaricata è quello di migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.
solution: Experience Manager
title: Immagine precaricata
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Immagine precaricata{#preload-image}

L’immagine di precaricamento è un’immagine di anteprima della risorsa statica che si carica subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie SDK del visualizzatore, le informazioni sulla risorsa e sul predefinito. Lo scopo dell’immagine precaricata è quello di migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.

L’immagine di precaricamento funziona bene per il metodo di incorporamento del visualizzatore più comune, che è l’incorporazione reattiva con altezza illimitata. Vedere l&#39;intestazione [Incorporamento design reattivo con altezza illimitata](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Tuttavia, questa funzione presenta alcune limitazioni quando si utilizzano altri metodi di incorporazione o opzioni di configurazione specifiche. Il rendering corretto dell’immagine precaricata potrebbe non riuscire nei seguenti casi:

* Quando il visualizzatore è di dimensioni fisse e la dimensione viene definita utilizzando l’attributo di configurazione `stagesize` all’interno del record predefinito del visualizzatore o nel file CSS del visualizzatore esterno per l’elemento contenitore del visualizzatore di livello superiore.
* Quando si utilizza il metodo di incorporazione delle dimensioni flessibili con larghezza e altezza definito per l’incorporazione del visualizzatore. Vedere l&#39;intestazione [Incorporamento di dimensioni flessibili con larghezza e altezza definita](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Potrebbe essere necessario disattivare la funzione di precaricamento immagine utilizzando l’ `preloadImage` attributo di configurazione se si utilizza il visualizzatore in una delle modalità operative elencate sopra.

Inoltre, l’immagine di precaricamento non viene utilizzata, anche se abilitata nella configurazione, se il visualizzatore è incorporato nell’elemento DOM è nascosto utilizzando l’impostazione `display:none` CSS o staccato dalla struttura DOM.

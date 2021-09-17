---
title: Immagine precaricata
description: L’immagine di precaricamento è un’immagine di anteprima della risorsa statica che viene caricata subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie, la risorsa e le informazioni di preimpostazione dell’SDK del visualizzatore. Lo scopo dell’immagine precaricata è quello di migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Immagine precaricata{#preload-image}

L’immagine di precaricamento è un’immagine di anteprima della risorsa statica che viene caricata subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie, la risorsa e le informazioni di preimpostazione dell’SDK del visualizzatore. Lo scopo dell’immagine precaricata è quello di migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.

L’immagine di precaricamento funziona bene per il metodo di incorporamento del visualizzatore più comune, che è l’incorporazione reattiva con altezza illimitata. Vedere l&#39;intestazione [Incorporamento design reattivo con altezza illimitata](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Tuttavia, questa funzione presenta alcune limitazioni quando si utilizzano altri metodi di incorporazione o opzioni di configurazione specifiche. Il rendering corretto dell’immagine precaricata potrebbe non riuscire nei seguenti casi:

* Quando il visualizzatore è di dimensioni fisse e la dimensione viene definita utilizzando l’attributo di configurazione `stagesize` all’interno del record predefinito del visualizzatore oppure nel file CSS del visualizzatore esterno per l’elemento contenitore del visualizzatore di livello superiore.
* Quando si utilizza il metodo di incorporazione delle dimensioni flessibili con larghezza e altezza definito per l’incorporazione del visualizzatore. Vedere l&#39;intestazione [Incorporamento di dimensioni flessibili con larghezza e altezza definita](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Se utilizzi il visualizzatore in una delle modalità operative elencate sopra, disattiva la funzione precarica immagine utilizzando l&#39;attributo di configurazione `preloadImage` .

Inoltre, l’immagine di precaricamento non viene utilizzata, anche se abilitata nella configurazione, se il visualizzatore è incorporato nell’elemento DOM è nascosto utilizzando l’impostazione `display:none` CSS o staccato dalla struttura DOM.

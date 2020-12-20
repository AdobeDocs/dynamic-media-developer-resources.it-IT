---
description: L’immagine di precaricamento è un’immagine di anteprima di risorsa statica che viene caricata subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie SDK per visualizzatori, le risorse e le informazioni sui predefiniti. Lo scopo dell’immagine precaricata è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.
seo-description: L’immagine di precaricamento è un’immagine di anteprima di risorsa statica che viene caricata subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie SDK per visualizzatori, le risorse e le informazioni sui predefiniti. Lo scopo dell’immagine precaricata è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.
seo-title: Immagine precaricata
solution: Experience Manager
title: Immagine precaricata
topic: Dynamic media
uuid: bae99269-fd55-485e-b78e-873b77541d91
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Precarica immagine{#preload-image}

L’immagine di precaricamento è un’immagine di anteprima di risorsa statica che viene caricata subito dopo aver chiamato il metodo init() e viene visualizzata mentre vengono scaricate le librerie SDK per visualizzatori, le risorse e le informazioni sui predefiniti. Lo scopo dell’immagine precaricata è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente i contenuti all’utente.

L’immagine di precaricamento funziona correttamente per il metodo di incorporamento più comune del visualizzatore, ovvero l’incorporazione reattiva con un’altezza illimitata. Vedere l&#39;intestazione [Incorporazione reattiva del design con altezza illimitata](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

La funzione presenta tuttavia alcune limitazioni quando vengono utilizzati altri metodi di incorporazione o opzioni di configurazione specifiche. Il rendering dell&#39;immagine di precaricamento potrebbe non riuscire correttamente nei seguenti casi:

* Quando le dimensioni del visualizzatore sono fisse e definite utilizzando l&#39;attributo di configurazione `stagesize` all&#39;interno del record del predefinito per visualizzatori oppure nel file CSS del visualizzatore esterno per l&#39;elemento contenitore del visualizzatore di livello principale.
* Quando viene utilizzato il metodo di incorporazione flessibile delle dimensioni con larghezza e altezza definito per il visualizzatore. Vedere l&#39;intestazione [Incorporamento delle dimensioni flessibile con larghezza e altezza definite](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Potrebbe essere necessario disattivare la funzione di precaricamento dell&#39;immagine utilizzando l&#39;attributo di configurazione `preloadImage` se si utilizza il visualizzatore in una delle modalità operative elencate sopra.

Inoltre, l&#39;immagine di precaricamento non viene utilizzata, anche se abilitata nella configurazione, se il visualizzatore è incorporato nell&#39;elemento DOM viene nascosto utilizzando l&#39;impostazione `display:none` CSS o scollegato dalla struttura DOM.

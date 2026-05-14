---
title: Precarica immagine
description: L’immagine di precaricamento è un’immagine di anteprima statica di una risorsa che viene caricata subito dopo la chiamata al metodo init() e viene visualizzata durante il download delle librerie SDK del visualizzatore, delle risorse e delle informazioni sui predefiniti. Lo scopo dell’immagine di precaricamento è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente il contenuto all’utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
TQID: 'https://experienceleague.adobe.com/GlTbkyDeUNGf4gjmEEGbh1NaQ-nOgPZLtrz9kH4eK7o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# Precarica immagine{#preload-image}

L’immagine di precaricamento è un’immagine di anteprima statica di una risorsa che viene caricata subito dopo la chiamata al metodo init() e viene visualizzata durante il download delle librerie SDK del visualizzatore, delle risorse e delle informazioni sui predefiniti. Lo scopo dell’immagine di precaricamento è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente il contenuto all’utente.

L’immagine di precaricamento funziona bene per il metodo di incorporamento più comune, ovvero l’incorporamento dinamico con altezza illimitata. Vedi l&#39;intestazione [Incorporamento design reattivo con altezza illimitata](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

La funzione, tuttavia, presenta alcune limitazioni quando si utilizzano altri metodi di incorporamento o opzioni di configurazione specifiche. Il rendering dell&#39;immagine di precaricamento potrebbe non riuscire nei seguenti casi:

* Quando il visualizzatore è di dimensioni fisse e la dimensione viene definita utilizzando l&#39;attributo di configurazione `stagesize` all&#39;interno del record del predefinito visualizzatore. Oppure, utilizzando il file CSS del visualizzatore esterno per l’elemento contenitore del visualizzatore di primo livello.
* Quando utilizzi l’incorporamento di dimensioni flessibili con il metodo di incorporamento del visualizzatore definito dalla larghezza e dall’altezza. Vedi l&#39;intestazione [Dimensione flessibile con larghezza e altezza definite](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Disattivare la funzione di precaricamento dell&#39;immagine utilizzando l&#39;attributo di configurazione `preloadImage` se si utilizza il visualizzatore in una delle modalità operative elencate sopra.

Inoltre, l&#39;immagine di precaricamento non viene utilizzata, anche se abilitata nella configurazione, se il visualizzatore è incorporato nell&#39;elemento DOM è nascosto utilizzando l&#39;impostazione CSS `display:none` o scollegato dalla struttura DOM.

---
title: Precarica immagine
description: L’immagine di precaricamento è un’immagine di anteprima statica di una risorsa che viene caricata subito dopo la chiamata al metodo init() e viene visualizzata durante il download delle librerie SDK del visualizzatore, delle risorse e delle informazioni sui predefiniti. Lo scopo dell’immagine di precaricamento è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente il contenuto all’utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Precarica immagine{#preload-image}

L’immagine di precaricamento è un’immagine di anteprima statica di una risorsa che viene caricata subito dopo la chiamata al metodo init() e viene visualizzata durante il download delle librerie SDK del visualizzatore, delle risorse e delle informazioni sui predefiniti. Lo scopo dell’immagine di precaricamento è migliorare visivamente il tempo di caricamento del visualizzatore e presentare rapidamente il contenuto all’utente.

L’immagine di precaricamento funziona bene per il metodo di incorporamento più comune, ovvero l’incorporamento dinamico con altezza illimitata. Vedi il titolo [Design reattivo con altezza illimitata](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

La funzione, tuttavia, presenta alcune limitazioni quando si utilizzano altri metodi di incorporamento o opzioni di configurazione specifiche. Il rendering dell&#39;immagine di precaricamento potrebbe non riuscire nei seguenti casi:

* Quando il visualizzatore è di dimensioni fisse e la dimensione viene definita utilizzando `stagesize` attributo di configurazione nel record del predefinito del visualizzatore o nel file CSS del visualizzatore esterno per l’elemento contenitore del visualizzatore di primo livello.
* Quando utilizzi l’incorporamento di dimensioni flessibili con il metodo di incorporamento del visualizzatore definito dalla larghezza e dall’altezza. Vedi il titolo [Dimensione flessibile che incorpora con larghezza e altezza definite](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Se utilizzi il visualizzatore in una delle modalità operative elencate qui sopra, disattiva la funzione di precaricamento dell&#39;immagine utilizzando `preloadImage` attributo di configurazione.

Inoltre, l’immagine di precaricamento non viene utilizzata, anche se abilitata nella configurazione, se il visualizzatore è incorporato nell’elemento DOM è nascosto tramite `display:none` Impostazione CSS o rimozione dalla struttura DOM.

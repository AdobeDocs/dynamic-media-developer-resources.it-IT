---
description: Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.
seo-description: Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.
seo-title: Note sulla compatibilità
solution: Experience Manager
title: Note sulla compatibilità
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# Note sulla compatibilità{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilità con set video adattivi precedenti. Per consentire la riproduzione, potrebbe essere necessario caricare nuovamente i set video adattivi.

## Generali {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Il ridimensionamento lato browser potrebbe rendere sfocata l&#39;interfaccia utente e le immagini durante lo zoom dell&#39;utente nella pagina. La formattazione dell&#39;interfaccia utente potrebbe anche non essere visualizzata correttamente a seconda dello zoom. Questo passerà allo schermo intero.
* A causa della limitazione delle dimensioni sui dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il gesto diapositiva per scambiare i fotogrammi in set di immagini incorporati invece di toccare il componente Campioni incorporato. Il componente è presente come indicatore visivo.
* Nei browser Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l&#39;intero schermo del dispositivo. ma ridimensiona l’applicazione alle dimensioni della finestra del browser.
* Il pulsante Chiudi non funziona in iOS 8.0 e iOS 8.1, ma funziona in iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Perdita di memoria visibile con i visualizzatori zoom e eCatalog. La navigazione ripetuta attraverso i frame potrebbe causare l&#39;arresto anomalo del browser.
* Toccando due volte un visualizzatore è possibile che l’intera pagina venga ingrandita invece che solo il visualizzatore con il ridimensionamento sul lato browser abilitato.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

## Nexus Galaxy {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Toccando due volte un visualizzatore è possibile che l’intera pagina venga ingrandita invece che solo il visualizzatore, con l’opzione di ridimensionamento sul lato browser attivata.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog mostra pagine affiancate non corrette con orientamenti orizzontali e verticali.

## Dispositivi mobili HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilità di disattivare lo zoom con le dita nativo è una &quot;funzione&quot; del wrapper HTC dell’interfaccia utente (SENSO HTC). Questa funzione può causare lo zoom di un’intera pagina quando si utilizza il gesto di zoom con le dita sul visualizzatore. Utilizzare invece un doppio tocco.
* Le icone delle mappe immagine potrebbero sovrapporsi se le mappe immagine sono piccole e si chiudono insieme.

## Visualizzatore video HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` il modificatore è supportato solo con il software HLS e la riproduzione Flash HDS. Non funziona quando la riproduzione utilizza il lettore nativo.
* Riproduzione progressiva OGG e WebM non supportata.
* Il ridimensionamento del browser potrebbe causare la visualizzazione del lettore video a dimensioni errate (includere le impostazioni del pannello di controllo del sistema operativo Windows).
* La ricerca di video con streaming HLS su Safari potrebbe non essere coerente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* La modalità Quirks non è supportata.
* La modalità di compatibilità non è supportata.
* Internet Explorer su dispositivo mobile non è supportato.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Gli eCatalog di grandi dimensioni potrebbero causare l’arresto anomalo del browser sull’iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o successivo: Le impostazioni del plug-in Internet potrebbero impedire la riproduzione del video Flash.
* La ricerca di video con streaming HLS su Safari potrebbe non essere coerente.
* Impossibile cercare di terminare il video in Safari 6 utilizzando lo streaming HLS.

---
description: Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.
solution: Experience Manager
title: Note sulla compatibilità
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---


# Note sulla compatibilità{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilità con i vecchi set video adattivi. Potrebbe essere necessario ricaricare i set video adattivi per consentire la riproduzione.

## Generali {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Il ridimensionamento lato browser può rendere sfocata l’interfaccia utente e le immagini quando l’utente ingrandisce la pagina. La formattazione dell’interfaccia utente potrebbe anche non essere visualizzata correttamente a seconda dello zoom. Questo passerà allo schermo intero.
* A causa della limitazione delle dimensioni sui dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il movimento di diapositiva per scambiare fotogrammi in set di immagini incorporati invece di toccare il componente campioni incorporati. Il componente è presente come indicatore visivo.
* Nei browser Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l’intero schermo del dispositivo. ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
* Il pulsante Chiudi non funziona con iOS 8.0 e iOS 8.1 ma funziona con iOS 8.2.

## Galassia SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Perdita di memoria visibile con i visualizzatori Zoom ed eCatalog. La navigazione ripetuta attraverso i frame può causare l&#39;arresto anomalo del browser.
* Se si tocca due volte un visualizzatore, l’intera pagina viene ingrandita invece che solo il visualizzatore e viene abilitata la funzione di ridimensionamento lato browser.

## Galassia S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

## Nexus galattico {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Se si tocca due volte un visualizzatore, l’intera pagina viene ingrandita invece che solo il visualizzatore e il ridimensionamento è attivato.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* L’eCatalog mostra una pagina non corretta con orientamento verticale e orizzontale.

## Dispositivi mobili HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilità di disabilitare lo zoom nativo con le dita è una &quot;funzione&quot; del wrapper HTC dell’interfaccia utente (HTC Sense). Questa funzione può causare lo zoom di un’intera pagina quando si utilizza il gesto &quot;pizzico per lo zoom&quot; sul visualizzatore. Utilizza invece un gesto con doppio tocco.
* Le icone delle mappe immagine possono sovrapporsi se le mappe immagine sono piccole e vicine tra loro.

## Visualizzatore video HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` Il modificatore è supportato solo con riproduzione software HLS e flash HDS. Non funziona quando la riproduzione utilizza il lettore nativo.
* Riproduzione progressiva OGG e WebM non supportata.
* Il ridimensionamento del browser può causare la visualizzazione del lettore video con dimensioni errate (incluse le impostazioni di visualizzazione del pannello di controllo del sistema operativo Windows).
* La ricerca video che utilizza lo streaming HLS su Safari potrebbe non essere coerente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Modalità Quirks non supportata.
* La modalità di compatibilità non è supportata.
* Internet Explorer su dispositivi mobili non supportato.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Gli eCatalog di grandi dimensioni possono causare l’arresto anomalo del browser sull’iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o successivo: Le impostazioni del plug-in Internet possono impedire la riproduzione del video Flash.
* La ricerca video che utilizza lo streaming HLS su Safari potrebbe non essere coerente.
* Impossibile cercare di terminare il video su Safari 6 utilizzando lo streaming HLS.

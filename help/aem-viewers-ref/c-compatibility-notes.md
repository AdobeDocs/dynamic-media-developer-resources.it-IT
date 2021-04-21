---
description: Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.
solution: Experience Manager
title: Note sulla compatibilità
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
translation-type: tm+mt
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Note sulla compatibilità{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilità con i vecchi set video adattivi. Ricarica i set video adattivi per consentire la riproduzione.

## Generali {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Il ridimensionamento lato browser causa la sfocatura dell’interfaccia utente e delle immagini durante lo zoom dell’utente sulla pagina. La formattazione dell&#39;interfaccia utente non viene visualizzata correttamente a seconda dello zoom e passa allo schermo intero.
* A causa della limitazione delle dimensioni sui dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il movimento di diapositiva per scambiare i fotogrammi in set di immagini incorporati invece di toccare il componente campioni incorporati. Il componente è presente come indicatore visivo.
* Nei browser Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l’intero schermo del dispositivo. ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
* Il pulsante Chiudi non funziona con iOS 8.0 e iOS 8.1 ma funziona con iOS 8.2.

## Galassia SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Perdita di memoria visibile con i visualizzatori Zoom ed eCatalog. La navigazione ripetuta attraverso i frame causa l&#39;arresto anomalo del browser.
* Se si tocca due volte un visualizzatore, l’intera pagina viene ingrandita invece che solo il visualizzatore e viene abilitata la funzione di ridimensionamento lato browser.

## Galassia S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

## Nexus galattico {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Se si tocca due volte un visualizzatore, l’intera pagina viene ingrandita invece che solo il visualizzatore e viene attivata la modifica in scala sul lato browser.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* L’eCatalog mostra una pagina non corretta con orientamento verticale e orizzontale.

## Dispositivi mobili HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilità di disabilitare lo zoom nativo con le dita è una &quot;funzione&quot; del wrapper HTC dell’interfaccia utente (HTC Sense). Questa funzione può causare lo zoom di un’intera pagina quando si utilizza il gesto &quot;pizzico per lo zoom&quot; sul visualizzatore. Utilizza invece un gesto con doppio tocco.
* Le icone delle mappe immagine si sovrappongono se le mappe immagine sono piccole e vicine tra loro.

## Visualizzatore video HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` Il modificatore è supportato solo con riproduzione software HLS e Flash HDS. Non funziona quando la riproduzione utilizza il lettore nativo.
* Riproduzione progressiva OGG e WebM non supportata.
* Il ridimensionamento del browser causa la visualizzazione del lettore video con dimensioni errate (incluse le impostazioni di visualizzazione del Pannello di controllo Campaign Windows®).
* La ricerca video che utilizza lo streaming HLS su Safari non è coerente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Modalità Quirks non supportata.
* La modalità di compatibilità non è supportata.
* Internet Explorer su dispositivi mobili non supportato.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Gli eCatalog di grandi dimensioni causano l’arresto anomalo del browser sull’iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o successivo: Le impostazioni del plug-in Internet impediscono la riproduzione del video del Flash.
* La ricerca video che utilizza lo streaming HLS su Safari non è coerente.
* Impossibile cercare di terminare il video su Safari 6 utilizzando lo streaming HLS.

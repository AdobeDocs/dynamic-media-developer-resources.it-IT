---
title: Note sulla compatibilità
description: Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Note sulla compatibilità{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Note sulla compatibilità per sistemi operativi, browser e dispositivi mobili.

## Blackberry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilità con i set di video adattivi precedenti. Ricarica set video adattivi per consentire la riproduzione.

## Generali {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Il ridimensionamento del lato browser rende sfocate l’interfaccia utente e le immagini man mano che l’utente si ingrandisce verso la pagina. La formattazione dell’interfaccia utente non viene visualizzata correttamente a seconda dello zoom e viene riportata a schermo intero.
* A causa delle dimensioni limitate dei dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il movimento della diapositiva per scambiare i fotogrammi nei set di immagini incorporati invece di toccare il componente Campioni incorporati. Il componente è presente come indicatore visivo.
* Nei browser di Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l&#39;intero schermo del dispositivo. Viene invece ridimensionata in base alle dimensioni della finestra del browser.
* Il pulsante Chiudi non funziona in iOS 8.0 e iOS 8.1, ma in iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Perdita di memoria rilevata con i visualizzatori Zoom ed eCatalog. La navigazione ripetuta attraverso i fotogrammi causa l’arresto anomalo del browser.
* Il doppio tocco su un visualizzatore determina lo zoom dell’intera pagina invece che del solo visualizzatore con ridimensionamento sul lato browser abilitato.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Il doppio tocco su un visualizzatore determina lo zoom dell’intera pagina invece che del solo visualizzatore, con la funzione di ridimensionamento lato browser abilitata.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* L’eCatalog mostra pagine affiancate non corrette con orientamenti in verticale e orizzontale.

## Dispositivi mobili HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilità di disabilitare lo zoom pinch nativo è una &quot;funzione&quot; del wrapper dell’interfaccia utente HTC (HTC Sense). Questa funzione può causare lo zoom di un&#39;intera pagina quando si utilizza il movimento &quot;pizzica per ingrandire&quot; sul visualizzatore. Al suo posto, tocca due volte.
* Le icone della mappa immagine si sovrappongono se le mappe immagine sono piccole e vicine tra loro.

## Visualizzatore video HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` Il modificatore è supportato solo con la riproduzione di HLS software e HDS di Flash. Non funziona se la riproduzione utilizza il lettore nativo.
* Riproduzione progressiva OGG e WebM non supportata.
* Il ridimensionamento del browser causa la visualizzazione del lettore video con dimensioni non corrette (incluse le impostazioni di visualizzazione del Pannello di controllo Campaign di Windows®).
* Le ricerche video con lo streaming HLS su Safari non sono coerenti.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Modalità non supportata.
* Modalità di compatibilità non supportata.
* Internet Explorer su dispositivi mobili non è supportato.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Gli eCatalog di grandi dimensioni causano l’arresto anomalo del browser su iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o versione successiva: le impostazioni del plug-in Internet impediscono la riproduzione di video di Flash.
* Le ricerche video con lo streaming HLS su Safari non sono coerenti.
* Impossibile cercare la fine del video su Safari 6 utilizzando lo streaming HLS.

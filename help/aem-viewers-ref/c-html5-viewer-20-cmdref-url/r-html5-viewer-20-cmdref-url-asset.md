---
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
title: asset
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Developer,Business Practitioner
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 2%

---

# risorsa{#asset}

Parametro comune a tutti i visualizzatori.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> ID risorsa del singolo video o set video adattivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questa proprietà è obbligatoria, a meno che non venga utilizzato il parametro `video` . Consulta [Supporto video esterno](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) in Video o [Supporto video esterno](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) in Video360.

Oppure

` asset= *`immagine`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> immagine  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica una singola immagine o un set carosello. Applica una doppia codifica HTTP a qualsiasi carattere non sicuro presente nel nome dell’immagine o nel nome del set carosello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Oppure

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListWithModifiersmultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> immagine  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica una singola immagine. Applica la doppia codifica HTTP a qualsiasi carattere non sicuro presente nel nome dell'immagine. </p> <p>Oppure specifica un riferimento a un set di immagini. Il visualizzatore recupera i set di immagini dal server utilizzando la richiesta <span class="codeph"> req=set IS </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un set di immagini esplicito, costituito da una sequenza ordinata di elementi o fotogrammi, separati da virgole. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un set di immagini esplicito in cui ogni fotogramma ha i propri modificatori Image Serving. In questo caso, l'elenco dei fotogrammi è racchiuso tra parentesi. Assicurati di applicare una doppia codifica HTTP a qualsiasi virgola presente nel modificatore Image Serving specifico per il fotogramma. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica un set 360 gradi multidimensionale esplicito con la seguente sintassi: </p> <p> <span class="codeph"> (  <span class="varname"> HorizontalSpinSet  </span>)[,(  <span class="varname"> HorizontalSpinSet  </span>)])  </span> </p> <p> dove <span class="codeph"> <span class="varname"> HorizontalSpinSet </span> </span> è un elenco di fotogrammi separati da virgola per un dato asse orizzontale. Tutti i <span class="codeph"> <span class="varname"> orizzontaliSpinSet </span> </span> devono avere lo stesso numero di fotogrammi. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificatori  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandi Image Serving; I separatori <span class="codeph"> &amp; </span> e <span class="codeph"> = </span> devono essere codificati per HTTP rispettivamente come <span class="codeph"> %26 </span> e <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Oppure

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetVideoswatchIdimageswatchIdsetIdswatchIdvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un riferimento a un set di file multimediali. Il visualizzatore recupera i set di file multimediali dal server utilizzando la richiesta req=set IS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video  </span> </span> </p> </td> 
   <td colname="col2"> <p> Set video singolo o adattivo. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> immagine  </span> </span> </p> </td> 
   <td colname="col2"> <p> Immagine singola. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> Set di campioni. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Immagine campione. </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> L'identificatore del tipo di elemento del set di file multimediali può essere uno dei seguenti: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>Per immagine singola. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset  </span> </p> <p>Per set di campioni nidificati. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> girare  </span> </p> <p>Per set 360 gradi. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video  </span> </p> <p>Per video singolo. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> set_video  </span> </p> <p>Per set video adattivi. </p> </li> 
     </ul> </p> <p> <p>Nota:  Questa funzione è supportata in Adobe Dynamic Media Classic; non è supportato in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificatori  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandi Image Serving; I separatori <span class="codeph"> &amp; </span> e <span class="codeph"> = </span> devono essere codificati per HTTP rispettivamente come <span class="codeph"> %26 </span> e <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Obbligatorio.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

Nessuno.

## Esempi {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Riferimento a una singola risorsa:

```
asset=Scene7SharedAssets/Backpack_B
```

Oppure

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

Oppure

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

Oppure

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

Oppure

```
asset=Viewers/space_station_360-AVS
```

Riferimento singolo a un set di immagini definito in un catalogo:

```
asset=Viewers/Pluralist
```

Set di immagini esplicito:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Set di immagini esplicito con modificatori Image Serving specifici per un fotogramma:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Riferimento singolo a un set 360 gradi definito in un catalogo:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Set 360 gradi esplicito:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Set 360 gradi multidimensionale esplicito:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Riferimento per set di file multimediali diversi:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Set di file multimediali misti esplicito:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

---
description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-title: Lettore video360
solution: Experience Manager
title: Lettore video360
topic: Dynamic media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# Lettore video360{#video-player}

Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video in corso di riproduzione non corrispondono alle dimensioni del lettore video, il contenuto video viene centrato all’interno dell’area di visualizzazione rettangolare del lettore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto del lettore video:

```
.s7video360viewer .s7video360player
```

**Proprietà CSS del lettore video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Potete localizzare il messaggio di errore visualizzato nei casi in cui il sistema non è in grado di riprodurre il video.

Vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Esempio: per impostare un visualizzatore video con le dimensioni del lettore video impostate su 512 x 288 pixel.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

L&#39;aspetto dell&#39;animazione del buffering è controllato dal seguente selettore di classe CSS:

```
.s7video360viewer .s7video360player .s7waiticon
```

**Proprietà CSS dell&#39;icona di attesa**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Margine sinistro dell'icona dell'animazione, in genere meno metà della larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Margine superiore dell'icona dell'animazione, in genere meno metà dell'altezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Manopola la grafica. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’animazione di buffering su una larghezza di 101 pixel e un’altezza di 29 pixel:

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```


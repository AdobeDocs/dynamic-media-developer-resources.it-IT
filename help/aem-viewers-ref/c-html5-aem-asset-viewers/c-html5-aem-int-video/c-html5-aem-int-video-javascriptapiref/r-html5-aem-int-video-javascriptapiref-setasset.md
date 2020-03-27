---
description: Riferimento API JavaScript per il visualizzatore video interattivo.
seo-description: Riferimento API JavaScript per il visualizzatore video interattivo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 80c670a4-1251-47f5-a66b-8ba5019df1ce
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore video interattivo.

`setAsset(asset[, data])`

Imposta la nuova risorsa e i dati facoltativi aggiuntivi. Potete chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene richiamata, `init()`il visualizzatore scambia la risorsa in fase di esecuzione.

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nuovo ID risorsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dati </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} oggetto JSON con i seguenti campi facoltativi (con distinzione tra maiuscole e minuscole): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage </span> - Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video. Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> caption </span> - posizione del nuovo file di sottotitoli. Se non viene specificato, il pulsante della didascalia non è visibile nell'interfaccia utente. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigazione </span> - URL o percorso del contenuto di navigazione WebVTT. Il file WebVTT deve essere distribuito da Image Server. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - URL o percorso del contenuto di dati interattivi WebVTT. Il file WebVTT deve essere gestito da Image Server. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```


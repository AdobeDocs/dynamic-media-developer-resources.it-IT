---
description: Impostazioni che consentono di migliorare la nitidezza delle immagini per i file TIF a piramide ottimizzati.
seo-description: Impostazioni che consentono di migliorare la nitidezza delle immagini per i file TIF a piramide ottimizzati.
seo-title: UnsharpMaskOptions
solution: Experience Manager
title: UnsharpMaskOptions
topic: Scene7 Image Production System API
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 9%

---


# UnsharpMaskOptions{#unsharpmaskoptions}

Impostazioni che consentono di migliorare la nitidezza delle immagini per i file TIF a piramide ottimizzati.

`unsharpMaskOptions=[ *`amount, radius, threshold, monochrome`*]`

## Parametri {#section-c3f0d03136ba4422819cb463bd393885}

Specificare un valore per le opzioni `unsharpMaskOptions` con `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nome </th>
   <th colname="col2" class="entry"> Tipo </th>
   <th colname="col3" class="entry"> Descrizione </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> amount</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controlla il contrasto applicato ai pixel del bordo. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Intervallo: 0,0 - 5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Predefinito: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controlla la nitidezza impostando il numero di pixel intorno al bordo di un’immagine. Il valore più adatto dipende dalle dimensioni dell’immagine. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Intervallo: 0,0 - 250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Con valori bassi potete rendere più nitidi solo i pixel dei bordi. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Valori alti aumentano la nitidezza di una banda più ampia di pixel. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> threshold</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Determina il modo in cui i pixel devono essere diversi dall’area circostante prima che vengano considerati pixel di un bordo e possano essere resi più nitidi. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Intervallo: 0 - 255 (solo numeri interi). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Predefinito: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monocromatico</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>I valori includono solo <span class="codeph"> 0</span> o <span class="codeph"> 1</span>. </p><p>Impostare su <span class="codeph"> 0</span> da applicare separatamente a ciascun componente di colore oppure su <span class="codeph"> 1</span> da applicare solo alla luminosità dell'immagine (intensità). Anche la maschera di livello o la maschera composita vengono rese più nitide. </p><p><span class="codeph"><span class="varname"> Le immagini </span></span> monocromei vengono ignorate per le immagini in scala di grigio. </p></td>
  </tr>
 </tbody>
</table>

## Esempio {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Utilizzata da {#section-db8124a5468b498694a780f8a56a4560}

Il tipo `unsharpMaskOptions` è utilizzato da:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Riferimento API Image Serving: op_usm](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)


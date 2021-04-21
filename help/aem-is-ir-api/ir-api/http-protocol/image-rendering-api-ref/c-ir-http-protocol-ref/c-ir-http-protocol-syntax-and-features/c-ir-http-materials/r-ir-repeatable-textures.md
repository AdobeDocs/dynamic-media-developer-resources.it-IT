---
description: Le texture ripetibili includono materiali interni ed esterni, come tessuti (sia per abbigliamento che per tappezzeria), rivestimenti per pavimenti da parete a parete, sfondi, materiali di controsoffitto, texture di grana di legno, tetti e materiali di rivestimento, e qualsiasi altra texture generica.
solution: Experience Manager
title: Trame ripetibili
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 3%

---


# Texture ripetibili{#repeatable-textures}

Le texture ripetibili includono materiali interni ed esterni, come tessuti (sia per abbigliamento che per tappezzeria), rivestimenti per pavimenti da parete a parete, sfondi, materiali di controsoffitto, texture di grana di legno, tetti e materiali di rivestimento, e qualsiasi altra texture generica.

Le texture ripetibili possono essere applicate a oggetti piatti, flowline, sketch, piani, muri e mobili. Se applicato a un oggetto non testurizzabile, l’oggetto viene dipinto con `color=` (o `bgc=` se `color=` non è specificato).

Un materiale è considerato una texture se include un attributo `src=` che specifica un&#39;immagine e se si trova in un MSS diverso da decal o muro bordo.

Durante il rendering, la texture viene allineata con l&#39;oggetto facendo corrispondere il punto `anchor=` del materiale della texture con il punto di origine della texture dell&#39;oggetto (come creato nella vignetta).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
   <th colname="col3" class="entry"> <p>Predefinito </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>immagine a texture ripetibile; obbligatorio </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione della texture </p> </td> 
   <td colname="col3"> <span class="codeph"> attributo::Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Punto di allineamento della texture </p> </td> 
   <td colname="col3"> <p>Angolo in alto a sinistra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modalità di ripetizione </p> </td> 
   <td colname="col3"> <p>0 (ripetizione diretta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Opzioni </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza). </p> </td> 
  </tr> 
 </tbody> 
</table>

Oltre a questi attributi di base, le texture ripetibili supportano i seguenti attributi di uso speciale per le applicazioni avanzate:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
   <th colname="col3" class="entry"> <p>Predefinito </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout=  </span> </a> </p> </td> 
   <td colname="col2"> <p>colore e spessore della scanalatura; utile per materiali ceramici/piastrelle di pietra </p> </td> 
   <td colname="col3"> <p>Grotta già presente nell'immagine </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modalità di allineamento (tra oggetti); utilizzato per applicazioni di tappezzeria </p> </td> 
   <td colname="col3"> <p>Corrispondente al centro </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Angolo di rotazione della trama; non supportato da oggetti muro </p> </td> 
   <td colname="col3"> <p>0 (nessuna rotazione) </p> </td> 
  </tr> 
 </tbody> 
</table>


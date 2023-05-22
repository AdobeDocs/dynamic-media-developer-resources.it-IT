---
title: Texture ripetibili
description: Le texture ripetibili comprendono i materiali interni ed esterni, come i tessuti (sia abbigliamento che tappezzeria), i rivestimenti del pavimento da parete a parete, le carte da parati, i materiali del controsoffitto, le texture dei grani di legno, i materiali per tetti e i rivestimenti laterali e qualsiasi altra texture generica.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---

# Texture ripetibili{#repeatable-textures}

Le texture ripetibili comprendono i materiali interni ed esterni, come i tessuti (sia abbigliamento che tappezzeria), i rivestimenti del pavimento da parete a parete, le carte da parati, i materiali del controsoffitto, le texture dei grani di legno, i materiali per tetti e i rivestimenti laterali e qualsiasi altra texture generica.

Le texture ripetibili possono essere applicate a oggetti piatti, linee di flusso, sketch, piani, pareti e cabinet. Quando viene applicato a un oggetto non testurizzabile, l&#39;oggetto viene dipinto con `color=` (o `bgc=` se `color=` non è specificato).

Un materiale è considerato una texture se include `src=` attributo che specifica un&#39;immagine e se si trova in un MSS diverso da decalcomania o bordo muro.

Durante il rendering, la texture viene allineata con l&#39;oggetto mediante la corrispondenza `anchor=` punto del materiale di texture con il punto di origine della texture dell&#39;oggetto (come creato nella vignettatura).

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Immagine texture ripetibile; obbligatorio </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione texture </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Risoluzione </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> ancoraggio= </span> </a> </p> </td> 
   <td colname="col2"> <p>Punto di allineamento della texture </p> </td> 
   <td colname="col3"> <p>Angolo in alto a sinistra </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= ripetizione </span> </a> </p> </td> 
   <td colname="col2"> <p>Modalità Ripeti </p> </td> 
   <td colname="col3"> <p>0 (ripetizione diretta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Opzioni </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza). </p> </td> 
  </tr> 
 </tbody> 
</table>

Oltre a questi attributi di base, le texture ripetibili supportano i seguenti attributi speciali per applicazioni avanzate:

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> malta= </span> </a> </p> </td> 
   <td colname="col2"> <p>Colore e spessore della scanalatura; utile per materiali in ceramica/pietra </p> </td> 
   <td colname="col3"> <p>Grout già presente nell'immagine </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Modalità di allineamento (tra oggetti); utilizzata per applicazioni di tappezzeria </p> </td> 
   <td colname="col3"> <p>Corrispondenza al centro </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Angolo di rotazione della texture; non supportato da oggetti di parete </p> </td> 
   <td colname="col3"> <p>0 (nessuna rotazione) </p> </td> 
  </tr> 
 </tbody> 
</table>

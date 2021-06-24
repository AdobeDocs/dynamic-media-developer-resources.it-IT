---
description: File materiale. Specifica i dati del materiale, sotto forma di un singolo riferimento al catalogo del materiale o come uno o due file di dati immagine o materiale, separati da una virgola.
solution: Experience Manager
title: src
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 2%

---

# src{#src}

File materiale. Specifica i dati del materiale, sotto forma di un singolo riferimento al catalogo del materiale o come uno o due file di dati immagine o materiale, separati da una virgola.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedRequestFile`*]`

`srcE= *`name`*`

`srcN= *`indice`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;parentesi graffa;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;race;'&amp;race;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;race;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;race;''</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID catalogo materiale (<span class="codeph"> attributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Voce di catalogo materiale (<span class="codeph"> catalogo::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>File di stile del materiale (<span class="filepath"> .vnc</span> o <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>File di dati immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Richiesta a Image Serving. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Richiedi il rendering dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Richiedi a un server esterno. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nome di un materiale incorporato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> indice</span> </p></td> 
  <td class="stentry"> <p>Numero di indice basato su 0 per un materiale incorporato. </p></td> 
 </tr> 
</table>

I materiali Texture, Decal e Wallpaper ripetibili richiedono una singola immagine, che può essere specificata come file o come richiesta incorporata.

I materiali del cabinet richiedono un file stile archivio ( [!DNL .vnc]), che non può essere specificato come richiesta nidificata. Un file immagine di texture è facoltativo per gli archivi e, se specificato, può essere un file o una richiesta incorporata.

I materiali di rivestimento per finestre richiedono un file di stile di rivestimento per finestre ( [!DNL .vnw]), che non può essere specificato come richiesta nidificata. Un file di texture è facoltativo e, se specificato, può essere un file o una richiesta incorporata.

Image Rendering utilizza le stesse regole di Image Serving per cercare cataloghi di materiali, voci di catalogo e file di dati. Per ulteriori informazioni, consulta la descrizione del tipo di dati *`object`* nella documentazione di Image Serving .

*`materialFile`* è un percorso relativo a  `attribute::RootPath`.

*`foreignReq`* può essere un URL relativo a  `attribute::RootUrl`, o un URL assoluto se  `attribute::AllowDirectUrls` è impostato.

Se *`catId`* non è specificato, viene utilizzato il catalogo di sessione.

`srcE=` e  `srcN=` fornire l&#39;accesso ai materiali incorporati nella vignetta.

## Formati di file supportati {#section-f2186d3eef834fc8bbecb2bc68daacad}

Image Rendering supporta gli stessi formati immagine sorgente di Dynamic Media Image Serving.

Le applicazioni che richiedono dati immagine in più risoluzioni diverse si comportano al meglio quando si utilizza il formato multi-risoluzione TIFF (PTIFF) piramidale di Scene7. Image Server include l&#39;utilità Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, fare riferimento alla descrizione dell&#39;utilità IC nella documentazione di Image Serving .

## Proprietà {#section-e68d03788d534e2184147987d51dfd0f}

Attributo materiale. Richiesto per tutti i materiali ad eccezione del colore solido (non consentito per i materiali a colori solidi). Tutte le stringhe sono sensibili all’uso di maiuscole e minuscole. *`index`* deve essere maggiore o uguale a 0.

## Predefinito {#section-dde549c1917540dc8f9555962202da3c}

Nessuno.

## Esempio {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS per un armadio colorato con una texture ripetibile separata:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Lo stesso materiale può essere posizionato in un catalogo di materiali `'cat`&#39; nel record &#39; `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

Una richiesta nidificata a Image Serving per ottenere un&#39;immagine di texture:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Consultate anche {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Cataloghi](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) materiali,  [attributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [attributo::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)

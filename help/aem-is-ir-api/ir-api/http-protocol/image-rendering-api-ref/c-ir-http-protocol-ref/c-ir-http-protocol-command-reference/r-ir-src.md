---
description: File materiale. Specifica i dati del materiale, sotto forma di un singolo riferimento a un catalogo di materiali o come uno o due file di immagine o di dati di materiale, separati da una virgola.
seo-description: File materiale. Specifica i dati del materiale, sotto forma di un singolo riferimento a un catalogo di materiali o come uno o due file di immagine o di dati di materiale, separati da una virgola.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# src{#src}

File materiale. Specifica i dati del materiale, sotto forma di un singolo riferimento a un catalogo di materiali o come uno o due file di immagine o di dati di materiale, separati da una virgola.

`src = *``*|{{ *``*| *``*}[, *`catalogEntryMaterialFileReqMaterialFile`*]`

`srcE= *`name`*`

`srcN= *`indice`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> MaterialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}|{'ir{'<span class="varname"> irReq</span>'}'|{'<span class="varname"> ForeignReq</span>'}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID catalogo materiale (<span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Voce catalogo materiale (<span class="codeph"> catalogo::Id</span>). </p></td> 
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
  <td class="stentry"> <p>Richiedete a Image Serving. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Richiedete il rendering dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> externalReq</span> </p></td> 
  <td class="stentry"> <p>Richiesta a un server esterno. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nome di un materiale incorporato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> indice</span> </p></td> 
  <td class="stentry"> <p>Numero indice basato su 0 per un materiale incorporato. </p></td> 
 </tr> 
</table>

I materiali Texture, Decal e Wallpaper ripetibili richiedono una singola immagine, che può essere specificata come un file o una richiesta incorporata.

I materiali di archivio richiedono un file di stile archivio ( [!DNL .vnc]), che non può essere specificato come richiesta nidificata. Un file immagine di texture è facoltativo per gli archivi e, se specificato, può essere un file o una richiesta incorporata.

I materiali per rivestimenti di finestre richiedono un file di stile rivestimenti finestre ( [!DNL .vnw]), che non può essere specificato come richiesta nidificata. Un file di texture è facoltativo e, se specificato, può essere un file o una richiesta incorporata.

Image Rendering utilizza le stesse regole di Image Serving per cercare cataloghi di materiali, voci di catalogo e file di dati. Per ulteriori informazioni, consultate la descrizione del tipo di *`object`* dati nella documentazione di Image Server.

*`materialFile`* è un percorso relativo a `attribute::RootPath`.

*`foreignReq`* può essere un URL relativo a `attribute::RootUrl`oppure un URL assoluto, se `attribute::AllowDirectUrls` è impostato.

Se non *`catId`* viene specificato, viene utilizzato il catalogo delle sessioni.

`srcE=` e `srcN=` fornire l&#39;accesso ai materiali incorporati nella vignettatura.

## Formati di file supportati {#section-f2186d3eef834fc8bbecb2bc68daacad}

Il rendering delle immagini supporta gli stessi formati delle immagini sorgente di Scene7 Image Server.

Le applicazioni che richiedono dati immagine a diverse risoluzioni si comportano nel modo migliore quando si utilizza il formato multirisoluzione TIFF (PTIFF) piramidale di Scene7. Image Server include l’utilità Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, consultare la descrizione dell’utility IC nella documentazione di Image Server.

## Proprietà {#section-e68d03788d534e2184147987d51dfd0f}

Attributo materiale. Obbligatorio per tutti i materiali eccetto i colori in tinta unita (non consentito per i materiali in tinta unita). Tutte le stringhe sono con distinzione tra maiuscole e minuscole. *`index`* deve essere uguale o superiore a 0.

## Predefinito {#section-dde549c1917540dc8f9555962202da3c}

Nessuno.

## Esempio {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS per un cabinet colorato con una texture ripetibile separata:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Lo stesso materiale potrebbe essere presente in un catalogo di materiali `'cat`&quot; nel record &#39; `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

Richiesta nidificata a Image Server per ottenere un’immagine texture:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Consultate anche {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Cataloghi](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)materiali, [attributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attributo::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)

---
title: src
description: File di materiale. Specifica i dati dei materiali, sotto forma di un singolo riferimento di catalogo dei materiali oppure come uno o due file di dati di immagini o materiali, separati da una virgola.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# src{#src}

File di materiale. Specifica i dati dei materiali, sotto forma di un singolo riferimento di catalogo dei materiali oppure come uno o due file di dati di immagini o materiali, separati da una virgola.

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`nome`*`

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
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID catalogo materiali (<span class="codeph"> attributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Voce del catalogo dei materiali (<span class="codeph"> catalogo::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>File di stile del materiale (<span class="filepath"> .vnc</span> o <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fileImmagine</span> </p></td> 
  <td class="stentry"> <p>File di dati immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Richiesta a Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Richiesta al rendering immagini. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Richiesta a un server esterno. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Nome <span class="varname"></span> </p></td> 
  <td class="stentry"> <p>Nome di un materiale incorporato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Indice <span class="varname"></span> </p></td> 
  <td class="stentry"> <p>Numero di indice basato su 0 per un materiale incorporato. </p></td> 
 </tr> 
</table>

I materiali Texture, Decal e Wallpaper ripetibili richiedono una singola immagine, che può essere specificata come file o richiesta incorporata.

I materiali di archivio richiedono un file di stile di archivio ( [!DNL .vnc]), che non può essere specificato come richiesta nidificata. Un file di immagine della trama è facoltativo per gli archivi e, se specificato, può essere un file o una richiesta incorporata.

Per i materiali per coperture per finestre è necessario un file di stile per coperture per finestre ( [!DNL .vnw]), che non può essere specificato come richiesta nidificata. Un file di trama è facoltativo e, se specificato, può essere un file o una richiesta incorporata.

Image Rendering utilizza le stesse regole di Image Server per la ricerca di cataloghi di materiali, voci di catalogo e file di dati. Per ulteriori informazioni, consulta la descrizione del tipo di dati *`object`* nella documentazione di Image Server.

*`materialFile`* è un percorso relativo a `attribute::RootPath`.

*`foreignReq`* Può essere un URL relativo a `attribute::RootUrl` o un URL assoluto se è impostato `attribute::AllowDirectUrls`.

Se *`catId`* non è specificato, viene utilizzato il catalogo di sessione.

`srcE=` e `srcN=` forniscono accesso ai materiali incorporati nella vignettatura.

## Formati di file supportati {#section-f2186d3eef834fc8bbecb2bc68daacad}

Image Rendering supporta gli stessi formati di immagine sorgente di Dynamic Media Image Server.

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato multi-risoluzione PTIFF (Scene7 pyramid TIFF). Image Server include l&#39;utility Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility IC nella documentazione di Image Server.

## Proprietà {#section-e68d03788d534e2184147987d51dfd0f}

Attributo materiale. Obbligatorio per tutti i materiali ad eccezione del colore in tinta unita (non consentito per i materiali a tinta unita). Tutte le stringhe fanno distinzione tra maiuscole e minuscole. *`index`* Deve essere uguale o maggiore di 0.

## Predefinito {#section-dde549c1917540dc8f9555962202da3c}

Nessuno.

## Esempio {#section-675865444f8a4d35b9fc6e58b36e3438}

MSS per un cabinet colorato con una texture ripetibile separata:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Lo stesso materiale potrebbe trovarsi in un catalogo dei materiali `'cat` nel record &#39;`12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

Una richiesta nidificata a Image Server per ottenere un’immagine della texture:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Consultate anche {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Cataloghi materiali](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attributo::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)

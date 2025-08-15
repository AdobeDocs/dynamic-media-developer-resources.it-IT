---
description: Specificatore oggetto di Source. Gli oggetti profilo immagine, SVG e ICC possono essere specificati come voci del catalogo immagini o percorsi di file relativi
solution: Experience Manager
title: oggetto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# oggetto{#object}

Specificatore oggetto di Source. Gli oggetti profilo immagine, SVG e ICC possono essere specificati come voci del catalogo immagini o percorsi di file relativi

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ID radice </span> </span> </p> </td> 
  <td class="stentry"> <p>nome del catalogo immagini ( <span class="codeph">, attributo::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID del record immagine, SVG, modello o profilo ICC nel catalogo immagini specificato, principale o predefinito </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> percorso </span> </span> </p> </td> 
  <td class="stentry"> <p>percorso e nome del file di profilo ICC, maschera o immagine relativa </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> oggetto </span> </span> </p> </td> 
  <td class="stentry"> <p>può verificarsi nel percorso dell'URL principale o in un comando <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> o <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catalogo immagini. Per ulteriori dettagli, vedere [Catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3). Se nel percorso URL è specificato *`rootId`*, tale catalogo diventerà il *catalogo principale* per questa richiesta. In caso contrario, viene utilizzato il catalogo predefinito come catalogo principale. Nella stessa richiesta è possibile utilizzare più cataloghi di immagini diversi.

Il server presuppone inizialmente che *`rootId`* sia omesso nei comandi `src=`, `mask=` e `icc=` e tenta di trovare una voce di catalogo nel catalogo principale. Il server tenta di utilizzare l&#39;intera stringa *`object`* come *`objId.`*

Se viene trovata una voce di catalogo, viene utilizzata; in caso contrario, il server tenta di trovare una corrispondenza con *`rootId`* di un catalogo immagini. Se viene identificato un catalogo, viene eseguita la ricerca di *`objId`*. Se viene trovata una voce e, questa viene utilizzata.

In caso contrario, *`object`* verrà considerato come un percorso di file esplicito. In questo caso, se `attribute::FullMatch` è impostato nel catalogo principale, il catalogo viene ignorato per questo oggetto e viene utilizzato il catalogo predefinito. Se `attribute::FullMatch` non è impostato, viene utilizzato il catalogo principale per l&#39;ulteriore elaborazione.

Sia *`rootId`* che *`objId`* fanno distinzione tra maiuscole e minuscole. *`path`* fa distinzione tra maiuscole e minuscole solo in UNIX.

Se si specifica un `/` iniziale, viene eseguita la ricerca nel catalogo predefinito anziché nel catalogo principale. Questa funzione è utile soprattutto quando un percorso esplicito richiede `default::RootPath` anziché `attribute::RootPath` del catalogo principale, ma può anche essere utilizzata per accedere alle voci del catalogo predefinito che altrimenti verrebbero ignorate dalle voci del catalogo principale.

Per informazioni dettagliate sulla conversione di *in un percorso di file fisico, consultare* Gestione del contenuto *nella* Guida alla configurazione del server *`path`*.

>[!NOTE]
>
>Virgola &#39;,&#39; caratteri non consentiti in *`object.`*

## Formati di file immagine supportati {#section-12c85aead78e4f759856ca9ff10637d7}

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility IC (Image Converter).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato multi-risoluzione PTIF (Dynamic Media pyramid TIFF). L&#39;utilità IC viene utilizzata per creare immagini PTIF da qualsiasi formato di immagine supportato.

## Esempi {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accesso a un&#39;immagine e a un profilo ICC in due diversi cataloghi di immagini**

Recuperare l&#39;immagine &#39;[!DNL myImage]&#39; nel catalogo immagini identificato come &#39;[!DNL myCatalog]&#39; e allegare il profilo ICC &#39;[!DNL sRGB]&#39; che si trova nel catalogo immagini denominato &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilizzo di un singolo catalogo immagini con livelli

**Creare una semplice immagine composita composta da tre livelli, tutti recuperati da &#39;[!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accesso diretto ai file immagine mentre si utilizza ancora un catalogo per fornire gli attributi**

Accedere a [!DNL my/image/path/myImage.tif] utilizzando gli attributi jpg predefiniti configurati in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consultate anche {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilità IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attributo::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)

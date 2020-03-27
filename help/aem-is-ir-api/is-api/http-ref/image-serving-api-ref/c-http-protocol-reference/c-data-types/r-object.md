---
description: Specifier oggetto di origine. Gli oggetti profilo Immagine, SVG e ICC possono essere specificati come voci di catalogo immagini o percorsi di file relativi
seo-description: Specifier oggetto di origine. Gli oggetti profilo Immagine, SVG e ICC possono essere specificati come voci di catalogo immagini o percorsi di file relativi
seo-title: object
solution: Experience Manager
title: object
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# object{#object}

Specifier oggetto di origine. Gli oggetti profilo Immagine, SVG e ICC possono essere specificati come voci di catalogo immagini o percorsi di file relativi

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span></span> </p> </td> 
  <td class="stentry"> <p>nome del catalogo immagini ( <span class="codeph"> attributo::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span></span> </p> </td> 
  <td class="stentry"> <p>id del record di profilo immagine, SVG, modello o ICC nel catalogo immagini specificato, principale o predefinito </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> percorso </span></span> </p> </td> 
  <td class="stentry"> <p>immagine relativa, maschera o percorso e nome del file profilo ICC </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span></span> </p> </td> 
  <td class="stentry"> <p>può verificarsi nel percorso dell'URL principale oppure in un <span class="codeph"> comando src= </span>, <span class="codeph"> mask= </span>, o <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catalogo immagini. Per informazioni dettagliate, consultate Catalogo [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) immagini. Se *`rootId`* viene specificato nel percorso URL, tale catalogo diventa il catalogo ** principale per la richiesta. In caso contrario, il catalogo predefinito viene utilizzato come catalogo principale. Nella stessa richiesta possono essere utilizzati più cataloghi di immagini diversi.

Il server presuppone inizialmente che *`rootId`* venga omesso nei `src=`, `mask=`e `icc=` comandi e tenterà di trovare una voce di catalogo nel catalogo principale. In effetti, il server tenta di utilizzare l&#39;intera *`object`* stringa come *`objId.`*

Se viene trovata una voce di catalogo, questa viene utilizzata; in caso contrario, il server tenterà di trovare una corrispondenza con il *`rootId`* catalogo immagini. Se un catalogo viene identificato, viene ricercato *`objId`*. Se viene trovata una voce, viene utilizzata.

In caso contrario, *`object`* si suppone che sia un percorso di file esplicito. In questo caso, se `attribute::FullMatch` è impostato nel catalogo principale, il catalogo viene ignorato per questo oggetto e viene utilizzato il catalogo predefinito. Se non `attribute::FullMatch` è impostato, il catalogo principale viene utilizzato per un&#39;ulteriore elaborazione.

Sia *`rootId`* che *`objId`* sono con distinzione tra maiuscole e minuscole. *`path`* fa distinzione tra maiuscole e minuscole solo in UNIX.

Se viene specificato un &#39;/&#39; iniziale, la ricerca nel catalogo predefinito viene effettuata al posto del catalogo principale. Questo è utile soprattutto quando un percorso esplicito richiede `default::RootPath` anziché quello del catalogo principale `attribute::RootPath`, ma può anche essere utilizzato per accedere alle voci del catalogo predefinito che altrimenti verrebbero sostituite dalle voci del catalogo principale.

Per informazioni dettagliate sulla *conversione del contenuto* in un percorso di file fisico, consultate la Guida alla configurazione del *server* *`path`* .

>[!NOTE]
>
>I caratteri virgola &#39;,&#39; non sono consentiti in *`object.`*

## Formati di file immagine supportati {#section-12c85aead78e4f759856ca9ff10637d7}

Per un elenco completo dei formati di file supportati, fare riferimento alla descrizione dell&#39;utilità IC (Image Converter).

Le applicazioni che richiedono dati immagine a diverse risoluzioni si comportano nel modo migliore quando si utilizza il formato multirisoluzione TIFF (PTIF) piramidale di Scene7. L’utility IC viene utilizzata per creare immagini PTIF da qualsiasi formato di immagine supportato.

## Esempi {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accesso a un’immagine e a un profilo ICC in due diversi cataloghi di immagini**

Recuperate l’immagine &#39; [!DNL myImage]&#39; nel catalogo immagini identificato come &#39; [!DNL myCatalog]&#39; e allegate il profilo ICC &#39; [!DNL sRGB]&#39; presente nel catalogo immagini denominato &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilizzo di un singolo catalogo immagini con livelli

**Create una semplice immagine composita composta da tre livelli, tutti recuperati da &#39;[!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accesso diretto ai file immagine mentre si continua a utilizzare un catalogo per fornire gli attributi**

Accesso [!DNL my/image/path/myImage.tif], utilizzando gli attributi jpg predefiniti configurati in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consultate anche {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)

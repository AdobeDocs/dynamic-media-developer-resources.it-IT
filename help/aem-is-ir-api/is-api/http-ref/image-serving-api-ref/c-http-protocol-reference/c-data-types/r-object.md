---
description: Specifier dell'oggetto di origine. Gli oggetti profilo immagine, SVG e ICC possono essere specificati come voci del catalogo immagini o percorsi di file relativi
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

Specifier dell&#39;oggetto di origine. Gli oggetti profilo immagine, SVG e ICC possono essere specificati come voci del catalogo immagini o percorsi di file relativi

`*`oggetto`*[/]{[ *`rootId`*/] *`objId`*}| *`percorso`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>nome del catalogo delle immagini ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
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
  <td class="stentry"> <p>può verificarsi nel percorso dell’URL principale o in un <span class="codeph"> src= </span>, <span class="codeph"> mask= maschera </span>, o <span class="codeph"> icc= </span> comando </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catalogo immagini. (vedere [Catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) per i dettagli.) Se *`rootId`* è specificato nel percorso URL, tale catalogo diventa *catalogo principale* per questa richiesta. In caso contrario, viene utilizzato il catalogo predefinito come catalogo principale. Nella stessa richiesta è possibile utilizzare più cataloghi di immagini diversi.

Il server presuppone inizialmente che *`rootId`* viene omesso in `src=`, `mask=`, e `icc=` e tenta di trovare una voce di catalogo nel catalogo principale. Il server tenta di utilizzare l&#39;intero *`object`* stringa come *`objId.`*

Se viene trovata una voce di catalogo, questa viene utilizzata; in caso contrario, il server tenta di trovare una corrispondenza con *`rootId`* di un catalogo immagini. Se viene identificato un catalogo, viene cercato *`objId`*. Se viene trovata una voce e, questa viene utilizzata.

Altrimenti, *`object`* viene considerato un percorso file esplicito. In questo caso, se `attribute::FullMatch` è impostato nel catalogo principale, quindi il catalogo viene ignorato per questo oggetto e viene utilizzato il catalogo predefinito. Se `attribute::FullMatch` non è impostato, il catalogo principale viene utilizzato per l’ulteriore elaborazione.

Entrambi *`rootId`* e *`objId`* sono sensibili all’uso di maiuscole e minuscole. *`path`* distingue tra maiuscole e minuscole solo in UNIX.

Se un&#39;interfaccia `/` viene specificato, viene eseguita la ricerca nel catalogo predefinito anziché nel catalogo principale. Questa funzione è particolarmente utile quando un percorso esplicito richiede `default::RootPath` anziché del catalogo principale `attribute::RootPath`, ma può anche essere utilizzato per accedere alle voci nel catalogo predefinito che altrimenti verrebbero ignorate dalle voci nel catalogo principale.

Fai riferimento a *Gestione del contenuto* nel *Guida alla configurazione del server* per informazioni dettagliate su come *`path`* viene convertito in un percorso di file fisico.

>[!NOTE]
>
>Le virgole &quot;,&quot; non sono consentite in *`object.`*

## Formati di file immagine supportati {#section-12c85aead78e4f759856ca9ff10637d7}

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility IC (Image Converter).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato a più risoluzioni Dynamic Medie pyramid TIFF (PTIF). L&#39;utilità IC viene utilizzata per creare immagini PTIF da qualsiasi formato di immagine supportato.

## Esempi {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accesso a un&#39;immagine e a un profilo ICC in due diversi cataloghi di immagini**

Recupera l&#39;immagine &#39; [!DNL myImage]&#39; nel catalogo immagini identificato come &#39; [!DNL myCatalog]&#39; e allegare il profilo ICC &#39; [!DNL sRGB]&#39; nel catalogo immagini denominato &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilizzo di un singolo catalogo immagini con livelli

**Crea una semplice immagine composita composta da tre livelli, tutti recuperati da &#39; [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accesso diretto ai file immagine mentre si utilizza un catalogo per fornire gli attributi**

Accesso [!DNL my/image/path/myImage.tif], utilizzando gli attributi jpg predefiniti configurati in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consultate anche {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilità IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask= maschera](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)

---
description: Specifier dell'oggetto di origine. Gli oggetti profilo Immagine, SVG e ICC possono essere specificati come voci di catalogo immagini o percorsi di file relativi
solution: Experience Manager
title: oggetto
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---


# object{#object}

Specifier dell&#39;oggetto di origine. Gli oggetti profilo Immagine, SVG e ICC possono essere specificati come voci di catalogo immagini o percorsi di file relativi

`*``*[/]{[ *``*/] *``*}| *`objectIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>nome del catalogo immagini ( <span class="codeph"> attributo::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID del record di profilo immagine, SVG, modello o ICC nel catalogo immagini specificato, principale o predefinito </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>nome e percorso del file di profilo ICC, maschera o immagine relativa </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> oggetto  </span> </span> </p> </td> 
  <td class="stentry"> <p>può verificarsi nel percorso URL principale o in un comando <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> o <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifica un catalogo di immagini. (Per ulteriori informazioni, consulta [Catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) .) Se *`rootId`* è specificato nel percorso URL, tale catalogo diventa il *catalogo principale* per questa richiesta. In caso contrario, il catalogo predefinito viene utilizzato come catalogo principale. Nella stessa richiesta possono essere utilizzati più cataloghi di immagini diversi.

Il server presuppone inizialmente che *`rootId`* sia omesso nei comandi `src=`, `mask=` e `icc=` e che tenti di trovare una voce di catalogo nel catalogo principale. In effetti, il server cerca di utilizzare l&#39;intera stringa *`object`* come *`objId.`*

Se viene trovata una voce di catalogo, questa viene utilizzata; in caso contrario, il server tenta successivamente di corrispondere a *`rootId`* di un catalogo di immagini. Se un catalogo è identificato, viene ricercato *`objId`*. Se viene trovata una voce e viene utilizzata.

In caso contrario, si presume che *`object`* sia un percorso di file esplicito. In questo caso, se `attribute::FullMatch` è impostato nel catalogo principale, il catalogo viene ignorato per questo oggetto e viene utilizzato il catalogo predefinito. Se `attribute::FullMatch` non è impostato, il catalogo principale viene utilizzato per ulteriori elaborazioni.

Sia *`rootId`* che *`objId`* sono sensibili all&#39;uso di maiuscole e minuscole. *`path`* fa distinzione tra maiuscole e minuscole solo in UNIX.

Se è specificato un &#39;/&#39; iniziale, la ricerca verrà eseguita al posto del catalogo principale. Questa funzione è utile soprattutto quando un percorso esplicito richiede `default::RootPath` anziché `attribute::RootPath` del catalogo principale, ma può anche essere utilizzata per accedere alle voci del catalogo predefinito che altrimenti verrebbero sostituite dalle voci del catalogo principale.

Per informazioni dettagliate sulla conversione di *`path`* in un percorso file fisico, fare riferimento a *Gestione dei contenuti* nella *Guida alla configurazione del server*.

>[!NOTE]
>
>I caratteri virgola &#39;,&#39; non sono consentiti in *`object.`*

## Formati di file immagine supportati {#section-12c85aead78e4f759856ca9ff10637d7}

Fare riferimento alla descrizione dell&#39;utilità IC (Image Converter) per un elenco completo dei formati di file supportati.

Le applicazioni che richiedono dati di immagine in più risoluzioni diverse si comportano al meglio quando si utilizza il formato Dynamic Media TIFF (PTIF) a piramide multirisoluzione. L&#39;utilità IC viene utilizzata per creare immagini PTIF da qualsiasi formato immagine supportato.

## Esempi {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accesso a un’immagine e a un profilo ICC in due diversi cataloghi di immagini**

Recupera l&#39;immagine &#39; [!DNL myImage]&#39; nel catalogo immagini identificato come &#39; [!DNL myCatalog]&#39; e allega il profilo ICC &#39; [!DNL sRGB]&#39; che si trova nel catalogo immagini denominato &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Utilizzo di un unico catalogo di immagini con livelli

**Crea un&#39;immagine composita semplice composta da tre livelli, tutti recuperati da &#39;  [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accesso diretto ai file di immagine mentre si utilizza ancora un catalogo per fornire attributi**

Accedi a [!DNL my/image/path/myImage.tif] utilizzando gli attributi jpg predefiniti configurati in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consultate anche {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilità](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attributo::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)

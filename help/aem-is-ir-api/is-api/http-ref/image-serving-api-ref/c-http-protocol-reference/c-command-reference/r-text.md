---
title: text
description: Testo livello. Specifica il testo e il contenuto di formattazione per un livello di testo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# text{#text}

Testo livello. Specifica il testo e il contenuto di formattazione per un livello di testo.

` text= *`stringa`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> stringa </span> </p> </td> 
  <td class="stentry"> <p>Stringa RTF (Rich Text Formatted) o stringa di testo normale. </p> </td> 
 </tr> 
</table>

Tutti i controlli relativi al tipo di carattere, al colore del carattere e alla formattazione di paragrafo vengono eseguiti utilizzando i comandi RTF. Per ulteriori informazioni, consultare [Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`text=` supporta il ridimensionamento automatico del testo per riempire il rettangolo di livello specificato con `size=`.

Vedere [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` supporta il ridimensionamento automatico del livello di testo per adattarlo al testo di cui è stato eseguito il rendering (quando `size=` non è specificato o quando è specificata solo la larghezza). In questo caso è possibile applicare solo uno dei comandi di allineamento RTF `\ql`, `\qr` e `\qc`. In caso contrario, viene restituito un errore.

## Proprietà {#section-8c0f020094a44c6b858454ef91ab4edf}

Attributo livello. Si applica a `layer=0` se `layer=comp`. Si escludono a vicenda con `src=` e `textPs=` nello stesso livello; prevale l&#39;ultima occorrenza di `text=`, `textPs=` e `src=` e determina se si tratta di un livello immagine o testo. Ignorato dai livelli degli effetti.

## Predefinito {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Nessuno.

## Esempio {#section-d011f765ec5c418d814a821019b0eef0}

Vedi gli esempi in [Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) e [Esempio A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-207b779ab67342a5acd343e6bcc749c4}

[Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Posizionamento testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)

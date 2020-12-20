---
description: Testo del livello. Specifica il testo e la formattazione del contenuto per un livello di testo.
seo-description: Testo del livello. Specifica il testo e la formattazione del contenuto per un livello di testo.
seo-title: Testo
solution: Experience Manager
title: Testo
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 4%

---


# Testo{#text}

Testo del livello. Specifica il testo e la formattazione del contenuto per un livello di testo.

` text= *`string`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string  </span> </p> </td> 
  <td class="stentry"> <p>Stringa in formato RTF o in formato RTF. </p> </td> 
 </tr> 
</table>

Tutti i controlli di formattazione di font, colore e paragrafo vengono eseguiti utilizzando i comandi RTF. Per ulteriori informazioni, fare riferimento a [Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`text=` supporta il ridimensionamento automatico del testo per riempire il rettangolo di livello specificato con  `size=`.

Vedere [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` supporta il ridimensionamento automatico del livello di testo per adattarlo al testo di cui è stato effettuato il rendering (se non  `size=` è specificato o se è specificata solo la larghezza). Si noti che in questo caso è possibile applicare solo uno dei comandi di allineamento RTF `\ql`, `\qr` e `\qc`; in caso contrario viene restituito un errore.

## Proprietà {#section-8c0f020094a44c6b858454ef91ab4edf}

Attributo layer. Si applica a `layer=0` se `layer=comp`. Esclusivo reciproco con `src=` e `textPs=` nello stesso livello; l&#39;ultima occorrenza di `text=`, `textPs=` e `src=` prevale e determina se si tratta di un&#39;immagine o di un livello di testo. Ignorato dai livelli degli effetti.

## Predefinito {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Nessuno.

## Esempio {#section-d011f765ec5c418d814a821019b0eef0}

Vedere gli esempi in [Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) e [Esempio A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-207b779ab67342a5acd343e6bcc749c4}

[Formattazione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) testo, posizionamento [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)testo,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)

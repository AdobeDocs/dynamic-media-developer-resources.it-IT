---
title: bgc
description: Visualizza colore di sfondo. Specifica il colore di sfondo dell'immagine composita (immagine di visualizzazione).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

Visualizza colore di sfondo. Specifica il colore di sfondo dell&#39;immagine composita (immagine di visualizzazione).

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> colore</span></span> </p> </td> 
  <td class="stentry"> <p>Valore colore grigio, RGB o CMYK. </p></td> 
 </tr> 
</table>

Specifica un colore di riempimento opaco da utilizzare per lo sfondo della visualizzazione. Visibile solo se l&#39;immagine composita ha aree trasparenti o se l&#39;immagine composita ha proporzioni diverse rispetto al rettangolo di visualizzazione. Ignorato se `fmt=tif-alpha` o `fmt=png-alpha`, o `req=mask`.

>[!NOTE]
>
>Il suffisso colore &#39;s&#39; viene ignorato da `bgc=`. Valori colore specificati con `bgc=` sono sempre associati al rispettivo spazio colore di output.

## Proprietà {#section-b729b50b1ea7433b82ba34ecd61839cd}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, o `fmt=swf-alpha`.

Qualsiasi valore alfa specificato con il colore viene ignorato.

*`color`* si presume che appartenga allo spazio colore di output (come specificato con `icc=`) e deve avere lo stesso tipo di pixel dell&#39;immagine di output. Se i tipi di pixel non corrispondono *`color`* viene convertito utilizzando una conversione naïve.

## Predefinito {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Esempio {#section-7bcdfbc0e1274e86a69d39186b090789}

Specifica un colore di sfondo esplicito per una richiesta di miniature:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Consultate anche {#section-1e55f9f98f1847918a1725836a27cfaa}

[colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)

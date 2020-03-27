---
description: Scala visualizzazione. Consente di ridimensionare l’immagine di cui è stato effettuato il rendering in base al fattore di scala specificato, rispetto alla vignettatura a risoluzione piena.
seo-description: Scala visualizzazione. Consente di ridimensionare l’immagine di cui è stato effettuato il rendering in base al fattore di scala specificato, rispetto alla vignettatura a risoluzione piena.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

Scala visualizzazione. Consente di ridimensionare l’immagine di cui è stato effettuato il rendering in base al fattore di scala specificato, rispetto alla vignettatura a risoluzione piena.

`scl= *`InvoiceFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> movFactor</span></span> </p></td> 
  <td class="stentry"> <p>Fattore di scala inversa (reale, 1,0 o superiore). </p></td> 
 </tr> 
</table>

Se `scl=` viene dopo `wid=` o `hei=` nell’URL, questi comandi vengono annullati e `scl=` definiscono le dimensioni dell’immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` dopo `scl=` l’URL, vengono annullati `scl=` e `wid=`/ `hei=` definiscono le dimensioni dell’immagine restituita dal server.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-170458cbd6984bd59a3434431258b20f}

Può verificarsi ovunque nella richiesta. Ignorato se `wid=` o `hei=` si verifica dopo `scl=` nella sequenza di comando.

Il ridimensionamento dell&#39;immagine con `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta.

## Predefinito {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Se non `wid=`, `hei=` né `scl=` vengono specificati, l&#39;immagine di risposta viene ridimensionata in modo da rientrare nella dimensione definita da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuota, l&#39;immagine di risposta ha le stesse dimensioni dell&#39;immagine di visualizzazione della vignettatura.

## Consultate anche {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)

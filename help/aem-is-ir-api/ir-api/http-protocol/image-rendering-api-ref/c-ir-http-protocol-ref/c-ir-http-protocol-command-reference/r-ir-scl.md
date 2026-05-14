---
title: scl
description: Scala vista. Ridimensiona l’immagine di cui è stato eseguito il rendering in base al fattore di scala specificato, rispetto alla vignettatura a risoluzione completa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
TQID: 'https://experienceleague.adobe.com/HeszuJDuoMh-RTfrnFklpJWqT28PQ74N8GfBe0yZl7k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 1%

---

# scl{#scl}

Scala vista. Ridimensiona l’immagine di cui è stato eseguito il rendering in base al fattore di scala specificato, rispetto alla vignettatura a risoluzione completa.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Fattore di scala inversa (reale, 1,0 o superiore). </p></td> 
 </tr> 
</table>

Se `scl=` viene dopo `wid=` o `hei=` nell&#39;URL, questi comandi vengono annullati e `scl=` definisce la dimensione dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` arriva dopo `scl=` nell&#39;URL, annullano `scl=` e `wid=`/ `hei=` definiscono le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-170458cbd6984bd59a3434431258b20f}

Può verificarsi ovunque all’interno della richiesta. Ignorato se `wid=` o `hei=` si verificano dopo `scl=` nella sequenza di comando.

Il ridimensionamento dell&#39;immagine con `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta.

## Predefinito {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Se `wid=`, `hei=` o `scl=` non sono specificati, l&#39;immagine di risposta viene ridimensionata in base alle dimensioni definite da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l&#39;immagine di risposta ha le stesse dimensioni dell&#39;immagine di visualizzazione della vignettatura.

## Consultate anche {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)

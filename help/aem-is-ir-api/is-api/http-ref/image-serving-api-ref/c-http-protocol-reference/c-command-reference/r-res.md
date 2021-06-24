---
description: Ridimensionamento delle immagini basato sulla risoluzione. Ridimensiona l'immagine alla risoluzione richiesta.
solution: Experience Manager
title: res
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---

# res{#res}

Ridimensionamento delle immagini basato sulla risoluzione. Ridimensiona l&#39;immagine alla risoluzione richiesta.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>risoluzione del target; tipicamente in pixel per pollice (reale). </p> </td> 
 </tr> 
</table>

Il fattore di scala viene calcolato dividendo *`val`* per `catalog::Resolution`. Questo comando non influisce sulla risoluzione di stampa dell&#39;immagine di risposta.

Per utilizzare questa funzione, la risoluzione delle immagini sorgente originali deve essere nota e impostata in `catalog::Resolution`. A seconda dell&#39;applicazione, le unità di risoluzione possono variare. Per texture 2D ripetibili o campioni di materiale, come sfondi o tessuti, la risoluzione può essere espressa in pixel/pollici o pixel/mm. Foto aeree e mappe possono essere meglio servite da pixel/miglia o pixel/km. In ogni caso, le unità utilizzate per `catalog::Resolution` devono essere uguali alle unità utilizzate per `res=`.

Oltre ad ottenere immagini a risoluzioni precise, `res=` può essere utilizzato anche per combinare più immagini con la stessa risoluzione, in modo che gli elementi visibili in queste immagini siano in proporzione precisa l&#39;uno con l&#39;altro.

>[!NOTE]
>
>Normalmente, un&#39;immagine composita viene ridimensionata in base alle dimensioni della visualizzazione di destinazione (specificate da `wid=`, `hei=` o `attribute::DefaultPix`) prima che venga restituita al client. Per evitare questo ridimensionamento e ottenere un&#39;immagine con la risoluzione esatta specificata da `res=`, può essere necessario disabilitare la modifica in scala della visualizzazione specificando esplicitamente `scl=1`. Questo indica al server di ritagliare l&#39;immagine composita in base alle dimensioni della visualizzazione di destinazione, anziché ridimensionarla.

## Proprietà {#section-fdbd16e59cff4952a3717146bc91412e}

Attributo immagine/maschera di origine. Ignorato dai livelli non associati a un&#39;immagine sorgente o a una maschera. Applicato al livello 0 è specificato per `layer=comp`. Ignorato se per lo stesso livello è specificato `scale=` o `size=` .

## Predefinito {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Se non viene specificato, `scale=` o `size=` determina il fattore di scala oppure, se non viene specificato nessuno dei due, l&#39;immagine viene utilizzata senza ridimensionamento.

## Esempio {#section-eb06f333e08e4247971fb1b18922597b}

Recupera un&#39;immagine di texture a una risoluzione dell&#39;oggetto di 12 pixel/pollice per l&#39;utilizzo con Image Rendering o Image Authoring. Specifichiamo il formato PNG senza perdite e il ricampionamento di qualità migliore per la migliore qualità possibile,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Consultate anche {#section-1f8a8f11772e493ca803c4511f397a11}

[catalogo::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)

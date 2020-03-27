---
description: Scala visualizzazione. Ridimensiona in scala l’immagine composita per l’inverso di vFactor.
seo-description: Scala visualizzazione. Ridimensiona in scala l’immagine composita per l’inverso di vFactor.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

Scala visualizzazione. Ridimensiona in scala l’immagine composita per l’inverso di vFactor.

`scl= *`InvoiceFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> InvoiceFactor</span> </p> </td> 
  <td class="stentry"> <p>Fattore di scala inversa (reale maggiore di 0,0). </p></td> 
 </tr> 
</table>

No scaling is applied when `scl=1`. *`invFactor`* con dimensioni maggiori di 1,0 e minori di 1,0 l’immagine composita viene ingrandita.

Se `scl=` è specificata e `wid=` e/o `hei=` è presente, l&#39;immagine viene ritagliata `wid=` e/o `hei=` dopo il ridimensionamento.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-60af012719db477db4a4703e9a6da5f5}

Visualizza attributo. Si applica indipendentemente dall’impostazione del livello corrente.

## Predefinito {#section-32502fa218a24e1f9c65f41c0260b56a}

Se non `wid=`, `hei=`e non `scl=` vengono specificati, l&#39;immagine di risposta avrà la dimensione dell&#39;immagine composita o, `attribute::DefaultPix`se inferiore, quella dell&#39;immagine.

## Esempio {#section-a33f6239476a4b438d939656ad99aa76}

Per un’applicazione comune di [, vedere l’esempio in](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) rotate= `scl=`.

## Consultate anche {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

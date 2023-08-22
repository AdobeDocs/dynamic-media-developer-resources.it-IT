---
title: scl
description: Scala vista. Ridimensiona l'immagine composita in base all'inverso di invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---

# scl{#scl}

Scala vista. Ridimensiona l&#39;immagine composita in base all&#39;inverso di invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Fattore di scala inversa (reale maggiore di 0,0). </p></td> 
 </tr> 
</table>

Non viene applicata alcuna scala quando `scl=1`. *`invFactor`* dimensioni maggiori di 1.0 per il ridimensionamento e dimensioni minori di 1.0 per l&#39;ingrandimento dell&#39;immagine composita.

Se `scl=` è specificato, e `wid=` e/o `hei=` sono presenti, l&#39;immagine viene ritagliata in `wid=` e/o `hei=` dopo il ridimensionamento.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-60af012719db477db4a4703e9a6da5f5}

Attributo vista. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-32502fa218a24e1f9c65f41c0260b56a}

Se nessuno dei due `wid=`, `hei=`, né `scl=` , l&#39;immagine di risposta avrà le dimensioni dell&#39;immagine composita oppure `attribute::DefaultPix`, a seconda di quale dei due valori è inferiore.

## Esempio {#section-a33f6239476a4b438d939656ad99aa76}

Vedi l’esempio in [rotate= ruota](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) per un&#39;applicazione comune `scl=`.

## Consultate anche {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

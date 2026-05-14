---
title: scl
description: Scala vista. Ridimensiona l'immagine composita in base all'inverso di invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
TQID: 'https://experienceleague.adobe.com/Evu9NXhBJE-Z4inLuaWJkiJikd2yslhec5q7C2azxKw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 2%

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

Nessuna scala applicata quando `scl=1`. Un valore *`invFactor`* maggiore di 1,0 viene ridimensionato e minore di 1,0 ingrandisce l&#39;immagine composita.

Se si specifica `scl=` e sono presenti anche `wid=` e/o `hei=`, l&#39;immagine viene ritagliata in `wid=` e/o `hei=` dopo il ridimensionamento.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-60af012719db477db4a4703e9a6da5f5}

Attributo vista. Viene applicato indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-32502fa218a24e1f9c65f41c0260b56a}

Se non si specificano né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta ha le dimensioni dell&#39;immagine composita o `attribute::DefaultPix`, a seconda di quale dei due valori è più basso.

## Esempio {#section-a33f6239476a4b438d939656ad99aa76}

Vedere l&#39;esempio in [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) per un&#39;applicazione comune di `scl=`.

## Consultate anche {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

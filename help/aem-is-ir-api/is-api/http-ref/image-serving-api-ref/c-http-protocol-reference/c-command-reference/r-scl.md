---
description: Vista scala. Consente di ridimensionare l'immagine composita in base all'inverso di vFactor.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# scl{#scl}

Vista scala. Consente di ridimensionare l&#39;immagine composita in base all&#39;inverso di vFactor.

`scl= *`InventoryFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> InventoryFactor</span> </p> </td> 
  <td class="stentry"> <p>Fattore di scala inversa (reale maggiore di 0,0). </p></td> 
 </tr> 
</table>

Non viene applicato alcun ridimensionamento quando `scl=1`. *`invFactor`* ingrandisce l&#39;immagine composita con dimensioni superiori a 1.0 e dimensioni inferiori a 1.0.

Se è specificato `scl=` e sono presenti anche `wid=` e/o `hei=`, l&#39;immagine viene ritagliata a `wid=` e/o `hei=` dopo il ridimensionamento.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-60af012719db477db4a4703e9a6da5f5}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-32502fa218a24e1f9c65f41c0260b56a}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta avrà le dimensioni dell&#39;immagine composita o `attribute::DefaultPix`, a seconda di quale dimensione è inferiore.

## Esempio {#section-a33f6239476a4b438d939656ad99aa76}

Vedi l&#39;esempio in [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) per un&#39;applicazione comune di `scl=`.

## Consultate anche {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

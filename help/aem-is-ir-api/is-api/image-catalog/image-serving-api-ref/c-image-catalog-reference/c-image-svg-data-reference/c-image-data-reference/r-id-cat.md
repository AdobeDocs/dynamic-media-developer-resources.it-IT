---
description: Identificatore record catalogo
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 4%

---

# ID {#id}

Valore chiave di indice in base al quale i record nel file di dati immagine vengono cercati da [!DNL Platform Server].

In genere, se una SKU ha più immagini, si tratta di un identificatore immagine breve e univoco, ad esempio un numero SKU, che può anche contenere una sorta di suffisso immagine. Può anche essere una stringa più complessa, più simile a un percorso di file, per supportare una facile installazione retroattiva dei siti web con Image Server.

## Proprietà {#id-properties}

Stringa di testo. Obbligatorio. Chiave di indice primaria per la tabella dati immagine. Ogni valore catalog::Id deve essere univoco all&#39;interno della tabella.

## Predefinito {#id-default}

Nessuno.

## Consultate anche {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)

---
description: Percorso file immagine.
solution: Experience Manager
title: Percorso
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: 'https://experienceleague.adobe.com/dpQY2E7P1LzEhYg05p6C5MQRvx9jgdMB-GrBReIIqig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 2%

---

# Percorso{#path}

Percorso file immagine.

Percorso e nome relativi o assoluti del file immagine di origine associato a questo record catalogo. Per trovare il file di dati, il server utilizza le regole di risoluzione dei percorsi descritte in Gestione dei dati di Source.

## Proprietà {#path-properties}

Stringa di testo. Obbligatorio per i record immagine. Può essere vuoto per i record modello. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#path-supported-image-file-formats}

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility Image Converter (IC).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato multi-risoluzione PTIFF (Dynamic Media pyramid TIFF). L&#39;utilità IC viene utilizzata per creare immagini PTIFF da qualsiasi formato di immagine supportato.

## Predefinito {#path-default}

Nessuno.

## Consultate anche {#path-seealso}

[Utilità IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->

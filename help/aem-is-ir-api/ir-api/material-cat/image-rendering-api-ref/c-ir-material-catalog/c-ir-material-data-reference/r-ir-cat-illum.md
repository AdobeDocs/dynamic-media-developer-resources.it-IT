---
title: Illum
description: Selettore mappa di illuminazione. Consente di selezionare in modo esplicito la mappa di illuminazione da utilizzare per il rendering di questo materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# Illum{#illum}

Selettore mappa di illuminazione. Consente di selezionare in modo esplicito la mappa di illuminazione da utilizzare per il rendering di questo materiale.

## Proprietà {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Impostate questo valore su -1 per selezionare automaticamente la mappa di illuminazione in base al valore di catalog::Gloss.

Impostare su 0, 1 o 2 per selezionare la mappa di illuminazione A, B o C. Il renderer sceglie la mappa di illuminazione più vicina disponibile nella vignettatura.

## Predefinito {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (selezione automatica)

## Consultate anche {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)

---
description: Percorso file vignetta. Percorso relativo e nome di un file di vignetta.
solution: Experience Manager
title: Percorso
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 10%

---


# Percorso{#path}

Percorso file vignetta. Percorso relativo e nome di un file di vignetta.

Il server combina questo valore con `attribute::RootPath` per creare il percorso effettivo del file di vignetta. Può anche essere un percorso assoluto.

## Proprietà {#section-b3b295feac084b56bd8a153c04987153}

Stringa di testo. Facoltativo. Se specificato, deve essere un percorso di file relativo o assoluto valido. Se vuoto, `vignette::Modifier` deve includere il comando `vignette=`.

## Predefinito {#section-a1d2133856084eb79a5be8230a4b38fd}

Nessuno.

## Consultate anche {#section-177131dad5804964bfb8957c1f6e5191}

[attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)

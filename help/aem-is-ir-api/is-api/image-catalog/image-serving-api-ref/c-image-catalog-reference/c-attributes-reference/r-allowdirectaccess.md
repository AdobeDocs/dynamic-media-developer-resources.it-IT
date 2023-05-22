---
description: Consente l’accesso diretto alle risorse basate su percorsi.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Consente l’accesso diretto alle risorse basate su percorsi.

Quando questo attributo viene definito, l&#39;accesso basato su percorso è consentito o limitato per i tipi di oggetto specificati, a seconda che `include` o `exclude` parola chiave utilizzata.

>[!NOTE]
>
>Se il `AllowDirectAccess` non è specificato, il valore predefinito è `exclude`.

* `include` consente l&#39;accesso per i tipi di oggetto specificati e limita l&#39;accesso per tutti gli altri.
* `exclude` limita l&#39;accesso per i tipi di oggetto specificati e consente l&#39;accesso per tutti gli altri.

Se nessuno dei due `include` né `exclude` è specificato, `include` viene presupposto.

È possibile controllare i seguenti tipi:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Esempi {#section-4c3765ebaa4245a799b454fc196f9237}

* Consenti accesso diretto solo per `IS` e `STATIC` tipi di oggetto

   `AllowDirectAccess=include:IS,STATIC`

* Consenti accesso diretto per tutti i tipi di oggetto eccetto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Consenti accesso diretto per *no* tipi di oggetto (ovvero non includere nessuno)

   `AllowDirectAccess=include:`

* Consenti accesso diretto per *tutto* tipi di oggetto (ovvero escludi nessuno)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` non è presente, `include` si presume)

   `AllowDirectAccess=IS,STATIC`

   Si tratta del valore predefinito utilizzato se `AllowDirectAccess` attributo non specificato per questa società.

* Non includere nessuno, equivalente a `include:` (se `include`/ `exclude` non è presente, `include` si presume)

   `AllowDirectAccess=`

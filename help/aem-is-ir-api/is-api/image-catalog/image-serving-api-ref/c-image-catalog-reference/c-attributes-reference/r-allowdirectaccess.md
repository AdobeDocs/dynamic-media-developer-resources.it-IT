---
description: Consenti accesso diretto alle risorse basate su percorsi.
seo-description: Consenti accesso diretto alle risorse basate su percorsi.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Consenti accesso diretto alle risorse basate su percorsi.

Quando questo attributo è definito, l&#39;accesso basato sul percorso è consentito o limitato per i tipi di oggetto specificati, a seconda che venga utilizzata la parola chiave `include` o `exclude`.

>[!NOTE]
>
>Se l&#39;attributo `AllowDirectAccess` non è specificato, il valore predefinito è `exclude`.

* `include` consente l&#39;accesso ai tipi di oggetto specificati e limita l&#39;accesso a tutti gli altri.
* `exclude` limita l&#39;accesso per i tipi di oggetto specificati e consente l&#39;accesso per tutti gli altri.

Se non viene specificato né `include` né `exclude`, si assume `include`.

È possibile controllare i seguenti tipi:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Esempi {#section-4c3765ebaa4245a799b454fc196f9237}

* Consenti accesso diretto solo per i tipi di oggetto `IS` e `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Consenti accesso diretto a tutti i tipi di oggetti eccetto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Consenti accesso diretto per i tipi di oggetto *no* (ovvero includi nessuno)

   `AllowDirectAccess=include:`

* Consenti accesso diretto per i tipi di oggetto *all* (ovvero escludi nessuno)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` non è presente, si presume `include`)

   `AllowDirectAccess=IS,STATIC`

   Si noti che è il valore predefinito utilizzato se l&#39;attributo `AllowDirectAccess` non è specificato per questa società.

* Includi nessuno, equivalente a `include:` (se `include`/ `exclude` non è presente, si presume `include`)

   `AllowDirectAccess=`


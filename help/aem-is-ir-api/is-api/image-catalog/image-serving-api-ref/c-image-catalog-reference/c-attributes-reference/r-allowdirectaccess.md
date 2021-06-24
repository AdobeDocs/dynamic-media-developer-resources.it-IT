---
description: Consenti accesso diretto alle risorse basate su percorsi.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '166'
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

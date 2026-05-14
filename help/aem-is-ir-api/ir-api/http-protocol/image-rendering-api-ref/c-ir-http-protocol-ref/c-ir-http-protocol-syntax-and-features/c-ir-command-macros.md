---
title: Macro dei comandi
description: Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Macro dei comandi{#command-macros}

Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** nome macro

Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di materiale o al catalogo predefinito.

*[!DNL name]* non fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caratteri.

Richiama le macro in qualsiasi punto di una richiesta dopo il punto &#39;?&#39; o in qualsiasi punto di un campo `vignette::Modifier`. Le macro possono rappresentare solo uno o più comandi di Image Rendering e devono essere separate da altri comandi con separatori &#39;&amp;&#39;.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro ignorano gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo flusso di lavoro è diverso da `vignette::Modifier`, dove i comandi nella stringa di richiesta sovrascrivono i comandi nella stringa `vignette::Modifier`, indipendentemente dalla posizione nella richiesta.

Le macro di comando non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per passare i valori dalla richiesta alla macro.

Le macro non possono essere nidificate.

**Esempio**

Le macro possono essere utili se gli stessi comandi o attributi devono essere applicati a diverse immagini sottoposte a rendering.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

È possibile definire una macro per gli attributi comuni:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro viene utilizzata nel modo seguente:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Poiché `qlt=` è diverso per la terza richiesta, il software sostituisce il valore dopo il richiamo della macro (specificando `qlt=` *before* `$render$`non è efficace).

**Vedere anche**

`catalog::MacroFile`, `catalog::Modifier`, riferimento definizione macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

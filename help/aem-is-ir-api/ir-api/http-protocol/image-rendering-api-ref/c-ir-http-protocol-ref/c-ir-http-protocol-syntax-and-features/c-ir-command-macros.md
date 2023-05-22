---
title: Macro dei comandi
description: Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Macro dei comandi{#command-macros}

Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.

`$ *[!DNL name]*$`

** *[!DNL name]* Nome ** macro

Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di materiale o al catalogo predefinito.

*[!DNL name]* non fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &quot;-&quot;, &quot;_&quot; e &quot;.&quot; caratteri.

Richiama le macro in qualsiasi punto di una richiesta dopo il punto interrogativo &#39;?&#39; o in qualsiasi punto di una `vignette::Modifier` campo. Le macro possono rappresentare solo uno o più comandi di Image Rendering e devono essere separate da altri comandi con separatori &#39;&amp;&#39;.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro ignorano gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo flusso di lavoro è diverso da `vignette::Modifier`, dove i comandi nella stringa di richiesta sostituiscono i comandi nella `vignette::Modifier` indipendentemente dalla posizione nella richiesta.

Le macro di comando non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per passare i valori dalla richiesta alla macro.

Le macro non possono essere nidificate.

**Esempio**

Le macro possono essere utili se gli stessi comandi o attributi devono essere applicati a diverse immagini sottoposte a rendering.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

È possibile definire una macro per gli attributi comuni:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro viene utilizzata nel modo seguente:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Perché `qlt=` è diverso per la terza richiesta, il software sostituisce il valore dopo che la macro è stata richiamata (specificando `qlt=` *prima di* `$render$`è inefficace).

**Consultate anche**

`catalog::MacroFile`, `catalog::Modifier`, Riferimento definizione macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

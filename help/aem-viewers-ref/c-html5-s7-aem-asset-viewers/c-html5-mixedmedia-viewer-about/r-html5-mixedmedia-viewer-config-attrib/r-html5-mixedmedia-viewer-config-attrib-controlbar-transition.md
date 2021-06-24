---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Utilizza <span class="codeph"> none</span> per visualizzare e nascondere istantaneamente. Utilizza <span class="codeph"> dissolvenza</span> per fornire un effetto graduale di dissolvenza in entrata e in uscita. </p> <p>La dissolvenza non è supportata in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardare</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e la barra di controllo del tempo nascosta. </p> <p> Se è impostato su <span class="codeph"> -1</span> il componente non attiva mai il suo effetto di visualizzazione automatica e rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta la durata in secondi dell'animazione di dissolvenza in entrata e in uscita. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`

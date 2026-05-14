---
title: ControlBar.transition
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
TQID: 'https://experienceleague.adobe.com/mTLUrXKC7m8pIC5Sqoor0M-N-vmwlZzM9WxnvwzlqD8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per Visualizzatore video interattivo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durata`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Imposta su <span class="codeph"> none</span> per mostrare/nascondere subito. </p> <p>Impostare su <span class="codeph"> dissolvenza</span> per ottenere un effetto di dissolvenza graduale in entrata/in uscita. Non supportato in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e quando la barra di controllo viene nascosta. Se è impostato su <span class="codeph"> -1</span>, il componente non attiva mai l'effetto Nascondi automatico e rimane quindi sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durata <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata/in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

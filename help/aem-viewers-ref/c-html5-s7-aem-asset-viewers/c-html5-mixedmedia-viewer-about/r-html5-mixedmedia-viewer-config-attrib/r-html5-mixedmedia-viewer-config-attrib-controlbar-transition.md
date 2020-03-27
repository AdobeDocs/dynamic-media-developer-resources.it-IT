---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.Transition
solution: Experience Manager
title: ControlBar.Transition
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.Transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohidedurata`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Utilizzate <span class="codeph"> none</span> per visualizzare e nascondere in modo istantaneo. Usate <span class="codeph"> la dissolvenza</span> per ottenere un effetto graduale di dissolvenza in entrata e in uscita. </p> <p>La dissolvenza non è supportata in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il tempo in secondi tra l'ultimo evento mouse/tocco registrato dalla barra di controllo e quello nascosto dalla barra di controllo tempo. </p> <p> Se è impostato su <span class="codeph"> -1</span> , il componente non attiva mai l’effetto Nascondi automatico e rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta la durata dell'animazione di dissolvenza in entrata e in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`

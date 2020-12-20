---
description: Il visualizzatore visualizza le aree dei risultati della ricerca sopra la visualizzazione principale per evidenziare parole o frasi trovate nel catalogo.
seo-description: Il visualizzatore visualizza le aree dei risultati della ricerca sopra la visualizzazione principale per evidenziare parole o frasi trovate nel catalogo.
seo-title: Effetto Ricerca
solution: Experience Manager
title: Effetto Ricerca
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Effetto di ricerca{#search-effect}

Il visualizzatore visualizza le aree dei risultati della ricerca sopra la visualizzazione principale per evidenziare parole o frasi trovate nel catalogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto delle aree dei risultati della ricerca è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Sfondo dell'area dei risultati della ricerca. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le aree dei risultati di ricerca con un riempimento giallo semi-trasparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```


---
title: Effetto di ricerca
description: Il visualizzatore visualizza le aree dei risultati di ricerca sopra la visualizzazione principale per evidenziare le parole o le frasi trovate nel catalogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Effetto di ricerca{#search-effect}

Il visualizzatore visualizza le aree dei risultati di ricerca sopra la visualizzazione principale per evidenziare le parole o le frasi trovate nel catalogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto delle aree dei risultati di ricerca è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> sfondo </span> </p> </td> 
   <td colname="col2"> <p>Sfondo dell'area dei risultati di ricerca. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le aree dei risultati di ricerca con un riempimento giallo semitrasparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

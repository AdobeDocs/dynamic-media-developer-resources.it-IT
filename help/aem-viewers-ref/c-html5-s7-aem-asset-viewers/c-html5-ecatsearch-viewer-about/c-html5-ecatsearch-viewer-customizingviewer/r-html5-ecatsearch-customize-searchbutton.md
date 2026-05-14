---
title: Pulsante Cerca
description: Pulsante Cerca
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ede7d887-526b-4e00-9885-166dc37627aa
TQID: 'https://experienceleague.adobe.com/4isGidoN0mJG46pDeAmgLqLr-8SZihdjUBEJ4HkBKVU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# Pulsante Cerca{#search-button}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto del pulsante è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7searchbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore </span> </p> </td> 
   <td colname="col2"> <p> Scostamento dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p> Distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo se questo pulsante è il primo di una riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta i selettori di attributi `state` e `selected`, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi.
>
>In particolare, `selected='false'` corrisponde allo stato iniziale del pulsante di scorrimento e `selected='true'` corrisponde allo stato in cui è attivo il pannello di ricerca.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un pulsante di ricerca di 28 x 28 pixel e visualizzare un&#39;immagine diversa per ciascuno dei quattro stati del pulsante, se selezionato o non selezionato.

```
.s7ecatalogsearchviewer .s7searchbutton{ 
 margin-top: 4px; 
 margin-left: 10px; 
 width:28px; 
 height:28px;  
 display: inline-block; 
 background-size:contain; 
} 
 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/Search_dark_up.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/Search_dark_down.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/Search_dark_over.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png);  
}
```

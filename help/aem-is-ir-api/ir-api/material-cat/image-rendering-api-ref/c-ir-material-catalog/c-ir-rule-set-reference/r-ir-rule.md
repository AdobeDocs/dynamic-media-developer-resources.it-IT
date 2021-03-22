---
description: Elemento della regola di richiesta. Uno o più sono facoltativi nell’elemento <ruleset> .
seo-description: Elemento della regola di richiesta. Uno o più sono facoltativi nell’elemento <ruleset> .
seo-title: regola
solution: Experience Manager
title: regola
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---


# rule{#rule}

Elemento della regola di richiesta. Uno o più sono facoltativi nell’elemento `<ruleset>`.

## Attributi {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Facoltativo. Il valore predefinito è &quot;break&quot;.

` Name=" *``*"` textOptional. Utilizzato per identificare l&#39;elemento `<rule>` nei registri di debug e nei messaggi di errore.

Inoltre, gli elementi `<rule>` possono definire uno qualsiasi dei seguenti attributi in qualsiasi combinazione. Se specificato e la regola corrisponde correttamente, sostituiscono gli attributi di catalogo corrispondenti per questa richiesta.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Attributo catalogo immagini corrispondente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attributo::DefautPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attributo::ErrorImage  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Scadenza  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attributo::Scadenza  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attributo::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attributo::RootUrl  </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori informazioni, consulta la descrizione dell’attributo del catalogo immagini corrispondente.

L&#39;attributo Scadenza sostituisce solo il valore dell&#39;attributo predefinito; viene ignorato se alla richiesta viene applicato un valore specifico `catalog::Expiration`.

## Dati {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facoltativo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facoltativo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facoltativo. </p> </td> 
 </tr> 
</table>

## Note {#section-a27b91f9a03047c0bb7edc0967fb4216}

Se sono specificati sia `<expression>` che `<substitution>` e non vengono utilizzate le sottostringhe acquisite, la prima sottostringa corrispondente viene sostituita con `<substitution>`.

Se `<expression>` non è specificato, qualsiasi percorso corrisponderà e `<substitution>` viene aggiunto alla fine del percorso.

Se `<substitution>` non è specificato, la sottostringa corrispondente viene rimossa.

Il valore `<addressfilter>` viene applicato solo quando si verifica una corrispondenza e prima che vengano applicate le regole di query.

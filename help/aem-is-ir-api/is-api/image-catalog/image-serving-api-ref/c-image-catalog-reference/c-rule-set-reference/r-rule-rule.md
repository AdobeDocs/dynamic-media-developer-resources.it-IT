---
title: regola
description: Elemento regola di richiesta. Una o più regole sono facoltative nell'elemento <set di regole>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---

# regola{#rule}

Elemento regola di richiesta. Una o più regole sono facoltative nell&#39;elemento `<ruleset>`.

## Attributi {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: facoltativo. Il valore predefinito è &quot;break&quot;.

`Replace = "first" | "all"`: facoltativo. Il valore predefinito è &quot;first&quot;.

`RequestType` = *&quot;`types`&quot;*: facoltativo. Specifica a quale contesto di input si applica la regola. *`types`* è un elenco separato da virgole, che può includere uno o più token elencati nella tabella seguente. Se `RequestType` non è specificato, la regola si applica alle richieste ricevute in tutti i contesti supportati.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>token</b> </p> </th> 
   <th class="entry"> <p><b>Contesto</b> </p> </th> 
   <th class="entry"> <p><b>Descrizione</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> è </span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Applicato alle richieste Image Server </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Applicato alle richieste di Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> statico</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Applicato alle richieste di contenuto statico </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: facoltativo. Utilizzato per identificare l&#39;elemento `<rule>` nei registri di debug e nei messaggi di errore.

`  *`Attributo`* ="value"`: facoltativo. Gli elementi `<rule>` possono definire i seguenti attributi in qualsiasi combinazione. Se specificato e la regola viene trovata correttamente, ignorano gli attributi di catalogo corrispondenti per questa richiesta. Il valore predefinito è `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> Attributo </span> </b> di <b> <span class="varname"> </th> 
   <th class="entry"> <p>Attributo catalogo immagini corrispondente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p>Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local">::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p>Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local">::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Scadenza <span class="codeph"></span> </p> </td> 
   <td> <p> Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local">::Scadenza</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p>Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local">::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local">::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local">::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local">::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> PercorsoSalvataggio</span> </p> </td> 
   <td> <p> Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local">::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p>Attributo <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local">::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori informazioni, consulta la descrizione dell’attributo del catalogo immagini corrispondente.

Gli attributi di scadenza sostituiscono solo i valori di attributo predefiniti. Se alla richiesta viene applicato un valore `catalog::Expiration` specifico, l&#39;override verrà ignorato.

## Dati {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;espressione&gt;</span> </p></td> 
  <td class="stentry"> <p>Facoltativo </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;sostituzione&gt;</span> </p></td> 
  <td class="stentry"> <p>Facoltativo </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>Facoltativo </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;intestazione&gt;</span> </p></td> 
  <td class="stentry"> <p>Facoltativo </p></td> 
 </tr> 
</table>

## Note {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Se sono specificati sia `<expression>` che `<substitution>` e le sottostringhe acquisite non vengono utilizzate, la prima sottostringa corrispondente viene sostituita con `<substitution>`.

Se `<expression>` non è specificato, nessun percorso corrisponde e `<substitution>` viene aggiunto alla fine del percorso.

Se `<substitution>` non è specificato, non si verifica alcuna trasformazione del percorso o della query, ma tutti gli attributi di catalogo specificati vengono ignorati. Se `<substitution>` è vuoto, la sottostringa corrispondente viene rimossa.

`<addressfilter>` viene applicato solo quando si verifica una corrispondenza e prima dell&#39;applicazione delle regole di query.

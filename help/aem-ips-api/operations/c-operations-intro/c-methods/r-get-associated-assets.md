---
description: Ottiene le risorse associate a una risorsa specificata e i dettagli sulla relativa relazione.
solution: Experience Manager
title: getAssociatedAssets
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 6%

---


# getAssociatedAssets{#getassociatedassets}

Ottiene le risorse associate a una risorsa specificata e i dettagli sulla relativa relazione.

Sintassi

## Tipi di utenti autorizzati {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Input (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Gestisci l’azienda proprietaria della risorsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Gestione risorse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matrice di campi di risposta desiderata. Vedi response- FieldArray/excludeFieldArray nell'introduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matrice dei campi di risposta esclusi. Vedi response- FieldArray/excludeFieldArray nell'introduzione. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse set e template contenenti la risorsa specifica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> MemberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse contenute nel set o nella risorsa modello specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse a cui viene fatto riferimento in un URL di livello o di modello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse proprietarie della risorsa specificata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivatoArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse utilizzate per generare la risorsa specificata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Il <span class="codeph"> generatorArray</span> elenca il modo in cui è stata creata la risorsa. Ad esempio, se <span class="codeph"> assetHandler</span> è una pagina di immagine di un PDF, questo conterrà lo strumento di elaborazione PDF e farà riferimento alla risorsa PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>La <span class="codeph"> generateArray</span> inverte il modo in cui è stata creata la risorsa. Ad esempio, il <span class="codeph"> generateArray</span> potrebbe contenere l’elenco di immagini generate da questo <span class="codeph"> assetHandler</span> se si tratta di una risorsa PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:Risorsa</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Informazioni sulla risorsa principale associata alla risorsa richiesta. Se non viene assegnata alcuna risorsa miniatura, il campo viene omesso nella risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puoi utilizzare i parametri `responseFieldArray` o `excludeFieldArray` per limitare la dimensione della risposta. In particolare, gli elementi `GenerationInfo` restituiti in `generatorArray` o `generatedArray` sono predefiniti per includere sia i record di origine che quelli di risorsa generati. Per un tipo di risorsa PDF, questo comportamento genera indesiderate copie multiple del record di risorse PDF &quot;originator&quot; nella risposta. Puoi eliminare questo problema aggiungendo `generatedArray/items/originator` a `excludeFieldArray`. In alternativa, puoi specificare un elenco esplicito di campi di risposta da includere in `responseFieldArray`.

## Esempi {#section-8946ea4b9cb94912a8408249c897f192}

L’esempio di base seguente è una richiesta per l’handle del generatore per un’immagine estratta da un PDF. Include un elemento `containerArray` di lunghezza uno con `assetHandle` del PDF.

**Request Contents (Richiesta contenuto)**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Risposta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

L’inverso dell’esempio precedente è il seguente:

**Request Contents (Richiesta contenuto)**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Risposta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

In questo esempio successivo, viene aggiunto un gruppo a una società con `groupHandleArray`. In questo esempio viene utilizzato un solo gruppo.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Risposta**

Nessuno.

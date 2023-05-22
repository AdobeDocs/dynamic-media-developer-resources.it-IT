---
title: Caricamento di risorse tramite HTTP POST nel servlet UploadFile
description: Caricamento delle risorse in [!DNL Dynamic Media] Classic include una o più richieste HTTP POST che impostano un processo per coordinare tutte le attività di registro associate ai file caricati.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# Caricamento di risorse tramite HTTP POST nel servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Il caricamento di risorse in Dynamic Media Classic prevede una o più richieste HTTP POST che impostano un processo per coordinare tutte le attività di registro associate ai file caricati.

Utilizza il seguente URL per accedere a UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Tutte le richieste di POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

**Accedere agli URL per le aree geografiche di Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Località geografica </p> </th> 
   <th colname="col2" class="entry"> <p>URL di produzione </p> </th> 
   <th colname="col3" class="entry"> <p>URL di staging (utilizzato per sviluppo e test di pre-produzione) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nord America </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Medio Oriente, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Giappone/Asia Pacifico </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Flusso di lavoro del processo di caricamento {#section-873625b9512f477c992f5cdd77267094}

Il processo di caricamento è costituito da uno o più POST HTTP che utilizzano un `jobHandle` per correlare l’elaborazione allo stesso processo. Ogni richiesta è `multipart/form-data` codificato ed è costituito dalle seguenti parti di forma:

>[!NOTE]
>
>Tutte le richieste di POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

|  parte modulo HTTP POST  |  Descrizione  |
|---|---|
| `auth`  |   Obbligatorio. Documento di intestazione di autenticazione XML che specifica le informazioni di autenticazione e client. Consulta **Richiedi autenticazione** in [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Facoltativo. Con ogni richiesta POST puoi includere uno o più file da caricare. Ogni parte di file può includere un parametro filename nell&#39;intestazione Content-Disposition utilizzata come nome file di destinazione in IPS se non `uploadPostParams/fileName` è specificato il parametro. |

|  parte modulo HTTP POST   |  uploadPostParams, nome elemento   |  Tipo   |  Descrizione   |
|---|---|---|---|
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento)   |   `companyHandle`  |  `xsd:string`  | Obbligatorio. Gestisce alla società in cui viene caricato il file.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `jobName`  |  `xsd:string`  | o `jobName` o `jobHandle` è obbligatorio. Nome del processo di caricamento.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `jobHandle`  |  `xsd:string`  | o `jobName` o `jobHandle` è obbligatorio. Gestisci un processo di caricamento avviato in una richiesta precedente.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `locale`  |  `xsd:string`  | Facoltativo. Lingua e codice del paese per la localizzazione.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `description`  |  `xsd:string`  | Facoltativo. Descrizione del processo.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `destFolder`  |  `xsd:string`  | Facoltativo. Percorso della cartella di destinazione per il prefisso di una proprietà del nome file, in particolare per i browser e altri client che potrebbero non supportare percorsi completi in un nome file.  |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `fileName`  |  `xsd:string`  | Facoltativo. Nome del file di destinazione. Sostituisce la proprietà del nome file. |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `endJob`  |  `xsd:boolean`  | Facoltativo. Il valore predefinito è false. |
| `uploadParams` (Obbligatorio. Un XML `uploadParams` documento che specifica i parametri di caricamento) | `uploadParams`  |  `types:UploadPostJob`  | Facoltativo se si tratta di una richiesta successiva per un processo attivo esistente. Se è presente un processo, `uploadParams` viene ignorato e vengono utilizzati i parametri di caricamento del processo esistenti. Consulta [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

All&#39;interno del `<uploadPostParams>` blocco è il `<uploadParams>` blocco che indica l’elaborazione dei file inclusi.

Consulta [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Anche se si può supporre che il `uploadParams` Il parametro può essere modificato per singoli file come parte dello stesso processo, in caso contrario. Usa lo stesso `uploadParams` parametri per l&#39;intero job.

La richiesta POST iniziale per un nuovo processo di caricamento deve specificare `jobName` , preferibilmente utilizzando un nome di processo univoco per semplificare il polling dello stato e le query del registro di processo successivi. Ulteriori richieste POST per lo stesso processo di caricamento devono specificare `jobHandle` parametro invece di `jobName`, utilizzando `jobHandle` valore restituito dalla richiesta iniziale.

La richiesta POST finale per un processo di caricamento deve impostare `endJob` Il parametro è impostato su true in modo che non vengano creati file POST futuri per questo processo. A sua volta, questo consente il completamento del processo subito dopo l’acquisizione di tutti i file POST. In caso contrario, il processo si interrompe se non vengono ricevute ulteriori richieste POST entro 30 minuti.

## Risposta UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Per una richiesta POST corretta, il corpo della risposta è un XML `uploadPostReturn` come XSD specifica nei seguenti documenti:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Il `jobHandle` restituito viene passato nel `uploadPostParams`/ `jobHandle` per qualsiasi richiesta POST successiva per lo stesso processo. Puoi utilizzarlo anche per eseguire il polling dello stato del processo con il `getActiveJobs` o per eseguire una query sui registri di processo con `getJobLogDetails` operazione.

In caso di errore durante l’elaborazione della richiesta POST, il corpo della risposta è costituito da uno dei tipi di errore API descritti in [Errori](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Esempio di richiesta POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Esempio di risposta di POST - operazione riuscita {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Esempio di risposta di POST - errore {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

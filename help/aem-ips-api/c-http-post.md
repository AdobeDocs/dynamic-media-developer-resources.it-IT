---
description: Il caricamento di risorse in Scene7 Production System richiede una o più richieste HTTP POST che configurano un processo per coordinare tutte le attività di registro associate ai file caricati.
seo-description: Il caricamento di risorse in Scene7 Production System richiede una o più richieste HTTP POST che configurano un processo per coordinare tutte le attività di registro associate ai file caricati.
seo-title: Caricamento delle risorse tramite POST HTTP nel servlet UploadFile
solution: Experience Manager
title: Caricamento delle risorse tramite POST HTTP nel servlet UploadFile
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# Caricamento delle risorse tramite POST HTTP nel servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Il caricamento di risorse in Scene7 Production System richiede una o più richieste HTTP POST che configurano un processo per coordinare tutte le attività di registro associate ai file caricati.

Utilizzate il seguente URL per accedere al Servlet UploadFile:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Tutte le richieste POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

**URL di accesso per le aree Scene7**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Posizione geografica </p> </th> 
   <th colname="col2" class="entry"> <p>URL produzione </p> </th> 
   <th colname="col3" class="entry"> <p>URL di gestione temporanea (da utilizzare per lo sviluppo e il test pre-produzione) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>America del Nord </p> </td> 
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

Il processo di caricamento è composto da uno o più POST HTTP che utilizzano in comune `jobHandle` per correlare l’elaborazione allo stesso processo. Ogni richiesta è `multipart/form-data` codificata e comprende le seguenti parti del modulo:

>[!NOTE]
>
>Tutte le richieste POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

| Parte modulo HTTP POST | Descrizione ||-|-||`auth`| Obbligatorio. Un documento authHeader XML che specifica l&#39;autenticazione e le informazioni sul client. Consultate **Richiedere l&#39;autenticazione** in [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Facoltativo. Potete includere uno o più file da caricare con ogni richiesta POST. Ogni parte del file può includere un parametro di nome file nell’intestazione Content-Disposition che viene utilizzato come nome file di destinazione in IPS se non viene specificato alcun `uploadPostParams/fileName` parametro. |

| Parte modulo HTTP POST | nome elemento uploadPostParams | Tipo | Descrizione ||-|-|-|-|-||`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento) | `companyHandle`|`xsd:string`| Obbligatorio. Gestite la società in cui viene caricato il file. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`jobName`|`xsd:string`| `jobName` È richiesto o `jobHandle` . Nome del processo di caricamento. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`jobHandle`|`xsd:string`| `jobName` È richiesto o `jobHandle` . Gestire un processo di caricamento avviato in una richiesta precedente. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`locale`|`xsd:string`| Opzionale. Lingua e codice del paese per la localizzazione. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`description`|`xsd:string`| Opzionale. Descrizione del processo. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`destFolder`|`xsd:string`| Opzionale. Percorso cartella di destinazione per specificare il prefisso per una proprietà del nome file, in particolare per i browser e altri client che potrebbero non supportare percorsi completi in un nome file. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`fileName`|`xsd:string`| Opzionale. Nome del file di destinazione. Sostituisce la proprietà nomefile. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`endJob`|`xsd:boolean`| Opzionale. Il valore predefinito è false. |
|`uploadParams` (Obbligatorio. Un `uploadParams` documento XML che specifica i parametri di caricamento)|`uploadParams`|`types:UploadPostJob`| Facoltativo se si tratta di una richiesta successiva per un processo attivo esistente. Se esiste un processo esistente, `uploadParams` viene ignorato e vengono utilizzati i parametri di caricamento del processo esistenti. Consulta [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

All&#39;interno del `<uploadPostParams>` blocco è presente il `<uploadParams>` blocco che indica l&#39;elaborazione dei file inclusi.

Consultate [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Anche se potete presumere che il `uploadParams` parametro possa essere modificato per singoli file come parte dello stesso processo, non è così. Usate gli stessi `uploadParams` parametri per l’intero processo.

La richiesta POST iniziale per un nuovo processo di caricamento deve specificare il `jobName` parametro, preferibilmente utilizzando un nome di processo univoco per semplificare il polling dello stato del processo successivo e le query del registro di processo. Ulteriori richieste POST per lo stesso processo di caricamento devono specificare il `jobHandle` parametro invece di `jobName`, utilizzando il `jobHandle` valore restituito dalla richiesta iniziale.

La richiesta POST finale per un processo di caricamento deve impostare il `endJob` parametro su true, in modo che nessun file POST futuro verrà impostato per questo processo. A sua volta, questo consente di completare il processo subito dopo l’acquisizione di tutti i file POST. In caso contrario, il processo si interrompe se non vengono ricevute altre richieste POST entro 30 minuti.

## Carica risposta POST {#section-421df5cc04d44e23a464059aad86d64e}

Per una richiesta POST corretta, il corpo della risposta sarà un `uploadPostReturn` documento XML, come specificato nel file XSD di seguito:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

La `jobHandle` restituzione viene passata nel parametro `uploadPostParams`/ `jobHandle` per tutte le richieste POST successive per lo stesso processo. È inoltre possibile utilizzarlo per il sondaggio dello stato del processo con l’ `getActiveJobs` operazione o per eseguire una query sui registri di processo con l’ `getJobLogDetails` operazione.

Se si verifica un errore durante l&#39;elaborazione della richiesta POST, il corpo della risposta è costituito da uno dei tipi di errore API come descritto in [Errori](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Esempio di richiesta POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```
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

## Esempio di risposta POST - success {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Esempio di risposta POST - errore {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```


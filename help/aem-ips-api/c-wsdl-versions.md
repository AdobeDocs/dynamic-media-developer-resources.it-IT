---
description: Il servizio Web IPS è supportato da un insieme di documenti WSDL (Web Services Description Language) a cui si accede da qualsiasi installazione IPS in cui è installato il componente Servizio Web IPS. Ogni versione API IPS include un nuovo file WSDL che fa riferimento a uno spazio dei nomi XML di destinazione con versione. Sono supportate anche le versioni precedenti dello spazio dei nomi WSDL per consentire la compatibilità con le applicazioni esistenti.
solution: Experience Manager
title: Versioni WSDL servizio Web IPS
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Versioni WSDL servizio Web IPS{#ips-web-service-wsdl-versions}

Il servizio Web IPS è supportato da un insieme di documenti WSDL (Web Services Description Language) a cui si accede da qualsiasi installazione IPS in cui è installato il componente Servizio Web IPS. Ogni versione API IPS include un nuovo file WSDL che fa riferimento a uno spazio dei nomi XML di destinazione con versione. Sono supportate anche le versioni precedenti dello spazio dei nomi WSDL per consentire la compatibilità con le applicazioni esistenti.

## Accesso WSDL {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Accedere ai file WSDL di Scene7 come illustrato di seguito.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Il valore predefinito per `<IPS_webapp>` è `scene7`.

**Posizione del servizio**

L&#39;URL del servizio è specificato nella sezione del servizio del documento WSDL del servizio Web IPS. L’URL del servizio è generalmente nel formato:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Accedere agli URL per le aree geografiche di Dynamic Medie**

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Medio Oriente, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Giappone/Asia Pacifico </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## WSDL supportati {#section-ebbba69880f94e9c823f1147974eb404}

Ricorda che potrebbe essere necessario modificare il codice se desideri utilizzare le funzioni nell’ultima versione dell’API IPS. L&#39;API IPS supporta WSDL per le seguenti versioni:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Versione di rilascio API </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>Spazio dei nomi API </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le applicazioni esistenti che devono essere modificate per utilizzare le nuove funzioni devono eseguire l’aggiornamento alla versione API più recente e potrebbe essere necessario apportare modifiche al codice esistente. Per ulteriori informazioni, vedere il log delle modifiche.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Associazioni**

Il servizio Web API IPS supporta solo un&#39;associazione SOAP.

**Trasporti supportati**

Il binding SOAP API IPS supporta solo il trasporto HTTP. Effettuare tutte le richieste SOAP utilizzando il metodo HTTPS POST.

**Intestazione azione SOAP**

Per elaborare una richiesta, impostare l&#39;intestazione HTTP SOAPAction sul nome dell&#39;operazione richiesta. L&#39;attributo del nome dell&#39;operazione nella sezione di associazione WSDL specifica il nome.

**Formato del messaggio**

Lo stile document/literal viene utilizzato per tutti i messaggi di input e output con tipi basati sul linguaggio di definizione dello schema XML ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) e specificate nel file WSDL. Tutti i tipi richiedono nomi qualificati che utilizzano il valore dello spazio dei nomi di destinazione specificato nel file WSDL.

**Richiedi autenticazione**

Il metodo preferito per trasmettere le credenziali di autenticazione nelle richieste API consiste nell’utilizzare `authHeader` come definito nel file WSDL API IPS.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Campi**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utente </span> </p> </td> 
   <td colname="col2"> <p> E-mail utente IPS valido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password </span> </p> </td> 
   <td colname="col2"> <p>Password per l’account utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Impostazioni locali facoltative per la richiesta. Consulta <b>Lingua</b> per i dettagli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Chiamata del nome dell'applicazione. Questo parametro è facoltativo, ma è consigliabile includerlo in tutte le richieste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Chiamata della versione dell'applicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Flag facoltativo per abilitare o disabilitare la compressione Gzip dell’XML di risposta. Per impostazione predefinita, le risposte vengono compresse in formato gzip se l’intestazione HTTP Accept-Encoding indica il supporto per gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Parametro facoltativo per ignorare il codice di stato HTTP per le risposte di errore. Per impostazione predefinita, le risposte di errore restituiscono il codice di stato HTTP 500 (Errore interno del server). Alcune piattaforme client, tra cui Adobe Flash, non sono in grado di leggere il corpo della risposta a meno che non venga restituito il codice di stato 200 (OK). </p> </td> 
  </tr> 
 </tbody> 
</table>

Il `authHeader` è sempre definito nello spazio dei nomi `http://www.scene7.com/IpsApi/xsd`, indipendentemente dalla versione API.

Di seguito è riportato un esempio di utilizzo di `authHeader` elemento in un’intestazione SOAP della richiesta:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Altri metodi di autenticazione delle richieste**

Se per qualche motivo l’applicazione client non può trasmettere il `authHeader` L’intestazione SOAP e le richieste API possono inoltre specificare le credenziali utilizzando l’autenticazione HTTP Basic (come specificato nella RFC 2617).

Per l’autenticazione HTTP Basic, la sezione dell’intestazione HTTP di ogni richiesta SOAP POST deve includere un’intestazione del modulo:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Dove `base64()` applica la codifica standard Base64, `<IPS_user_email>` è l&#39;indirizzo e-mail di un utente IPS valido e `<password>` è la password dell&#39;utente.

Invia preventivamente l’intestazione Autorizzazione con la richiesta iniziale. Se nella richiesta non sono incluse credenziali di autenticazione, `IpsApiService` non risponde con un codice di stato `401 (Unauthorized)`. Invece, un codice di stato di `500 (Internal Server Error)` viene restituito un corpo dell&#39;errore SOAP che indica che la richiesta non può essere autenticata.

Prima di IPS 3.8, l’autenticazione tramite l’intestazione SOAP era implementata utilizzando `AuthUser` e `AuthPassword` elementi nello spazio dei nomi `http://www.scene7.com/IpsApi`. Ad esempio:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Questo stile è ancora supportato per la compatibilità con le versioni precedenti, ma è stato dichiarato obsoleto a favore del `authHeader` elemento.

**Richiedi autorizzazione**

Dopo l&#39;autenticazione delle credenziali del chiamante, la richiesta viene controllata per assicurarsi che il chiamante sia autorizzato a eseguire l&#39;operazione richiesta. L&#39;autorizzazione si basa sul ruolo utente del chiamante e può anche richiedere il controllo della società target, dell&#39;utente target e di altri parametri operativi. Inoltre, gli utenti di Image Portal devono appartenere a un gruppo con le autorizzazioni necessarie per eseguire determinate operazioni su cartelle e risorse. La sezione Riferimento operazioni descrive i requisiti di autorizzazione per ciascuna operazione.

**Richiesta e risposta SOAP di esempio**

L’esempio seguente mostra un’ `addCompany` operazione, incluse le intestazioni HTTP:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

E la risposta corrispondente:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**Errori SOAP**

Quando un&#39;operazione rileva una condizione di eccezione, viene restituito un errore SOAP come corpo del messaggio SOAP al posto della risposta normale. Ad esempio, se un utente non amministratore tenta di inviare il precedente `addCompany` richiesta, viene restituita la seguente risposta:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```

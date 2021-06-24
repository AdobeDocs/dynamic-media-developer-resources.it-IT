---
description: Il servizio Web IPS è supportato da un set di documenti WSDL (Web Services Description Language) a cui si accede da qualsiasi installazione IPS in cui è installato il componente Servizio Web IPS. Ogni versione dell’API IPS include un nuovo file WSDL che fa riferimento a uno spazio dei nomi XML di destinazione con versione. Sono supportate anche le versioni precedenti dello spazio dei nomi WSDL per consentire la compatibilità con le applicazioni esistenti.
solution: Experience Manager
title: Versioni WSDL del servizio Web IPS
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 1%

---

# Versioni WSDL del servizio Web IPS{#ips-web-service-wsdl-versions}

Il servizio Web IPS è supportato da un set di documenti WSDL (Web Services Description Language) a cui si accede da qualsiasi installazione IPS in cui è installato il componente Servizio Web IPS. Ogni versione dell’API IPS include un nuovo file WSDL che fa riferimento a uno spazio dei nomi XML di destinazione con versione. Sono supportate anche le versioni precedenti dello spazio dei nomi WSDL per consentire la compatibilità con le applicazioni esistenti.

## Accesso WSDL {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Accedi alle WSDL di Scene7 come mostrato di seguito.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Il valore predefinito per `<IPS_webapp>` è `scene7`.

**Posizione del servizio**

L&#39;URL del servizio è specificato nella sezione del servizio del documento WSDL del servizio Web IPS. L’URL del servizio è in genere del modulo:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**URL di accesso per le aree geografiche di Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Posizione geografica </p> </th> 
   <th colname="col2" class="entry"> <p>URL di produzione </p> </th> 
   <th colname="col3" class="entry"> <p>URL di staging (da utilizzare per lo sviluppo e il test di pre-produzione) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>America del Nord </p> </td> 
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

## WSDL supportate {#section-ebbba69880f94e9c823f1147974eb404}

Tieni presente che potrebbe essere necessario modificare il codice se desideri utilizzare le funzionalità dell’ultima versione dell’API IPS. L’API IPS supporta WSDL per le seguenti versioni:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Versione API </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>Spazio dei nomi API </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2. </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le applicazioni esistenti che devono essere modificate per utilizzare le nuove funzionalità devono eseguire l’aggiornamento alla versione API più recente e potrebbero dover apportare modifiche al codice esistente. Per ulteriori informazioni, consulta il registro delle modifiche .

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Binding**

Il servizio Web API IPS supporta solo il binding SOAP.

**Trasporti supportati**

Il binding SOAP API IPS supporta solo il trasporto HTTP. Effettua tutte le richieste SOAP utilizzando il metodo HTTPS POST.

**Intestazione azione azione azione SOAP**

Per elaborare una richiesta, imposta l&#39;intestazione HTTP SOAPAction sul nome dell&#39;operazione richiesta. L&#39;attributo nome operazione nella sezione di binding WSDL specifica il nome.

**Formato del messaggio**

Lo stile document/literal viene utilizzato per tutti i messaggi di input e output con tipi basati sul linguaggio di definizione dello schema XML ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) e specificato nel file WSDL. Tutti i tipi richiedono nomi qualificati utilizzando il valore dello spazio dei nomi di destinazione specificato nel file WSDL.

**Richiedi autenticazione**

Il metodo preferito per passare le credenziali di autenticazione nelle richieste API è quello di utilizzare l’elemento `authHeader` come definito nella WSDL API IPS.

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
   <td colname="col2"> <p> E-mail utente IPS valida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password </span> </p> </td> 
   <td colname="col2"> <p>Password per account utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Impostazioni internazionali facoltative per la richiesta. Per ulteriori informazioni, consulta <b>Impostazioni internazionali</b> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName  </span> </p> </td> 
   <td colname="col2"> <p> Chiamata del nome dell'applicazione. Questo parametro è facoltativo, ma è consigliabile includerlo in tutte le richieste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion  </span> </p> </td> 
   <td colname="col2"> <p> Chiamata della versione dell'applicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse  </span> </p> </td> 
   <td colname="col2"> <p> Flag facoltativo per abilitare o disabilitare la compressione gzip dell'XML di risposta. Per impostazione predefinita, le risposte sono compresse con Gzip se l'intestazione HTTP Accept-Encoding indica il supporto per gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> errorHttpStatusCode  </span> </p> </td> 
   <td colname="col2"> <p> Parametro facoltativo per sostituire il codice di stato HTTP per le risposte agli errori. Per impostazione predefinita, le risposte di errore restituiscono il codice di stato HTTP 500 (Errore interno del server). Alcune piattaforme client, incluso l’Flash di Adobe, non sono in grado di leggere il corpo della risposta a meno che non venga restituito un codice di stato 200 (OK). </p> </td> 
  </tr> 
 </tbody> 
</table>

L’elemento `authHeader` è sempre definito nello spazio dei nomi `http://www.scene7.com/IpsApi/xsd`, indipendentemente dalla versione API.

Di seguito è riportato un esempio di utilizzo dell’elemento `authHeader` in un’intestazione SOAP di richiesta:

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

Se per qualche motivo non è possibile che l’applicazione client passi l’intestazione SOAP `authHeader`, le richieste API possono anche specificare le credenziali tramite l’autenticazione HTTP Basic (come specificato nella RFC 2617).

Per l’autenticazione HTTP Basic, la sezione dell’intestazione HTTP di ogni richiesta SOAP POST deve includere un’intestazione del modulo:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Dove `base64()` applica la codifica standard Base64, `<IPS_user_email>` è l&#39;indirizzo e-mail di un utente IPS valido e `<password>` è la password dell&#39;utente.

Invia l’intestazione Autorizzazione in modo preventivo con la richiesta iniziale. Se nella richiesta non sono incluse credenziali di autenticazione, `IpsApiService` non risponde con un codice di stato di `401 (Unauthorized)`. Al contrario, viene restituito un codice di stato di `500 (Internal Server Error)` con un corpo di errore SOAP che indica che la richiesta non può essere autenticata.

Prima di IPS 3.8, l’autenticazione tramite intestazione SOAP è stata implementata utilizzando gli elementi `AuthUser` e `AuthPassword` nello spazio dei nomi `http://www.scene7.com/IpsApi`. Ad esempio:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Questo stile è ancora supportato per la compatibilità con le versioni precedenti ma è stato dichiarato obsoleto a favore dell’elemento `authHeader` .

**Richiesta di autorizzazione**

Dopo l&#39;autenticazione delle credenziali del chiamante, la richiesta viene controllata per assicurarsi che il chiamante sia autorizzato a eseguire l&#39;operazione richiesta. L’autorizzazione si basa sul ruolo utente del chiamante e può richiedere anche il controllo della società di destinazione, dell’utente di destinazione e di altri parametri operativi. Inoltre, gli utenti di Image Portal devono appartenere a un gruppo con le autorizzazioni necessarie per eseguire determinate operazioni relative a cartelle e risorse. La sezione Operazioni descrive i requisiti di autorizzazione per ciascuna operazione.

**Richiesta e risposta SOAP di esempio**

L&#39;esempio seguente mostra un&#39;operazione completa `addCompany`, comprese le intestazioni HTTP:

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

Quando un’operazione rileva una condizione di eccezione, viene restituito un errore SOAP come corpo del messaggio SOAP al posto della risposta normale. Ad esempio, se un utente non amministratore tenta di inviare la richiesta precedente `addCompany`, viene restituita la risposta seguente:

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

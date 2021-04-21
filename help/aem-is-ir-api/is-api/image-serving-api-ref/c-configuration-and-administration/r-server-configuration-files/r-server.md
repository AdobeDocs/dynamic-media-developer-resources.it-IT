---
description: Contiene le impostazioni del server della piattaforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

Contiene le impostazioni del server della piattaforma.

Quando si modifica questo file XML, è necessario prestare attenzione a mantenere una sintassi XML valida, altrimenti il server Platform potrebbe non avviarsi.

Affinché le modifiche abbiano effetto, Platform Server deve essere riavviato dopo aver modificato questo file.

Il diagramma seguente illustra quali impostazioni possono essere modificate in questo file. Per una descrizione di queste impostazioni, fare riferimento alle sezioni corrispondenti presenti in questo documento. Tieni presente che questo diagramma non è una rappresentazione completa di [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```


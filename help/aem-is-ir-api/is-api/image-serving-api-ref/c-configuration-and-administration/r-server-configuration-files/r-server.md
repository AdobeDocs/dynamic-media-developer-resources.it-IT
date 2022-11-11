---
description: Contiene le impostazioni del server della piattaforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

Contiene le impostazioni del server della piattaforma.

Quando si modifica questo file XML, prestare attenzione a mantenere una sintassi XML valida, altrimenti la [!DNL Platform Server] potrebbero non avviarsi.

Affinché le modifiche abbiano effetto, il [!DNL Platform Server] deve essere riavviato dopo la modifica del file.

Il diagramma seguente illustra quali impostazioni possono essere modificate in questo file. Per una descrizione di queste impostazioni, fare riferimento alle sezioni corrispondenti presenti in questo documento. Nota che questo diagramma non è una rappresentazione completa di [!DNL server.xml].

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

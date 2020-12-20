---
description: Contiene le impostazioni del server della piattaforma.
seo-description: Contiene le impostazioni del server della piattaforma.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# server.xml{#server-xml}

Contiene le impostazioni del server della piattaforma.

Durante la modifica di questo file XML, è necessario mantenere una sintassi XML valida, in caso contrario il server della piattaforma potrebbe non avviarsi.

Affinché le modifiche abbiano effetto, il server piattaforma deve essere riavviato dopo la modifica di questo file.

Nel diagramma seguente sono illustrate le impostazioni che possono essere modificate in questo file. Per una descrizione di queste impostazioni, fare riferimento alle sezioni corrispondenti presenti in precedenza nel documento. Nota che questo diagramma non è una rappresentazione completa di [!DNL server.xml].

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


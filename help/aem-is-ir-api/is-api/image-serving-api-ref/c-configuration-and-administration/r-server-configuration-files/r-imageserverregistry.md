---
description: Contiene le impostazioni di configurazione del server immagini.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
TQID: 'https://experienceleague.adobe.com/UdMACutToNmpsXnhU0jAaItCZJ8r0RTxirjaqXSpa0c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene le impostazioni di configurazione del server immagini.

Quando si modifica questo file XML, è necessario prestare attenzione a mantenere una sintassi XML valida, altrimenti il server immagini potrebbe non essere avviato.

Per rendere effettive le modifiche, riavviare il server immagini dopo aver modificato il file. Solo i valori degli elementi elencati di seguito sono supportati per la modifica. Modificare qualsiasi altro contenuto di questo file solo se consigliato dal supporto tecnico di Dynamic Media.

>[!NOTE]
>
>Non modificare la struttura di `<imageserverregistry>`, incluso l&#39;ordine degli elementi. Prestare attenzione quando si modifica il file, altrimenti il server immagini potrebbe non avviarsi.

Di seguito sono illustrati gli elementi che è possibile modificare. Sono presenti altri elementi che non devono essere modificati. L’ordine degli elementi di seguito non riflette l’ordine in cui devono essere presenti nel file.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Note {#section-7217f011f69f41e7af4f3983d7776d6f}

Possono essere presenti più elementi `<RootPath>` (uno per ogni cartella di file di dati di origine). Image Server esegue la ricerca nei percorsi principali nell&#39;ordine specificato per trovare un file di origine specifico.

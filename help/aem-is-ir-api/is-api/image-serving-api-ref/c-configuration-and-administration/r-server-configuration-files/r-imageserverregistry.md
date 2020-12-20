---
description: Contiene le impostazioni di configurazione del server immagini.
seo-description: Contiene le impostazioni di configurazione del server immagini.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene le impostazioni di configurazione del server immagini.

Quando si modifica questo file XML, è necessario mantenere una sintassi XML valida. In caso contrario, il server immagini potrebbe non avviarsi.

Per rendere effettive le modifiche, riavviare il server immagini dopo aver modificato il file. Per la modifica sono supportati solo i valori degli elementi elencati di seguito. Modificate qualsiasi altro contenuto di questo file solo se richiesto dal supporto tecnico di Scene7.

>[!NOTE]
>
>Non modificate la struttura di `<imageserverregistry>`, incluso l&#39;ordine degli elementi. Prestate attenzione quando modificate il file, in caso contrario il server immagini potrebbe non avviarsi.

Di seguito sono illustrati gli elementi che possono essere modificati. Sono presenti altri elementi che non devono essere modificati. L&#39;ordine degli elementi di seguito non riflette l&#39;ordine in cui devono essere presenti nel file.

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

Potrebbero essere presenti più elementi `<RootPath>` (uno per ciascuna cartella di file di dati di origine). Image Server esegue la ricerca nei percorsi principali nell’ordine specificato per trovare un particolare file sorgente.

---
title: VisualizzatorePanoramico
description: Costruttore, crea un'istanza di Visualizzatore panoramico di HTML5.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%
---
# VisualizzatorePanoramico{#panoramicviewer}

`PanoramicViewer([config])`
Costruttore, crea un&#39;istanza di Visualizzatore panoramico di HTML5.

## Parametro {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} oggetto di configurazione JSON facoltativo, consente di passare tutte le impostazioni del visualizzatore al costruttore ed evitare di chiamare singoli metodi di impostazione. Contiene le seguenti proprietà:

* containerId: {String} ID del contenitore DOM (normalmente un DIV) in cui viene inserito il visualizzatore. Non è necessario creare l’elemento contenitore nel momento in cui viene chiamato questo metodo, tuttavia il contenitore deve esistere quando init() viene eseguito. Obbligatorio
* parametri: oggetto JSON {Object} con parametri di configurazione del visualizzatore in cui il nome della proprietà è un&#39;opzione di configurazione specifica del visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio
* gestori: oggetto JSON {Object} con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell&#39;evento del visualizzatore supportato e il valore della proprietà è un riferimento della funzione JavaScript al callback appropriato. Per ulteriori informazioni sugli eventi visualizzatore, consulta la sezione Callback di eventi. Facoltativo.


## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```

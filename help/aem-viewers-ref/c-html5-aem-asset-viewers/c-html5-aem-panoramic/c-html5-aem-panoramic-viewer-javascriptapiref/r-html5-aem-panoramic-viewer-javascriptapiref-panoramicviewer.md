---
title: VisualizzatorePanoramico
description: Costruttore, crea un'istanza di Visualizzatore panoramico di HTML5.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '161'
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

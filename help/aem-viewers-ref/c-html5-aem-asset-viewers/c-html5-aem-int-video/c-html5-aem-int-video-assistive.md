---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi,Accessibilità
role: Developer,Business Practitioner
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` . Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin` e `aria-valuemax` per descrivere la posizione corrente del cursore.

Le miniature hanno il ruolo `dialog` con l’attributo `aria-label` controllato dal simbolo di localizzazione `ThumbnailGridView.LABEL` . Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, l’attributo `aria-selected` viene impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l’attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di quel componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, l’attributo `aria-selected` viene impostato su `true`.

Gli elenchi a discesa sono attivati dai pulsanti con l’attributo aggiuntivo `aria-haspopup` impostato su `true` e l’attributo `aria-controls` che fa riferimento all’elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` con elementi secondari con il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label` .

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;attributo `aria-labelledby` fa riferimento all&#39;elemento di intestazione della finestra di dialogo.

---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,Business Practitioner
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Supporto della tecnologia di assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` . Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin` e `aria-valuemax` per descrivere la posizione corrente del cursore.

Gli elenchi a discesa sono attivati dai pulsanti con l’attributo aggiuntivo `aria-haspopup` impostato su `true` e l’attributo `aria-controls` che fa riferimento all’elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` con elementi secondari con il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label` .

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;attributo `aria-labelledby` fa riferimento all&#39;elemento di intestazione della finestra di dialogo.

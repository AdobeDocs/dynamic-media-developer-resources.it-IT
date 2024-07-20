---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

La visualizzazione principale ha il ruolo `application`. In `aria-roledescription` viene fornita una breve descrizione della visualizzazione principale, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente della visualizzazione principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera vengono forniti utilizzando `aria-describedby`. Il testo dell&#39;hint di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se per una risorsa è definita un&#39;etichetta nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

La visualizzazione principale ha il ruolo `application`. In `aria-roledescription` viene fornita una breve descrizione della visualizzazione principale, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente della visualizzazione principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera vengono forniti utilizzando `aria-describedby`. Il testo dell&#39;hint di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se per una risorsa è definita un&#39;etichetta nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l&#39;attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di quel componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, l&#39;attributo `aria-selected` viene impostato su `true`.

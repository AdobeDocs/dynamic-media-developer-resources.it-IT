---
title: Supporto tecnologico per assistenza
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di livello superiore ha un ruolo `region` e `aria-label` impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con la `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con il `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, la funzione `aria-disabled` attributo viene impostato di conseguenza.

La vista principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dalla `ROLE_DESCRIPTION` simbolo di localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti di tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal `USAGE_HINT` simbolo di localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData , la variabile `aria-label` attributo è impostato con il valore di tale etichetta.

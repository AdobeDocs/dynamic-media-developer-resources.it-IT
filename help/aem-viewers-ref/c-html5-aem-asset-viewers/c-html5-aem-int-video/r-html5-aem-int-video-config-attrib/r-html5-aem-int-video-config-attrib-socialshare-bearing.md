---
title: Condivisione.social
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
TQID: 'https://experienceleague.adobe.com/qKnLf2xkrrKsHuakGsY4V3hK6LwzuzvGRMSDE4RJKCc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 1%

---

# Condivisione.social{#socialshare-bearing}

Attributo di configurazione per Visualizzatore video interattivo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|adatta-verticale|adatta-laterale</span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione di scorrimento per il contenitore pulsanti. Se è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sposta nella direzione specificata senza alcun controllo dei limiti aggiuntivo, che può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se è impostato su <span class="codeph"> adattamento verticale</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare. Quindi, tenta di stendere il pannello in una delle seguenti direzioni da tale posizione di base: in basso, a destra, a sinistra. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e ripete i tentativi di rollout da una direzione superiore, destra e sinistra. </p> <p>Se è impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile, ma sposta la base a destra per prima, provando le direzioni di rollout verso destra, verso il basso e verso l'alto. Quindi sposta la base verso sinistra, provando le direzioni di rollout verso sinistra, verso il basso e verso l'alto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

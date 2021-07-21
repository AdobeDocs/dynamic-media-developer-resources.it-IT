---
description: Contiene le impostazioni di configurazione del supervisore del server.
solution: Experience Manager
title: SupervisorRegistry.xml
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: cc6a16fb-fd70-431f-aad6-adb99d4da062
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# SupervisorRegistry.xml{#supervisorregistry-xml}

Contiene le impostazioni di configurazione del supervisore del server.

Durante la modifica di questo file XML, assicurarsi di mantenere una sintassi XML valida, altrimenti il server immagini potrebbe non avviarsi.

Riavvia Image Serving dopo aver modificato questo file per assicurarti che le modifiche abbiano effetto. Per la modifica sono supportati solo i valori di elemento/attributo evidenziati di seguito. Modifica tutti gli altri contenuti di questo file solo se richiesto dal supporto tecnico Dynamic Media.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Dynamic Media Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Dynamic Media SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Dynamic Media Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```

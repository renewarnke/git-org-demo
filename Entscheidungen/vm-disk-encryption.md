---
# Configuration for the Jekyll template "Just the Docs"
parent: Entscheidungen
nav_order: 100
title: ADR Template

# These are optional elements. Feel free to remove any of them.
status: "akzeptiert"
date: 2023-10-20
deciders: Rene Warnke - rene@warnke.cloud
consulted: XY
informed: AB
---
<!-- we need to disable MD025, because we use the different heading "ADR Template" in the homepage (see above) than it is foreseen in the template -->
<!-- markdownlint-disable-next-line MD025 -->
# Disk Verschlüsselung

## Kontext und Problembeschreibung

Auf Grund von regulatorischen Vorgaben müssen VM Disks mit eigenem Schlüssel verschlüsselt werden, hierfür gibt es in Azure mehrere Optionen.

<!-- This is an optional element. Feel free to remove. -->
## Entscheidungstreiber

* Regulatorische Vorgabe zur Verschlüsselung mit eigenem Key
* Möglichst geringe Einschränkungen in der Nutzung

## Optionen

* Azure Disk Encryption
* Host based Encryption

## Entscheidung

Entscheidung: Host based Encryption
Azure Host based Encryption erfüllt die regulatorische Anforderung mit geringstem Impact auf andere Azure Dienste wie z.B. Backup oder verwaltung der VM

<!-- This is an optional element. Feel free to remove. -->
### Konsequenzen

* Good, because {positive consequence, e.g., improvement of one or more desired qualities, …}
* Bad, because {negative consequence, e.g., compromising one or more desired qualities, …}
* … <!-- numbers of consequences can vary -->

<!-- This is an optional element. Feel free to remove. -->
### Überprüfung

Zur Überwachung der Compliance aller VMs wird eine globale Azure Policy definiert, die den Status der Encryption überwacht und fehlerhafte Ressourcen auflistet.


## Mehr Informationen

{You might want to provide additional evidence/confidence for the decision outcome here and/or
 document the team agreement on the decision and/or
 define when/how this decision should be realized and if/when it should be re-visited.
Links to other decisions and resources might appear here as well.}

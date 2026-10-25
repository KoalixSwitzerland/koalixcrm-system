# 10. Quality Requirements

This chapter documents quality requirements (non-functional requirements) and quality scenarios.

> **Note:** Quality requirements cannot be reliably extracted from source code alone.
> This chapter serves as a placeholder for manual documentation of quality goals such as:
>
> - Performance (response times, throughput, resource utilization)
> - Availability (uptime targets, failover strategy)
> - Security (authentication, authorization, data protection targets)
> - Scalability (load handling, horizontal/vertical scaling goals)
> - Maintainability (code quality metrics, test coverage targets)
> - Usability (accessibility targets, user experience goals)

## Quality Attribute Scenarios (System-Design)

The following quality attribute scenarios describe measurable performance, scalability, and
reliability targets for the system-design phase:

- [QAS-0001: EAV-Attributfilter auf getypten Wertetabellen bei 10 000 SKUs (B-Tree-Pfad)](quality_attribute_scenario_0001.md)
- [QAS-0002: JSONB-Spiegel-Listenabfrage bei 10 000 SKUs und 200 Attributen pro Produkt (GIN-Pfad)](quality_attribute_scenario_0002.md)
- [QAS-0003: Kombinierter Attributfilter (typisierte Tabelle + JSONB-Spiegel) bei 10 000 SKUs unter gleichzeitiger Last](quality_attribute_scenario_0003.md)

## Sicherheitsanforderungen (Abhängigkeits-Schwachstellen-Gate)

Die folgenden Requirements beschreiben das Schwachstellen-Gate für Abhängigkeiten des Backends
(Security, Wartbarkeit). Sie liegen im Requirement-Verzeichnis von Kapitel 1.

- [REQ-0029: Das System blockiert den Merge nach `develop` bei HIGH/CRITICAL in Anwendungsbibliotheken der gebauten Images](../01_introduction_and_goals/requirements/REQ-0029.md)
- [REQ-0030: Das System berichtet Schwachstellen in Betriebssystempaketen der Basis-Images bei jedem Lauf und blockiert nie](../01_introduction_and_goals/requirements/REQ-0030.md)
- [REQ-0031: Das System führt Ausnahmen in genau einer Datei `.trivyignore.yaml`, jeder Eintrag mit Begründung und Ablaufdatum](../01_introduction_and_goals/requirements/REQ-0031.md)
- [REQ-0032: Das System bezieht den Scan aus dem öffentlichen zentralen Repository `QuantalQ/quaq-vulnerability-scan`, fixiert per Commit-SHA](../01_introduction_and_goals/requirements/REQ-0032.md)
- [REQ-0033: Das System liefert lokal mit einem einzigen Befehl auf einem lokal gebauten Image dasselbe Urteil wie CI](../01_introduction_and_goals/requirements/REQ-0033.md)
- [REQ-0034: Das System scannt wöchentlich das aktuelle Release-Image, berichtet und blockiert nie](../01_introduction_and_goals/requirements/REQ-0034.md)
- [REQ-0035: Das System führt bei Release, Rebuild, Snapshot und Deployment kein eigenes Schwachstellen-Gate aus](../01_introduction_and_goals/requirements/REQ-0035.md)
- [REQ-0036: Der Branch `develop` ist der Standard-Branch des Repositories `koalixcrm`](../01_introduction_and_goals/requirements/REQ-0036.md)
- [REQ-0037: Das System erhält Sicherheitsupdates als Dependabot-Pull-Requests gegen den Standard-Branch](../01_introduction_and_goals/requirements/REQ-0037.md)

# Design-Prinzipien Prompt-Vorlage

## Grundlegende Anforderungen

Bei der Entwicklung und Implementierung von Code-Lösungen sind folgende Design-Prinzipien zwingend einzuhalten:

---

## 🐍 Python SDK Libraries
**Verwende ausschließlich aktuelle Python SDK Libraries:**
- Nutze immer die neueste stabile Version verfügbarer Python SDKs
- Priorisiere offizielle SDKs gegenüber Community-Bibliotheken
- Überprüfe regelmäßig auf Updates und Sicherheitspatches
- Dokumentiere verwendete SDK-Versionen in `requirements.txt` oder `pyproject.toml`

**Beispiel-Anforderung für Prompts:**
```
Verwende die aktuellste Version der Azure Python SDK (azure-*), AWS SDK (boto3), oder Google Cloud SDK (google-cloud-*). Stelle sicher, dass alle Dependencies auf dem neuesten Stand sind.
```

---

## 📋 MIT-Lizenz Compliance
**Berücksichtige ausschließlich GitHub-Projekte mit MIT-Lizenz:**
- Überprüfe vor der Integration die Lizenz jedes GitHub-Projekts
- Akzeptiere nur Projekte mit expliziter MIT-Lizenz
- Dokumentiere alle verwendeten externen Abhängigkeiten mit ihren Lizenzen
- Vermeide GPL, AGPL oder proprietäre Lizenzen

**Beispiel-Anforderung für Prompts:**
```
Suche nach GitHub-Projekten, die das Problem lösen, aber verwende ausschließlich solche mit MIT-Lizenz. Überprüfe die LICENSE-Datei oder das Repository-Lizenz-Badge.
```

---

## 🐳 Docker Compose Architektur
**Alle Lösungen müssen mittels Docker Compose aufgebaut werden:**
- Erstelle immer eine `docker-compose.yml` für die gesamte Anwendungsarchitektur
- Nutze separate Services für verschiedene Komponenten (API, Database, Frontend, etc.)
- Implementiere Gesundheitschecks für alle Services
- Definiere Volumes für persistente Daten
- Verwende Environment-Variablen für Konfiguration
- Stelle sicher, dass alle Services über Docker-Netzwerke kommunizieren

**Beispiel-Anforderung für Prompts:**
```
Erstelle eine vollständige Docker Compose-Lösung mit separaten Services für jede Komponente. Inkludiere Health Checks, Environment-Variablen und Volumes für persistente Daten. Die Lösung muss mit einem einzigen `docker-compose up` befehl startbar sein.
```

---

## 📝 Standard Prompt-Template

**Verwende diese Vorlage für alle Entwicklungsanfragen:**

```
AUFGABE: [Beschreibung der zu entwickelnden Lösung]

TECHNISCHE ANFORDERUNGEN:
- Python: Verwende die neuesten stabilen SDK-Versionen für alle Cloud-Provider und Services
- Lizenzen: Nutze ausschließlich GitHub-Projekte mit MIT-Lizenz
- Deployment: Vollständige Docker Compose-Lösung mit Multi-Service-Architektur

DELIVERABLES:
1. Vollständiger Python-Code mit aktuellen SDKs
2. requirements.txt/pyproject.toml mit aktuellen Versionen
3. Dockerfile(s) für alle Services
4. docker-compose.yml mit:
   - Service-Definitionen
   - Health Checks
   - Environment-Variablen
   - Volumes für persistente Daten
   - Netzwerk-Konfiguration
5. README.md mit Setup- und Usage-Anweisungen
6. Lizenz-Dokumentation aller verwendeten Abhängigkeiten

QUALITÄTSKRITERIEN:
- Code muss production-ready sein
- Alle Services müssen unabhängig skalierbar sein
- Konfiguration über Environment-Variablen
- Logging und Monitoring-Integration
- Security Best Practices befolgen
```

---

## 🔧 Validierung

Vor der Implementierung prüfe:
- [ ] Sind alle Python SDKs aktuell?
- [ ] Haben alle GitHub-Dependencies eine MIT-Lizenz?
- [ ] Ist die Docker Compose-Architektur vollständig?
- [ ] Sind Health Checks implementiert?
- [ ] Ist die Lösung mit einem Command startbar?

---

## 📚 Ressourcen

- [Python Package Index (PyPI)](https://pypi.org/) - Für aktuelle SDK-Versionen
- [GitHub License Search](https://github.com/search?q=license%3Amit) - MIT-lizenzierte Projekte
- [Docker Compose Reference](https://docs.docker.com/compose/) - Best Practices
- [SPDX License List](https://spdx.org/licenses/) - Lizenz-Referenz

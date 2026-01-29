# Anleitung für Lehrpersonen

Diese Vorlage wurde speziell für die 8-wöchige Unterrichtseinheit **Softwareentwicklung & Projektmanagement** (4. Jahrgang) vorbereitet.

## 📋 Überblick über die Vorlage

### Was ist bereits implementiert?
- ✅ **Komplette Projektstruktur** (src/, tests/, docs/)
- ✅ **Basis-Klassen** (Product, Warehouse, Movement)
- ✅ **Port-Adapter-Architektur** für Lehrzwecke
- ✅ **Service-Layer** mit echten Use-Cases
- ✅ **PyQt6 GUI-Skeleton**
- ✅ **Unit & Integration Tests**
- ✅ **Vollständige Dokumentations-Vorlagen**
- ✅ **Git-Workflow-Dokumentation**
- ✅ **Projektmanagement-Struktur** (PSP, Gantt, etc.)

### Was müssen Schüler/innen ergänzen?
- **Weitere Adapter** (SQLite, JSON, etc.)
- **Erweiterte Reports** (Grafiken, Statistiken)
- **GUI-Finalisierung** (weitere Features, Styling)
- **Test-Coverage** (100% anstreben)
- **Eigene Dokumentation** (persönliche Changelogs)
- **Projektmanagement-Dokumente** als PDF

## 🎓 Wie wird die Vorlage verwendet?

### Phase 1: Projektstart (Woche 1-2)
1. **Schüler/innen erhalten** dieses Repository
2. **Rollen verteilen:**
   - Rolle 1: Contract Owner
   - Rolle 2: Businesslogik & Report A
   - Rolle 3: Report B & Tests
   - Rolle 4: GUI & Interaktion
3. **Setup durchführen:**
   ```bash
   pip install -e .
   pip install -e ".[dev]"
   pytest tests/ -v  # Verifizieren dass alles lädt
   ```
4. **Erstes v0.1-Tag erstellen**

### Phase 2: Verstehen der Architektur (Woche 2-3)
- Schüler/innen studieren `docs/architecture.md`
- Schüler/innen arbeiten `GIT_WORKFLOW.md` durch
- Code-Review erste Änderungen durchführen

### Phase 3: Entwicklung & Expansion (Woche 3-8)
- Schüler/innen erweitern Funktionalität
- Regelmäßige Commits mit guten Meldungen
- Mergekonflikte als **Lernmomente** verstehen
- Wöchentliche Meilenstones (v0.2 bis v1.0)

### Phase 4: Abschluss (Woche 8)
- Retrospektive durchführen
- v1.0 Final releasen
- Persönliche Changelogs zusammenfassen
- Präsentation vorbereiten

## 👨‍🏫 Lehrpersonen-Checkliste

### Vor dem Projekt
- [ ] Vorlage den Schüler/innen bereitstellen
- [ ] Rollen erklären (docs/projektmanagement.md)
- [ ] Git-Workflow zeigen (GIT_WORKFLOW.md)
- [ ] Erwartungen klären (test coverage, dokumentation, teamwork)

### Während des Projekts
- [ ] **Wöchentliche Checkpoints:**
  - Commits überprüfen
  - Tests laufen lassen (`pytest tests/`)
  - Dokumentation aktualisiert?
- [ ] **Mergekonflikte als Lernchance:**
  - Schüler/innen dokumentieren in `docs/changelog_<name>.md`
  - Zeigen wie man Git-Konflikte elegant löst
- [ ] **Code-Reviews:**
  - Vor dem Merge zu develop
  - Feedback zu Architektur, Tests, Dokumentation
- [ ] **Meilestones überprüfen:**
  - v0.1: Projekt läuft, Tests grün
  - v0.2: Schnittstellen dokumentiert, Git-Konflikte gelöst
  - v0.3: Kernlogik + GUI funktionieren
  - v0.4: Reports implementiert
  - v0.5: Tests umfassend, stabiler Code
  - v1.0: Fertig, dokumentiert, präsentierbar

### Bewertungskriterien (Vorschlag)

| Kriterium | Gewichtung | Fokus |
|-----------|-----------|-------|
| **Code-Qualität** | 25% | Architektur, SOLID, Testbarkeit |
| **Tests** | 20% | Coverage 90%+, Unit + Integration |
| **Dokumentation** | 20% | contracts.md, architecture.md, Changelogs |
| **Git & Versionskontrolle** | 15% | Commits, Mergekonflikte, Branches |
| **Projektmanagement** | 15% | Zusammenarbeit, Rollen, Kommunikation |
| **Präsentation** | 5% | Finale Ausführung, Demo |

### Häufig gestellte Fragen von Schüler/innen

**F: Wie starte ich die GUI?**
```bash
python -m src.ui
```

**F: Wie führe ich Tests aus?**
```bash
pytest tests/ -v
pytest --cov=src tests/  # Mit Coverage
```

**F: Was ist ein Mergekonflikt und wie löse ich ihn?**
→ Siehe GIT_WORKFLOW.md, Sektion "Mergekonflikt-Handling"

**F: Wie dokumentiere ich meine Arbeit?**
→ Persönliche `docs/changelog_<name>.md` führen nach jedem Commit

**F: Was ist ein Port und was ist ein Adapter?**
→ Siehe `docs/architecture.md`, Sektion "Schichten-Modell"

**F: Wie schreibe ich einen guten Test?**
→ Siehe `docs/tests.md` und `tests/unit/test_domain.py` (Beispiele)

## 🔍 Was Schüler/innen gelernt haben

Nach diesem Projekt können Schüler/innen:

1. ✅ **Versionsverwaltung meistern**
   - Git-Branches, Commits, Pull Requests, Mergekonflikte

2. ✅ **Professionelle Architektur designen**
   - Port-Adapter-Pattern, SOLID-Prinzipien, Separation of Concerns

3. ✅ **Automatisiertes Testing verstehen**
   - Unit-Tests, Integration-Tests, Test-Driven Development, Coverage

4. ✅ **In Teams zusammenarbeiten**
   - Rollen, Kommunikation, Code-Reviews, Mergekonflikte

5. ✅ **Vollständig dokumentieren**
   - Code-Dokumentation, Schnittstellen-Docs, Architektur-Dokumentation

6. ✅ **GUI-Anwendungen entwickeln**
   - PyQt6, User Experience, Integration mit Geschäftslogik

7. ✅ **Agile Vorgehensweise nutzen**
   - Iterative Entwicklung, Meilestones, Retrospektiven

## 📊 Erfolgsmetriken für die Klasse

**v0.1:** 
- [ ] Repository lädt sauber
- [ ] Tests grün
- [ ] Rollen klar definiert

**v0.2:**
- [ ] Schnittstellen dokumentiert
- [ ] Erstes Mergekonflikt dokumentiert gelöst
- [ ] Git-Workflow etabliert

**v0.3:**
- [ ] GUI lädt
- [ ] Geschäftslogik funktioniert
- [ ] Unit-Tests für Domain

**v0.5:**
- [ ] 80%+ Test-Coverage
- [ ] Alle Reports implementiert
- [ ] Dokumentation 80% vollständig

**v1.0:**
- [ ] 90%+ Test-Coverage
- [ ] Alle Schüler/innen haben Changelog
- [ ] Präsentation funktioniert
- [ ] Keine kritischen Bugs

## 🎯 Tipps für erfolgreiche Durchführung

1. **Klare Erwartungen setzen** - Was ist eine gute PR? Wann ist ein Commit zu klein?
2. **Regelmäßige Feedback-Schleifen** - Nicht bis zur Woche 8 warten
3. **Mergekonflikte nicht vermeiden, sondern nutzen** - Das ist der Lernpunkt!
4. **Test-Culture von Anfang an** - "Kein Merge ohne rote Tests"
5. **Dokumentation ist Code** - Dasselbe Level an Qualität
6. **Pairing für schwierige Aufgaben** - Besonders bei GUI und Tests
7. **Feiere kleine Wins** - v0.2 Tag erstellt? Wunderbar!

## 📚 Zusätzliche Ressourcen für Schüler/innen

- **Git:**
  - https://git-scm.com/doc
  - https://github.github.com/training-kit/

- **Python & OOP:**
  - https://docs.python.org/3/tutorial/
  - https://pydantic-docs.helpmanual.io/ (für Validierung)

- **Testing:**
  - https://docs.pytest.org/
  - https://en.wikipedia.org/wiki/Test-driven_development

- **GUI:**
  - https://www.riverbankcomputing.com/static/Docs/PyQt6/ (PyQt6 Docs)

- **Software Architecture:**
  - Clean Architecture (Robert C. Martin)
  - Domain-Driven Design (Eric Evans)

## 🚀 Erweiterungs-Ideen für Schüler/innen

Wenn Schüler/innen schneller sind, können sie:

1. **SQLite-Adapter** implementieren statt nur In-Memory
2. **CSV-Export** für Reports hinzufügen
3. **Benutzer-Authentifizierung** implementieren
4. **Datenbank-Migrations** mit Alembic
5. **REST-API** mit FastAPI
6. **Docker-Container** für die Anwendung
7. **CI/CD Pipeline** mit GitHub Actions

## 📞 Support & Troubleshooting

### Setup-Probleme
```bash
# Python-Version checken
python --version  # Sollte 3.10+ sein

# Fresh install
pip install --upgrade pip
pip install -e .
pip install -e ".[dev]"

# Tests verifizieren
pytest tests/ -v
```

### Import-Fehler
```bash
# Pfad überprüfen
python -c "import src.domain.product; print('OK')"

# conftest.py überprüfen
cat tests/conftest.py
```

### GUI funktioniert nicht
```bash
# PyQt6 installieren
pip install PyQt6>=6.6.0

# Direkt testen
python -m src.ui
```

---

**Template Version:** 0.1  
**Vorbereitet für:** 8-Wochen Softwareentwicklung & Projektmanagement  
**Ziel:** Professionelle Vorbereitung auf echte Projektarbeit  
**Letztes Update:** 2025-01-20

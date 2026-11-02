# Git Workflow

## Branches
- `main` ist immer lauffähig.
- Neue Arbeit in `feat/<name>`, `fix/<name>`, `chore/<name>`.
- Klein halten, früh mergen. Bei Solo-Projekten reicht Merge ohne Review.

## Commits (Conventional Commits)
- Format: `typ: kurze Beschreibung` (Präsens, Englisch)
- Typen: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`
- Ein Commit = eine logische Änderung.

## Releases
- Versionen als Tag: `v0.1.0` (Semantic Versioning: MAJOR.MINOR.PATCH)
- Release erst, wenn `DEFINITION_OF_DONE.md` abgehakt ist.

## Immer
- [ ] `.gitignore` zu Beginn anlegen (Build-Ordner, IDE-Dateien)
- [ ] Keine Secrets, Keys oder Passwörter im Repo
- [ ] Signing Keys und `.env` separat sichern

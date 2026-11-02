# ci-flutter

Workflow-uri GitHub Actions reutilizabile pentru aplicațiile Flutter iOS:

- `ios-unsigned.yml` — IPA nesemnat pentru AltStore/Sideloadly, publicat ca release.
- `ios-testflight.yml` — build semnat + upload TestFlight; verifică expirarea
  ultimului build (reînnoire programată) și versiunea aprobată în App Store.

Fiecare aplicație le apelează cu `uses: kappado2000/ci-flutter/.github/workflows/<fișier>@main`
și `secrets: inherit`. Pași proprii unei aplicații: `ci/prebuild.sh` în repo-ul ei
(primește secretele în `SECRETS_JSON`).

Repo-ul e public: aici nu intră secrete, ID-uri sau URL-uri private.

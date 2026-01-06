# E-ITS (EITS) audit — töökorralduse prompt/mall

Kopeeri see käsk Cursor chatti ja täida `[... ]` kohad.

## Sisend (anna agentile)

- Süsteemi nimi: `[nimi]`
- Omanik/asutus: `[asutus]`
- Auditi eesmärk: `[esmärk]` (nt E-ITS vastavus, parendusplaan, ettevalmistus sertifitseerimiseks)
- Skoop: `[komponendid, teenused, keskkonnad]`
- Andmed: `[isikuandmed? eriliigilised? logid? salastatud?]`
- Autentimine/autoriseerimine: `[OIDC? OAuth? AD? rollid?]`
- Integratsioonid: `[välised süsteemid, API-d, sõnumid]`
- CI/CD: `[GitHub Actions/GitLab/Jenkins; skaneeringud]`
- Operatsioonid: `[monitoring, varundus, intsident, change mgmt]`
- E-ITS meetmete kataloog:
  - kui olemas: lisa fail/tekst või nimeta versioon
  - kui puudub: ütle “kataloogi pole”, agent teeb kategooriapõhise raami

## Väljund (mida agent teeb)

Palun tee järgmised väljundid repo-sse kausta `docs/eits-audit/`:

1. `auditiplaan.md` (skoop, ajakava, rollid, intervjuud, tõendus)
2. `meetmete-maatriks.md` (meede → kontroll → tõendus → omanik → staatus → lünk → tegevus)
3. `protsessikirjeldused/` (eraldi failid vähemalt: ligipääs, muutused, intsident, varundus/taaste, logimine/monitooring, tarnijad)
4. `toendusmaterjali-nimekiri.md` (konkreetsete viidetega: failiteed, süsteemid, reportid)
5. `lunkade-ja-parandusplaan.md` (prioriteet, risk, töömaht, tähtaeg, vastutaja)

Lisaks:

- kui repo-s on konfiguratsiooni/koode, mis juba katab mõne meetme (nt auditilogimine, trace-id, RFC7807), viita nendele ja kirjuta “kuidas see auditis tõendab”.
- ära lisa tundlikke andmeid.


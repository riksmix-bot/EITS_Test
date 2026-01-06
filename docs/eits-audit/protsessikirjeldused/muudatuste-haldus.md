# Protsess: muudatuste haldus (Change Management)

## 1. Eesmärk

Tagada, et muudatused (kood, konfiguratsioon, infrastruktuur) on planeeritud, hinnatud, testitud, heaks kiidetud ja jälgitavad ning ei langeta turbetaset.

## 2. Skoop

- Kehtib: kõik muudatused, mis mõjutavad teenuse funktsionaalsust, turvet, kättesaadavust või andmeid.
- Keskkonnad: [dev/test/stage/prod].
- Erandid: kiireloomulised turvapaigad (kirjeldatud all).

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: SDLC, koodireview, CI/CD, tagasipööramine, haavatavused, auditilogid.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Muudatuse esitaja | kirjeldab muudatuse |  |  |
| Tech lead | tehniline hinnang, riskid |  |  |
| Teenuseomanik | äri- ja prioriteedikinnitus |  |  |
| Infoturve | turberiski hinnang (vajadusel) |  |  |
| Ops/SRE | deploy ja rollback |  |  |

## 5. Sisendid ja väljundid

- Sisendid: muudatuse taotlus (ticket/PR), riskihinnang, testitulemused, skaneeringud.
- Väljundid: kinnitatud muudatus, release notes, deploy log, auditijälg.

## 6. Sammud (töövoog)

1. **Taotlus**: muutus luuakse ticketina/PR-ina (kirjeldus, ulatus, risk, tagasipööramine).
2. **Tehniline kontroll**: koodireview + automaatsed kontrollid (lint/test/build/scan).
3. **Heakskiit**: teenuseomanik (ja vajadusel infoturve) kinnitab prod muudatuse.
4. **Juhtimine**: muudatus ajastatakse ja teavitatakse (kui teenus mõjutatud).
5. **Rakendamine**: deploy vastavalt release protsessile.
6. **Järelkontroll**: monitooring/alertid, smoke test, vajadusel rollback.
7. **Sulgemine**: ticket/PR suletakse koos viidetega tõenditele (checks, logid).

### Kiireloomuline turvapaik (erand)

- Lubatud ainult turvariski vähendamiseks.
- Nõuab minimaalset dokumentatsiooni: põhjus, risk, testitulemus, kinnitaja.
- Järelkontroll ja järelreview 24–72h jooksul.

## 7. Logimine ja tõendusmaterjal

- PR-id, reviewd, CI “checks”, artefaktid, deploy logid, release notes.
- Jälgitavus: muudatus peab olema seostatav konkreetse ticket/PR ID-ga.

## 8. Mõõdikud ja regulaarne ülevaatus

- Muudatuste läbimisaeg.
- Muudatuste edukus (% rollback, incident rate).
- Turvapaikade rakendamise aeg (SLA).

## 9. Erandolukorrad ja eskalatsioon

- Ebaõnnestunud deploy → rollback + incident käsitlus.
- Kriitiline turvalõhe → infoturve + teenuseomanik + kiirprotsess.


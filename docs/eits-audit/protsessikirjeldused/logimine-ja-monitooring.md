# Protsess: logimine ja monitooring

## 1. Eesmärk

Tagada süsteemi töökindluse ja infoturbe jälgitavus: sündmused logitakse, auditilogid on eristatavad ja terviklusega, ning monitooring/alertid tuvastavad olulised anomaaliad.

## 2. Skoop

- Kehtib: rakenduslogid, auditilogid, ligipääsulogid, infrastruktuuri logid.
- Keskkonnad: [prod] (ja vajadusel stage).

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: auditilogimine, intsidentide käsitlus, integratsioonid (correlation-id/trace).

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Ops/SRE | logi kogumine, säilitus, dashboardid, alertid |  |  |
| Infoturve | turbesündmuste reeglid ja ülevaatus |  |  |
| Arendus | logimise standardid ja korrektsus |  |  |
| Teenuseomanik | alertide prioriteedid/SLO |  |  |

## 5. Sisendid ja väljundid

- Sisendid: logimispoliitika, sündmusekataloog, SLO/SLI, riskid.
- Väljundid: dashboardid, alertireeglid, auditilogid, raportid.

## 6. Sammud (töövoog)

1. **Logimisstandard**: määratletakse, mida logitakse ja millal (sh tundliku info punastamine).
2. **Auditilogid**: ärisündmused logitakse struktureeritult ja eraldi kanalisse.
3. **Kogumine**: logid suunatakse keskseks kogumiseks (turvaline transport).
4. **Säilitus & ligipääsud**: säilitusaeg ja ligipääsud on rollipõhised.
5. **Monitooring**: luuakse SLI/SLO dashboardid ja alertireeglid.
6. **Ülevaatus**: regulaarselt vaadatakse üle alertide kvaliteet ja logi-kate.

## 7. Logimine ja tõendusmaterjal

- Logimispoliitika ja näidised (punastatud).
- Dashboardide/alertide nimekiri.
- Auditilogide näide (punastatud), säilituse seaded.

## 8. Mõõdikud ja regulaarne ülevaatus

- Logi katvus (kriitilised sündmused kaetud).
- Alertide “noise” määr (false positives).
- SLO täitmine ja intsidentide trendid.

## 9. Erandolukorrad ja eskalatsioon

- Logi kogumise rike: eskalatsioon Ops; riskihinnang infoturbe poolt.
- Kriitiline turbealert: incident protsess käivitub (vt `intsidentide-kasitlus.md`).


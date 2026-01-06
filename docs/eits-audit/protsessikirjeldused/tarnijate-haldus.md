# Protsess: tarnijate ja teenusepakkujate haldus

## 1. Eesmärk

Tagada, et kolmandate osapooltega seotud riskid on hinnatud, lepingulised turbenõuded on määratletud ning tarnija täitmist jälgitakse auditeeritavalt.

## 2. Skoop

- Kehtib: pilveteenused, majutus, arenduspartnerid, integratsioonipartnerid, kriitilised tarkvaratarnijad.
- Hõlmab: valik, leping, riskihinnang, pidev järelvalve, lõpetamine.

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: riskijuhtimine, ligipääsud, andmekaitse, logimine, jätkusuutlikkus.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Teenuseomanik | tarnija kasutuse otsus; kriitilisus |  |  |
| Hankija/lepingu haldur | leping ja SLA |  |  |
| Infoturve | turbenõuded; riskihinnang |  |  |
| Ops/SRE | tehnilised integratsiooninõuded |  |  |
| DPO (kui kohaldub) | andmetöötlusleping; privaatsus |  |  |

## 5. Sisendid ja väljundid

- Sisendid: tarnija kirjeldus, teenuse kriitilisus, andmed, integratsioonid.
- Väljundid: riskihinnang, turbenõuete lisa, SLA, audititõendid (sertid/raportid), ülevaatusprotokoll.

## 6. Sammud (töövoog)

1. **Eelhindamine**: kriitilisus ja andmed (kas on PII, kas on “kõrge mõju”).
2. **Turbenõuded**: lepingusse lisatakse minimaalsed nõuded (krüpto, logid, teavitused, audit).
3. **Riskihinnang**: infoturve hindab tarnija riskid ja kontrollid.
4. **Kinnitamine**: teenuseomanik kinnitab tarnija kasutuse.
5. **Järelvalve**: regulaarsed ülevaatused (nt kord aastas), sertide uuendused, intsidenditeated.
6. **Lõpetamine**: lepingu lõppemisel andmete tagastus/kustutus, ligipääsude sulgemine.

## 7. Logimine ja tõendusmaterjal

- Lepingud ja turbenõuete lisa.
- Sertifikaadid/raportid (ISO, SOC, pen-test summary, kui olemas).
- Tarnija intsidentide teavituste logi (kui on olnud).
- Ülevaatuse protokollid ja otsused.

## 8. Mõõdikud ja regulaarne ülevaatus

- Kriitiliste tarnijate ülevaatused tehtud ajaks (%).
- Avatud kõrge riskiga tarnijate leidude arv.

## 9. Erandolukorrad ja eskalatsioon

- Tarnija turbeintsident: incident protsess + lepingujärgne teavitamine.
- Tarnija kontrolli puudujääk: parandusplaan või alternatiivne tarnija; eskalatsioon.


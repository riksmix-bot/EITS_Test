# Protsess: riskijuhtimine

## 1. Eesmärk

Tagada, et infoturberiske hinnatakse järjepidevalt, otsused (vähendamine/aktsepteerimine/üleandmine/vältimine) on dokumenteeritud ning riskid seotakse konkreetsete meetmete ja tegevusplaanidega.

## 2. Skoop

- Kehtib: süsteemi/teenuse riskid (turve, kättesaadavus, terviklus, konfidentsiaalsus, vastavus).
- Sagedus: vähemalt [aastas] ja oluliste muudatuste järel.

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: juhtimine, kontrollid, järelvalve, audit.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Teenuseomanik | riskide omanik; otsused |  |  |
| Infoturve | metoodika; ülevaatus; nõustamine |  |  |
| Arendus/Ops | riskide sisend; leevendusmeetmed |  |  |
| Juhtkond | riskide aktsepteerimine (vajadusel) |  |  |

## 5. Sisendid ja väljundid

- Sisendid: arhitektuur, andmed, muutused, intsidentide ajalugu, auditileiud, tarnijad.
- Väljundid: riskiregister, riskihinnang, aktsepteerimisotsused, parandusplaan.

## 6. Sammud (töövoog)

1. **Identifitseerimine**: riskid kogutakse (workshop, threat modeling, leiud).
2. **Hindamine**: mõju × tõenäosus; olemasolevad kontrollid.
3. **Otsus**: vähenda / aktsepteeri / väldi / anna üle.
4. **Tegevusplaan**: konkreetne meede, omanik, tähtaeg, mõõdik.
5. **Jälgimine**: regulaarselt kontrollitakse täitmist ja muutusi riskis.
6. **Ülevaatus**: vähemalt [aastas] ja pärast suuri muudatusi.

## 7. Logimine ja tõendusmaterjal

- Riskiregister (versioon, kuupäev, omanik).
- Aktsepteerimisotsused (kes, millal).
- Seosed parandusplaaniga (`lunkade-ja-parandusplaan.md`).

## 8. Mõõdikud ja regulaarne ülevaatus

- Avatud kõrge riskiga kirjete arv ja vanus.
- Parandusplaani täitmise % tähtaegadeks.

## 9. Erandolukorrad ja eskalatsioon

- Uus kõrge risk: eskalatsioon teenuseomanik + infoturve.
- “Blocker” sõltuvus/tarnija: eskalatsioon juhtkonda.


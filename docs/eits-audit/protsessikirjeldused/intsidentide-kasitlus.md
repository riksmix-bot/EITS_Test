# Protsess: infoturbeintsidentide käsitlus

## 1. Eesmärk

Tagada, et infoturbeintsidendid tuvastatakse, klassifitseeritakse, lahendatakse ja dokumenteeritakse viisil, mis vähendab mõju ning loob auditeeritava järeljälje ja parendustegevused.

## 2. Skoop

- Kehtib: kõik turbeintsidendid ja kahtlased sündmused (sh andmeleke, konto kompromiteerimine, DoS, pahavara, logi-anomaaliad).
- Keskkonnad: [prod] (ja vajadusel teised).

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: logimine/monitooring, eskalatsioon, teavitused, õppetunnid.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Incident manager | juhib käsitlust ja koordineerib |  |  |
| Ops/SRE | tehniline reageerimine ja taastamine |  |  |
| Arendus | vea parandus, hotfix |  |  |
| Infoturve | uurimine, risk, tõendid, teavitused |  |  |
| Teenuseomanik | ärimõju, otsused, kommunikatsioon |  |  |
| DPO (kui kohaldub) | andmekaitse hindamine/teavitused |  |  |

## 5. Sisendid ja väljundid

- Sisendid: alert, kasutajate teavitus, logi-anomaalia, välise osapoole teade, auditileid.
- Väljundid: incident ticket, ajajoon, toimingud, taastamine, juurpõhjus, parandusplaan, (vajadusel) teavitused.

## 6. Sammud (töövoog)

1. **Tuvastus**: sündmus tuvastatakse (alert/teade).
2. **Triaging**: esmane hinnang (tõsidus, ulatus, kas on PII).
3. **Klassifitseerimine**: tüüp + prioriteet + owner määramine.
4. **Piiramine (containment)**: ligipääsude piiramine, liikluse filtreerimine, kompromiteeritud võtmete vahetus.
5. **Uurimine**: logid, auditilogid, süsteemijäljed; tõendite säilitamine.
6. **Likvideerimine (eradication)**: haavatavuse eemaldamine, paigad, konfiguratsioon.
7. **Taastamine (recovery)**: teenuse normaliseerimine, järelvalve tugevdamine.
8. **Sulgemine**: raport (mõju, ajajoon, RCA, õppetunnid) + parandusmeetmed.

## 7. Logimine ja tõendusmaterjal

- Incident ticket (ID), ajajoon, seotud alertid, logi väljavõtted (punastatud), tehtud muudatused (PR-id).
- Säilitusaeg: [täida].

## 8. Mõõdikud ja regulaarne ülevaatus

- MTTD (mean time to detect), MTTR (mean time to recover).
- Korduvate intsidentide määr.
- Pärast-intsidendi parandusmeetmete täitmise %.

## 9. Erandolukorrad ja eskalatsioon

- Kriitiline intsident: kohene eskalatsioon (infoturve + teenuseomanik + ops).
- Isikuandmete rikkumise kahtlus: DPO kaasamine ja teavituste protsess vastavalt nõuetele.


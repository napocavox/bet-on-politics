# Bet on Politics — notă de idee

**Data:** 2026-11-21
**Stare:** idee brută, nevalidată

## Ideea
Aplicație în care utilizatorii pariază pe evenimente politice (alegeri, moțiuni, numiri, legi), cu câștiguri în bani reali.

## Întrebări deschise (de rezolvat înainte de orice cod)

### 1. Legalitate — blocantul principal
- În România, jocurile de noroc cu bani reali cer licență ONJN (OUG 77/2009). Licențierea presupune capital, garanții, KYC/AML, server auditat. *[cunoscut]*
- Dacă pariurile pe evenimente politice sunt permise explicit, interzise sau zonă gri în RO — **neverificat**. *[de verificat]*
- ONJN a blocat platforme de prediction markets (ex. Polymarket) în contextul alegerilor recente — *[cred că da, de confirmat]*. Semnal că autoritatea e ostilă exact acestui segment.
- Alternativă juridică: structurare ca instrument financiar (model Kalshi în SUA) → în UE ar intra sub MiFID II / ASF, și mai costisitor.

### 2. Modelul de business — care dintre ele?
- **Bookmaker** (tu fixezi cotele, îți asumi riscul) — necesită capital și expertiză de pricing.
- **Exchange / prediction market** (utilizatorii pariază între ei, tu iei comision) — risc mic, dar problema „cold start": fără lichiditate, piața e moartă.
- **Fără bani reali** (puncte, clasamente, premii sponsorizate) — evită licența, dar nu mai e ideea inițială.

### 3. Diferențiere
- Ce oferă față de Polymarket, Kalshi, Betfair sau bookmakerii licențiați care au deja piețe politice? Focus local (politică românească / est-europeană) e singurul avantaj evident.

### 4. Riscuri specifice
- Manipulare și insider information (politicienii și staff-ul lor știu rezultatul înainte).
- Dispute de rezolvare (cine decide „rezultatul" la evenimente ambigue?).
- Risc reputațional / politic: acuzații de influențare a alegerilor.
- Volum sezonier (vârfuri doar în ani electorali).

## Următorul pas propus
Verificare juridică (ONJN + un avocat pe gambling) **înainte** de orice prototip.

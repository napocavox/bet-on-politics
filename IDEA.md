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

## Decizii (2026-11-21)
1. **Model:** piață între utilizatori, cu monedă internă. Premiile vin de la sponsori; la egalitate între câștigători se face tombolă.
2. **Obiect:** nu rezultatul alegerilor, ci **promisiunile electorale** și **termenele proiectelor publice anunțate**.
3. **Scop declarat:** un indicator al (ne)încrederii în administrația publică.

## Analiză a deciziilor

### Monedă internă + sponsori + tombolă
- Un joc de noroc presupune trei lucruri: miză, hazard și premiu. Dacă moneda e **gratuită, nu se poate cumpăra și nu se poate preschimba în bani**, miza dispare. Probabil ieșim astfel din regimul de licență ONJN. *[inferență — de confirmat juridic]*
- Tombola reintroduce hazardul. Concursurile promoționale cu premii au regim propriu: regulament public, eventual autorizare, impozit pe premii. *[detaliile neverificate]*
- **Conturi multiple:** cu monedă gratuită și premii reale, oamenii vor crea conturi în plus ca să aibă mai multe șanse. E nevoie de verificarea identității (telefon sau ID) chiar fără bani reali.
- **Sponsorii:** de ce ar plăti o firmă ca să fie asociată cu ideea că „primăria X nu-și ține promisiunile"? Sponsorii plauzibili sunt ONG-urile de bună guvernare, presa și fundațiile, nu brandurile comerciale. Sponsorii politici trebuie excluși (conflict de interese).
- Piețele cu bani fictivi pot prezice bine: există studii care le găsesc comparabile cu cele pe bani reali. *[cunoscut, dar pe sport, nu pe politică locală]*

### Promisiuni și proiecte în loc de alegeri
- **Rezolvare:** promisiunile sunt de obicei vagi („vom moderniza..."). Fiecare piață are nevoie de un criteriu verificabil, de o sursă oficială pentru verificare și de o dată-limită.
- **Proiecte fără termen cunoscut:** o piață are nevoie de un termen. Soluția e o scară de întrebări: „Va fi recepționat X până la 2027-06? până la 2027-12? până la 2028-12?". Din prețuri rezultă o distribuție a datei probabile de finalizare.
- **Indicator cu adevărat nou:** decalajul dintre termenul oficial anunțat și termenul pe care îl estimează piața („decalajul de credibilitate").
- **Există deja ceva asemănător:** urmăritoare de promisiuni precum Factual.ro sau PolitiFact. *[cred că da]* Ce aducem nou e prognoza cu termen, nu evaluarea făcută după.

### „Măsură a încrederii populației" — corecție
- Prețul măsoară **probabilitatea estimată de îndeplinire**, nu încrederea. Cineva bine informat și cineva cinic pot da aceeași probabilitate din motive diferite.
- Participanții se aleg singuri, deci nu sunt reprezentativi pentru populație. Prețul e stabilit de cei mai activi utilizatori.
- Formulare corectă: **estimarea colectivă a credibilității angajamentelor publice**. Pentru „încrederea populației" e nevoie de sondaj, eventual comparat cu piața.

## Decizii (runda 2)
- Venit din **reclame** (model de aplicație clasică), pe lângă sponsori.
- Un participant poate intra în **oricâte** predicții.
- Sursa evenimentelor: **anunțurile primăriilor** (ex.: metroul din Cluj).
- Mecanism: **un participant = o predicție per proiect** = data exactă (zi, lună, an) a dării în folosință.

## Analiză (runda 2)

### Nu mai e o piață, e un concurs de estimări
- Nu există prețuri și nici schimburi între participanți, deci „piața între pariori" nu mai există. Moneda internă **devine inutilă**.
- E mai simplu și mai curat: rezultatul e **distribuția estimărilor** („înțelepciunea mulțimii"). Indicatorul principal: **mediana estimărilor minus data oficială** = decalajul de credibilitate.
- Ca să funcționeze înțelepciunea mulțimii, estimările trebuie să fie independente. **Distribuția celorlalți se afișează doar după ce trimiți estimarea**, altfel participanții se iau unii după alții.

### Regula de câștig
- Șansa de a nimeri ziua exactă e foarte mică, deci regula trebuie să fie **„câștigă cel mai apropiat"** (eroare absolută în zile). La egalitate, tombolă.
- **Avantajul celor care intră târziu:** cine estimează cu o lună înainte de inaugurare știe mult mai mult. Variante:
  (a) estimările se închid la o dată fixă;
  (b) runde anuale, cu clasament separat pe fiecare rundă;
  (c) scor ajustat după cât de devreme ai estimat.
  Recomandare: **(b)**, care oferă și o serie de timp a credibilității.
- **„Dat în folosință"** trebuie definit dinainte: recepția lucrărilor? prima cursă cu pasageri? Iar dacă proiectul se deschide pe etape, se face câte o predicție pe etapă.

### Orizontul lung
- Proiecte ca metroul se termină peste ani. Premiul s-ar acorda abia atunci, iar participanții și sponsorii se pierd pe drum.
- Soluție: **etape intermediare scurte** (contract semnat, autorizație emisă, start forare, stație X finalizată). Asta ține utilizatorii activi și dă rezultate rapid.

### Sursa datelor
- Anunțul primăriei e chiar afirmația care se testează. Sursa care confirmă rezultatul trebuie să fie **independentă** (presă, documente de recepție, SEAP), nu doar primăria.
- Preluarea automată din comunicate e fragilă. La început, o listă selectată manual (10–20 de proiecte) e mai realistă.

### Reclame
- Venitul din reclame depinde de numărul de utilizatori. La câteva mii de utilizatori activi pe lună, un public de nișă local aduce cel mult zeci sau sute de euro pe lună. *[speculație de ordin de mărime, CPM pentru România neverificat]*
- Se poate porni așa, dar reclamele nu vor acoperi premiile. Premiile rămân sarcina sponsorilor.

## Următorul pas propus
Verificare juridică (ONJN + un avocat pe gambling) **înainte** de orice prototip.

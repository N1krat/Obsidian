# 🐾 Operation Purrlington — Task Board

> Hackathon command centre. Keep this up to date throughout the competition.
> **Freeze:** 12:30 | **Checkpoints:** 20:30 (evening) + 08:30 (morning)

---

## 🏆 Scoring at a Glance

| Component | Măsurare | Greutate |
|-----------|----------|----------|
| Tickets rezolvate (oficiale + găsite de noi) | Teste automate | **50%** |
| System performance | Suite automată la checkpoints | **20%** |
| Freestyle feature(s) | Juriu live + demo 5 min | **30%** |

### Formula per ticket
```
score = 0.4 · V  (dacă trece la 20:30)
      + 0.6 · V  (dacă trece la 08:30)
```

| 20:30 | 08:30 | Scor | Ce înseamnă |
|-------|-------|------|-------------|
| ✅ | ✅ | 1.0 · V | Full marks |
| ❌ | ✅ | 0.6 · V | Terminat târziu, dar merge |
| ✅ | ❌ | 0.4 · V | Regresia costă restul |
| ❌ | ❌ | 0 | Neimplementat / greșit |

### Rubrica PR (manual grading)
- **Correctness** — 0.7 · W (problema e rezolvată?)
- **Quality** — 0.2 · W (fix solid, nu hack?)
- **Evidence** — 0.1 · W (PR descrie ce era greșit, cum s-a reparat, cum se verifică?)

### Formula performance
```
score = ⅓ · puncte_20:30 + ⅔ · puncte_08:30
```

### Criterii freestyle (30% din total)
| Criteriu | Puncte |
|----------|--------|
| Relevanță și fit pentru Kiki | 25 |
| Integrare în sistemul existent (idee nouă, nu reskin) | 25 |
| Execuție tehnică | 25 |
| Completitudine și UX | 10 |
| Demo live + pitch | 15 |

---

## ⚙️ Setup Checklist

- [x] Fork repo: `https://github.com/SigmoidAI/faf-hackathon-challenge-public.git`
- [x] Creează repo privat și invită: `@dimatrubca`, `@MrCrowley21`
- [x] Fiecare membru contribuie prin **propriile commit-uri**
- [ ] Acces Coolify (link pe email → "Forgot password?" pentru primul login)
- [ ] Verifică variabilele de mediu din spreadsheet-ul organizatorilor
- [ ] Deploy end-to-end funcțional **înainte de primul checkpoint**
- [ ] Reset baze de date înaintea fiecărei perioade de testare (re-aplică seed data)

---

## ⏰ Deadlines

| Oră | Eveniment |
|-----|-----------|
| **20:30** | 🔴 Checkpoint 1 — teste automate live |
| **08:30** | 🔴 Checkpoint 2 — teste automate live |
| **12:30** | 🛑 Freeze — stop coding, încep prezentările |
| **12:30+** | 🎤 Prezentare 5 min per echipă (tickets + demo freestyle) |

> ⚠️ Dacă niciun serviciu nu e live la checkpoint → scor 0 pentru acel run. Deploy early!
> ⚠️ În fereastra de testare, inbound traffic e restricționat la adresa graderului — normal să pară down.

---

## 🔀 Branch-uri & Responsabilități

| Branch | Owner | Acoperire |
|--------|-------|-----------|
| `dev/frontend` | — | `frontend/` — React, toate feature panels |
| `dev/python-services` | — | `services/airport/` + `services/parrot/` |
| `dev/hotel-beach` | — | `services/hotel/` + `services/beach/` |
| `dev/infra` | — | `gateway/` + `services/broadcast/` |

---

## 📋 Convenție PR

**Nume:** `<ticket_type>_<ticket_name>`
Exemple: `bug_fix_gate_overflow`, `feature_add_priority_lane`, `security_sanitize_parrot_input`

**Tipuri:** `bug` | `feature` | `research` | `security` | `freestyle`

**Descriere obligatorie în fiecare PR:**
1. Ce era greșit / ce lipsea
2. Cum s-a reparat / implementat
3. Cum se verifică (pași de reproducere sau test)

> Orice nu se poate verifica automat e evaluat din PR-urile merged. Fără descriere = 0 la Evidence (0.1·W).

---

## 🚫 Reguli Critice

- **NU schimba contractul public** — endpoint names, paths, request/response schemas, status codes, guests JSON (în afara câmpurilor `avatar` și `personality`). Orice modificare de rută sau payload rupe graderul.
- **Orice schimbare → PR** → merge în `main` → `main` e ce se deployează și se gradează.
- **Branches nemerged = 0 puncte.** Codul neajuns în `main` nu contează.
- **Gateway** trebuie să reflecte starea curentă a serviciilor fără lag.
- **Freestyle feature** trebuie să fie ceva nou, nu un reskin.
- **AI policy:** AI poate fi folosit pentru înțelegere și raționament. Codul trebuie scris și comitat de voi. Dacă majoritatea commiturilor dintr-un PR cu schimbări semnificative sunt de la un agent → 0 puncte pe PR-ul respectiv.

---

## 🎫 Tickets Oficiale (din Trello)

> Mută statusul pe măsură ce lucrezi: `Todo` → `In Progress` → `In Review` → `Done`

### 🐛 Bugs

| # | Titlu | Serviciu | Branch | Puncte | Status |
|---|-------|----------|--------|--------|--------|
| B1 | — | — | — | — | ⬜ Todo |
| B2 | — | — | — | — | ⬜ Todo |
| B3 | — | — | — | — | ⬜ Todo |

### ✨ Feature Requests

| # | Titlu | Serviciu | Branch | Puncte | Status |
|---|-------|----------|--------|--------|--------|
| F1 | — | — | — | — | ⬜ Todo |
| F2 | — | — | — | — | ⬜ Todo |

### 🔬 Research Tickets

| # | Titlu | Serviciu | Branch | Puncte | Status |
|---|-------|----------|--------|--------|--------|
| R1 | — | — | — | — | ⬜ Todo |

### 🔒 Security Tickets

| # | Titlu | Serviciu | Branch | Puncte | Status |
|---|-------|----------|--------|--------|--------|
| S1 | — | — | — | — | ⬜ Todo |

---

## 🕵️ Bugs Găsite de Noi (self-found)

> Când găsești un bug nedocumentat: creează ticket pe Trello, deschide PR cu fix, adaugă aici.
> Format PR: `bug_<descriere_scurta>`

---

### 🔴 CRITICAL — Beach Service (`dev/hotel-beach`)

#### SF-B1 · `addClient()` nu este implementat — SSE complet broken
- **Fișier:** `services/broadcast/src/eventBus.ts`
- **Problemă:** Funcția `addClient(res)` are corp gol (`//TODO: Add client`). Clientul nu e adăugat în array-ul `clients[]`, deci `broadcast()` nu trimite niciodată nimic. **Întregul sistem de real-time events nu funcționează.**
- **Fix:** Adaugă `clients.push(res)` în corpul funcției `addClient`.
- **Branch:** `dev/infra`
- **Status:** ⬜ Todo

#### SF-B2 · `BookActivityUseCase` nu verifică capacitatea — overbooking garantat
- **Fișier:** `services/beach/src/main/kotlin/application/usecase/BookActivityUseCase.kt`
- **Problemă:** `execute()` adaugă vizitatorul la `bookedVisitors` fără a verifica `activity.isFull()`. Activitățile pot fi suprabooking la infinit.
- **Fix:** Verifică `if (activity.isFull()) return "Activity is full"` înainte de add. Returnează eroare în loc de `null`. Controller-ul trebuie să răspundă cu 409 Conflict.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

#### SF-B3 · `bookedVisitors` nu sunt persistați în DB — toate rezervările beach se pierd la restart
- **Fișier:** `services/beach/src/main/kotlin/infrastructure/repository/PostgresActivityRepository.kt`
- **Problemă:** `save()` actualizează doar `name`, `description`, `capacity` — nu există nicio tabelă sau logică pentru a salva lista de vizitatori bokați. `findAll()` și `findById()` construiesc `Activity` cu `bookedVisitors = mutableSetOf()` (mereu gol). Deci `remaining()` returnează mereu `capacity` complet, indiferent de cât de mulți au booked.
- **Fix:** Creează o tabelă de joncțiune `activity_bookings(activity_id, visitor_id)`. `save()` să persiste bookedVisitors. `findById()` și `findAll()` să încarce bookedVisitors din DB.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

#### SF-B4 · NullPointerException — activity not found aruncă crash în loc de 404
- **Fișier:** `services/beach/src/main/kotlin/application/usecase/BookActivityUseCase.kt`, `CancelActivityUseCase.kt`, `ActivityController.kt`
- **Problemă:** `activity!!` aruncă NPE dacă activitatea nu există. `getActivity()` în controller la fel cu `activity!!.id`. Nu există niciodată un răspuns 404.
- **Fix:** Verifică null și returnează eroare corespunzătoare. Controller să răspundă cu `HttpStatusCode.NotFound`.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

#### SF-B5 · `CancelActivityUseCase` nu verifică dacă vizitatorul era bocat
- **Fișier:** `services/beach/src/main/kotlin/application/usecase/CancelActivityUseCase.kt`
- **Problemă:** `remove(visitorId)` pe un set nu dă eroare dacă elementul nu există. Oricine poate "anula" o rezervare inexistentă și primește 200 OK.
- **Fix:** Verifică că `visitorId` este în `bookedVisitors` înainte de remove, altfel returnează eroare.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

#### SF-B6 · `BookActivityUseCase` nu verifică dacă vizitatorul e check-in la hotel
- **Fișier:** `services/beach/src/main/kotlin/application/usecase/BookActivityUseCase.kt`
- **Problemă:** Există `VisitorRepository` cu câmpul `checkedIn`, dar nu e niciodată consultat la booking. Oricine poate booka activități fără să fie check-in.
- **Fix:** Apelează `visitorRepository.findById(visitorId)` și verifică `checkedIn == true`.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

---

### 🔴 CRITICAL — Hotel Service (`dev/hotel-beach`)

#### SF-B7 · Rezervare creată în DB ÎNAINTE de verificarea airport — date murdare la eșec
- **Fișier:** `services/hotel/src/reservation/reservation.service.ts`, metoda `create()`
- **Problemă:** `prisma.reservation.create()` e apelat la linia ~70, iar `rejectIfGuestHasNotClearedAirport()` e apelat DUPĂ (linia ~90). Dacă guest-ul nu a trecut prin airport, excepția e aruncată dar rezervarea rămâne în DB cu status CONFIRMED.
- **Fix:** Mută verificarea airport ÎNAINTE de `prisma.reservation.create()`.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

---

### 🔴 CRITICAL — Airport Service (`dev/python-services`)

#### SF-B8 · Logică inversată la asignarea gate-urilor pentru pasageri EU
- **Fișier:** `services/airport/gate_manager.py`, metoda `assign_and_enqueue()`
- **Problemă:** `gate = all_gate if len(all_gate.queue) < len(eu_gate.queue) else eu_gate` — pasagerii EU sunt trimiși la gate ALL dacă e mai scurt. Logica corectă: EU passengers preferă EU gates; ALL gate e doar fallback.
- **Fix:** `gate = eu_gate if len(eu_gate.queue) <= len(all_gate.queue) else all_gate`
- **Branch:** `dev/python-services`
- **Status:** ⬜ Todo

---

### 🔒 SECURITY — Hotel Service (`dev/hotel-beach`)

#### SF-S1 · SQL Injection în `findActiveByGuestId`
- **Fișier:** `services/hotel/src/reservation/reservation.service.ts`, linia ~145
- **Problemă:** `Prisma.raw(\`'${guestId}'\`)` interpolează direct input-ul utilizatorului în SQL. Un `guestId` de forma `' OR 1=1 --` poate citi toată tabela.
- **Fix:** Înlocuiește cu `prisma.reservation.findFirst()` (Prisma ORM, parametrizat) sau folosește `Prisma.sql` cu parametru, nu `Prisma.raw`.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

#### SF-S2 · SQL Injection în `cancel()`
- **Fișier:** `services/hotel/src/reservation/reservation.service.ts`, linia ~170
- **Problemă:** `Prisma.raw(\`'${id}'\`)` în UPDATE — același pattern injectabil.
- **Fix:** Folosește `prisma.reservation.update({ where: { id }, data: { status: 'CANCELLED' } })`.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

---

### 🔒 SECURITY — Gateway (`dev/infra`)

#### SF-S3 · `AuthMiddleware` este complet ineficient
- **Fișier:** `gateway/auth.go`
- **Problemă:** Ambele ramuri ale if-ului (`key valid` și `else`) apelează `next.ServeHTTP(w, r)`. Middleware-ul nu respinge nicio cerere — orice request trece indiferent de cheia internă.
- **Fix:** Ramura `else` trebuie să returneze 401/403, nu să continue chain-ul.
- **Branch:** `dev/infra`
- **Status:** ⬜ Todo

---

### 🐛 Bugs Medii — Gateway (`dev/infra`)

#### SF-B9 · Race condition în rate limiter — două lock-uri separate
- **Fișier:** `gateway/ratelimit.go`, metoda `allow()`
- **Problemă:** Citirea `cur := w.count` și incrementul `w.count++` se fac sub două lock-uri separate. Între cele două unlock/lock, un alt goroutine poate citi același `cur` și ambii trec de limită.
- **Fix:** Combină citirea și incrementul sub un singur lock.
- **Branch:** `dev/infra`
- **Status:** ⬜ Todo

#### SF-B10 · `cancel()` hotel — UPDATE înainte de verificarea existenței rezervării
- **Fișier:** `services/hotel/src/reservation/reservation.service.ts`, metoda `cancel()`
- **Problemă:** `$executeRaw UPDATE` rulează mai întâi, indiferent dacă rezervarea există. Abia după se verifică cu `findFirst`. Logic incorect și confuz.
- **Fix:** Verifică existența rezervării cu `findUnique` înainte de UPDATE, returnează 404 dacă nu există.
- **Branch:** `dev/hotel-beach`
- **Status:** ⬜ Todo

---

### 🐛 Bugs Medii — Broadcast (`dev/infra`)

#### SF-B11 · Port default greșit în Broadcast
- **Fișier:** `services/broadcast/src/server.ts`
- **Problemă:** `const PORT = process.env.PORT || 3000` — portul default e 3000 (conflictează cu Hotel). Config-ul spune broadcast trebuie pe 3002.
- **Fix:** Schimbă fallback-ul în `|| 3002`.
- **Branch:** `dev/infra`
- **Status:** ⬜ Todo

---

## 🌟 Freestyle Feature(s)

### Feature 1: [Nume TBD]

**Ce face:**
> _Descrie ideea_

**De ce ajută Kiki:**
> _Motivează relevanța_

**Integrare tehnică:**
> _Cum se conectează la sistemul existent_

**Owner:** —
**Branch:** `freestyle/<feature-name>`
**PR:** —
**Status:** ⬜ Todo

---

## 🏗️ Arhitectura Rapidă

```
Frontend (React 19, :5173)
    │
    └─► Gateway (Go, :8000)  ◄── SSE events
            │
    ┌───────┼───────────┬──────────────┐
    ▼       ▼           ▼              ▼
Airport  Hotel       Beach          Parrot
(Python  (NestJS     (Kotlin        (FastAPI
Flask    :3000)      Ktor :8080)    :3003)
:3001)
            │           │              │
            └───────────┴──────────────┘
                        │
                   Broadcast
                 (Node.js SSE :3002)
```

### Regula gateway
Orice serviciu nou sau endpoint nou trebuie adăugat și în gateway (`gateway/`) — frontend vorbește **exclusiv** cu gateway-ul pe `/api/<service>/*`.

---

## 📊 Progress Tracker

### Checkpoint 20:30
- [ ] Toate serviciile pornite și reachable
- [ ] DB reset + seed aplicat
- [ ] Minim X tickets mergate în `main`
- [ ] Freestyle feature vizibil (chiar și parțial)

### Checkpoint 08:30
- [ ] Toate serviciile pornite și reachable
- [ ] DB reset + seed aplicat
- [ ] Toate ticket-urile finalizate mergate
- [ ] Freestyle feature complet și demo-ready

### Prezentare 12:30
- [ ] Slide/demo pregătit
- [ ] Acoperit: ce tickets am rezolvat
- [ ] Acoperit: freestyle — ce este, de ce ajută Kiki, cum funcționează
- [ ] Demo live funcțional

---

## 🔗 Links Utile

- Repo bază: `https://github.com/SigmoidAI/faf-hackathon-challenge-public.git`
- Collaboratori de invitat: `@dimatrubca`, `@MrCrowley21`
- Env variables: spreadsheet organizatori (link în ghid)
- Coolify docs: getting-started + Docker Compose guide
- Trello board: (link de la organizatori)

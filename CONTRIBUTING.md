# Smjernice za doprinos

Dobrodošli! Ovaj vodič pruža sve detalje koji su vam potrebni za učinkovit doprinos projektu. Hvala vam što nam pomažete učiniti **GenAi** boljim alatom za developere širom svijeta. 💡

---

## 📋 Sadržaj

1. [Kodeks ponašanja](#kodeks-ponašanja)
2. [Kako mogu doprinijeti?](#kako-mogu-doprinijeti)
3. [Smjernice za Pull Request](#smjernice-za-pull-request)
4. [Standardi kodiranja](#standardi-kodiranja)
5. [Razvojno postavljanje](#razvojno-postavljanje)
6. [Testiranje](#testiranje)
7. [Deployment](#deployment)
8. [Docker Deployment](#docker-deployment)
9. [VS Code Dev Containers integracija](#vs-code-dev-containers-integracija)

---

## 🛡️ Kodeks ponašanja

Ovaj projekt se vodi našim **Kodeksom ponašanja**. Sudjelovanjem se slažete pridržavati ovog kodeksa. Prijavite neprihvatljivo ponašanje održavateljima projekta.

---

## 🛠️ Kako mogu doprinijeti?

### 1️⃣ Prijavljivanje bugova ili zahtjeva za značajke

- Provjerite issue tracker kako biste izbjegli duplikate.
- Koristite predloške za issue-e (ako su dostupni).
- Pružite detaljne, relevantne informacije i korake za reprodukciju bugova.

### 2️⃣ Doprinosi kodu

1. Forkajte repozitorij.
2. Stvorite feature ili fix branch.
3. Napišite i testirajte svoj kod.
4. Pošaljite pull request (PR).

### 3️⃣ Pridružite se kao glavni contributor

Zainteresirani za održavanje i razvoj projekta? Ispunite naš [Obrazac za prijavu contributora](https://forms.gle/TBSteXSDCtBDwr5m7).

---

## ✅ Smjernice za Pull Request

### PR Checklist

- Granajte se od **main** brancha.
- Ažurirajte dokumentaciju, ako je potrebno.
- Testirajte sve funkcionalnosti ručno.
- Fokusirajte se na jednu značajku/bug po PR-u.

### Proces pregleda

1. Ručno testiranje od strane pregledavača.
2. Potreban je pregled najmanje jednog održavatelja.
3. Odgovorite na komentare iz pregleda.
4. Održavajte čistu commit povijest.

---

## 📏 Standardi kodiranja

### Opće smjernice

- Slijedite postojeći stil koda.
- Komentirajte kompleksnu logiku.
- Držite funkcije malim i fokusiranim.
- Koristite smislena imena varijabli.

---

## 🖥️ Razvojno postavljanje

### 1️⃣ Početno postavljanje

- Klonirajte repozitorij:
  ```bash
  git clone https://github.com/stackblitz-labs/bolt.diy.git
  ```
- Instalirajte ovisnosti:
  ```bash
  pnpm install
  ```
- Postavite environment varijable:
  1. Preimenujte `.env.example` u `.env.local`.
  2. Dodajte svoje API ključeve:
     ```bash
     GROQ_API_KEY=XXX
     HuggingFace_API_KEY=XXX
     OPENAI_API_KEY=XXX
     ...
     ```
  3. Opcionalno postavite:
     - Debug razinu: `VITE_LOG_LEVEL=debug`
     - Veličinu konteksta: `DEFAULT_NUM_CTX=32768`

**Napomena**: Nikada ne commitajte svoju `.env.local` datoteku u kontrolu verzija. Već je u `.gitignore`.

### 2️⃣ Pokretanje razvojnog poslužitelja

```bash
pnpm run dev
```

**Savjet**: Koristite **Google Chrome Canary** za lokalno testiranje.

---

## 🧪 Testiranje

Pokrenite test suite sa:

```bash
pnpm test
```

---

## 🚀 Deployment

### Deploy na Cloudflare Pages

```bash
pnpm run deploy
```

Osigurajte da imate potrebne dozvole i da je Wrangler konfiguriran.

---

## 🐳 Docker Deployment

Ovaj odjeljak opisuje metode za deployment aplikacije korištenjem Dockera. Procesi za **Development** i **Production** su odvojeno navedeni radi jasnoće.

---

### 🧑‍💻 Razvojno okruženje

#### Opcije za izgradnju

**Opcija 1: Helper skripta**

```bash
# Development build
npm run dockerbuild
```

**Opcija 2: Direktna Docker build naredba**

```bash
docker build . --target bolt-ai-development
```

**Opcija 3: Docker Compose profil**

```bash
docker compose --profile development up
```

#### Pokretanje razvojnog kontejnera

```bash
docker run -p 5173:5173 --env-file .env.local bolt-ai:development
```

---

### 🏭 Produkcijsko okruženje

#### Opcije za izgradnju

**Opcija 1: Helper skripta**

```bash
# Production build
npm run dockerbuild:prod
```

**Opcija 2: Direktna Docker build naredba**

```bash
docker build . --target bolt-ai-production
```

**Opcija 3: Docker Compose profil**

```bash
docker compose --profile production up
```

#### Pokretanje produkcijskog kontejnera

```bash
docker run -p 5173:5173 --env-file .env.local bolt-ai:production
```

---

### Coolify Deployment

Za jednostavan proces deploymenta, koristite [Coolify](https://github.com/coollabsio/coolify):

1. Uvezite svoj Git repozitorij u Coolify.
2. Odaberite **Docker Compose** kao build pack.
3. Konfigurirajte environment varijable (npr. API ključeve).
4. Postavite start naredbu:
   ```bash
   docker compose --profile production up
   ```

---

## 🛠️ VS Code Dev Containers integracija

`docker-compose.yaml` konfiguracija je kompatibilna s **VS Code Dev Containers**, što olakšava postavljanje razvojnog okruženja direktno u Visual Studio Code.

### Koraci za korištenje Dev Containers

1. Otvorite command paletu u VS Code-u (`Ctrl+Shift+P` ili `Cmd+Shift+P` na macOS-u).
2. Odaberite **Dev Containers: Reopen in Container**.
3. Odaberite **development** profil kada se to od vas zatraži.
4. VS Code će ponovno izgraditi kontejner i otvoriti ga s prethodno konfiguriranim okruženjem.

---

## 🔑 Environment varijable

Osigurajte da je `.env.local` pravilno konfiguriran sa:

- API ključevima.
- Kontekst-specifičnim konfiguracijama.

Primjer za `DEFAULT_NUM_CTX` varijablu:

```bash
DEFAULT_NUM_CTX=24576 # Koristi 32GB VRAM
```

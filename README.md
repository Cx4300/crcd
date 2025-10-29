# GenAi | Hrvatski poslovni AI!

[![GenAi: AI-Powered Full-Stack Web Development u pregledniku](./public/social_preview_index.jpg)](https://genai.hr)

Dobrodošli u GenAi, hrvatski poslovni AI asistent koji vam omogućuje AI-powered full-stack web development direktno u vašem pregledniku! GenAi podržava OpenAI, Anthropic, Ollama, OpenRouter, Gemini, LMStudio, Mistral, xAI, HuggingFace, DeepSeek i Groq modele - i lako se proširuje za korištenje bilo kojeg drugog modela podržanog Vercel AI SDK-om!

-----

**GenAi | Hrvatski poslovni AI** je izgrađen kao najbolji open source AI coding assistant prilagođen hrvatskom tržištu!

## Sadržaj

- [Pridružite se zajednici](#pridružite-se-zajednici)
- [Značajke](#značajke)
- [Postavljanje](#postavljanje)
- [Pokretanje aplikacije](#pokretanje-aplikacije)
- [Dostupne naredbe](#dostupne-naredbe)
- [Doprinos](#doprinos)
- [Najčešća pitanja](#najčešća-pitanja)

## Pridružite se zajednici

Pridružite se našoj zajednici i surađujte s drugim developerima!

## Značajke

- **AI-powered full-stack web development** za **NodeJS aplikacije** direktno u vašem pregledniku
- **Podrška za više LLM modela** s proširivom arhitekturom za integraciju dodatnih modela
- **Prilaganje slika u promptove** za bolje kontekstualno razumijevanje
- **Integrirani terminal** za pregled izvršavanja LLM naredbi
- **Vraćanje koda na prethodne verzije** za lakše debugiranje i brže izmjene
- **Preuzimanje projekata kao ZIP** za jednostavan prijenos ili sinkronizacija u lokalnu mapu
- **Docker podrška** za jednostavno postavljanje
- **Deploy** direktno na **Netlify**

## Postavljanje

Ako ste novi u instalaciji softvera s GitHuba, ne brinite! Ako naiđete na bilo kakve probleme, slobodno pošaljite "issue" ili poboljšajte ovu dokumentaciju.

## Brzo preuzimanje

[![Preuzmi najnovije izdanje](https://img.shields.io/github/v/release/stackblitz-labs/bolt.diy?label=Preuzmi%20GenAi&sort=semver)](https://github.com/stackblitz-labs/bolt.diy/releases/latest) ← Kliknite ovdje za najnoviju verziju!

- Zatim **kliknite source.zip**

## Preduvjeti

Prije nego započnete, trebat ćete instalirati dva važna softvera:

### Instalacija Node.js

Node.js je potreban za pokretanje aplikacije.

1. Posjetite [Node.js stranicu za preuzimanje](https://nodejs.org/en/download/)
2. Preuzmite "LTS" (Long Term Support) verziju za vaš operativni sustav
3. Pokrenite instalaciju, prihvaćajući zadane postavke
4. Provjerite je li Node.js pravilno instaliran:
   - **Za Windows korisnike**:
     1. Pritisnite `Windows + R`
     2. Upišite "sysdm.cpl" i pritisnite Enter
     3. Idite na "Advanced" tab → "Environment Variables"
     4. Provjerite pojavljuje li se `Node.js` u "Path" varijabli
   - **Za Mac/Linux korisnike**:
     1. Otvorite Terminal
     2. Upišite ovu naredbu:
        ```bash
        echo $PATH
        ```
     3. Potražite `/usr/local/bin` u rezultatu

## Pokretanje aplikacije

Imate dvije opcije za pokretanje GenAi: direktno na vašem računalu ili korištenjem Dockera.

### Opcija 1: Direktna instalacija (Preporučeno za početnike)

1. **Instalirajte Package Manager (pnpm)**:

   ```bash
   npm install -g pnpm
   ```

2. **Instalirajte projektne ovisnosti**:

   ```bash
   pnpm install
   ```

3. **Pokrenite aplikaciju**:

   ```bash
   pnpm run dev
   ```

### Opcija 2: Korištenje Dockera

Ova opcija zahtijeva određeno poznavanje Dockera, ali pruža izoliranije okruženje.

#### Dodatni preduvjet

- Instalirajte Docker: [Preuzmi Docker](https://www.docker.com/)

#### Koraci:

1. **Izgradite Docker Image**:

   ```bash
   # Korištenje npm skripta:
   npm run dockerbuild

   # ILI korištenje direktne Docker naredbe:
   docker build . --target bolt-ai-development
   ```

2. **Pokrenite Container**:
   ```bash
   docker compose --profile development up
   ```

## Konfiguracija API ključeva i pružatelja usluga

### Dodavanje vaših API ključeva

Postavljanje API ključeva u GenAi je jednostavno:

1. Otvorite početnu stranicu (glavni sučelje)
2. Odaberite željenog pružatelja usluga iz padajućeg izbornika
3. Kliknite ikonu olovke (edit)
4. Unesite svoj API ključ u sigurno polje za unos

![Sučelje za konfiguraciju API ključa](./docs/images/api-key-ui-section.png)

### Konfiguracija prilagođenih osnovnih URL-ova

Za pružatelje usluga koji podržavaju prilagođene osnovne URL-ove (kao što su Ollama ili LM Studio), slijedite ove korake:

1. Kliknite ikonu postavki u bočnoj traci za otvaranje izbornika postavki
   ![Lokacija gumba za postavke](./docs/images/bolt-settings-button.png)

2. Idite na karticu "Providers"
3. Potražite svog pružatelja usluga koristeći traku za pretraživanje
4. Unesite svoj prilagođeni osnovni URL u predviđeno polje
   ![Konfiguracija osnovnog URL-a pružatelja usluga](./docs/images/provider-base-url.png)

> **Napomena**: Prilagođeni osnovni URL-ovi su posebno korisni kada pokrećete lokalne instance AI modela ili koristite prilagođene API krajnje točke.

### Podržani pružatelji usluga

- Ollama
- LM Studio
- OpenAILike

## Postavljanje korištenjem Git-a (Samo za developere)

Ova metoda je preporučena za developere koji žele:

- Doprinijeti projektu
- Ostati ažurirani s najnovijim promjenama
- Prebacivati se između različitih verzija
- Stvoriti prilagođene modifikacije

#### Preduvjeti

1. Instalirajte Git: [Preuzmi Git](https://git-scm.com/downloads)

#### Početno postavljanje

1. **Klonirajte repozitorij**:

   ```bash
   git clone -b stable https://github.com/stackblitz-labs/bolt.diy.git
   ```

2. **Navigirajte do direktorija projekta**:

   ```bash
   cd bolt.diy
   ```

3. **Instalirajte ovisnosti**:

   ```bash
   pnpm install
   ```

4. **Pokrenite razvojni poslužitelj**:
   ```bash
   pnpm run dev
   ```

5. **(OPCIONALNO)** Prebacite se na Main branch ako želite koristiti pre-release/testbranch:
   ```bash
   git checkout main
   pnpm install
   pnpm run dev
   ```
   Napomena: Budite svjesni da ovo može imati beta funkcionalnosti i veću vjerojatnost grešaka nego stabilno izdanje

>**Otvorite WebUI za testiranje (Zadano: http://localhost:5173)**
>   - Početnici:
>     - Pokušajte koristiti sofisticirani Provider/Model kao što je Anthropic s Claude Sonnet 3.x modelima za najbolje rezultate
>     - Objašnjenje: Sistemski prompt trenutno implementiran u GenAi ne može pokriti najbolje performanse za sve pružatelje usluga i modele. Stoga bolje funkcionira s nekim modelima nego s drugima, čak i ako su sami modeli savršeni za programiranje
>     - Budućnost: Planirana je Plugin/Extensions biblioteka kako bi postojali različiti sistemski promptovi za različite modele, što će pomoći u postizanju boljih rezultata

#### Ostanite ažurirani

Za dobivanje najnovijih promjena iz repozitorija:

1. **Spremite svoje lokalne promjene** (ako ih ima):

   ```bash
   git stash
   ```

2. **Preuzmite najnovija ažuriranja**:

   ```bash
   git pull
   ```

3. **Ažurirajte ovisnosti**:

   ```bash
   pnpm install
   ```

4. **Vratite svoje lokalne promjene** (ako ih ima):
   ```bash
   git stash pop
   ```

#### Rješavanje problema s Git postavljanjem

Ako naiđete na probleme:

1. **Čista instalacija**:

   ```bash
   # Uklonite node module i lock datoteke
   rm -rf node_modules pnpm-lock.yaml

   # Očistite pnpm cache
   pnpm store prune

   # Ponovno instalirajte ovisnosti
   pnpm install
   ```

2. **Resetirajte lokalne promjene**:
   ```bash
   # Odbacite sve lokalne promjene
   git reset --hard origin/main
   ```

Ne zaboravite uvijek commitati svoje lokalne promjene ili ih stashati prije preuzimanja ažuriranja kako biste izbjegli konflikte.

---

## Dostupne naredbe

- **`pnpm run dev`**: Pokreće razvojni poslužitelj.
- **`pnpm run build`**: Gradi projekt.
- **`pnpm run start`**: Pokreće izgrađenu aplikaciju lokalno koristeći Wrangler Pages.
- **`pnpm run preview`**: Gradi i pokreće produkcijsku verziju lokalno.
- **`pnpm test`**: Pokreće test suite koristeći Vitest.
- **`pnpm run typecheck`**: Pokreće TypeScript provjeru tipova.
- **`pnpm run typegen`**: Generira TypeScript tipove koristeći Wrangler.
- **`pnpm run deploy`**: Deploya projekt na Cloudflare Pages.
- **`pnpm run lint:fix`**: Automatski ispravlja linting probleme.

---

## Doprinos

Pozdravljamo doprinose! Pogledajte naš [Vodič za doprinos](CONTRIBUTING.md) za početak.

---

## Najčešća pitanja

Za odgovore na uobičajena pitanja, probleme i popis preporučenih modela, posjetite našu [FAQ stranicu](FAQ.md).

# Licenciranje

**Tko treba komercijalnu WebContainer API licencu?**

GenAi source kod je distribuiran kao MIT, ali koristi WebContainers API koji [zahtijeva licenciranje](https://webcontainers.io/enterprise) za produkcijsku upotrebu u komercijalnom okruženju s ciljem profita. (Prototipovi ili POC-ovi ne zahtijevaju komercijalnu licencu.) Ako koristite API za zadovoljavanje potreba vaših klijenata, potencijalnih klijenata i/ili zaposlenika, potrebna vam je licenca kako biste osigurali sukladnost s našim Uvjetima pružanja usluge. Korištenje API-ja kršenjem ovih uvjeta može rezultirati opozvanjem vašeg pristupa.

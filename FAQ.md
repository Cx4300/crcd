# Najčešća pitanja (FAQ)

<details>
<summary><strong>Koji su najbolji modeli za GenAi?</strong></summary>

Za najbolje iskustvo s GenAi, preporučujemo korištenje sljedećih modela:

- **Claude 3.5 Sonnet (stara verzija)**: Najbolji sveukupni coder, pruža izvrsne rezultate u svim slučajevima korištenja
- **Gemini 2.0 Flash**: Iznimna brzina uz održavanje dobrih performansi
- **GPT-4o**: Snažna alternativa Claude 3.5 Sonnetu sa sličnim mogućnostima
- **DeepSeekCoder V2 236b**: Najbolji open source model (dostupan putem OpenRouter, DeepSeek API-ja ili self-hosted)
- **Qwen 2.5 Coder 32b**: Najbolji model za self-hosting s razumnim hardverskim zahtjevima

**Napomena**: Modeli s manje od 7b parametara obično nemaju sposobnost pravilne interakcije s GenAi!

</details>

<details>
<summary><strong>Kako postići najbolje rezultate s GenAi?</strong></summary>

- **Budite specifični o vašem stacku**:
  Navedite frameworke ili biblioteke koje želite koristiti (npr. Astro, Tailwind, ShadCN) u vašem početnom promptu. To osigurava da GenAi postavlja projekt prema vašim preferencijama.

- **Koristite ikonu za poboljšanje prompta**:
  Prije slanja prompta, kliknite ikonu _enhance_ kako bi AI poboljšao vaš prompt. Možete urediti predložena poboljšanja prije slanja.

- **Prvo postavite osnove, zatim dodajte značajke**:
  Osigurajte da je temeljna struktura vaše aplikacije na mjestu prije uvođenja napredne funkcionalnosti. To pomaže GenAi-u da uspostavi čvrstu osnovu na kojoj se može graditi.

- **Grupirajte jednostavne upute**:
  Kombinirajte jednostavne zadatke u jedan prompt kako biste uštedjeli vrijeme i smanjili potrošnju API kredita. Na primjer:
  _"Promijeni shemu boja, dodaj mobilnu responzivnost i ponovno pokreni razvojni poslužitelj."_
</details>

<details>
<summary><strong>Kako mogu doprinijeti GenAi?</strong></summary>

Pogledajte naš [Vodič za doprinos](CONTRIBUTING.md) za više detalja o tome kako se uključiti!

</details>

<details>
<summary><strong>Koji su budući planovi za GenAi?</strong></summary>

Posjetite naš Roadmap za najnovija ažuriranja.
Nove značajke i poboljšanja su na putu!

</details>

<details>
<summary><strong>Zašto postoji toliko otvorenih problema/pull requestova?</strong></summary>

GenAi je započeo kao mali showcase projekt koji je brzo prerastao u masivan zajednički napor!

Formiramo tim održavatelja za upravljanje potražnjom i pojednostavljenje rješavanja problema. Održavatelji su rockstars, a također istražujemo partnerstva koja pomažu projektu da napreduje.

</details>

<details>
<summary><strong>Kako se lokalni LLM-ovi uspoređuju s većim modelima poput Claude 3.5 Sonneta za GenAi?</strong></summary>

Iako se lokalni LLM-ovi brzo poboljšavaju, veći modeli poput GPT-4o, Claude 3.5 Sonneta i DeepSeek Codera V2 236b još uvijek nude najbolje rezultate za kompleksne aplikacije. Naš tekući fokus je poboljšanje promptova, agenata i platforme kako bi se bolje podržali manji lokalni LLM-ovi.

</details>

<details>
<summary><strong>Uobičajene greške i rješavanje problema</strong></summary>

### **"Došlo je do greške pri obradi ovog zahtjeva"**

Ova generička poruka o grešci znači da nešto nije u redu. Provjerite oboje:

- Terminal (ako ste pokrenuli aplikaciju s Dockerom ili `pnpm`).
- Developer konzolu u vašem pregledniku (pritisnite `F12` ili desni klik > _Inspect_, zatim idite na karticu _Console_).

### **"x-api-key header nedostaje"**

Ova greška se ponekad rješava ponovnim pokretanjem Docker kontejnera.
Ako to ne funkcionira, pokušajte se prebaciti s Dockera na `pnpm` ili obrnuto. Aktivno istražujemo ovaj problem.

### **Prazan pregled pri pokretanju aplikacije**

Prazan pregled često se javlja zbog haluciniranog lošeg koda ili netočnih naredbi.
Za rješavanje problema:

- Provjerite developer konzolu za greške.
- Zapamtite, pregledi su osnovna funkcionalnost, tako da aplikacija nije pokvarena! Radimo na tome da ove greške učinimo transparentnijim.

### **"Sve radi, ali su rezultati loši"**

Lokalni LLM-ovi poput Qwen-2.5-Codera su moćni za male aplikacije, ali su još eksperimentalni za veće projekte. Za bolje rezultate, razmislite o korištenju većih modela poput GPT-4o, Claude 3.5 Sonneta ili DeepSeek Codera V2 236b.

### **"Primljena strukturirana iznimka #0xc0000005: access violation"**

Ako dobivate ovo, vjerojatno ste na Windowsu. Rješenje je obično ažuriranje [Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

### **"Miniflare ili Wrangler greške u Windowsu"**

Morat ćete se uvjeriti da imate najnoviju verziju Visual Studio C++ instaliranu (14.40.33816).

</details>

---

Imate još pitanja? Slobodno nas kontaktirajte ili otvorite issue u našem GitHub repozitoriju!

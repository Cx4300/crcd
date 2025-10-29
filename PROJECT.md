# Upravljanje projektom GenAi

Prvo: ovo zvuči smiješno, znamo. "Upravljanje projektom" dolazi iz svijeta enterprise stvari, a ovaj projekt je daleko od toga - još uvijek je anarhija svuda 😉

Ali moramo se nekako organizirati, zar ne?

> tl;dr: Imamo project board s epicima i značajkama. Koristimo PR-ove kao change log i kao materijalizirane značajke. Pronađite ga [ovdje](https://github.com/orgs/stackblitz-labs/projects/4).

Evo kako strukturiramo dugoročnu viziju, srednjoročne sposobnosti softvera i kratkoročna poboljšanja.

## Strateški epici (dugoročno)

Strateški epici definiraju područja u kojima se proizvod razvija. Obično se ovi epici ne preklapaju. Oni bi trebali omogućiti osnovnom timu da definira što vjeruju da je najvažnije i na čemu bi trebalo raditi s najvećim prioritetom.

Možete pronaći [epice kao issue-e](https://github.com/stackblitz-labs/bolt.diy/labels/epic) koji vjerojatno nikada neće biti zatvoreni.

Koja je korist / svrha epica?

1. Prioritizacija

Npr. mogli bismo reći "upravljanje datotekama je trenutno važnije od kvalitete". Tada bismo mogli razmišljati o tome koje značajke bi unaprijedile "upravljanje datotekama". To mogu biti različite značajke, kao što su "upload lokalnih datoteka", "import iz repozitorija" ili također undo/redo/commit.

Na više-manje redovnom sastanku posvećenom tome, osnovni tim raspravlja koji epici najviše znače, skicira značajke i zatim provjerava tko može raditi na njima. Nakon sastanka, ažuriraju roadmap (barem za sljedeći razvojni ciklus) i na taj način komuniciraju gdje je fokus trenutno.

2. Grupiranje značajki

Povezivanjem značajki s epicima, možemo ih držati zajedno i dokumentirati _zašto_ ulažemo rad u određenu stvar.

## Značajke (srednjoročno)

Svi vjerojatno znamo desetak metodologija prema kojima se opisuju značajke (User story, business funkcija, nazovite to kako želite).

Međutim, namjerno opisujemo značajke na nejasni način. Zašto? Svi vole jasne, dobro definirane kriterije prihvaćanja, zar ne? Pa, svaki product owner to voli, jer zna što će dobiti kada bude gotovo.

Ali: **ovdje nema vlasnika ovog proizvoda**. Stoga dajemo _maksimalnu fleksibilnost developeru koji doprinosi značajku_ - kako bi mogao unijeti svoje ideje i imati najviše zabave implementirajući je.

Značajka stoga pokušava opisati _što_ treba poboljšati, ali ne detaljno _kako_.

## PR-ovi kao materijalizirane značajke (kratkoročno)

Nakon što developer počne raditi na značajki, draft-PR _može_ biti otvoren što prije kako bi se podijelilo, opisalo i raspravljalo kako bi značajka trebala biti implementirana. Ali: ovo nije obavezno. Samo pomaže dobiti ranu povratnu informaciju i uključiti druge developere. Ponekad developer samo želi započeti i zatim otvoriti PR kasnije.

U labavo organiziranom projektu, može se također dogoditi da se otvori više PR-ova za istu značajku. To nije pravi problem: Obično su ljudi koji su strastveni o rješenju spremni udružiti snage i dovršiti ga zajedno. A ako je drugi developer bio brži u realizaciji iste značajke: Budite sretni što je gotovo, zatvorite PR i potražite sljedeću značajku za implementaciju 🤓

## PR-ovi kao change log

Nakon što je PR spojen, squashed commit sadrži cijeli PR opis što omogućuje dobar change log.
Svi autori commita u PR-u su spomenuti u squashed commit poruci i postaju contributori 🙌

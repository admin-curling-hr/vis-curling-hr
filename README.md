# Curling klub Vis — web stranica

Stranica kluba na **https://vis.curling.hr** (GitHub Pages, grana `main`, korijen repozitorija).
Potpuno samostalna: ne koristi ništa sa stranica Hrvatskog curling saveza (curling.hr).
Repozitorij: `admin-curling-hr/vis-curling-hr`. Do studenoga 2026. stranica je bila u mapi `vis/`
repozitorija `admin-curling-hr/curling-hr` (ta mapa je uklonjena, bez preusmjeravanja).

## Datoteke

```
index.html            — početna stranica kluba (O klubu, kontakt, akti)
vis.css               — stilovi (zajednički za index.html i pristupnica.html)
logo.png              — logotip kluba (zaglavlje, ikona, PDF)
statut.pdf            — Statut kluba
pristupnica.html      — obrazac Pristupnice (bez poveznice u izborniku osim s početne)
pristupnica.css       — stilovi obrasca
pristupnica.js        — logika obrasca i izrada PDF-a u pregledniku (tekstovi i postavke na vrhu)
vendor/jspdf/         — biblioteka jsPDF (MIT) za izradu PDF-a
fonts/                — Liberation Sans (podskup, OFL) za hrvatska slova u PDF-u
.nojekyll             — GitHub Pages poslužuje datoteke kakve jesu (bez Jekylla)
CNAME                 — prilagođena domena vis.curling.hr (postavlja GitHub, ne brisati)
```

Pristupnica se ispunjava u pregledniku; podaci se nigdje ne šalju, PDF se izrađuje na uređaju
i član ga šalje klubu na vis@curling.hr.

## Domena

`vis.curling.hr` je u Cloudflareu (zona curling.hr) zapis **CNAME → `admin-curling-hr.github.io`**,
*DNS only* (sivi oblak). U repozitoriju: *Settings → Pages → Custom domain* = `vis.curling.hr`,
*Enforce HTTPS* uključeno.

## Statistika posjeta

Cloudflare Web Analytics (bez kolačića): Cloudflare → *Observability → Analytics → Web analytics* →
`vis.curling.hr`, način *Enable with JS Snippet installation* (domena je sivi oblak, pa automatsko
ubacivanje ne radi). Skripta je u `<head>` stranica `index.html` i `pristupnica.html` i učitava se samo
na `vis.curling.hr`. Nova HTML stranica treba dobiti isti blok.

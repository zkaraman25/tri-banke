# Tri banke — pozivnica

Jedan HTML fajl (index.html) + slika za WhatsApp preview (og.png).
Nema builda, nema ovisnosti.

## Objava (GitHub + Cloudflare Pages)

1. GitHub: New repository, ime `tri-banke`, vidljivost **Public**
   (besplatni GitHub hosting/integracije traže public repo).
2. "uploading an existing file" → povuci `index.html`, `og.png` i ovaj
   README → Commit.
3. Cloudflare: dash.cloudflare.com → Workers & Pages → Create → Pages
   → **Connect to Git** → odaberi repo `tri-banke`.
   Framework preset: None. Build command: prazno. Output directory: `/`.
   → Save and Deploy.
4. Stranica je na `https://tri-banke.pages.dev`. Svaki commit na main
   se sam objavi za ~30 sekundi.

Ako projekt nazoveš drugačije, u `index.html` promijeni domenu u
`og:url` i `og:image` (dvije linije u <head>) i commitaj.

## Prije slanja pozivnice (checklista)

1. Power Automate: u trigeru regeneriraj SAS potpis → kopiraj novi URL.
2. `index.html` → CONFIG → zalijepi novi `FLOW_URL`.
3. CONFIG → `DEMO: false`.
4. Commit → pričekaj deploy → otvori stranicu **na mobitelu**:
   pjesma (klik na ploču), prijava sa svojim imenom, popup,
   run history flowa = Succeeded, novi red u Excelu (s kolonom Cuga).
5. Tek onda šalji link na WhatsApp.

## Terminal varijanta (opcionalno)

    git clone https://github.com/TVOJ-USERNAME/tri-banke.git
    cd tri-banke
    # kopiraj index.html, og.png, README.md u ovaj folder
    git add -A && git commit -m "pozivnica" && git push

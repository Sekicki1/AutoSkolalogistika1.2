# Auto škola Logistika - sajt

Ovo je čist statički sajt (HTML + CSS + malo vanilla JS, bez ikakvih eksternih build alata ili
zavisnosti od bilo kog dizajn-alata). Spreman za GitHub Pages.

## Hostovanje na GitHub Pages
1. Napravi novi GitHub repozitorijum (ili iskoristi postojeći).
2. Ubaci sadržaj ovog foldera (`index.html` i `assets/`) u root repozitorijuma - sada nema
   fajlova preko par MB, tako da "Add file → Upload files" u browseru treba da radi normalno.
3. Settings → Pages → Source: postavi na `main` granu, `/ (root)` folder.
4. Sačekaj minut-dva, sajt će biti dostupan na `https://<korisnicko-ime>.github.io/<repo-ime>/`.

## Struktura
- `index.html` - kompletan sajt, jedna stranica
- `assets/` - sve slike (logo, vozila, galerija, recenzije, pozadina)

## Napomena o videu u hero sekciji
Pozadinski video je uklonjen iz ovog paketa (bio je prevelik za GitHub web upload). Umesto njega,
hero pozadina sada koristi statičku fotografiju (grayscale, 30% providnosti) - nema više fajlova
preko par MB u celom paketu, tako da "upload files" u browseru treba da radi bez problema. Ako
kasnije poželiš video pozadinu, host-uj je eksterno (Cloudflare Stream, Mux, Streamable) i ubaci
je kao `<video src="https://...">` ili `<iframe>`, umesto lokalnog fajla.

## Šta je urađeno
Sajt je edge-to-edge (nema neželjenih margina na `html`/`body`, sekcije su pune širine, sadržaj
je centriran unutar `max-width: 1180px` kontejnera). Sve interakcije (glatki skrol, custom kursor
u obliku zastavice, animacija brojanja statistike, pop-in animacije za "Za vas smo obezbedili" i
Galeriju, zvezdice ocena, lightbox za slike, hover efekti na dugmadima i navigaciji) su prevedene
u čist CSS + vanilla JavaScript - nema zavisnosti od bilo kog internog alata, radi svuda gde radi
običan HTML sajt.

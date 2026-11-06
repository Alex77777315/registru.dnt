# DNT CENTRAL

**One Organization. One System. One Direction.**

Platforma digitală a Direcției Naționale a Tinerilor (DNT).

## Structură

| Folder | Conținut |
|---|---|
| `site-public/` | Site-ul public (HTML static, merge oriunde). Se publică automat pe GitHub Pages. |
| `evidenta-intern/` | Evidența internă a Board-ului: voluntari, filiale, registru intrare/ieșire, departamente, audit. |
| `evidenta-intern/seed-departamente.json` | Cele 8 departamente cu responsabilități și reguli (date demonstrative editabile). |
| `assets/` | Logo DNT. |

## Site public

1. Creează repository-ul pe GitHub și urcă tot conținutul.
2. Settings → Pages → Source: **GitHub Actions**.
3. La fiecare push pe `main` se publică folderul `site-public/`.
4. În `site-public/index.html` schimbă `CONTACT_EMAIL` cu adresa reală.

## Evidența internă

`evidenta-intern/index.html` a fost construită pentru a rula ca pagină publicată pe claude.ai (baza de date, accesul pe board și exportul vin din runtime-ul acelei platforme). **Nu funcționează deschisă direct din fișier sau pe GitHub Pages.**

Pentru o platformă proprie, următorul pas este migrarea la Next.js + Supabase (autentificare, PostgreSQL, RLS pe roluri, storage pentru documente). Colecțiile curente (`volunteers`, `branches`, `departments`, `register`, `audit`) se mapează direct pe tabele.

## Notă GDPR

Nu se stochează CNP. Datele personale nu se afișează public. Voluntarii minori necesită acord parental înregistrat.

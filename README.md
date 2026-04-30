# Playdate PartyApp — Website

Statische Website für [playdate-party.app](https://playdate-party.app),
gehostet auf GitHub Pages.

## Inhalt

- `index.html` — Landing-Page
- `privacy.html` — Datenschutzerklärung (DSGVO + österreichisches DSG)
- `impressum.html` — Impressum (§ 5 ECG + § 25 Mediengesetz)
- `style.css` — Shared styles
- `CNAME` — verknüpft das GitHub-Pages-Deployment mit der Custom-Domain

## Deployment

1. Repo auf GitHub erstellen: `playdate-website` (public)
2. Diesen Ordner-Inhalt in den `main` branch pushen
3. **Settings → Pages** → Source: `Deploy from a branch` → Branch `main` / `(root)`
4. Custom domain: `playdate-party.app` (CNAME-File ist bereits drin)
5. „Enforce HTTPS" aktivieren (sobald GitHub das Zertifikat bereitgestellt hat,
   dauert ~10 min nach DNS-Propagation)

## DNS bei Porkbun

Folgende Records anlegen (Domain-Management → DNS):

```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
CNAME www   mikevallas.github.io   (bzw. dein-username.github.io)
```

Propagation: 10–60 Minuten.

## Updates

Lokal Änderungen machen → committen → pushen.
GitHub Pages deployt automatisch.

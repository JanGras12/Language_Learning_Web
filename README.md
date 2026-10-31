# Quadern d'Idiomes

Quadern d'estudi web per a japonès (A1–B2), rus, coreà, xinès, alemany i àrab (A1–B1): alfabet, gramàtica, vocabulari per nivells i categories, transliteració i IPA. Interfície en català (i anglès, parcialment).

## Avís

- El contingut l'ha generat una IA (Claude) i **no l'ha revisat cap parlant nadiu**. Pot contenir errors de traducció, vocalització, formes verbals o pronunciació.
- Els nivells (A1, A2, B1, B2) són estimacions, no llistes oficials.
- El progrés («Après») es desa només al navegador de cada persona (localStorage). Si s'esborren les dades del navegador, es perd.

## Estructura

- `index.html`: tota l'aplicació (HTML, CSS i JavaScript en un sol fitxer).
- `data/<idioma>.json`: contingut de cada idioma (ja, ru, ko, zh, de, ar).
- `data/stats.json`: recompte de paraules per categoria i nivell.
- `.nojekyll`: fa que GitHub Pages serveixi els fitxers tal com són.

## Provar-ho al teu ordinador

Cal un servidor local (obrir `index.html` amb doble clic no funciona, perquè el navegador bloqueja la lectura de `data/`):

```
cd carpeta-del-quadern
python3 -m http.server 8000
```

i obre http://localhost:8000

## Publicar-ho a GitHub Pages (gratuït)

1. Crea un compte a github.com (si no en tens).
2. Crea un repositori nou i **públic** (p. ex. `quadern-idiomes`).
3. Dins el repositori: **Add file → Upload files**, arrossega-hi el contingut d'aquesta carpeta (`index.html`, la carpeta `data`, `.nojekyll`, `README.md`) i fes **Commit changes**.
4. **Settings → Pages**. A «Build and deployment», «Source»: **Deploy from a branch**; branca `main`, carpeta `/ (root)`; **Save**.
5. Al cap d'uns minuts la pàgina és a `https://<el-teu-usuari>.github.io/quadern-idiomes/`.

Nota: `.nojekyll` comença amb un punt i alguns sistemes l'amaguen; si no el pots pujar, la pàgina hauria de funcionar igualment.

## Actualitzar-ho

Torna a pujar `index.html` i/o els fitxers de `data/` que hagin canviat (Upload files substitueix els que tenen el mateix nom).

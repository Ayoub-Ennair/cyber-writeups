# Ayoub Ennair — Cybersecurity Fieldnotes / Carnets de terrain cyber

Blog bilingue FR/EN de writeups CTF, notes de labs autorisés et recherche en cybersécurité. Thème : [Fuwari](https://github.com/saicaca/fuwari) (Astro, licence MIT).

## Publication manuelle sur GitHub Pages

1. Crée sur GitHub un dépôt **public** nommé exactement `cyber-writeups` sous le compte `Ayoub-Ennair`. Si ce compte ou ce dépôt n’est pas le bon, adapte `site` et `base` dans `astro.config.mjs`, ainsi que les liens de `src/config.ts`.
2. Depuis ce dossier, lance :
   ```bash
   git init -b main
   git add .
   git commit -m "Set up bilingual cybersecurity writeups blog"
   git remote add origin https://github.com/Ayoub-Ennair/cyber-writeups.git
   git push -u origin main
   ```
3. Dans GitHub : **Settings → Pages → Build and deployment → Source → GitHub Actions**.
4. Ouvre l’onglet **Actions** et vérifie le workflow “Deploy Astro site to GitHub Pages”. À la fin, le blog sera à : <https://ayoub-ennair.github.io/cyber-writeups/>.

Le workflow redéploie automatiquement à chaque `push` sur `main`. Le dépôt public et le site Pages sont consultables par tous. Ne publie ni secrets, ni tokens, ni identifiants, ni données de cible réelle.

## Écrire un article

- Crée un fichier Markdown dans `src/content/posts/`, par exemple `src/content/posts/nom-du-challenge.md`.
- Copie le frontmatter et les rubriques depuis [`WRITEUP_TEMPLATE.md`](./WRITEUP_TEMPLATE.md).
- Mets `draft: false` pour publier et `lang: fr` ou `lang: en` pour déclarer la langue de l’article. Le thème gère un billet dans une langue à la fois ; ce starter n’ajoute pas un sélecteur automatique de traductions jumelles.
- Pour prévisualiser localement : Node.js 20+, pnpm 9+ ; `pnpm install`, puis `pnpm dev`.
- Pour vérifier la sortie : `pnpm build`.

## Personnalisation

- Site, profil et liens : `src/config.ts`.
- URL GitHub Pages : `astro.config.mjs`.
- Présentation bilingue : `src/content/spec/about.md`.
- Marque SVG : `public/assets/images/cyber-mark.svg`.

## Usage responsable

Les writeups doivent rester dans le cadre de CTF/labs autorisés. Expurge les preuves, évite les données personnelles et n’inclus jamais de valeurs secrètes.

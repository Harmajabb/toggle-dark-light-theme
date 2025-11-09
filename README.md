# 🌙 React Toggle Light/Dark Theme

Petit composant React + TypeScript pour basculer entre le thème clair et le thème sombre.  
Développé par **Léa François** – Wild Code School.

---

## Aperçu
![Aperçu du composant Toggle light](./image.png)
![Aperçu du composant Toggle dark](./image-dark.png)

---

## Utilisation

### 1. Copier les fichiers

Copiez `Toggle.tsx` et `Toggle.css` dans votre dossier `src/` de projet React.

### 2. Importer le composant

`import Toggle from "./Toggle";`

`function App() {`
`  return (`
`    <div>`
`      <Toggle />`
`    </div>`
`  );`
`}`

### 3. Ajouter les styles

Importez le fichier CSS dans votre composant principal (généralement `App.tsx` ou `index.tsx`) et assuerez-vous d'avoir les styles pour les thèmes clair et sombre dans votre CSS global.

`:root[data-theme="light"] {`
`  --bg: #ffffff;`
`  --fg: #111111;`
`}`

`:root[data-theme="dark"] {`
`  --bg: #111111;`
`  --fg: #ffffff;`
`}`

`body {`
`  background: var(--bg);`
`  color: var(--fg);`
`  transition: background 0.3s, color 0.3s;`
`}`

---

## Fonctionnement

- Le composant utilise un état local `(Local Storage)` pour suivre le thème actuel (clair ou sombre).
- Si aucun thème n'est stocké, il détecte la préférence du système de l'utilisateur.
- Le thème est appliqué en ajoutant un attribut `data-theme` à l'élément racine `<html>`.
- Le bouton affiche une icône de soleil pour le thème clair et une icône de lune pour le thème sombre.

---

## Personnalisation

Vous pouvez personnaliser les styles dans `Toggle.css` pour correspondre à l'esthétique de votre application.
J'ai laissé une classe `theme-toggle` pour le bouton, que vous pouvez styliser selon vos besoins.
Merci de ne pas toucher au Aria pour l'accessibilité !

Exemple de styles de base dans `Toggle.css` :

`.theme-toggle {`
`  background: var(--fg);`
`  color: var(--bg);`
`  border: none;`
`  border-radius: 12px;`
`  padding: 0.6rem 1rem;`
`  font-size: 1rem;`
`  cursor: pointer;`
`  transition: 0.3s;`
`}`

`.theme-toggle:hover {`
`  opacity: 0.8;`
`}`

---

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## Details techniques

- **Langage** : TypeScript + React
- **Stockage** : Local Storage pour mémoriser le thème choisi
- **Accessibilité** : Utilisation des attributs ARIA pour une meilleure expérience utilisateur
- **Compatibilité** : Fonctionne avec les préférences de thème du système d'exploitation
- **Niveau** : Débutant à intermédiaire

## Contributions

Tu peux faire un fork de ce projet pour modifier ou améliorer le composant selon tes besoins (ajout de fonctionnalités, amélioration des styles, etc.).
N'hésite pas à proposer des pull requests si tu souhaites contribuer au projet !

## Auteur 

Développé par **Léa François** – Wild Code School, promo bootcamp septembre 2025.
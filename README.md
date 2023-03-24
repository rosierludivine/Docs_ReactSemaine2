# Docs_ReactSemaine2

mon git [https://github.com/rosierludivine/ReactProjetSemaine2](https://github.com/rosierludivine/ReactProjetSemaine2)
exemple pour le readme  bendahmanam/b2-assets.git
npm run … sert a executer des script exemple si npm run toto affiche echo run toto

#Vite 
Ameliorer l’experience développeur remplace CRA (create react table ) pnpm plus rapide instantanée 
Apporte de l’expérience passez par vite 
Migration le projet JS avec Vite 
sdk (software developpement kit)

//Installation de Vite
    npm create vite@latest
// Le nom du fichier 
// on passe 
//on choisi React
// Javascript 

// lancer le projet/ allez dans le dossier du projet
    npm install 
//lancer 
    npm run dev
    
#Installation de l’Outils Tailwinds
Lien: [https://tailwindcss.com/](https://tailwindcss.com/)
[https://tailwindcss.com/docs/guides/vite](https://tailwindcss.com/docs/guides/vite)
Tailwinds est une Bibliothèques de classes css, 
-D periode de développement 
Après  avoir créer notre projet

// Créer un projet react avec tailwind et Vue avancées 
    npm create vite@latest my-project -- --template react
    cd my-project
    
Pour ajouter tailwind sur un project react déjà créer avec Vite
// Générer un fichier pour savoir comment sa fonctionne 

npx tailwindcss init -p
// remplacer les informations dans le fichier générer
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

//Copier coller c'est trois ligne ci dessous a la place du css 
@tailwind base;
@tailwind components;
@tailwind utilities;

// Dans le terminal pour tester 
npm run dev

// Dans App.jsx colelr ceci 
export default function App() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}

// Pour le relancer 
npm run dev

Génère du code par rapport a ce qu’on veux, ne vas pas tout installer tout le css 
taille par défaut du rem 1 taille de la taille de la police , le rem s’adapte a la taille de police par défaut du navigateur. unité relatives ( c’est a dire qu’elle a des références)

#createRouter
Librairie qui permet de simulé,
Yarn, npm, pnpm

Installer 
creer une app react  avec  la librairie vite 
ce mettre dans le fichier de notre app 
installer le packages
php run dev ( car il est marquer dans le packages.json dans le cle script “dev”= “vite” )


Soit autrement 

`npm install react-router-dom localforage match-sorter sort-by`
`react-router-dom` ce que nous voulons 
nous pouvons y verifié sur [npm](https://www.npmjs.com/) 
Si il y a des vulnérabilités  faite “npm audit fix —force”
Changez tout le css par rapport au lien **[found here](https://gist.githubusercontent.com/ryanflorence/ba20d473ef59e1965543fa013ae4163f/raw/499707f25a5690d490c7b3d54c65c65eb895930c/react-router-6.4-tutorial-css.css)**
les deuxs chevrons <> est la balises parents sans noms remplace les div (balise vide)
autre techniques react.fragements

#Firebase
**SGBDR:** système de gestion de base de données relationnelle
Suivre la documentation de Firebase [https://firebase.google.com/docs/firestore/quickstart?hl=fr](https://firebase.google.com/docs/firestore/quickstart?hl=fr)
**Firebase:** est un ensemble d’outils pour héberger et de gérer l’authentification d’une base de données.
**Back end at the service** (gestion des utilisateurs, bdd, infrastructure, securité, ….)
API fetch effectuer des call https 
asynchronisme lancer une opération et nous auront pas encore la réponse

//Afficher des donnée depuis une API
useEffect(
// Premier parametre : une fonction 
()=>{
getDitto },
//Pacer le code a executer ici 
fetch ('https:///pokeapi.co/api/v2pokemon/ditto').then(httpReponse)=>{
const getDitto = async ()=>{
const httpResponse = await fetch('https://pokeapi.co/api/v2/pokemon/ditto');
const ditto = await httpResponse.json();
//tester 
console.log ('dracaufeu', dracaufeu )
}

Ajout des éléments dans firebase 

// Add a second document with a generated ID.
import { database, collection } from "firebase/firestore"; 

// Ajouter dans USEEFFECT

AddDocuments

// en dessous en dehors du use Effect 
const AddDocument = async (/*les props des valeur voulu */)=>{
try {
  const docRef = await addDoc(collection(database, "eleves"/*mettre le bon noms de du documents*/*/), {
    Age:"16"
		Nom:"pksn"
  });

  console.log("Document written with ID: ", docRef.id);
} catch (e) {
  console.error("Error adding document: ", e);
}

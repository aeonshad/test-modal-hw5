# Composant React Modale

<a href='https://fr.react.dev/'><img alt="Static Badge" src="https://img.shields.io/badge/version-18.2.0-blue?style=flat&logo=React&label=React"></a>
<a href='https://www.npmjs.com/'><img alt="Static Badge" src="https://img.shields.io/badge/version-10.2.4-red?style=flat&logo=NPM&label=NPM"></a>
<a href='https://github.com/aeonshad/test-modal-hw5/blob/main/README.md'><img alt="Static Badge" src="https://img.shields.io/badge/version-English%7CAnglais-%2322802b?style=flat&logo=readme&logoColor=%23b3bd68&label=Readme"></a>

Un composant de fenêtre modale simple et personnalisable pour les applications React.

## Table des matières

-   [Installation](#installation)
-   [Utilisation](#utilisation)
-   [Propriétés](#propriétés)
-   [Exemple](#exemple)
-   [Styles](#styles)
-   [License](#license)

## Installation

Pour installer le composant Modal dans votre projet React, vous pouvez utiliser npm ou yarn :

```bash
npm install react-modal-hw
```

ou

```bash
yarn add react-modal-hw
```

## Utilisation

Pour utiliser le composant Modal dans votre application React, importez-le dans votre fichier et incorporez-le dans votre code JSX ou JS.

```jsx
import React, { useState } from 'react';
import Modal from 'react-modal-hw';

const App = () => {
    const [isOpen, setIsOpen] = useState(false);

    const toggleModal = () => {
        setIsOpen(!isOpen);
    };

    return (
        <div>
            <button onClick={toggleModal}>Open Modal</button>
            <Modal isOpen={isOpen} onClose={toggleModal}>
                <h2>Modal Title</h2>
                <p>This is the content of the modal.</p>
                <button onClick={toggleModal}>Close Modal</button>
            </Modal>
        </div>
    );
};

export default App;
```

## Propriétés

Le composant Modal accepte les propriétés suivantes :

-   `isOpen` (obligatoire) : Un booléen indiquant si la modale doit être affichée ou non.
-   `onClose` (obligatoire) : Une fonction de rappel appelée lorsque la modale doit être fermée.
-   `children` : Les éléments à afficher à l'intérieur de la modale.

## Exemple

Vous pouvez trouver un exemple d'utilisation du composant Modal dans le fichier `src/App.jsx`. Pour exécuter l'exemple, suivez ces étapes :

1. Cloner le référentiel.
2. Accédez au répertoire du projet dans le terminal.
3. Exécutez `npm install` ou `yarn install` pour installer les dépendances.
4. Exécutez `npm start` ou `yarn start` pour démarrer l'application.

## Styles

Le composant Modal ne fournit pas de styles par défaut pour la fenêtre modale elle-même. Vous êtes libre d'ajouter vos propres styles CSS pour personnaliser l'apparence de la modale selon vos besoins. Cependant, le composant peut inclure des styles par défaut pour l'overlay (l'arrière-plan sombre qui apparaît derrière la modal), la fenêtre ainsi que le bouton de fermeture. Si vous souhaitez personnaliser ces styles, vous pouvez utiliser les classes CSS suivantes :

-   `modal-overlay` : Classe pour l'overlay de la modale.
-   `modal-container` : Classe pour la fenêtre modale elle-même.
-   `modal-btn-close` : Classe pour le bouton de fermeture de la modale.
-   `modal-btn-close-icon` : Classe pour l'icône du bouton de fermeture de la modale.
-   `modal-btn-close-icon:hover` : Pseudo-classe lors d'un survol sur l'icône du bouton de fermeture de la modale.

## License

Ce projet est sous licence [MIT](LICENSE).

---

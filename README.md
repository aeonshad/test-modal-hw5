# React Modal Component

![React](https://img.shields.io/badge/build-18.2.0-blue?style=flat&logo=react&label=React&link=https%3A%2F%2Ffr.react.dev%2F)(https://fr.react.dev/)
![npm](https://img.shields.io/badge/build-10.2.4-red?style=flat&logo=NPM&label=NPM&link=https%3A%2F%2Fwww.npmjs.com%2F)(https://www.npmjs.com/)

A simple and customizable modal window component for React applications.

## Table of Contents

-   [Installation](#installation)
-   [Usage](#usage)
-   [Props](#props)
-   [Example](#example)
-   [Styles](#styles)
-   [License](#license)

## Installation

To install the modal component in your React project, you can use npm or yarn:

```bash
npm install react-modal-hw
```

or

```bash
yarn add react-modal-hw
```

## Usage

To use the Modal component in your React application, import it into your file and incorporate it into your JSX or JS code.

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

## Props

The Modal component accepts the following props:

-   `isOpen` (required): A boolean indicating whether the modal should be displayed or not.
-   `onClose` (required): A callback function called when the modal should be closed.
-   `children`: The elements to be displayed inside the modal.

## Example

You can find an example of using the Modal component in the `src/App.jsx` file. To run the example, follow these steps:

1. Clone the repository.
2. Navigate to the project directory in the terminal.
3. Run `npm install` or `yarn install` to install the dependencies.
4. Run `npm start` or `yarn start` to start the application.

## Styles

The Modal component does not provide default styles for the modal window itself. You are free to add your own CSS styles to customize the appearance of the modal as needed. However, the component may include default styles for the overlay (the dark background that appears behind the modal), the window, and the close button. If you wish to customize these styles, you can use the following CSS classes:

-   `modal-overlay`: Class for the modal overlay.
-   `modal-container`: Class for the modal window itself.
-   `modal-btn-close`: Class for the close button of the modal.
-   `modal-btn-close-icon`: Class for the close button icon of the modal.
-   `modal-btn-close-icon:hover`: Pseudo-class when hovering over the close button icon of the modal.

## License

This project is licensed under the [MIT](LICENSE).

---


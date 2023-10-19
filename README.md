# Redux Toolkit

#### Docs

[Redux Toolkit Docs](https://redux-toolkit.js.org/introduction/getting-started)

#### Installer le modèle

```sh
npx create-react-app my-app --template redux
```

- @latest

```sh
npx create-react-app@latest my-app --template redux
```

#### Application existante

```sh
npm install @reduxjs/toolkit react-redux
```

#### @reduxjs/toolkit

se compose de quelques bibliothèques

- redux (bibliothèque de base, gestion de l'état)
- immer (permet de muter l'état)
- redux-thunk (gère les actions asynchrones)
- reselect (simplifie les fonctions des réducteurs)

#### Extras

- redux devtools
- combiner les réducteurs

#### react-redux

connecte notre application à redux

#### Setup Store

- créer store.js

```js
import { configureStore } from "@reduxjs/toolkit";

export const store = configureStore({
  reducer: {},
});
```

#### Setup Provider

- index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import App from "./App";
// import store and provider
import { store } from "./store";
import { Provider } from "react-redux";

ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>,
  document.getElementById("root")
);
```

#### Setup Cart Slice

- fonctionnalité de l'application
- créer le dossier features/cart
- créer cartSlice.js


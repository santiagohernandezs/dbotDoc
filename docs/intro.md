---
sidebar_position: 1
slug: /
---

# Introducción

Veamos como funciona **dbot**, aquí encontraras toda la documentación

### Lo que necesitas

- [Node.js](https://nodejs.org/en/download/) versión 17 o superior:
  - Recomendamos que lo hagas a través de [nvm](https://github.com/nvm-sh/nvm) (Node Version Manager) para que el cambio entre versiones de node sea mucho más sencillo.
- Un editor de código como [Visual Studio Code](https://code.visualstudio.com/) (recomendado), [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), entre otros.
- Una cuenta de [Discord](https://discord.com/).
- Una cuenta de [GitHub](https://github.com/).
- Previos conocimientos de [JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript).

# Comenzando desde cero

## Inicio rápido

Si lo que quieres es algo rápido puedes clonar el [repositorio de github](https://github.com/santiagohernandezs/dbot) de dbot.

### Instalación

:::caution

Para instalar dbot, necesitas tener instalado [Node.js](https://nodejs.org/en/download/) versión 17 o superior.

:::

Ubicate en la carpeta donde tienes el bot y ejecuta el siguiente comando:

```bash
C:\Path\to\bot\folder> npm install
```

:::info

Este comando instalará todas las dependencias necesarias para que el bot funcione.

:::

## Inicio Manual

Si quieres hacerlo manualmente, sigue los siguientes pasos.

Primero, debes iniciar un paquete npm.

```bash
npm init -y
```

:::info

El comando anterior creará un archivo `package.json` en la carpeta donde se ejecutó el comando.

:::

Esta será la estructura de carpetas que debes tener:

```
dbbot
  ├── commands
  ├── events
  ├── src
  │    ├── main.js
  │    └── config.json
  ├── handlers
  ├── .gitignore
  └── package.json
```

### Instalación

debes instalar las siguientes dependencias:

```bash
npm install discord.js @discordjs/rest @discordjs/builders --save
```

También necesitas instalar el linterm, usaremos [ESLint](https://eslint.org/):

```bash
npm init @eslint/config
```

Y finalmente instalaremos nodemon para que el bot se reinicie automáticamente cuando se hagan cambios en el código:

```bash
npm install nodemon --save-dev
```

Tu archivo package.json debería lucir de la siguiente manera

```json
{
  "name": "dbot",
  "version": "1.0.0",
  "description": "bot de discord",
  "main": "index.js",
  "scripts": {
    "nodemon": "nodemon ."
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "eslint": "^8.28.0",
    "nodemon": "^2.0.20"
  },
  "dependencies": {
    "@discordjs/builders": "^1.3.0",
    "@discordjs/rest": "^1.3.0",
    "discord.js": "^14.6.0"
  }
}
```

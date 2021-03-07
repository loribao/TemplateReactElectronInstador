# Template  react + electron + instalador
##  Assista o vídeo no youtube
[![Alt text](https://img.youtube.com/vi/tUbJR1uuXsg/0.jpg)](https://youtu.be/tUbJR1uuXsg)

## Retratação dos comandos de terminal apresentados no video.
    -   npx create-react-app my-app
    -   cd my-app
    -   npm i -D nodemon electron electron-builder wait-on cross-env concurrently
    -   npm i electron-is-dev  
    -   

## No seu package.json não pode faltar as seguintes especificações:
### Consulte o package.json disponivel neste repositorio.
-       "name": "<nome da sua aplicação",
-       "version": "0.1.0",
-       "private": true,
-       "main": "public/electron.js",
-       "homepage": "./",
-       "build": {
-        "appId": "com.meutemplate"},
-       "scripts": {
-       "react-start": "react-scripts start",
-       "react-build": "react-scripts build",
-       "react-test": "react-scripts test",
-       "react-eject": "react-scripts eject",
-       "electron-build": "electron-builder",
-       "release": "yarn react-build && electron-builder --publish=always",
-       "build": "yarn react-build && yarn electron-build",
-       "start": "concurrently \"cross-env BROWSER=none yarn react-start\" \"wait-on http://localhost:3000 && electron .\"",
-       "start:nodemon": "nodemon --exec 'npm start'"}

# Start, Build e Release
### start:
-   npm start ou  yarn start
#### Para rodar durante o desenvolvimento

### Build
npm build ou yarn build
#### Binario na pasta "dist"

### Release
npm run release ou yarn release
#### Para publicar seu pacote em um repositorio. Atenção: é preciso ter um token do repositorio/plataforma para publicar.
#### Confira a documentação em https://www.electron.build/

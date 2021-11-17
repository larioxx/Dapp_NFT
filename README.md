# Dapp_NFT

Este repositorio proporciona una manera agradable y fácil de vincular un contrato inteligente NFT existente a una Dapp. Hay dos formas de usar este repositorio, puede ir por la ruta simple o por la más compleja.

La ruta simple es tan simple que todo lo que necesita hacer es descargar la carpeta de compilación en la página de lanzamiento y cambiar la configuración para que se ajuste a sus necesidades. (Siga el video para ver un recorrido).

La ruta más compleja le permite agregar funcionalidad adicional si se siente cómodo con la codificación en react.js. (Siga las instrucciones a continuación para llevar a cabo este recorrido).

## Instalación 🛠️

Si está clonando el proyecto, ejecútelo primero; de lo contrario, puede descargar el código fuente en la página de lanzamiento y omitir este paso.

```sh
git clone https://github.com/larioxx/Dapp_NFT.git
```

Asegúrese de tener instalado node.js para que pueda usar npm, luego ejecute:

```sh
npm install
```

## Uso ℹ️

Para hacer uso de esta dapp, todo lo que necesita hacer es cambiar las configuraciones para apuntar a su contrato inteligente, así como actualizar las imágenes y el archivo del tema.

En su mayor parte, todos los cambios estarán en la carpeta `public`.

Para vincular su contrato inteligente existente, vaya al archivo `public/config/config.json` y actualice los siguientes campos para que se ajusten a los detalles de su contrato inteligente, red y mercado. El campo de costo debe estar en wei.

Nota: esta dapp está diseñada para funcionar con el contrato inteligente NFT previsto, que solo toma un parámetro en la función de acuñado "mintAmount". Pero puede cambiar eso en el archivo "App.js" si necesita usar un contrato inteligente que requiere 2 parámetros.

```json
{
  "CONTRACT_ADDRESS": "0x424b6fF8c704F867e2f5cB11ABb8379276Bf6C0C",
  "SCAN_LINK": "https://polygonscan.com/token/0x424b6ff8c704f867e2f5cb11abb8379276bf6c0c",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "Matic",
    "ID": 137
  },
  "NFT_NAME": "LightniX",
  "SYMBOL": "LX",
  "MAX_SUPPLY": 10000,
  "WEI_COST": 250000000000000000,
  "DISPLAY_COST": 0.25,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/lightnix",
  "SHOW_BACKGROUND": true
}
```

Asegúrese de copiar el ABI del contrato de remix y pegarlo en el archivo `public/config/abi.json`.
(sigue el video de si tienes problemas con esta parte).

Ahora necesitaras crear y cambiar 2 imágenes y un gif en la carpeta `public/config/images`,`bg.png`, `example.gif` y `logo.png`.

A continuación, cambie los colores del tema a su gusto en el archivo `public/config/theme.css`.

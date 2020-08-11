# Start

*  🔖 **Compiler**
*  🔖 **Start**
*  🔖 **Project**

___

## 📑 Compiler

### 🏷️ **[Cordova](https://cordova.apache.org/)**

Apache Cordova ou plus anciennement Apache Callback ou PhoneGap, est un framework open-source développé par la Fondation Apache. Il permet de créer des applications pour différentes plateformes en HTML, CSS et JavaScript.

![image](https://raw.githubusercontent.com/seeren-training/Cordova/master/wiki/resources/cordova.png)

___

## 📑 [Start](https://www.npmjs.com/package/cordova)

Installer la package de façon globale ou non.

```bash
npm i cordova
```

Exécuter le CLI pour voir les commandes disponibles.

```bash
npx cordova
```

### 🏷️ **[Create](https://cordova.apache.org/docs/en/9.x/guide/cli/index.html)**

La commande create initialise un projet.

```bash
npx cordova create foo io.foo.app FooApp
```

Changer le répertoire.

```bash
cd foo
```

___

## 📑 Project

Un projet a été généré, décrivons le.

### 🏷️ **[config.xml](https://cordova.apache.org/docs/fr/latest/config_ref/)**

C'est dans ce fichier que les liens vers les icônes et plashscreen se font (@see cordova res), que les préférences sont paramétrés tout comme les autorisations et les différents plugins. Le détail de chaque plateform est référencé dans ce fichier.

### 🏷️ **www**

Seul les éléments présents dans ce dossier seront déployés sur device, les ressources de développement doivent se trouver à l’extérieur. En cas d'utilisation de webpack vous devez faire correspondre les points d'entré et de sortie.

### 🏷️ **index.html**

Situé dans le dossier `www` il est le point d'entré d'affichage du programme dans la Web View. Vous remarquez un lien JavaScript vers un fichier cordova.js qui n'est pas présent: cela est normal et il est requis pour les fonctionnalités qui concernent le device.

___

👨🏻‍💻 Manipulation

Créer un projet et adaptez votre stack technique ou installez cordova dans un projet existant que vous configurez en rapport à ces contraintes.

___
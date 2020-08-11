# Build

*  🔖 **WebBrowser**
*  🔖 **Device**

Cordova peut builder sur plusieurs [platforms](https://cordova.apache.org/docs/fr/latest/guide/cli/#ajouter-des-plates-formes), pour obtenir la liste:

```bash
npx cordova platform
```

___

## 📑 WebBrowser

Pour effectuer un build dans un navigateur web, installons la platform:

```bash
npx cordova platform add browser
```

Pour lancer un build sur la platform:

```bash
npx cordova run browser
```

Alors quelle différence avec une éxécution sans la platform browser? La diférence est la prise en charge de cordova et ses plugins. Le document est également enrichi, il possède le type d'évènement [deviceready](https://cordova.apache.org/docs/fr/latest/cordova/events/events.deviceready.html) qui signal que le device émulé est prêt à utiliser cordova

```js
document.addEventListener('deviceready', onDeviceReady, false);
```

Vous pouvez constater que l'objet est disponible.

```js
console.log(cordova);
```

___

👨🏻‍💻 Manipulation

Lancer votre application sur web browser.

___

## 📑 Device

Pour effectuer un build dans un navigateur web, installons la platform:

```bash
npx cordova platform add android
```

Pour lancer un build sur la platform:

```bash
npx cordova run android --device
```

Et la tout ne se passe pas comme prévu: il y a des prérequis au run sur device.


### 🏷️ **[Pré-requis](https://ionicframework.com/docs/developing/android)**

Il faut plusieurs choses:

* Java 8
* Graddle
* SDK Build Tools
* Accept licenses
* Activer le mode développeur

#### Android Studio

Avec Java en prérequis de base, le plus simple pour installer le graddle et les SDK build tools d'installation [Android Studio](https://developer.android.com/studio/).

Une fois installé, créez un projet vide et effectuez les updates.

#### Licenses

Vous devez accepter les licenses des SDK Build Tools, pour se faire avec un terminal exécuter le sdkmanager.

```bash
ANDROID_HOME/tools/bin/sdkmanager --licenses
```

Et répondez oui aux différentes questions.

#### Graddle

Si le graddle n'est pas trouvé lors du build, ajouter le en variables d'environnemet.

#### Mode Développeur

En fonction de votre téléphone, activez le mode développeur et autorisez le debugage USB.

___

👨🏻‍💻 Manipulation

Lancer votre application sur votre device.

___


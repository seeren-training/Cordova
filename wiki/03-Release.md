# Relase

*  🔖 **Build**
*  🔖 **Keystore**
*  🔖 **Sign**
*  🔖 **Optimise**

___

## 📑 Build

Construisez l'application:

```bash
npx cordova build --release android
```

Le fichier APK non signé a été généré à: .`/platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk`
___

## 📑 Keystore

Générer un keystore avec `keytool`.

```bash
keytool -genkey -v -keystore [KEYSTORE_NAME].keystore -alias [KEYSTORE_ALIAS] -keyalg RSA -keysize 2048 -validity 10000

keystore password? : xxxxxxx
What is your first and last name? :  xxxxxx
What is the name of your organizational unit? :  xxxxxxxx
What is the name of your organization? :  xxxxxxxxx
What is the name of your City or Locality? :  xxxxxxx
What is the name of your State or Province? :  xxxxx
What is the two-letter country code for this unit? :  xxx
```

Le keystore a été généré à: `./[KEYSTORE_NAME].keystore`, déplacez-le à côté de l'APK non signé.

___

## 📑 Sign

Déplacer vers le répertoire APK non signé.

```bash
cd ./platforms/android/app/build/outputs/apk/release
```

Signez l'APK avec jarsigner.

```bash
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore [KEYSTORE_NAME].keystore app-release-unsigned.apk [KEYSTORE_ALIAS]
```

___

## 📑 Optimise

Alignez l'APK avec zipalign.

```bash
[ANDROID_HOME]/Sdk/build-tools/[VERSION]/zipalign.exe -v 4 app-release-unsigned.apk app-release.apk
```

___

👨🏻‍💻 Manipulation

Créez une release puis créez un compte sur Google Play et téléchargez l'APK
___

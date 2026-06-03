# Androidアプリ化手順

## 前提

- Android Studio をインストール済み
- Android SDK Platform 36 をインストール済み
- `ANDROID_HOME` が Android SDK の場所を指している
- プロジェクト場所は、このリポジトリを配置した任意のフォルダ

## 1. ブラウザ版を確認

```powershell
npm run serve
```

Chrome で開く:

```text
http://localhost:3000/index.html
```

## 2. Android用にWebファイルを同期

```powershell
npm run android:sync
```

このコマンドで `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png` を `www` にコピーし、CapacitorでAndroid側へ同期します。

## 3. Debug APKを作成

```powershell
cd android
.\gradlew.bat assembleDebug
cd ..
```

APKの出力先:

```text
android\app\build\outputs\apk\debug\app-debug.apk
```

整理済みコピー先:

```text
artifacts\apk\app-debug.apk
```

## 4. 実機へインストール

接続端末を確認:

```powershell
adb devices
```

端末が1台だけの場合:

```powershell
adb install -r android\app\build\outputs\apk\debug\app-debug.apk
adb shell monkey -p com.dailyhub.diary -c android.intent.category.LAUNCHER 1
```

端末が複数ある場合は実機IDを指定:

```powershell
adb -s 38d0dfdf install -r android\app\build\outputs\apk\debug\app-debug.apk
adb -s 38d0dfdf shell monkey -p com.dailyhub.diary -c android.intent.category.LAUNCHER 1
```

## 5. Android Studioで作業する場合

Android Studio で開くフォルダ:

```text
<project-root>\android
```

APK作成:

```text
Build > Build Bundle(s) / APK(s) > Build APK(s)
```

## よく使うコマンド

Web変更後にAPKまで作る:

```powershell
npm run android:build
```

Android Studioを開く:

```powershell
npx cap open android
```

## 注意点

- `index.html` を変更したら、必ず `npm run android:sync` を実行してからAPKを作る
- Android Studioで直接 `www` や `android/app/src/main/assets/public` を編集しない
- 基本の編集対象はプロジェクト直下の `index.html`, `manifest.json`, `sw.js`

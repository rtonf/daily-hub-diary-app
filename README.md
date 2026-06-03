# デイリー・ハブ

日記、毎日の目標、予定、リマインダーを一画面中心で管理するPWA/Androidアプリです。

## 主な機能

- 日記メモ
- 毎日の予定管理
- 継続チェック
- 週間レポート
- ブラウザ通知リマインダー
- PWA対応
- CapacitorによるAndroid APK化

## 開発環境

- Node.js
- npm
- Android Studio
- Android SDK
- Capacitor

## ブラウザで起動

```powershell
npm install
npm run serve
```

ブラウザで開く:

```text
http://localhost:3000/index.html
```

## Android用に同期

```powershell
npm run android:sync
```

## Debug APKを作成

```powershell
npm run android:build
```

APKは以下に出力されます。

```text
android\app\build\outputs\apk\debug\app-debug.apk
```

詳しい手順は [BUILD_ANDROID.md](BUILD_ANDROID.md) を参照してください。

## 公開範囲

このリポジトリには、アプリのソースコード、PWA設定、Androidプロジェクト設定、ビルド手順を含めます。

以下は公開対象外です。

- `node_modules`
- APKやAABなどのビルド成果物
- 検証スクリーンショット
- ブラウザ検証プロファイル
- Android Studioの個人設定
- `android/local.properties`

## ライセンス

MIT License

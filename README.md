# デイリー・ハブ

日記、今日の予定、継続チェック、リマインダーを1画面にまとめて管理するPWA/Androidアプリです。

## 主な機能

- 今日の予定一覧と予定追加
- 日記の保存、削除、過去検索
- 1〜3個の継続チェック
- 週間レポート
- 月間カレンダー
- ブラウザ通知リマインダー
- PWA対応
- CapacitorによるAndroid APKビルド

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

ブラウザで開きます。

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

公開対象外の例:

- `node_modules`
- APK/AABなどのビルド成果物
- 検証スクリーンショット
- ブラウザ検証プロファイル
- Android Studioの個人設定
- `android/local.properties`

## ライセンス

MIT License

**[日本語](#時計-clock-app) | [English](#clock-app)**

# 時計 (Clock App)

Windows 11 標準の「時計」アプリを模した、シンプルなブラウザ動作の時計アプリケーションです。単一の HTML ファイルのみで構成されており、ビルドや依存パッケージのインストールなしにそのまま動作します。

## デモ

`index.html` をブラウザで開くだけで利用できます。

## 主な機能

### タイマー
- 複数のタイマーをカード形式で管理（初期状態で 1分・3分・5分・10分のプリセットを用意）
- 名前付きタイマーの追加・編集・削除
- 円形プログレスリング表示で残り時間を可視化
- 編集モードでのタイマー削除
- タイマー終了時にアラーム音とトースト通知を表示
- 設定したタイマーは `localStorage` に保存され、再読み込み後も保持

### ストップウォッチ
- 開始・停止・リセット操作
- ラップ計測機能（最速・最遅ラップをハイライト表示）
- 1/100 秒単位での計測表示

### 設定
- アプリテーマの切り替え（システム設定に合わせる／ライト／ダーク）
- タイマーとアプリ設定を初期状態に戻すリセット機能

### UI/UX
- サイドナビゲーション（PC幅）とボトムナビゲーション（モバイル幅）によるレスポンシブ対応
- ダーク／ライトテーマ切り替え（システムのカラースキームにも自動追従）
- Windows 風のフォント・配色・操作感を再現

## 技術構成

- **HTML / CSS / JavaScript** のみで構築（フレームワーク不使用）
- 外部リソース:
  - [Font Awesome](https://fontawesome.com/)（アイコン表示）
  - [Google Fonts - BIZ UDPGothic](https://fonts.google.com/)（フォント）
- データ永続化には `localStorage` を使用（サーバー・バックエンドは不要）
- タイマー終了音は `alarm.wav`（同リポジトリ内に配置）を再生

## 使い方

1. このリポジトリをクローン、またはダウンロードする
   ```bash
   git clone <このリポジトリのURL>
   ```
2. `index.html` をブラウザで開く

サーバーを立てる必要はありません。ローカルファイルとして直接開くだけで動作します。

## ファイル構成

```
.
├── index.html   # アプリ本体（HTML / CSS / JS をすべて含む単一ファイル）
├── alarm.wav    # タイマー終了時に再生されるアラーム音
└── README.md
```

## ライセンス

本リポジトリの内容は、個人的な学習・利用目的に限り閲覧・利用できます。**複製、再配布、公開（フォークしての公開や別リポジトリへの転載を含む）は禁止します。** 利用を希望される場合は、事前に作者にご連絡ください。

---

# Clock App

A simple, browser-based clock application inspired by the native Windows 11 "Clock" app. Built as a single HTML file with no build step or dependencies required.

## Demo

Just open `index.html` in your browser to use it.

## Features

### Timer
- Manage multiple timers as cards (ships with 1, 3, 5, and 10 minute presets by default)
- Add, edit, and delete named timers
- Circular progress ring showing remaining time
- Delete timers via edit mode
- Alarm sound and toast notification when a timer finishes
- Timers are saved to `localStorage` and persist across page reloads

### Stopwatch
- Start, stop, and reset controls
- Lap tracking (fastest and slowest laps are highlighted)
- Displays time down to hundredths of a second

### Settings
- Switch app theme (Use system setting / Light / Dark)
- Reset button to restore timers and app settings to their defaults

### UI/UX
- Responsive layout with a side nav (desktop) and bottom nav (mobile)
- Light/dark theme toggle, with automatic system color scheme detection
- Windows-style fonts, colors, and interactions

## Tech Stack

- Built with plain **HTML / CSS / JavaScript** only (no frameworks)
- External resources:
  - [Font Awesome](https://fontawesome.com/) for icons
  - [Google Fonts - BIZ UDPGothic](https://fonts.google.com/) for typography
- Uses `localStorage` for data persistence (no backend/server required)
- Plays `alarm.wav` (included in this repo) when a timer finishes

## Usage

1. Clone or download this repository
   ```bash
   git clone <this-repo-url>
   ```
2. Open `index.html` in your browser

No server setup is needed — it works by opening the file directly.

## File Structure

```
.
├── index.html   # The app itself (HTML / CSS / JS all in one file)
├── alarm.wav    # Alarm sound played when a timer finishes
└── README.md
```

## License

The contents of this repository may be viewed and used for personal, non-commercial purposes only. **Copying, redistribution, and republishing (including public forks or reposting to other repositories) are not permitted.** Please contact the author before any other use.

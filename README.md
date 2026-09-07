# ITSUKI

**Interactive Terminal Service for Unified Karaoke Integration**

ITSUKIは、PCに保存したカラオケ動画をスマホやPCのブラウザから検索・予約し、VLCで順番に再生するローカルカラオケ統合ツールです。

## できること

- 曲名・歌手・タイアップ・年代・外国語曲などから選曲
- スマホから予約、予約順変更、リモコン操作
- DB未紐づけ動画もデジ像風の「フォルダから選曲」で直接予約
- VLCによる動画再生と予約一覧表示
- 参加者別の履歴・ランキング
- 会場/動画ルート別の標準音量
- ファイル名からON/OFFボーカル判定
- KVDBの人物別名義・所属グループ/メンバー検索
- Googleスプレッドシートへの予約リスト同期（任意）
- 設定・履歴・ランキング・紐づけ情報の選択バックアップ/復元
- 管理画面から最新版確認・ダウンロード

## 導入

1. GitHub Releasesから最新の `ITSUKI_vX.X.X.zip` をダウンロードします。
2. ZIPを展開します。公開ZIPの中身は `ITSUKI.exe` と `README.txt` だけです。
3. [VLC media player](https://www.videolan.org/vlc/) をインストールします。
4. `ITSUKI.exe` を起動します。
5. リモコンから管理者認証し、管理画面で楽曲DBと動画ルートを設定します。初期PINは `0000` です。
6. 「動画を再スキャン」を実行します。

設定や履歴はEXEとは別のPCデータ領域へ保存されるため、通常の更新では新しいEXEへ差し替えても引き継がれます。

## 基本的な使い方

1. ITSUKIを起動
2. 参加者のスマホをITSUKIへ接続できるLAN/Wi-Fiへ接続
3. TOP画面から曲を検索、または「フォルダから選曲」
4. 選曲者を指定して予約
5. 予約順にVLCで再生

管理者はブラウザの管理画面から、動画スキャン、紐づけ確認、音量設定、バックアップ、更新確認、ITSUKI本体の終了などを操作できます。

## 詳しい使い方

管理者向けの詳細手順は、リポジトリにある **`help.html`** をブラウザで開いてください。

`help.html` は単体で開ける管理者向けマニュアルです。設定項目、動画スキャン、DB、フォルダ選曲、リモコン、バックアップ、更新、トラブル対応まで詳しく説明しています。

## 開発版から公開版を作る

開発環境では `build_public.bat` をダブルクリックするとPyInstallerで公開版を生成します。ビルド時には同梱の `ITSUKI.ico` がEXE/ショートカット用アイコンとして適用されます。失敗した場合はウインドウを閉じず、`build_public.log` に原因を残します。

生成物：

```text
release/
├─ github/
│  ├─ README.md
│  ├─ help.html
│  └─ THIRD_PARTY_NOTICES.md
└─ github_release/
   ├─ ITSUKI_vX.X.X/
   │  ├─ ITSUKI.exe
   │  └─ README.txt
   └─ ITSUKI_vX.X.X.zip
```

`github/` はGitHubリポジトリへ掲載する資料、`github_release/` はGitHub Releasesへ登録する配布物です。公開ZIPのルートには `ITSUKI.exe` と `README.txt` の2ファイルだけが入ります。

## 名称

- 正式名称: **Interactive Terminal Service for Unified Karaoke Integration**
- 通称: **ITSUKI**

## 注意

ITSUKIは動画ファイルそのものや楽曲DBを配布しません。利用する動画・音源・データの権利や利用条件は各自で確認してください。

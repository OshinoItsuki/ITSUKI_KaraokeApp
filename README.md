# ITSUKI

**Interactive Terminal Service for Unified Karaoke Integration**

ITSUKIは、PCに保存したカラオケ動画をスマホやPCのブラウザから検索・予約し、VLCで順番に再生するローカルカラオケ統合ツールです。

## できること

- 曲名・歌手名・タイアップ・年代・外国語曲などから選曲
- スマホやPCから予約、予約順変更、リモコン操作
- 「＋♪ とりあえず300」に気になる曲を一旦保存
- DBが無い動画も「フォルダから選曲」から直接予約
- VLCによる動画再生と予約一覧表示
- 履歴・ランキング
- ON/OFFボーカル判定
- 設定・履歴・紐づけ情報などの選択バックアップ / 復元
- Googleスプレッドシートへの予約リスト同期（任意）

## 必要なもの

- Windows PC
- [VLC media player](https://www.videolan.org/vlc/)
- [Google Chrome](https://www.google.com/chrome/)
- 自分で用意したカラオケ動画
- 楽曲DBは任意

## はじめかた

1. [Releases](https://github.com/OshinoItsuki/ITSUKI_KaraokeApp/releases) から最新版ZIPをダウンロードして展開します。
2. VLCとChromeが無ければインストールします。
3. `ITSUKI.exe` を起動します。
4. リモコン画面から管理者PIN `0000` で管理画面を開きます。
5. 動画ルートを設定して「動画を再スキャン」を実行します。
6. スマホを同じLAN / Wi-Fiへ接続してTOP画面から選曲します。

## 楽曲DBがなくても使えます

楽曲DBは必須ではありません。DBが無い場合でも、スキャン済みの動画をフォルダ階層から探して予約できます。詳しくは [フォルダから選曲](https://oshinoitsuki.github.io/ITSUKI_KaraokeApp/#folder-selection) を確認してください。

楽曲DBを自分で作りたい場合は、[KaraokeSong DB Editorはこちらからダウンロードできます](https://github.com/OshinoItsuki/KaraokeSong_DB_Editor)。

## 詳しい使い方

管理者向けの詳しい設定・操作手順は **[Web版HELP](https://oshinoitsuki.github.io/ITSUKI_KaraokeApp/)** で確認できます。Release版には同じ内容の `help.html` も同梱しているため、ITSUKIを使うPCではインターネット接続なしでも確認できます。

## バグ報告・機能追加要望

[GitHub Issues](https://github.com/OshinoItsuki/ITSUKI_KaraokeApp/issues) からお願いします。

## 注意

ITSUKIは動画・音源・楽曲DBそのものを配布しません。利用する動画・音源・データの権利や利用条件は各自で確認してください。

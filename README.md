# ITSUKI

**Interactive Terminal Service for Unified Karaoke Integration**

ITSUKIは、PCに保存したカラオケ動画をスマホやPCのブラウザから検索・予約し、VLCで順番に再生するローカルカラオケ統合ツールです。

## できること

- 曲名・歌手名・タイアップ・年代・外国語曲などから選曲
- 新曲・更新曲を週（W番号）単位で確認
- 歌手検索の完全一致 / 部分一致 / 前方一致、別名義・グループ候補の表示切替
- スマホやPCから予約、予約順変更、リモコン操作
- 選曲者に加えて「一緒に歌う人」を参加者から登録
- 「＋♪ とりあえず300」に気になる曲を一旦保存
- DBが無い動画も「フォルダから選曲」から直接予約
- VLCによる動画再生、曲終了時のNEXT表示・目安Kcal演出
- 履歴・ランキング
- ON/OFFボーカル判定
- DB・紐づけ間違い通報と管理者確認 / CSV出力
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


## v1.0.3

- HELPの楽曲DB説明に、外国語曲 / パート分け / アニメ・ゲーム映像 / MV・PV / LIVE の分類条件を追加

## v1.0.2

- 管理者HELPの便利機能にTailscaleで外部ネットワークからアクセスする手順を追加
- Tailscale公式ダウンロードページへのリンクを追加
- ITSUKIのリモコンにあるLAN / Tailscale QR切替の使い方を追記

## v1.0.0

- ITSUKI 初回公開版
- 曲終了 / 演奏停止時のNEXT表示と目安Kcal演出を正式搭載
- Kcalは `00.0` 形式の3桁7セグ表示、最大99.9 Kcalに調整
- 新曲・更新曲の週別表示、歌手検索フィルター、一緒に歌う人、間違い通報、とりあえず300などを搭載
- ローカル同梱HELPとGitHub Pages向けHELPを同一原本から生成
- 更新確認は公式GitHub Releaseを参照し、初回Release公開前の404を正常な「Release未公開」状態として扱う
- 管理画面の待機BGM標準音量変更を待機再生へ即時反映

## v0.6.4

- 選曲予約画面のフルパスは、必要な時だけ `\` / `/` を折り返し候補にして横幅に合わせて改行
- TOPの「新曲・更新曲」表記を復元
- 新曲・更新曲の週ナビを4週固定から、管理画面の表示日数に含まれる全WEEKの可変表示へ変更
- WEEKが横幅に収まらない場合は横スクロールし、選択中の週を中央寄せ＋両端フェードで前後週を視認可能に変更
- 曲終了時のNEXT帯を参考デザイン寄りの斜めピンクタブ＋明色レールへ調整
- Kcalメーターを多重リング化し、数値を独自7セグ描画に変更

## v0.6.3

- 曲終了時のNEXT表示を見やすく調整（NEXT文字・帯を大型化）
- Kcal表示を参考デザイン寄りに調整し、数値を円内で大きく表示
- 新曲・更新曲を1週間ずつ表示するページ式へ変更
- 新曲ページ上部に `◁ [Wxx] Wxx ... ▷` の週移動ナビを追加

## v0.6.2

- 曲終了時のNEXTオーバーレイを、予約通知と同じ64bit対応Win32描画基盤へ統一
- 全画面の透明レイヤー方式をやめ、NEXT帯とKcal表示部分だけをTOPMOST表示する方式へ変更
- NEXTウインドウ生成時の64bitハンドル破損を修正


## v0.6.1

- 曲終了時のNEXT表示と次曲遷移を安定化
- 「演奏停止」でも現在フレームを止めてNEXT/Kcalを表示
- 新曲・更新曲一覧を起動時・再スキャン時に事前生成して高速化
- 「一緒に歌う人」を折りたたみ式に変更
- 選曲画面の動画フルパス表示を見やすく調整
- `stop.bat` のlocalhost終了処理を修正

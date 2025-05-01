# LiNEA40
LiNEA40は1Uトラックボール搭載の薄型軽量キーボードキットです。
![LiNEA40 Assembly](https://github.com/keyfreaks/LiNEA40/blob/main/image/linea40.jpg)

## ビルドガイド（ハードウェア編）
[ビルドガイドはこちら](https://note.com/i_love_diy/n/n2b31ef46d301)  
⚠️ **重要注意点**：
- PMW3610トラックボールセンサーは**270℃以下**で素早くはんだ付け
- バッテリー接続の極性厳守（逆極性のまま電源を入れるとマイコンが壊れる）
- ケース組み立て時にリセットスイッチが折れやすい（ビルドガイドの記述になるべく忠実に作業）

## ファームウェア設定ガイド

### 1. 設定リポジトリの取得
1. [zmk-config-LiNEA40リポジトリ](https://github.com/keyfreaks/zmk-config-LiNEA40)にアクセス
2. 右上の `Fork` ボタンをクリック
3. 自分のアカウントを選択してフォーク作成

### 2. キーマップ編集
1. [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)にアクセス
2. GitHubログイン後、フォークしたリポジトリを選択
3. ビジュアルエディタでレイアウトを変更
4. `Save to GitHub` で変更を反映

### 3. ファームウェアビルド
1. 自分のリポジトリで `Actions` タブを開く
2. .github/workflows/build.yml を選択し、ワークフローを実行(run workflowボタンをクリック)
3. 完了後、`Artifacts` のfirmwareをクリックしてzipファイルをダウンロード
4. ダウンロードしたfirmware.zipを解凍してUF2ファイルを取得

### 4. 書き込み手順
1. USBケーブルを接続
2. リセットスイッチを素早く2回押す
3. 出現したドライブにUF2ファイルをコピー

## サポート
[公式Discord]あり（別途ご案内）

## ライセンス
FWについてはMITライセンスで提供

# Explore Me

Windows 11 のエクスプローラーと同じ見た目・操作で使える、タブと 2 画面のファイラーです。

- 2 画面（左右のペイン）とタブ。片方からもう片方へ Shift+F5 でコピー、Shift+F6 で移動
- エクスプローラーと同じキー操作・右クリックメニュー（「その他のオプションを確認」で Windows 本来のメニューも）
- クイックルック（Space で大きなプレビュー）、コマンドパレット（Ctrl+K）
- ワークスペース（開いているタブ一式を保存して呼び出す）、カラーラベル、仮置き（Ctrl+S で集めてまとめて移動）
- 容量の内訳、フラット表示、サブフォルダーの検索（Everything・Windows のインデックスがあれば使う）
- zip の作成・展開、7z・rar・tar.gz などの展開
- 日本語 / 英語、ライト / ダーク

## 使い方

エクスプローラーと同じように使えます。操作の一覧はアプリの中で **F1**、設定は **Ctrl+,**（または右上の歯車）です。

### 画面

- 左のナビゲーション: ホーム・ピン留めしたフォルダー・PC（ドライブ）・ワークスペース・仮置き
- 右側: 左右 2 つのペイン。それぞれにタブがあり、クリックした側が操作の対象になります（Ctrl+Shift+D で 1 画面にも）
- 起動するとホーム（よく使う場所・ドライブ・最近使った項目）が開きます

### よく使う操作

| 操作 | キー |
| --- | --- |
| 戻る / 上のフォルダーへ | Backspace / Alt+↑ |
| アドレスバーに入力 | Ctrl+L（Alt+D・F4） |
| このフォルダーを絞り込み / サブフォルダーも検索 | Ctrl+E / Ctrl+Shift+F |
| 新しいタブ / タブを閉じる | Ctrl+T / Ctrl+W |
| 1 画面 / 2 画面の切り替え | Ctrl+Shift+D |
| 反対側のペインへコピー / 移動 | Shift+F5 / Shift+F6 |
| 大きなプレビュー（クイックルック） | Space |
| コマンドパレット（操作やフォルダーを名前で探す） | Ctrl+K |
| 仮置きに入れる（あとでまとめて移動・コピー） | Ctrl+S |
| 元に戻す / やり直す | Ctrl+Z / Ctrl+Y |
| 表示の切り替え（大アイコン / 中アイコン / 一覧 / 詳細） | Ctrl+Shift+2 / 3 / 5 / 6 |
| 隠しファイルの表示 | Ctrl+H |

- 右クリックは Windows 11 風のメニューです。7-Zip などが加えた項目も含む Windows 本来のメニューは、Shift+右クリックか「その他のオプションを確認」から
- 書庫（zip・7z・rar・tar.gz など）は右クリックの「ここに展開」で展開できます
- 「フォルダーを Explore Me で開く」を設定でオンにすると、デスクトップやほかのアプリから開いたフォルダーも Explore Me で開きます

## ダウンロード

[Releases](../../releases/latest) から `ExploreMe-Setup-<版>.exe` をダウンロードして実行します。

### 動作環境

| 項目 | 内容 |
| --- | --- |
| OS | Windows 11（64 ビット、x64） |
| Windows 10 | 未確認（動く見込みはありますが、確認していません） |
| ARM 版 Windows | 未確認 |
| インストール | ユーザーごと（管理者権限は不要）。インストール先は選べます |

### 「Windows によって PC が保護されました」と出たら

このアプリはコード署名をしていないため、初めて実行するときに Windows の SmartScreen がこの画面を出すことがあります。
**「詳細情報」→「実行」** で進めてください。

心配な場合は、ダウンロードしたファイルが本物か確かめられます。各リリースのページに SHA-256 の値を載せています。PowerShell で次を実行し、同じ値か比べてください。

```powershell
Get-FileHash .\ExploreMe-Setup-0.1.0.exe -Algorithm SHA256
```

## 更新

起動したときに新しい版を確認し、裏でダウンロードして、アプリを終了したときに更新します（設定 → バージョン情報で切り替えられます）。
通信するのは、この更新の確認（GitHub）だけです。使い方などの情報は送りません。

## アンインストール

Windows の「設定 → アプリ → インストールされているアプリ」から Explore Me をアンインストールします。
「フォルダーを Explore Me で開く」をオンにしていた場合も、元のエクスプローラーに戻ります。

## ライセンス

無料で使えます（個人・法人とも）。再配布・改変はできません。詳しくは [LICENSE](LICENSE) を見てください。
同梱しているソフトウェア（Electron、7-Zip など）はそれぞれのライセンスに従います（インストール先の `THIRD_PARTY_NOTICES.txt`）。

## 著作権

Copyright (c) 2026 ternando0831-lang

## フィードバック

不具合の報告や要望は、アプリの「設定 → フィードバック」からメールで送れます。

## 既知の制限

- 7z・rar などは展開だけです（作成は zip のみ）。パスワード付きの書庫は展開できません
- 古い日本語の書庫（Shift_JIS の名前の lzh・tar など）は、名前が正しく展開されないことがあります
- 最大化している間は、ウィンドウの枠に Mica（半透明の背景）がかかりません

---

## English

Explore Me is a tabbed, dual-pane file manager for Windows that looks and works like the Windows 11 File Explorer.

**Basics**: two panes with tabs (Ctrl+Shift+D for a single pane), Explorer's keys and right-click menu (Shift+right-click for the full Windows menu), Space for Quick Look, Ctrl+K for the command palette, Shift+F5 / Shift+F6 to copy / move to the other pane, Ctrl+S to collect items and move them later. F1 lists every shortcut; Ctrl+, opens Settings. The UI is available in English (Settings → General → Language).

**Download** `ExploreMe-Setup-<version>.exe` from [Releases](../../releases/latest). Requires Windows 11 (64-bit, x64); Windows 10 and Windows on ARM have not been tested. Installs per user (no administrator rights needed).

**"Windows protected your PC"**: the installer is not code-signed, so SmartScreen may show this on first run. Choose **More info → Run anyway**. Each release page lists the SHA-256 of the installer (`Get-FileHash <file> -Algorithm SHA256`).

**Updates**: the app checks for a new version at start-up, downloads it in the background and installs it when you quit (can be turned off in Settings → About). The update check (GitHub) is the only network access; no usage data is sent.

**License**: free for personal and business use; redistribution and modification are not permitted. See [LICENSE](LICENSE). Bundled third-party software (Electron, 7-Zip and others) is covered by its own licenses (`THIRD_PARTY_NOTICES.txt` in the installation folder).

**Feedback**: Settings → Feedback in the app opens an email.

Copyright (c) 2026 ternando0831-lang

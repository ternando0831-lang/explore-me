# Explore Me

Windows 11 のエクスプローラーと同じ見た目・操作で使える、タブと 2 画面のファイラーです。

- 2 画面（左右のペイン）とタブ。片方からもう片方へ Shift+F5 でコピー、Shift+F6 で移動
- エクスプローラーと同じキー操作・右クリックメニュー（「その他のオプションを確認」で Windows 本来のメニューも）
- クイックルック（Space で大きなプレビュー）、コマンドパレット（Ctrl+K）
- ワークスペース（開いているタブ一式を保存して呼び出す）、カラーラベル、仮置き（Ctrl+S で集めてまとめて移動）
- 容量の内訳、フラット表示、サブフォルダーの検索（Everything・Windows のインデックスがあれば使う）
- zip の作成・展開、7z・rar・tar.gz などの展開
- 日本語 / 英語、ライト / ダーク

## ダウンロード

[Releases](../../releases/latest) から `ExploreMe-Setup-<版>.exe` をダウンロードして実行します。

動作環境: Windows 11（64 ビット）。Windows 10 では確認していません。

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

## フィードバック

不具合の報告や要望は、アプリの「設定 → フィードバック」からメールで送れます。

## 既知の制限

- 7z・rar などは展開だけです（作成は zip のみ）。パスワード付きの書庫は展開できません
- 古い日本語の書庫（Shift_JIS の名前の lzh・tar など）は、名前が正しく展開されないことがあります
- 最大化している間は、ウィンドウの枠に Mica（半透明の背景）がかかりません

---

## English

Explore Me is a tabbed, dual-pane file manager for Windows that looks and works like the Windows 11 File Explorer.

**Download** `ExploreMe-Setup-<version>.exe` from [Releases](../../releases/latest). Requires Windows 11 (64-bit); Windows 10 has not been tested.

**"Windows protected your PC"**: the installer is not code-signed, so SmartScreen may show this on first run. Choose **More info → Run anyway**. Each release page lists the SHA-256 of the installer (`Get-FileHash <file> -Algorithm SHA256`).

**Updates**: the app checks for a new version at start-up, downloads it in the background and installs it when you quit (can be turned off in Settings → About). The update check (GitHub) is the only network access; no usage data is sent.

**License**: free for personal and business use; redistribution and modification are not permitted. See [LICENSE](LICENSE). Bundled third-party software (Electron, 7-Zip and others) is covered by its own licenses (`THIRD_PARTY_NOTICES.txt` in the installation folder).

**Feedback**: Settings → Feedback in the app opens an email.

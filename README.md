# Explore Me

English | [日本語](#日本語)

A tabbed, dual-pane file manager for Windows that looks and works like the Windows 11 File Explorer.

- Two panes side by side, each with tabs. Shift+F5 copies and Shift+F6 moves the selection to the other pane
- The same keys and right-click menu as File Explorer (plus the full Windows menu under "Show more options")
- Quick Look (Space for a large preview) and a command palette (Ctrl+K)
- Workspaces (save and reopen a whole set of tabs), color labels, and the Shelf (collect items with Ctrl+S, then move or copy them together)
- Disk usage, flat view, and search through subfolders (uses Everything or the Windows index when available)
- Create and extract zip files; extract 7z, rar, tar.gz and more
- English / Japanese, light / dark

## Usage

It works like File Explorer. Press **F1** in the app for every shortcut, and **Ctrl+,** (or the gear at the top right) for Settings.

### The window

- Navigation on the left: Home, pinned folders, This PC (drives), Workspaces, the Shelf
- On the right: two panes, each with its own tabs; the one you last clicked is the one you work in (Ctrl+Shift+D switches to a single pane)
- The app opens on Home (frequent places, drives and recent items)
- The language follows Windows (English or Japanese); change it in Settings → General → Language

### Common shortcuts

| Action | Keys |
| --- | --- |
| Back / up one folder | Backspace / Alt+↑ |
| Type in the address bar | Ctrl+L (Alt+D, F4) |
| Filter this folder / search subfolders too | Ctrl+E / Ctrl+Shift+F |
| New tab / close tab | Ctrl+T / Ctrl+W |
| Single pane / two panes | Ctrl+Shift+D |
| Copy / move to the other pane | Shift+F5 / Shift+F6 |
| Large preview (Quick Look) | Space |
| Command palette (find commands and folders by name) | Ctrl+K |
| Put on the Shelf (move or copy them together later) | Ctrl+S |
| Undo / redo | Ctrl+Z / Ctrl+Y |
| Large icons / medium icons / list / details | Ctrl+Shift+2 / 3 / 5 / 6 |
| Show hidden files | Ctrl+H |

- Right-click opens a Windows 11 style menu. For the full Windows menu (including items added by 7-Zip and other apps), Shift+right-click or choose "Show more options"
- Extract an archive (zip, 7z, rar, tar.gz and more) with "Extract here" in its right-click menu
- Turn on "Open folders with Explore Me" in Settings to open folders from the desktop and other apps in Explore Me as well

## Download

Download `ExploreMe-Setup-<version>.exe` from [Releases](../../releases/latest) and run it.

### System requirements

| | |
| --- | --- |
| OS | Windows 11 (64-bit, x64) |
| Windows 10 | Not tested (it is expected to work, but has not been checked) |
| Windows on ARM | Not tested |
| Installation | Per user (no administrator rights needed); you can choose the folder |

### If Windows shows "Windows protected your PC"

The installer is not code-signed, so Windows SmartScreen may show this screen the first time you run it.
Choose **More info → Run anyway**.

To make sure the file is the genuine one, compare its SHA-256 with the value on the release page. In PowerShell:

```powershell
Get-FileHash .\ExploreMe-Setup-0.1.0.exe -Algorithm SHA256
```

The installer is scanned on VirusTotal for each release. v0.1.0: [0 / 68 detections](https://www.virustotal.com/gui/file/bdbf9b5019b8655c13963fef48c4287a22ec304126816409d23b792a4a385a23) (scanned on 2026-09-23).

## Updates

The app checks for a new version when it starts, downloads it in the background and installs it when you quit (turn this off in Settings → About).
The update check (GitHub) is the only network access. No usage data is sent.

## Privacy

- Your files are handled on your PC only; nothing about them is sent anywhere
- The update check is a request to GitHub, which may record your IP address under GitHub's own privacy statement
- Feedback is sent from your own mail app. The author uses your email address and message only to reply and to improve the app, keeps them only as long as needed, and does not share them except as required by law. To ask about, correct or delete them, write to the feedback address shown in the app

## Uninstall

Uninstall Explore Me from Windows Settings → Apps → Installed apps.
If "Open folders with Explore Me" was on, folders open in File Explorer again.

## License

Free for personal and business use. Redistribution and modification are not permitted. See [LICENSE](LICENSE).
Bundled third-party software (Electron, 7-Zip and others) is covered by its own licenses (`THIRD_PARTY_NOTICES.txt` in the installation folder). The source code of the bundled 7-Zip (GNU LGPL) is attached to each release.

## Copyright

Copyright (c) 2026 ternando0831-lang

Windows and Visual Studio Code are trademarks of the Microsoft group of companies. Other product names are trademarks of their respective owners.

## Feedback

Send bug reports and requests by email from Settings → Feedback in the app.

## Known limitations

- 7z, rar and the like can be extracted, not created (only zip can be created). Password-protected archives cannot be extracted
- Old Japanese archives (lzh, tar and others with Shift_JIS names) may not extract with the right file names
- While the window is maximized, its frame does not show Mica (the translucent backdrop)

---

# 日本語

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
- 表示言語は Windows に合わせます（日本語か英語）。設定 → 全般 → 言語 で変えられます

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

インストーラーはリリースごとに VirusTotal で検査しています。v0.1.0: [検出 0 / 68](https://www.virustotal.com/gui/file/bdbf9b5019b8655c13963fef48c4287a22ec304126816409d23b792a4a385a23)（2026-09-23 に検査）。

## 更新

起動したときに新しい版を確認し、裏でダウンロードして、アプリを終了したときに更新します（設定 → バージョン情報で切り替えられます）。
通信するのは、この更新の確認（GitHub）だけです。使い方などの情報は送りません。

## 個人情報

- ファイルはすべて PC の中だけで扱い、外部には何も送りません
- 更新の確認は GitHub への通信で、GitHub は自社のプライバシー方針に従って IP アドレスを記録することがあります
- フィードバックは利用者自身のメールアプリから送られます。受け取ったメールアドレスと内容は、返信とアプリの改善のためだけに使い、必要な期間だけ保管し、法令に基づく場合を除いて第三者に提供しません。開示・訂正・削除のご依頼は、アプリに表示しているフィードバックの宛先へ

## アンインストール

Windows の「設定 → アプリ → インストールされているアプリ」から Explore Me をアンインストールします。
「フォルダーを Explore Me で開く」をオンにしていた場合も、元のエクスプローラーに戻ります。

## ライセンス

無料で使えます（個人・法人とも）。再配布・改変はできません。詳しくは [LICENSE](LICENSE) を見てください。
同梱しているソフトウェア（Electron、7-Zip など）はそれぞれのライセンスに従います（インストール先の `THIRD_PARTY_NOTICES.txt`）。同梱の 7-Zip（GNU LGPL）のソースコードは、各リリースに添付しています。

## 著作権

Copyright (c) 2026 ternando0831-lang

Windows・Visual Studio Code は Microsoft グループの商標です。その他の製品名は、それぞれの権利者の商標です。

## フィードバック

不具合の報告や要望は、アプリの「設定 → フィードバック」からメールで送れます。

## 既知の制限

- 7z・rar などは展開だけです（作成は zip のみ）。パスワード付きの書庫は展開できません
- 古い日本語の書庫（Shift_JIS の名前の lzh・tar など）は、名前が正しく展開されないことがあります
- 最大化している間は、ウィンドウの枠に Mica（半透明の背景）がかかりません

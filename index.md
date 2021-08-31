---
marp: true
title: Visual Studio Code で Linux サーバ上のファイルを直接編集できる拡張機能 "Remote - SSH" が便利だった件
theme: s2
headingDivider: 2
paginate: true
---

# Visual Studio Code で Linux サーバ上のファイルを直接編集できる拡張機能 "Remote - SSH" が便利だった件

<!-- _class: lead -->
<!-- _backgroundImage: url(https://marp.app/assets/hero-background.jpg) -->

## Visual Studio Code とは？

- プログラマ向けのエディタ
- 豊富な「拡張機能」で機能を追加可能
- Microsoft が開発
- Windows、Linux、macOS で動作
- VSCode とも呼ばれている

## 拡張機能 "Remote - SSH" とは？

SSH で Linux サーバに接続してファイルを直接編集できる

## VSCode のインストール

以下からダウンロードしてインストールする。

https://code.visualstudio.com/

## Remote - SSH のインストール

以下の URL で `Install` ボタンをクリックするか、
VSCode の「拡張機能」サイドバーで検索してインストールする。

https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh

## SSH の設定

C:\\Users\\ユーザー名\\.ssh\\config へ以下のように記入

    # パスワードを使用して接続する場合
    Host 設定名
      HostName ホスト名
      User ユーザー名

    # SSH認証鍵を使用して接続する場合
    Host 設定名
      HostName ホスト名
      IdentityFile 秘密鍵のパス
      User ユーザー名

## Remote - SSH を使う (1)

<div class="flex-container">

1. リモートエクスプローラーをクリック
2. `SSH Targets` を選択

![リモートエクスプローラー](https://raw.githubusercontent.com/saasan/vscode-remotessh/master/assets/remote-explorer.png)

</div>

## Remote - SSH を使う (2)

3. 接続したいホストにマウスを合わせると出る ![Connect to Host in New Window](https://raw.githubusercontent.com/saasan/vscode-remotessh/master/assets/connect.png) をクリック
4. 新しいウィンドウが開く
5. 上部に `Select the platform of the remote host "設定名"` と表示されるので Linux を選択
6. パスワード認証の場合は `Enter password for ユーザー名@ホスト名` と表示されるためパスワードを入力

## Remote - SSH を使う (3)

7. サイドバーの `フォルダーを開く` をクリック
8. 編集したいファイルがあるフォルダを選択
9. `OK` をクリック
10. `このフォルダー内のファイルの作成者を信頼しますか?` が表示されたら `はい、作成者を信頼します` をクリック
11. 選択したフォルダの内容がサイドバーに表示される
12. ファイルを開くとそのまま編集できる

## 編集以外の便利機能

- `Ctrl + @` でコンソールを開いてコマンドを実行可能
- フォルダが Git で管理されているリポジトリであれば、VSCode のソース管理機能でコミットなども可能

## 終わり

<!-- _class: lead -->

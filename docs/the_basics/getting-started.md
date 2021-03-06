# はじめる

React Nativeにようこそ! このページではあなたがアプリを今すぐ作れるように、
システムへのReact Nativeのインストールをお手伝いします。
React Nativeをすでにインストール済みなら、
[チュートリアル](tutorial.md)にスキップできます。
手順はあなたの開発OSによって少し違っていて、iOSとAndroidどちらの開発を始めたいかに
よっても変わってきます。iOSとAndroid両方を開発したいならそれでもいいですが、
セットアップが少し違ってくるので、始めるにあたりどちらか一つ選んでください。

## LinuxとWindowsのiOS対応
非対応です。
残念ながら、AppleはiOSの開発をMacのみ許可しています。もしあなたがiOSアプリを
作りたいもののMacを持っていないなら、かわりにAndroidでの手順で試し始められます。

## Mac + iOSで必要なもの

Xcode、node.js、React Nativeのコマンドライン・ツール、Watchman。

##  Mac + Androidで必要なもの

Android Studio、node.js、React Nativeのコマンドライン・ツール、Watchman.


### Mac iOS/Android共通
nodeとwatchmanは[Homebrew](http://brew.sh/)を通してインストールすることをおすすめします。

```
brew install node
brew install watchman
```

Nodeを入れるとnpmも入り、React Nativeのコマンドライン・インターフェースを
インストールできます。

```
npm install -g react-native-cli
```

パーミッションのエラーが出たならsudo付きで試してください: `sudo npm install -g react-native-cli`。

`Cannot find module 'npmlog'`というエラーがでたら、先にこれを実行してください: `curl -0 -L http://npmjs.org/install.sh | sudo sh`.

### Mac iOSのみ
Xcodeをインストールする最も簡単な方法は[Mac App Store](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)でやることです。

### Mac Androidのみ
[Android Studio](https://developer.android.com/studio/install.html)をダウンロードしてインストールしてください。

Javaのコードを変更する予定なら、ビルドを高速化する[Gradleデーモン](https://docs.gradle.org/2.9/userguide/gradle_daemon.html) をおすすめします。

## Linux + Androidで必要なもの

node.jsとReact Nativeのコマンドライン・ツール、Watchman、Android Studio。

##  Windows + Android

node.jsとReact Nativeのコマンドライン・ツール、Watchman、Android Studio。

### Linux + Androidのみ
[あなたのLinuxディストリビューションのインストール手順](https://nodejs.org/en/download/package-manager/)にしたがって、Node.js 4以上をインストールしてください。

### Windows + Androidのみ
おすすめのインストール方法はnode.jsとPython2を[Chocolatey](https://chocolatey.org)で
やることです。Chocolateyは人気のあるWindows用パッケージ・マネージャです。管理者権限で
コマンド・プロンプトを開いて実行してください:

```
choco install nodejs.install
choco install python2
```

### Windows/Linux共通Android向け
Nodeを入れるとnpmも入り、React Nativeのコマンドライン・インターフェースを
インストールできます。

```
npm install -g react-native-cli
```

[Android Studio](https://developer.android.com/studio/install.html)をダウンロードしてインストールしてください。

Javaのコードを変更する予定なら、ビルドを高速化する[Gradleデーモン](https://docs.gradle.org/2.9/userguide/gradle_daemon.html) をおすすめします。

### Linux + Androidのみ

[Watchman](https://facebook.github.io/watchman)はFacebookによって作られたツールで
ファイルシステム上での変更を監視します。インストールはパフォーマンスを向上させますが、
インストールするのが手間だったらなしでも動きます。[Watchmanインストールガイド](https://facebook.github.io/watchman/docs/install.html#installing-from-source)にしたがって
ソースからのコンパイルとインストールをしてください。

## React Nativeのインストールをテストする(Mac)

### iOS

React Nativeのコマンドライン・ツールを使って"AwsomeProject"という新しいReact Nativeのプロジェクトを生成します。そして、新しく出来たフォルダの中で`react-native run-ios`を実行してください。

```
react-native init AwesomeProject
cd AwesomeProject
react-native run-ios
```

すぐにiOSシミュレータ上で新しいアプリが動いているのが見れるでしょう。`react-native run-ios`はアプリを実行する方法の一つでしかなく、XocdeやNuclide上で直接実行することもできます。

### Android

React Nativeのコマンドライン・ツールを使って"AwsomeProject"という新しいReact Nativeのプロジェクトを生成します。そして、新しく出来たフォルダの中で`react-native run-android`を実行してください。

```
react-native init AwesomeProject
cd AwesomeProject
react-native run-android
```

すべてが上手くいけばすぐにAndroidエミュレータ上で新しいアプリが動いているのが見れるでしょう。`react-native run-android`はアプリを実行する方法の一つでしかなく、Android StudioやNuclide上で直接実行することもできます。

## あなたのアプリを修正する(Mac)

アプリの実行に成功したので、修正してみましょう。

### iOS

- `index.ios.js`を好きなテキスト・エディタで開いて何行か変更します。
- iOSシミュレータ上で`Command⌘ + R` を打って、アプリをリロード、変更を確認しましょう!

### Android

- `index.android.js`を好きなテキスト・エディタで開いて何行か変更します。
- `R` を二回打つか開発メニューから`Reload`を選んで変更を確認しましょう!

### 以上です!

おめでとうございます。はじめてのReact Nativeアプリの実行に成功しました。


## React Nativeのインストールをテストする(Linux、Windows)

React Nativeのコマンドライン・ツールを使って"AwsomeProject"という新しいReact Nativeのプロジェクトを生成します。そして、新しく出来たフォルダの中で`react-native run-android`を実行してください。

```
react-native init AwesomeProject
cd AwesomeProject
react-native run-android
```

すべてが上手くいけばすぐにAndroidエミュレータ上で新しいアプリが動いているのが見れるでしょう。

よくある問題は`react-native run-android`を実行した際にパッケージャが始まらないことです。
`react-native start`で手動で実行できます。

### Windowsのみ
Windowsで`ERROR  Watcher took too long to load`が出たら、[このファイル](https://github.com/facebook/react-native/blob/5fa33f3d07f8595a188f6fe04d6168a6ede1e721/packager/react-packager/src/DependencyResolver/FileWatcher/index.js#L16)のタイムアウトの時間を上げてみてください。(`node_modules/react-native/`配下)

If you hit a `ERROR  Watcher took too long to load` on Windows、 try increasing the timeout in [this file](https://github.com/facebook/react-native/blob/5fa33f3d07f8595a188f6fe04d6168a6ede1e721/packager/react-packager/src/DependencyResolver/FileWatcher/index.js#L16) (under your `node_modules/react-native/`).

## あなたのアプリを修正する(Linux、Windows)

アプリの実行に成功したので、修正してみましょう。

- `index.android.js`を好きなテキスト・エディタで開いて何行か変更します。
- `R` を二回打つか開発メニューから`Reload`を選んで変更を確認しましょう!

### 以上です!

おめでとうございます。はじめてのReact Nativeアプリの実行に成功しました。

## さて次は?

- この新しいReact Nativeのコードをすでにあるアプリケーションに追加したいなら
[連携ガイド](../guides/integration-with-existing-apps.md)をチェックしてください。

- 上手くいかなかったのなら[トラブルシューティング](../quick_start/troubleshooting.md)のページを見てください。

- もっとReact Nativeについて学びたいのなら、 [チュートリアル](tutorial.md)を続けてください。

[次](tutorial.md)


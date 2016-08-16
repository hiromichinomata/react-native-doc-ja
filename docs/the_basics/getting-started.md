# coding: utf-8
# Getting Started

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

## Android

React Nativeのコマンドライン・ツールを使って"AwsomeProject"という新しいReact Nativeのプロジェクトを生成します。そして、新しく出来たフォルダの中で`react-native run-android`を実行してください。

```
react-native init AwesomeProject
cd AwesomeProject
react-native run-android
```

すべてが上手くいけばすぐにAndroidエミュレータ上で新しいアプリが動いているのが見れるでしょう。`react-native run-android`はアプリを実行する方法の一つでしかなく、Android StudioやNuclide上で直接実行することもできます。

<block class="mac ios android" />

### Modifying your app

Now that you have successfully run the app、 let's modify it.

<block class="mac ios" />

- Open `index.ios.js` in your text editor of choice and edit some lines.
- Hit `Command⌘ + R` in your iOS Simulator to reload the app and see your change!

<block class="mac android" />

- Open `index.android.js` in your text editor of choice and edit some lines.
- Press the `R` key twice or select `Reload` from the Developer Menu to see your change!

<block class="mac ios android" />

### That's it!

Congratulations! You've successfully run and modified your first React Native app.

<center><img src="img/react-native-congratulations.png" width="150"></img></center>

<block class="windows linux android" />

## Testing your React Native Installation

Use the React Native command line tools to generate a new React Native project called "AwesomeProject"、 then run `react-native run-android` inside the newly created folder.

```
react-native init AwesomeProject
cd AwesomeProject
react-native run-android
```

If everything is set up correctly、 you should see your new app running in your Android emulator shortly.

> A common issue is that the packager is not started automatically when you run
`react-native run-android`. You can start it manually using `react-native start`.

<block class="windows android" />

> If you hit a `ERROR  Watcher took too long to load` on Windows、 try increasing the timeout in [this file](https://github.com/facebook/react-native/blob/5fa33f3d07f8595a188f6fe04d6168a6ede1e721/packager/react-packager/src/DependencyResolver/FileWatcher/index.js#L16) (under your `node_modules/react-native/`).

<block class="windows linux android" />

### Modifying your app

Now that you have successfully run the app、 let's modify it.

- Open `index.android.js` in your text editor of choice and edit some lines.
- Press the `R` key twice or select `Reload` from the Developer Menu to see your change!

### That's it!

Congratulations! You've successfully run and modified a React Native app.

<center><img src="img/react-native-congratulations.png" width="150"></img></center>

<block class="mac windows linux ios android" />

## Now What?

- If you want to add this new React Native code to an existing application、 check out the [Integration guide](docs/integration-with-existing-apps.html).

- If you can't get this to work、 see the [Troubleshooting](docs/troubleshooting.html#content) page.

- If you're curious to learn more about React Native、 continue on
to the [Tutorial](docs/tutorial.html).


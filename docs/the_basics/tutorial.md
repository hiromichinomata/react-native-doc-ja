React NativeはReactに似ていますが、ブロックを作るのにWebコンポーネントの代わりにネイティブ・コンポーネントを使っています。
なので、React Nativeアプリの基本的構造を理解するには、JSX、コンポーネント、`state`や`props`といった基本的なReactの概念を理解する必要があります。
もしすでにReactを知っていても、React Native固有の部分を学ぶ必要があります。このチュートリアルはReactの経験のありなしに関わらずすべての人を対象としています。

さて、はじめてみましょう。

## Hello World

古風な伝統に従うなら、私たちは"Hello, world"という以外には何もしないアプリをはじめに作らねばなりません。以下がそうです。

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text } from 'react-native';

class HelloWorldApp extends Component {
  render() {
    return (
      <Text>Hello world!</Text>
    );
  }
}

AppRegistry.registerComponent('HelloWorldApp', () => HelloWorldApp);
```

興味を惹かれたなら、Webシミュレーター上で直接サンプルコードをいじることができます。
またあなたの`index.ios.js`か`index.android.js`に貼り付けてローカルマシン上の実際のアプリを作れます。

## 何が起きているのか

ここにあるいくつかはJavascriptのようには見えないかもしれません。パニックにならないで。これは未来です。

はじめに、ES2015 (またの名をES6)はJavaScriptの幾つかの改良で、現在の公式標準の一部ですがまだ全てのブラウザでサポートされていません。なのでWeb開発ではまだ広く使われていませんが、React NativeはES2015サポートが同梱されているので互換性を気にすることなく使えます。`import`、`from`、`class`、`extends`、`() =>`といった上の例のなかにある文法はすべてES2015の機能です。もしES2015に慣れ親しんでいないのなら、このチュートリアルにあるようなサンプル・コードを読むことで、要点がつかめると思います。望むなら、[このページ](https://babeljs.io/docs/learn-es2015/)にはES2015の機能の良い概要が書いてあります。

このコード例内の他の普通でない部分は`<Text>Hello world!</Text>`です。これはJSXといって、Javascript内にXMLを埋め込むための文法です。多くのフレームワークでは固有のテンプレート言語を使ってマークアップ言語にコードを埋め込んでいます。Reactでは反対です。JSXでコードの中にマークアップ言語を書きます。Web上のHTMLのように見えますが、Webの`<div>`や`<span>`の代わりにReactコンポーネントを使います。この場合、`<Text>`はビルトインのコンポーネントで何らかのテキストを表示するだけです。

## コンポーネントとAppRegistry

なのでこのコードは新しい`コンポーネント`である`HelloWorldApp`を定義して`AppRegistry`に登録しています。あなたがReact Nativeのアプリを作る際には新しいコンポーネントをたくさん作ることでしょう。スクリーン上に見える全ては何かのコンポーネントです。コンポーネントはとてもシンプルです。唯一要求されるのは`render`関数で描画用のJSXを返します。

`AppRegistry`はReact Nativeにどのコンポーネントが全体のアプリケーションのルートとなるか伝えているだけです。あなたが`AppRegistry`について考える機会は多くはないでしょう。アプリ全体の中で`AppRegistry.registerComponent`を呼ぶのは一回だけでしょう。例の中には含まれているので 、すべてを`index.ios.js`か`index.android.js`に貼り付けるだけで動かすことができます。

## このアプリは大したことをしないのですが、

いい指摘です。コンポーネントにもっと色々やってもらうには[Propsについて学ぶ](props.md)必要があります。

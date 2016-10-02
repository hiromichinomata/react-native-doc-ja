コンポーネントを操作するのには２種類のデータタイプ `props` と `state`があります。 `props` は親によってセットされ、コンポーネントのライフタイムの中で固定です。変化するデータに対しては `state`　を使う必要があります。

一般的に、コンストラクター中で `state` を初期化する必要があり、それから値を変えたいときに `setState` を呼びます。

例えば、いつも点滅しているテキストを作りたいとしましょう。テキスト自体は点滅するコンポーネントが作られた際に一度だけ作成されるのでテキスト自体は `prop`　です。 *テキストが現在オンかオフか* は時間によって変わり、`state`　の中にあるべきです。

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text, View } from 'react-native';

class Blink extends Component {
  constructor(props) {
    super(props);
    this.state = {showText: true};

    // 毎秒stateをトグルする
    setInterval(() => {
      this.setState({ showText: !this.state.showText });
    }, 1000);
  }

  render() {
    let display = this.state.showText ? this.props.text : ' ';
    return (
      <Text>{display}</Text>
    );
  }
}

class BlinkApp extends Component {
  render() {
    return (
      <View>
        <Blink text='点滅するのが好き' />
        <Blink text='イエス、点滅は最高' />
        <Blink text='なぜ人はこれをHTMLの外にもっていったの？' />
        <Blink text='私を見て私を見て私を見て' />
      </View>
    );
  }
}

AppRegistry.registerComponent('BlinkApp', () => BlinkApp);
```

実際のアプリケーションではstateをタイマーと一緒に設定したくはないでしょう。新しいデータがサーバーやユーザーの入力から届いた際にstateをセットしたいかもしれません。あなたはデータフローをコントロールするために [Redux](http://redux.js.org/index.html) のようなステートコンテナを使うことができます。その際には `setState` を直接呼ぶよりはReduxを使ってstateを修正した法がいいでしょう。

stateはReact中で動くのと同じように動きます。なので、stateのハンドリングの詳細は [React.Component API](https://facebook.github.io/react/docs/component-api.html)で確認できます。

この時点で、ほとんどの例が味気ないデフォルトのブロックテキストを使っていることにがっかりしているかもしれません。見た目をより美しくするには、[スタイルについて学ぶ](style.md) 必要があります。

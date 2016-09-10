多くのコンポーネントは作成時にパラメーターを渡すことでカスタマイズできます。この作成時パラメーターを`props`といいます。

例えば、基本的なReact Nativeコンポーネントのひとつに`Image`があります。画像を作成する際に
`source`というプロパティーを使うことで何の画像を表示するかコントロールできます。

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Image } from 'react-native';

class Bananas extends Component {
  render() {
    let pic = {
      uri: 'https://upload.wikimedia.org/wikipedia/commons/d/de/Bananavarieties.jpg'
    };
    return (
      <Image source={pic} style={{width: 193, height: 110}}/>
    );
  }
}

AppRegistry.registerComponent('Bananas', () => Bananas);
```

JSXに変数`pic`を埋め込むために`{pic}`とかっこで囲むことに気をつけてください。JSX中のカッコ内にはどんなJavaScriptも書けます。

あなたは自身のコンポーネント内で`props`を使うこともできます。これによってアプリ内のいろいろな場所で使える
単一コンポーネントを作ることができ、それぞれの場所で少しだけ違ったプロパティをもっています。
あなたの`render`関数内で`this.props`を参照してください。以下が例です:

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text, View } from 'react-native';

class Greeting extends Component {
  render() {
    return (
      <Text>Hello {this.props.name}!</Text>
    );
  }
}

class LotsOfGreetings extends Component {
  render() {
    return (
      <View style={{alignItems: 'center'}}>
        <Greeting name='Rexxar' />
        <Greeting name='Jaina' />
        <Greeting name='Valeera' />
      </View>
    );
  }
}

AppRegistry.registerComponent('LotsOfGreetings', () => LotsOfGreetings);
```

プロパティーとして `name` を使うことで`Greeting`コンポーネントをカスタマイズしていて、あいさつ一つ一つにコンポーネントを再利用できます。この例ではJSX内で`Greeting`コンポーネントをまるでビルトインのコンポーネントのように使っています。これを実現できるのがReactのクールなところです。 もし違ったUIセットが欲しくなったら、単に新しいものを作ってしまえばいいのです。

今回出た他の新規項目は`View`コンポーネントです。`View`は他のコンポーネントのコンテナとして有用で、スタイルとレイアウトをコントロールできます。

`props`と基本的な`Text`、`Image`、`View`コンポーネントで、多種の静的画面を作成できます。時間でアプリを変更する方法について学ぶには[ステートについて学ぶ](state.md)必要があります。

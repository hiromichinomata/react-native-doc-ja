React Nativeでは、ステイルを定義するのに特別な言語や文法を使いません。 Javascriptでアプリケーションのスタイルを定義するだけです。全てのコアコンポーネントは `style` という名前のpropをサポートしています。スタイルの名前や値は通常WebでCSSが動くのと同じですが、名前が `background-color` のかわりに `backgroundColor` のように書かれています。

`style` プロパティーは特に真新しくない JavaScriptオブジェクトです。 それが一番シンプルで、例で使っています。また、あなたはスタイルの配列を渡すことも出来ます。配列中で最後のスタイルが優先なので、スタイルの継承を使えます。

コンポーネントの複雑性が増すに連れ、一つの場所で複数のスタイルを定義するのに `StyleSheet.create` を使うのがクリーンでいいでしょう。以下が例です。

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, StyleSheet, Text, View } from 'react-native';

class LotsOfStyles extends Component {
  render() {
    return (
      <View>
        <Text style={styles.red}>ただの赤</Text>
        <Text style={styles.bigblue}>ただのビッグブルー</Text>
        <Text style={[styles.bigblue, styles.red]}>ビッグブルー、そしれ赤</Text>
        <Text style={[styles.red, styles.bigblue]}>赤、そしてビッグブルー</Text>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  bigblue: {
    color: 'blue',
    fontWeight: 'bold',
    fontSize: 30,
  },
  red: {
    color: 'red',
  },
});

AppRegistry.registerComponent('LotsOfStyles', () => LotsOfStyles);
```

一つの共通パターンとしてコンポーネントが `style` プロパティーを受け付けるようにすることがあり、サブコンポーネントのスタイルを順番に決めるのに使われます。あなたはこれをCSSのようなスタイルの *カスケード* に使えます。

テキストをカスタマイズする方法はもっとあります。完全なリストを確認するには [テキストコンポーネント・レファレンス](../text.md)　を参照してください。

さてテキストをきれいにすることができました。スタイル関係の次のステップは [コンポーネントのサイズをコントロールする方法を学ぶ](height-and-width.md)です。

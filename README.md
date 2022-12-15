# This project is forked from [cssivision/react-native-qrcode](https://github.com/cssivision/react-native-qrcode)

# react-native-qrcode3
A react-native component to generate [QRcode](http://en.wikipedia.org/wiki/QR_code), not only support English.

## Installation
```sh
npm install react-native-qrcode3 --save

# If you do n’t have react-native-webview installed, you need to install it
npm install react-native-webview --save
```
## Usage
```jsx
'use strict';

import React, { Component } from 'react'
import QRCode from 'react-native-qrcode2';

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'http://facebook.github.io/react-native/',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },

    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Available Props

prop      | type                 | default value
----------|----------------------|--------------
`value`   | `string`             | `http://facebook.github.io/react-native/`
`size`    | `number`             | `128`
`bgColor` | `string` (CSS color) | `"#000"`
`fgColor` | `string` (CSS color) | `"#FFF"`

<img src='qrcode.png' height = '256' width = '256'/>

## changelog
- 0.3.0
  - Use react-native-webview instead react-native's WebView

## Licenses

All source code is licensed under the [MIT License](https://github.com/cssivision/react-native-qrcode2/blob/master/LICENSE).

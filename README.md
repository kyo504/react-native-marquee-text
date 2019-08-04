# react-native-marquee

A pure JavaScript marquee text component for react native.

## Installation

```
npm install --save react-native-marquee
or
yarn add react-native-marquee
```

## Usage

```
import React, { Component } from 'react';
import { StyleSheet, View } from 'react-native';
import MarqueeText from 'react-native-marquee';

export default class MarqueeTextSample extends Component {
  render() {
    return (
      <View style={styles.container}>
        <MarqueeText
          style={{ fontSize: 24 }}
          duration={3000}
          marqueeOnStart
          loop
          marqueeDelay={1000}
          marqueeResetDelay={1000}
        >
          Lorem Ipsum is simply dummy text of the printing and typesetting industry and typesetting industry.
        </MarqueeText>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
  },
});
```

## Properties

| Prop                  | Type     | Optional | Default                   | Description
| --------------------- | -------- | -------- | ------------------------- | -----------
| style                 | StyleObj | true     | -                         | text style
| duration              | number   | true     | 3000                      | Number of milliseconds until animation finishes from start.
| loop                  | boolean  | true     | false                     | Set this true when animation repeats.
| marqueeOnStart        | boolean  | true     | false                     | Set this true while waiting for new data from a refresh.
| marqueeResetDelay     | number   | true     | 0                         | Number of milliseconds to wait before resetting the marquee position after it finishes.
| marqueeDelay          | number   | true     | 0                         | Number of milliseconds to wait before starting or restarting marquee.
| onMarqueeComplete     | function | true     | -                         | Callback function for when the marquee completes its animation
| useNativeDriver       | boolean  | true     | false                     | Set this truen if you want to use native driver
| easing                | function | true     | inOut                     | Easing function to define animation curve.

## Methods

These methods are optional, you can use the isOpen property instead

| Prop             | Params          | Description                          |
| :--------------- |:---------------:| :---------------:|
| startAnimation   | delay           | Start animation  |
| stopAnimation    | -               | Stop animation   |

## Contribution

Do you have any idea or want to change something? Just open an issue. Contributions are always welcome.

## Lisence

[MIT Lisence](https://opensource.org/licenses/MIT)

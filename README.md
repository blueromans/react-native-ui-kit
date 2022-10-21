<img alt="React Native Ui Kit" src="https://user-images.githubusercontent.com/29883389/197212969-5c3b98c8-63d2-4cf9-af35-05e1f26d4e37.png">

# React Native Ui Kit

A flexible and easy way to manage ui Android and IOS!

[![npm](https://img.shields.io/npm/v/@blueromans/react-native-ui-kit)](https://www.npmjs.com/package/@blueromans/react-native-ui-kit) ![Supports Android,iOS](https://img.shields.io/badge/platforms-android%20%7C%20ios-lightgrey.svg) [![NPM](https://img.shields.io/npm/dm/@blueromans/react-native-ui-kit)](https://www.npmjs.com/package/@blueromans/react-native-ui-kit)
![MIT License](https://img.shields.io/npm/l/@blueromans/react-native-ui-kit.svg)

## Table of Contents

- [React Native Ui Kit](#react-native-ui-kit)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Installation](#installation)
    - [With react-native-cli](#with-react-native-cli)
  - [Usage](#usage)
    - [Theming](#theming)
    - [Components](#components)
      - [ActivityIndicator](#activityindicator)
      - [Badge](#badge)
      - [Button](#button)
        - [Props](#props)
          - [mode](#mode)
          - [children (required)](#children-required)
  - [Troubleshooting](#troubleshooting)

## Requirements

- [React Native 0.64.0+](https://reactnative.dev)
- [React Native Safe Area Context](https://www.npmjs.com/package/react-native-safe-area-context)
- [React Native Svg](https://www.npmjs.com/package/react-native-svg)
- [React Native Masket Text](https://www.npmjs.com/package/react-native-masked-text)
- [React Native Vector Icons](https://www.npmjs.com/package/react-native-vector-icons)

## Installation

### With react-native-cli

1. Install library

   from npm

   ```bash
   npm install @blueromans/react-native-ui-kit react-native-safe-area-context react-native-svg react-native-masked-text react-native-vector-icons
   ```

   from yarn

   ```bash
   yarn add @blueromans/react-native-ui-kit react-native-safe-area-context react-native-svg react-native-masked-text react-native-vector-icons
   ```

2. Link native code

   ```bash
   cd ios && pod install
   ```

## Usage

### Theming

### Components

#### ActivityIndicator

<img width="300" src="https://user-images.githubusercontent.com/29883389/197247955-a2afc205-cbc0-428f-894b-6f6b0124bb17.gif">

Activity indicator is used to present progress of some activity in the app.

```javascript
import React from 'react';
import { ActivityIndicator } from '@blueromans/react-native-ui-kit';

const MyComponent = () => (
  <ActivityIndicator animating={true} color={'red'} />
);

export default MyComponent;
);
```

#### Badge

<img width="300" src="https://user-images.githubusercontent.com/29883389/197246620-cda0b1ca-670a-4076-b463-af009287027a.png">

Badges are small status descriptors for UI elements. A badge consists of a small circle, typically containing a number or other short set of characters.

```javascript
import React from 'react';
import { Badge } from '@blueromans/react-native-ui-kit';

const MyComponent = () => (
  <Badge>3</Badge>
);

export default MyComponent;
);
```

#### Button

<img width="300" src="https://user-images.githubusercontent.com/29883389/197247692-7ccd23c4-fec8-487e-b6f2-7e410837b3c0.png">

A button is component that the user can press to trigger an action.

```javascript
import React from 'react';
import { Button } from '@blueromans/react-native-ui-kit';

const MyComponent = () => (
  <Button icon="camera" mode="contained" onPress={() => console.log('Pressed')}>
    Press me
  </Button>
);

export default MyComponent;
```

##### Props

###### mode

Type: 'text' | 'outlined' | 'contained'
Default value: 'text'
Mode of the button.

- text - flat button without background or outline.
- outlined - button with an outline without background.
- contained - button with a background color.

###### children (required)

Type: React.ReactNode
Label text of the button.

## Troubleshooting

If you have build errors, then it might be caused by caching issues, please try:

```bash
watchman watch-del-all
rm -fr $TMPDIR/react-*
react-native start --reset-cache

Or,

rm -rf node_modules
yarn
react-native start --reset-cache
```

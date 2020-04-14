# react-native-stylized-placeholder is deprecated
This library is deprecated now and will not be supported. React Native team has fixed placeholder issue for now (https://github.com/facebook/react-native/commit/e6057095adfdc77ccbbff1c97b1e86b06dae340b).

## Description
Custom React Native TextInput for styling placeholder and prevent bug with allowFontScaling property for TextInput's placeholder.

## Installation
Run command in the folder of your project: `npm install react-native-stylized-placeholder`

## Usage
Import and use CustomTextInput.
```javascript
import CustomTextInput from 'react-native-stylized-placeholder';
    
<CustomTextInput name='restoreEmail'
	style={STYLES.input}
	onChangeText={(text) => {
		this.setState({text: text})
	}}
	placeholder={"Placeholder text"}
	underlineColorAndroid={"#ff0000"}
	autoFocus={true}
	onRef={ref => this.input = ref}
	allowFontScaling={false}
	placeholderStyle={{top: 10, left: 10, fontSize: 16}}
/>
```
Use onRef property instead of TextInput's ref property.
Use placeholderStyle to pass object with styles for placeholder text. To correct placeholder's position pass into the placeholderStyle top/bottom/left/right positioning style properties.
    

## Why
Default React Native functionality doesn't support style property for TextInput's placeholder. Also, there are some known bugs with `allowFontScaling={false}` property for TextInput and its placeholder.

RN issues:
* https://github.com/facebook/react-native/issues/17898
* https://github.com/facebook/react-native/issues/18786
* https://github.com/facebook/react-native/issues/15886
* https://github.com/facebook/react-native/issues/18827

This library will fix this temporary issues in your React Native application.

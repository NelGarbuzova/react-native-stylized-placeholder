# react-native-stylized-placeholder

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
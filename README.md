# Today I Learned by *Owen Ramirez*

[React Native](https://reactnative.dev/) and [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) official documentation reading personal journal

[My URL github pages](https://brightcoders-bootcamps.github.io/today-i-learned-OwenRamire/)

## Week 1

### Thur 23th, July 2020 *JavaScript.- **Introduction***
In this reading I learn the things about what you should already know to start with JavaScript. The 
definition of what is JavaScript? examples about how can javaScript be used in the client-side and the server-side.
A little comparison of JavaScript to Java because they can be sound like similar, but they are differents starting with the syntax.
I leard the meaning of ECMA (European Computer Manufacturers Association) and what they do.
And finally how can you started writting JavaScript   


### Fri 24th, July 2020 *JavaScript.- **Grammar and types***
In this reading talks about the syntax of this programming language, the three ways that you can declare and the differences of the 
variables in JS, the ways of how can you evaluate your variable to prevent an error, the scope of your variables.
Also talks about the data structure and the types for example null,booleans, numbers, strings, etc

## Week 2

### Mon 27th, July 2020 *RN.- **Core Components and Native Components***
I start thinking about what is React Native? In the documentation of RN says that is a framework for build and Android and iOS 
applications using React.
The difference between using components in Android and iOS. And with this framework we have a native components to work with this two OS called core components.
You can see all them in the [React Native documentation](https://reactnative.dev/docs/components-and-apis) and a table with the core component that you'll mostly work (with his descriptions, how can you use that component in Android or iOS and a web analog to understand how works that component if you're familiarity on the web development) 

### Tues 28th, July 2020 *RN.- **React Fundamentals***
As the name of this framework React native runs on React, so we can use the same core concepts that React has. 
- A **component** is a part of your code that you can split in reusable pieces. To define a component is write a  
  function (
   ```javascript
   const yourComponent = () => { 
     return(); 
   };
   //or 
  function yourComponent() {
    return(); 
  };
  ```
  ) or it could be as a class (
  ```javascript
  class YourClass extends React.Component {
    render() {
      return ();
    }
  ```
)
- **JSX** let us write inside of a component, as an example of JSX in the react native documentation
  ```javascript 
  const Cat = () => {
   const name = "Maru";
     return (
       <Text>Hello, I am {name}!</Text> //Hello, I am Maru
     );
  }

  export default Cat;
  ```  
- **Props** let us to customize our components and make it more reusable just changing the properties of the component
- **States** are useful for handling data that is going to change over the time  

### Wed 29th, July 2020 *RN.- **Troubleshooting***
In this section we can check the common issues when you setting up React Native, for example the port of the server (8081) that it could be use it when you start the server. To solve that problem you can kill the process in that port or if you want, you can change the port of the server. 
Other problem it could be the missing libraries when you add it manually if you're using Xcode setting, in the documentation you can have the solution in the exactly files
If you have an issue and you can't find it here you can search in the [issues in Github](https://github.com/facebook/react-native/issues/)  
  
### Thur 30th, July 2020 *RN.- **Platform Specific Code***
When you are building your app, maybe you want to make a little difference in your visual components in Android and iOS. React Native  provides you two ways:
- **Platform module:** 
  - OS method: this module can detect in which OS the app is running, so you can change the properties of your components or do a specific task for example:
  ```javascript
  import { Platform, StyleSheet } from 'react-native';

  const styles = StyleSheet.create({
    height: Platform.OS === 'ios' ? 200 : 100
  });
  //in this example if the OS is iOS the height will be 200 and if is Android will be 100
  ``` 
  - select method: this give you an object where keys can be Android, iOS, native and default that returns the most fitting value for the platform
- **Platform-specific extensions:** with this modules you can split your files as *yourFile**.ios.js*** or *yourFile**.android.js*** and 
  when you import the file RN will detect when the file has an .ios. or .android. 
 
### Fri 31st, July 2020 *RN.- **Setting up the development environment***
In this section I learn the two ways to build my first React Native app and they are: 
- **Expo CLI:** this is the easiest way to start with RN if you don't have any experience on mobile development.
  You could choose download the Expo CLI or try using the web browser in [Snack](https://snack.expo.io/).
  - To get started you just need lastest version of Node.js and run ```javascript npm install -g expo-cli``` to install the Expo CLI and done you can create a new proyect with ```javascript   expo init MyProject```  
- **React Native CLI:** This is the way to start with RN if you already familiar with mobile development because you require Xcode or Android Studio to get started
  - To get started it depends of what OS are you running in the PC that you work and if you want to run in an iOS or an Android. Check the documentation to [get started](https://reactnative.dev/docs/environment-setup).  

## Week 3

### Mon 3rd, August 2020 *RN.- **Out-of-Tree Platforms***
React native isn't just to build for android and iOS, there are other projects that bring RN to other platflorms for example:
- [React Native Windows](https://github.com/Microsoft/react-native-windows)
- [React Native DOM](https://github.com/vincentriemer/react-native-dom)
- [React Native Turbolinks](https://github.com/lazaronixon/react-native-turbolinks)
- [React Native Desktop](https://github.com/status-im/react-native-desktop-qt)
- [React Native macOS](https://github.com/ptmt/react-native-macos)

### Tues 4th, August 2020 *RN.- **Runing On Device***
You can choose work with a virtual device or a physical device, but is good that you test your project in a physical device. 
first it will depend if you run the project in Android or iOS and what is the OS of your machine. If you are using Expo CLI, just scan the QR code that appears when start the server 
to know more about the instructions that you need to follow, go to [Running on device](https://reactnative.dev/docs/running-on-device) section  

### Wed 5th, August 2020 *RN.- **Fast Refresh***
Fast refresh is a React Native feature that allows us to watch the changes of our project in a second or two.
This fast refresh works when you edit a module that export React componentes, if  have a module with export that isn't a React component, the fast refresh will re-run both the module and the other modules importing it.
When fast refresh is running and if you have a syntax error you just need to fix the error and save the file and in a moment you can see the changes and the redbox will disappear    

### Thur 6th, August 2020 *RN.- **Testing***
It is so important to test our projects because if there are bugs will produce bad user experience. We need to test because we can make mistakes and its better that we 
find the bugs and not the users because we can fix those problems before we realease our app. 
Testing the project help us to understand the codebase, also make automated testing means less time with manual testing.
To test our apps we can chose differents ways for example: 
- **Static Analysis:** checks our code for errors as we write it 
- **Unit Test:** cover the smallest part of code, like individual functions or classes
- **Integration Test:** real individual units are combined and tested together to ensure that their cooperation works as expected. 
- **End-to-End Test (E2E):** verify our app is working as expected on a device

### Fri 7th, August 2020 *RN.- **Using Libraries***
With React Native you're not limited, if the core components and APIs that React Native brings to you are not enough, you can search a library that you need 
because RN has a community of developers that develop new libraries. To do this you need a package manager (npm CLI or yarn classic) and follow the library's instructions to download the library that you need 
 
## Week 4

### Mon 10th, August 2020 *RN.-**Upgrading to new React Native versions***
We need to upgrade our React Native version because with the new upgrades we can use new APIs, components, dev tools, etc.
- **Expo projects:** to upgrade our projects with expo, we require update the `react-native`, `react` and `expo` package versions in our `package.json` file. To do this go to [Upgrading Expo SDK Walkthrough](https://docs.expo.io/workflow/upgrading-expo-sdk-walkthrough/?redirected)
- **React Native projects:** there are two ways to do this, by using React Native CLI or with Upgrade Helper.
	- [React Native CLI](https://github.com/react-native-community/cli): this comes with `upgrade` command that provides a one-step operation to upgrade the source files with a minimum conflict.
	  Just run `npx react-native upgrade` or if you want a specific version, just pass the version as an argument like this `npx reac-native upgrade 0.61.0-rc.0`. 
	  The project is upgraded using `git apply` with 3-way merge and it may happen that you will need to resolve a fiw conflicts. Follow the documentation in the part of [resolve the conflict](https://reactnative.dev/docs/upgrading#2-resolve-the-conflicts) to see an example.
	- [Upgrade Helper](https://react-native-community.github.io/upgrade-helper/): is a web tool to help you out when upgrading your apps by providing the full set of changes happening between any two versions. After that, just follow the instructions of what do you need to modify or go to [Upgrade helper in the react native documentation](https://reactnative.dev/docs/upgrading#upgrade-helper) for more information

### Tues 11th, August 2020 *RN.- **Using TypeScript***
The oficial documentation of [TypeScript](https://www.typescriptlang.org/) says that is a language which builds on JavaScript. This language you can use it in React Native because this framework supports TypeScript. This works transforming your files to JavaScript works via Babel as a non-TypeScript React Native Project
To get started there are differents ways, for example: 
- With a **new project:**
	- You can use TypeScript template, just run `npx react-native init MyApp --template react-native-template-typescript`
	- If you work with Expo, use Ignite `ignite new MyTSProject` after install expo (`npm install -g expo-cli`)    
- With an **existing project:**
	- Add TypeScript to your project `npm install --save-dev typescript @types/jest @types/react @types/react-native @types/react-test-renderer` or `yarn add --dev typescript @types/jest @types/react @types/react-native @types/react-test-renderer`
	- follow the instructions of [how will you configure your files](https://reactnative.dev/docs/typescript#adding-typescript-to-an-existing-project)

### Wed 12th, August 2020 *RN.- **Style***
All the core components in React Native have a style prop, with this prop you can give styles at your components. The style names and vaules usually match how CSS works on the web, 
the only thing that change is that the names use camel casing for example if you want put a background color in CSS it'll be `background-color: red` and in React Native it'll be `backgroundColor: 'red'`.
- You can use the styles in the component: 
	- ``` javascript
           <Text style={{color: 'red'}}>I'm red</Text>
	  ```   
- Or you can use the `StyleSheet` and `StyleSheet.create()` function of react native to create a several styles:
	- ```javascript
	  import React from 'react';
	  import {Text, StyleSheet} from 'react-native';

	  export default const app = () => {
	    return <Text style={styles.text}>I'm text</Text>;
	  }
	  
	  const styles = StyleSheet.create({
	    text: {
	      color: 'red',
	      fontSize: 30,
	    }
	  });
	  ```

### Thur 13th, August 2020 *RN.- **Height and Width***
This two properties are to determine their size on the screen. In React Native all dimensions are unitless and represent density-independent pixels.
for example:
```javascript
import React from 'react';
import {View} from 'react-native';

export default const app = () => {
  return (
    <View>
      <View style={{width: 50, height: 50, backgroundColor: 'red'}}/>
      <View style={{width: 100, height: 100, backgroundColor: 'blue'}}/> 
    </View>
  );
} 
```   
With this two props the dimensions of your components always will be the same size.
But with **Flex dimensions** you can give at your components their size dinamically based on the available space 
for example: 
```javascript
import React from 'react';
import {View} from 'react-native';

export default const app = () => {
  return (
    // This view will use all the available screen
    <View style={{flex: 1>
      <View style={{flex: 1, backgroundColor: 'red'}}/>
      <View style={{flex: 2, backgroundColor: 'blue'}}/>
    </View>
  );
}

```

### Fri 14th, August 2020 *RN.- **Layout with Flexbox***
Flexbox is designed to provide a consistent layout on different screen size. Flexbox works the same way in React Native as it does in CSS on the web, with a few exceptions, for example in React Native `flexDirection` by default is *column* instead of *row*    
- [Flex](https://reactnative.dev/docs/flexbox#flex) with `flex` you can  define how your items are going to fill on the screen in the available space 
  ```javascript
  import React from 'react';
  import {View} from 'react-native';
  
  export default const app = () => {
    return (
      /* This view will use all the available screen. 
      The two views that are inside of this view, their space will be divided according their flex property
      the 1st have 1 and the 2nd have 2.
      This means that the space will be 1 + 2 = 3, the 1st will have 1/3 of the space and the 2nd will have 2/3 of the space*/
      <View style={{flex: 1}}>
        <View style={{flex: 1, backgroundColor: 'red'}}/>
        <View style={{flex: 2, backgroundColor: 'blue'}}/>
      </View>
    );
  }
  ```
- [flexDirection](https://reactnative.dev/docs/flexbox#flex-direction) this property control the direction of the children.
- [justifyContent](https://reactnative.dev/docs/flexbox#justify-content) describe how to align children within the main axis of their container 
- [alignItems](https://reactnative.dev/docs/flexbox#align-items) describe how to align children along the cross acis of their container
- [alignSelf](https://reactnative.dev/docs/flexbox#align-self) the same options and effect as `alignItems` but this property affect a single child instead all the children
- [alignContent](https://reactnative.dev/docs/flexbox#align-content) defines the distribution of lines along the cross-axis. Only affect when the items are wrapped to multiple lines using `flexWrap`
- [flexWrap](https://reactnative.dev/docs/flexbox#flex-wrap) controls what happens when the children overflow the size of the container along the main axis

## Week 5

### Mon 17th, August 2020 *JS.- **Date()***
[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
To create a new Date object:
``` javascript 
    var myDate = new Date([parameters])
```
- myDate will be our `Date` object
- `Date` without `new` returns the expected date in a string representation
- The parameters on the syntax it can be:
        - Nothing: it will create the date and hour of today
        - a string that represent a date in the next form: "Month Day, Year Hour:Minute:second
          ``` javascript 
	    var Xmas95 = new Date("December 25, 1995 13:30:00")
	  ``` 
	  if you omit hour, minute or seconds, the value will be zero 
	- Also you can use integer values 
	  ```javascript
	    var Xmas95 = new Date(1995, 11, 25, 9, 30, 0); // December 25th 1995 9:30:00
	  ```
Check all the methods in [instance methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#) 

### Tues 18th, August 2020 *RN.- **Images***
React Native provides  unified way of managing images and other media assets in your apps.
- To add a static image: 
  ``` javascript 
      <Image source={require('./my-image.png')} /> 
  ```
you could name your images like `my-image.ios.png` `my-image.android.png` and RN the will pick the correct image for the platform.   
All the images require a size (width, height), if the image's size needs to be dynamically, you can use flex propeties. And if you need the image's size static you'll use `width: undefined height: undefined`
- to network image:
  ``` javascript 
      <Image source={{uri: 'https://reactjs.org/logo-og.png'}} style={{width: 400, height: 400}} />
  ```

### Wed 19th, August 2020 *RN.- **Color Reference***
The colors properties usually match how CSS works on the web.
RN support:
- `rbg()` and `rgba()`
- `hsl()` and `hsla()`
- color's name (RN only supports lowercase color names. Uppercase color names aren't supported)  
React Native has several color APIs designed to allow you to take full advantage of your platform's design and user preferences:
- [PlatformColor](https://reactnative.dev/docs/platformcolor)
- [DynamicColorIOS](https://reactnative.dev/docs/dynamiccolorios).
you can check some [color keywords here](https://reactnative.dev/docs/colors#color-keywords)   

### Thur 20th, August 2020 *RN.- **Handling Touches***
The users interact with our apps through touch. RN provide us components to handle that touches, but in this section the most intersted part is the buttons.
We can create a button like this: 
```javascript
  <Button onPress={() => {
    alert('You tapped me ')
    }} 
    title='Press me'
  />
``` 
But you can use more Touchable components to build your own buttons that React Native provide you. Example of these components are: 
- [TouchableHighlight](https://reactnative.dev/docs/touchablehighlight): the view's background will be darkened when the user presses down on the button
- [TouchableNativeFeedback](https://reactnative.dev/docs/touchablenativefeedback): this is on Android to display ink surface reaction ripple that respond to the user's touch
- [TouchableOpacity](https://reactnative.dev/docs/touchableopacity): this will reduce the opacity of the button
- [TouchableWithputFeedback](https://reactnative.dev/docs/touchablewithoutfeedback): don't show something when the user press the button

### Fri 21st, August 2020 *RN.- **Navigating Between Screens***
Almost all the mobile apps manage navigation between screens. You could use the [ReactNavigation](https://reactnavigation.org/) library. This library provides a straightforward navigation solution, with the ability to present common stack navigation and tabbed navigation patterns on both Android and iOS.
But if you'd like to achive a native look and feel on both Android and iOS, or you're integrating React Native into an app that already manages navigation natively, you might need [react-native-navigation](https://github.com/wix/react-native-navigation). 

## Week 6 

### Mon 24th, August 2020 *JS.- **Classes***
The classes are "special function" like the function expression and function declarations. We can create a class using the reserved word `class` and his name:
```javascript
  class Polygon {
    constructor(height, width) {
       this.name = 'Polygon';
       this.height = height;
       this.width = width;
    }
  }
```
The constructor method is a special method to create and start an object created with a
`class`. The constructor can use the reserved word `super` to call the super class's constructor.
With the keyword `extends` we can create a child class from another for example: 
```javascript
  class Polygon {
    constructor(height, width) {
      this.name = 'Polygon';
      this.height = height;
      this.width = width;
    }
  }

  class Square extends Polygon {
    constructor(length) {
      super(length, length);
      this.name = 'Square';
    }
  }	
```

### Tues 25th, August 2020 *RN.- **Animations***
Animations allow us to convey physically believable motion in our interface. React native provides two complementary animation systems: 
	- `Animated`: for granular and interactive control of specific values. It's designed to express a wide variety of interesting animation and interation patterns in a very performant way. `Animated`exports six animatable components types: `View` `Text` `Image` `ScrollView` `Flatlist` and `SectionList`, but we can create our own using `Animated.createAnimatedComponent()`
	- `LayoutAnimation`: allow us to globally configure `create` and `update` animations that will be used for all views in the next render/layout cycle. It is useful for doing `Flexbox` layout updates.

### Wed 26th, August 2020 *React.- **Introducing Hooks***
Hooks are the new addition i React 16.8. With this new feature we can use *States* without writing a `Class`, hooks are also available in React Native since the 0.59 version.
Hooks solve a wide variety of seemingly  unconnected problems in React:
	- Hard to reuse stateful logic between components: React doesn't offer a way to "attach" reusable behavior to component 
	- Complex components become hard to understand: We’ve often had to maintain components that started out simple but grew into an unmanageable mess of stateful logic and side effect 
	- Classes confuse both people and machines: classes can be a large barrier to learning React. You have to understand how `this` works in JavaScript  

### Thur 27th, August 2020 *RN.- **Gesture Responder System*** 
The Gesture Responder System manages the lifecycle of gestures in your app. For example, the app needs to determine if the touch is scrolling, sliding on a widget, or tapping.
##### Best practices:
	- **feedback/highlighting:** show the user what is handling their touch
	- **cancel-ability:** the user should be able to abort it mid-touch by dragging finger away

### Fri 28th, August 2020 *JS.- **NaN** *
NaN is a variable in global scope. His initial value is  Not-A-Numbre. In modern browsers, NaN is non-configurable, non-writable property. There are five different types of operations that return NaN in a program: 
	- Number cannot be parsed (`parseInt('blabla')` or `Number(undefined)`)
	- Math operation if the result isn't a real number (e.g `Math.sqrt(-1)`)
	- Operand of an argument is NaN (`0 * Infinity`)
	- Any operation that involves a stringand isn't an addition operation (`'foo' / 3`)
`NaN` compares unequal (`==`, `!=`, `===`, `!==`) to any other value including to another `NaN` value. Use `Number.isNaN()` or `isNaN()`to most clearly determine if a value is `NaN`

## Week 7

### Mon 31st, August 2020 *React.- **Component State***
`setState()` schedules and update to a component's state object. When the `state` change, the component responds by re-rendering.
#### Differences between `state` and `props`
| `state` | `props` |
| ------- | ------- |
| `state` manage **within** the component (similar to variables declared within a fuction)       |  `props` get passed to the componet (similar to function parameters) |
| The `state` starts with a default value when a component mounts and then suffers from mutations in time | A Component cannot change its `props`|

### Tues 1st, September 2020 *RN.- **Performance Overview***
- JS frame rate (JavaScript thread): 
	- Here your React application will live and all your business logic run here Updates to native-backed views are batched and sent over to the native side at the end of each iteration of the event loop, before the frame deadline (if all goes well). If the JavaScript thread is unresponsive for a frame, it will be considered a dropped frame.
- UI frame rate (main thread): 
	 - Many people have noticed that performance of NavigatorIOS is better out of the box than Navigator. The reason for this is that the animations for the transitions are done entirely on the main thread, and so they are not interrupted by frame drops on the JavaScript thread.

### Wed 2nd, September 2020 *RN.- **RAM Bundles and Inline Requires***
The Random Access Modules (RAM) bundle format is useful for apps that have large number of screens, but generally it is useful to apps that have large amounts of code that aren't needed for a while after startup. 
- Loading JavaScript: Before RN can execute JS code, that code must be loaded into memory and parsed. 
	- for example, in a standard bundle if you load a 50mb bundle, all 50mb must be loaded and parsed before any of it can be executed, but with RAM bundles you can load only the portion of the 50mb that you actually need at startup
- Enable the RAM format: 
	- on iOS: 
		- the RAM format will create a single indexed file that react native will load one module at a time
		- Enable the RAM format in Xcode by editing the build phase "Bundle React Native code and images". Before `../node_modules/react-native/scripts/react-native-xcode.sh` add `export BUNDLE_COMMAND="ram-bundle"`:
		```
		  export BUNDLE_COMMAND="ram-bundle"
		  export NODE_BINARY=node
		  ../node_modules/react-native/scripts/react-native-xcode.sh
		```
	- On Android:
		- the RAM format will create a set of files for each module. But, you can force Android to create a single file, like iOS, but using multiple files can be more performant and requires less memory.
		- Enable the RAM format by editing your `android/app/build.gradle` file. Before the line `apply from: "../../node_modules/react-native/react.gradle"` add or amend the `project.ext.react` block:
		```
		project.ext.react = [
  		   bundleCommand: "ram-bundle",
		]
		```
		- use th following lines if you want to use a single indexed file: 
		```
		project.ext.react = [
  		   bundleCommand: "ram-bundle",
  		   extraPackagerArgs: ["--indexed-ram-bundle"]
		]
		```

### Thur 3rd, September 2020 *RN.- **JavaScript Runtime*** 
Using React Native we're going to be running our JS code in two environments:
- RN will use JavaScriptCore, the JS engine that powers Safari Note that on iOS, JavaScriptCore does not use JIT due to the absence of writable executable memory in iOS apps.
- When using Chrome debugging, all JavaScript code runs within Chrome itself, communicating with native code via WebSockets. Chrome uses V8 as its JavaScript engine.
#### JS Syntax Transformers
Syntax transformers make writing code more enjoyable by allowing you to use new JavaScript syntax without having to wait for support on all interpreters.
React Native ships with the Babel JavaScript compiler. 

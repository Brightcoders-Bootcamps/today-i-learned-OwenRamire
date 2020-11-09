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

### Fri 4th, September 2020 *RN.- **Timers***
Timers are an important part of an application and React Native implements the browser timers.These are some examples of timers: 
- `setTimeout`, `clearTimeout`
- `setInterval`, `celarInterval`
- `setImmediate`, `celarImmediate`
- `requestAnimationFrame`, `cancelAnimationFrame`
#### InteractionManager 
With `InteractionManager` we can make long-running work that it scheduled to start after any interaction/animations have completed. Applications can schedule tasks to run after interactions with the following:
```javascript
  InteractionManager.runAfterInteractions(() => {
    // ...long-running synchronous task...
  });
```

## Week 8

### Mon 7th, September 2020 *RN.- **Using Hermes***
Hermes is an open-source JavaScript engine optimized for running React Native apps on Android. Use Hermes gives us:
- improved start-up time
- decreased memory usage
- snaller app size
To add Hermes, we need at least the RN version 0.60.4. If you don't have it go to [Upgrading to new React Native versions](https://reactnative.dev/docs/upgrading) and then come back here.
The **Windows users** to use Hermes requieres [Microsoft Visual C++ 2015 Redistrubutable](https://www.microsoft.com/en-us/download/details.aspx?id=48145)
Now you have everything, start with
- edit your `android/app/build.grade` like this
  ```
  project.ext.react = [
     entryFile: "index.js",
     // put this line in true
     enableHermes: false
     // like this:
     enableHermes: true // clean and rebuild if changing
  ]
  ```
- if you are using ProGuard, you'll need to add these rules in `proguard-rules.pro`:
  ```
  -keep class com.facebook.hermes.unicode.** { *; }
  -keep class com.facebook.jni.** { *; }
  ```
- if you've already build your app at least once, clean the build: 
  `$ cd android && ./gradlew clean`
  and **that's it** you can run your app as normal.

### Tues 8th, September 2020 *RN.-**Connectivity(Networking)***
You might need to make a POST request to a REST API or may need to fetch a chunk of static content from another server in your app.
React Native provides the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) for your networking needs. 
This is an example using fetch in RN:
```javascript
import React, { useEffect, useState } from 'react';
import { ActivityIndicator, FlatList, Text, View } from 'react-native';

export default App = () => {
  const [isLoading, setLoading] = useState(true);
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('https://reactnative.dev/movies.json')
      .then((response) => response.json())
      .then((json) => setData(json.movies))
      .catch((error) => console.error(error))
      .finally(() => setLoading(false));
  }, []);

  return (
    <View style={{ flex: 1, padding: 24 }}>
      {isLoading ? <ActivityIndicator/> : (
        <FlatList
          data={data}
          keyExtractor={({ id }, index) => id}
          renderItem={({ item }) => (
            <Text>{item.title}, {item.releaseYear}</Text>
          )}
        />
      )}
    </View>
  );
};

```
Also if you don't want to use `fetch` you could use third party libraries like [frisbee](https://github.com/niftylettuce/frisbee) or [axios](https://github.com/axios/axios), also you can use the `XMLHttpRequest API` directly:
```javascript
var request = new XMLHttpRequest();
request.onreadystatechange = (e) => {
  if (request.readyState !== 4) {
    return;
  }

  if (request.status === 200) {
    console.log('success', request.responseText);
  } else {
    console.warn('error');
  }
};

request.open('GET', 'https://mywebsite.com/endpoint/');
request.send();
```

### Wed 09th, September 2020 *RN.- **Security***
It is impossible to build software that is completely impenetrable. So, we need to know about the best practices for storing sensitive information, authentication, network security and tools that will help us secure our app.
#### Storing Sensitive Info:
- **Never store sensitive API keys** in your app code. If you must have an API key or a secret to access some resource from your app, the most secure way to handle this would be to build an orchestration layer between your app and the resource.
#### Async Storage 
- is a community-maintained module for React Native that provides an asynchronous, unencrypted, key-value store. Async Storage is not shared between apps.
	- Async Storage is the React Native equivalent of Local Storage from the web
#### Secure Storage
- React Native does not come bundled with any way of storing sensitive data. However, there are pre-existing solutions for Android and iOS platforms like:
	- **iOS - Keychain Services**
	- **Android - Secure Shared Preferences**
	- **Android - Keystore**
### Thur 10th, September 2020 *RN.- **Native Module Setup***
Native modules are usually distributed as npm packages, except that on top of the usual Javascript they will include some native code per platform.
To get set up with the basic project structure for a native module we will use the community tool called [Bob](https://github.com/react-native-community/bob). We will execute the basic `create` script:
`npx @react-native-community/bob create react-native-awesome-module
`

### Fri 11th, September 2020 *React.- **Hooks at a glance***
Hooks are functions that let us "hook into" React state and lifecycle feature from function components, this feature doesn't work with the class components. React provides a few built-in Hooks like useState: 
```javascript
// a function component using the state feature with Hooks:
import React, {useState} from 'react';

export default function App() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);
  // you can create all the Hooks that you need
  return (
     <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

// a class component using state: 
import React from 'react';

export default class App() extends React.Component {
  constructor(props) {
     super(props);
     this.state = {
        count: 0,
     };
  }
  render () {
     return (
        <div>
           <p>You clicked {this.state.count} times</p>
           <button onClick={() => this.setState({this.state.count + 1})}>
              Click me
           </button>
        </div>
     );
  }
}
```
You’ve likely performed data fetching, subscriptions, or manually changing the DOM from React components before. We call these operations “side effects” (or “effects” for short) because they can affect other components and can’t be done during rendering.
The Effect Hook, `useEffect`, adds the ability to perform side effects from a function component. It serves the same purpose as `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` in React classes, but unified into a single API.
```javascript
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```
using the Hook `useEffect` you are telling React to run your "effect" function after flushing changes to the DOM. By default React runs the effects after every render, including the first render.
#### Rules of Hooks
Hooks are JS functions but they impose two additional rules:
- Only call them **at the top level**. Don't call them inside loops, conditions, or nested functions.
- only call them in **React function commponents**. Don't call them in regular JS functions

## Week 9

### Mon 14th, September 2020 *React.- Using the State Hook*
```javascript
function Example(props) {
   return <div />;
}
// -------------
const Example = (props) => {
   return <div />; 
}
```
this two example of a function component in React.But, theses components are "stateless components" because we can't use `states` in a function component. Here is where Hooks can work.
Hooks is a special function that let us "hook into" React feature. For example if we want to use `state` in a function component, the `useState` Hook will help us to use the `state` in our component without a class. This is an advantage because we don't have to rewrite our function component into a class component.
If we want a counter using states, in a class component it'll be like this:
```javascript
import React, {Component} from 'react';

class Example extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }
```
In a function component, we have no `this`, so we can’t assign or read `this.state`. Instead, we call the useState Hook directly inside our component:
```javascript
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);
  // This is similar to this.state.count and this.setState in a class
```
`useState` is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.
If we want to read the current state: 
```javascript
// instead to use:
<p> the value of the count is {this.state.count} </p>

// we just call the variable count
<p> the value of the count is {count} </p>
```
And is we want to update the state:
```javascript
 // instead to use: 
 <button onClick={() => this.setState({ count: this.state.count + 1 })}>
    Click me
  </button>

  // we use 
  <button onClick={() => setCount(count + 1)}>
    Click me
  </button>
```

### Tues 15th, September 2020 *React.- Using the Effect Hook*
The Effect Hook lets you perform side effects in function components.
Data fetching, setting up a subscription, and manually changing the DOM in React components are all examples of side effects.
There are two common kinds of side effects in React components: those that don’t require cleanup, and those that do.
Effect without cleanup: run some additional code after React has updated the DOM. Examples of this effects are network requests, manual DOM mutations and logging. 
**Example using classes:** 
```javascript
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }
  /* 
   *  we want to perform the same side effect regardless of whether the component
   *  just mounted, or if it has been updated
  */
  componentDidMount() {
    document.title = `You clicked ${this.state.count} times`;
  }
  componentDidUpdate() {
    document.title = `You clicked ${this.state.count} times`;
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```
**Example using Hooks:**
```javascript
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);
  
  /*
    using this Hook, we tell React that our component needs to do something after render.
  */
  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

### Wed 16th, Septermber 2020 *React.- Rules of Hook*
Hooks are JS functions, but we need to follow two rules when using them.
- Only call them at the top level: don´t call Hooks inside loops, conditions or nested functions. 
- Only call them from React Functions: don't call Hooks from regular JS functions. Instead:
	- call Hooks from React function components
	- call Hooks from custom Hooks
We have a plugin called [eslint-plugin-react-hooks](https://www.npmjs.com/package/eslint-plugin-react-hooks) that enforces these two rules.

### Thur 17th, September 2020 *React.- Building your own Hooks*
Building our own Hooks lets us extract component logic into reusable functions. Imagine that we have a component from a chat application that displays a message indicating if a friend is online or offline:
```javascript
import React, { useState, useEffect } from 'react';

function FriendStatus(props) {
  const [isOnline, setIsOnline] = useState(null);
  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });

  if (isOnline === null) {
    return 'Loading...';
  }
  return isOnline ? 'Online' : 'Offline';
}
```
Now let’s say that our chat application also has a contact list, and we want to render names of online users with a green color. We could copy and paste similar logic above into our FriendListItem component but it wouldn’t be ideal
```javascript
import React, { useState, useEffect } from 'react';

function FriendListItem(props) {
  const [isOnline, setIsOnline] = useState(null);
  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });

  return (
    <li style={{ color: isOnline ? 'green' : 'black' }}>
      {props.friend.name}
    </li>
  );
}
```
When we want to share logic between two JS function, we extract it to a third function. A custom Hook is a JavaScript function whose name starts with **”use”** and that may call other Hooks. Taken the example of the chat we can create our first custom Hook like `useFriendStatus`
```javascript
import { useState, useEffect } from 'react';

function useFriendStatus(friendID) {
  const [isOnline, setIsOnline] = useState(null);

  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }

    ChatAPI.subscribeToFriendStatus(friendID, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(friendID, handleStatusChange);
    };
  });

  return isOnline;
}
```
The purpose of our `useFriendStatus` Hook is to subscribeus to a friend's status. And now we can use it like this: 
```javascript

function FriendStatus(props) {
  // we call our new Hook and storage into a constant
  const isOnline = useFriendStatus(props.friend.id);

  if (isOnline === null) {
    return 'Loading...';
  }
  return isOnline ? 'Online' : 'Offline';
}


function FriendListItem(props) {
  const isOnline = useFriendStatus(props.friend.id);

  return (
    <li style={{ color: isOnline ? 'green' : 'black' }}>
      {props.friend.name}
    </li>
  );
}
```
 All we did was to extract some common code between two functions into a separate function.

## Week 10

### Mon 21st, September 2020 *RN.- Direct Manipulation*
When we need to make changes directly to a component without using `state`/`props` to trigger a re-render of the entire subtree. For example, using React in the browser we sometimes need to directly modify a DOM node and the same is true for views in mobile apps. `setNativeProps`is the *React Native* equivalent to setting properties directly on a DOM node.
**NOTE:** Use setNativeProps when frequent re-rendering creates a performance bottleneck.
We will typically only be using it for creating continuous animations to avoid the overhead of rendering the component hierarchy and reconciling many views. 
Example of `setNativeProps` with TouchableOpacity component:
```javascript
/*
We'll use setNativeProps to update the opacity of its child component
*/
setOpacityTo(value) {
  // Redacted: animation related code
  this.refs[CHILD_REF].setNativeProps({
    opacity: value
  });
},
```
This allows us to write the following code and know that the child will have its opacity updated in response to taps, without the child having any knowledge of that fact or requiring any changes to its implementation:
```javascript 
<TouchableOpacity onPress={this._handlePress}>
  <View style={styles.button}>
    <Text>Press me!</Text>
  </View>
</TouchableOpacity>
```
If `setNativeProps` wasn't available, one way to do the changes might be store the opacity value in the state and then update the state whenever `onPress` is fired:
```javascript 
constructor(props) {
  super(props);
  this.state = {
     myButtonOpacity: 1,
  };
}

render() {
  return (
    <TouchableOpacity onPress={() => this.setState({myButtonOpacity: 0.5})}
                      onPressOut={() => this.setState({myButtonOpacity: 1})}>
      <View style={[styles.button, {opacity: this.state.myButtonOpacity}]}>
        <Text>Press me!</Text>
      </View>
    </TouchableOpacity>
  )
}
```
In that example React needs to re-render the component hierarchy each time the opacity changes, even though other properties of the view and its children haven't changed. Usually this overhead isn't a concern but when performing continuous animations and responding to gestures, judiciously optimizing your components can improve your animations' fidelity.

### Tues 22nd, September 2020 *JavaScript.- Regular expressions*
Regular expressions are patterns used to match character combinations in strings. Also In JavaScript, regular expressions are also objects.
We can use these patterns with 
- the methods of `RegExp`: 
	- `exec()`
	- `test()`
- the methods of `String`:
	- `replace()`
	- `replaceAll()`
	- `search()`
	- `split()`
How can we create a regular expression? There are two ways: 
- using regular expression literal. which consists of a pattern enclosed between slashes:
  ```javascript
  /*
    With this pattern will matches character combinations in strings
    only when the exact sequence "abc" occurs
  */
  let re = /abc/;
  ```
	- Regular expression literals provide compilation of the regular expression when the script is loaded.
	- If the regular expression remains constant, using this can improve performance.
- calling the constructor function of the `RegExp` object:
  ```javascript
  let re = new RegExp('abc');
  ```
	- Using the constructor provides runtime ompilation of the regular expression.  
	- Use it when you know the regular expression pattern will be changing, or you don't know the pattern and are getting it from another source
##### using special characters
for example if we want to find one or more "b" or find white spaces in the last example. We can include special characters in the pattern. For example, match a single "a" followed by **zero** or **more** "b" followed by "c", we'd use the pattern `/ab*c/`, with the `*` we're saying that "0 or more occurrences of the preciding item", in this case the string "cdd**abbbbc**debc" will match 

### Wed 23th, September 2020 *JavaScript.- this*
The value of `this` is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called.
```javascript
const test = {
   props: 42,
   func: function() {
      return this.props;
   },
}

console.log(test.func());
// expected output: 42
```
- **value:** A property of an execution context (global, function or eval) that, is always a reference to an object and in strict mode can be any value.
	- *Global context (outside of any function):* `this` refers to the global object whether in strict mode or not.
	```javascript
	// In the browser, the window object is also the global object
	console.log(this === window); // the output will be true

	this.b = 'Hello world';
	console.log(window.b)
	// the output will be Hello world

	/*
	   We can easily get the global object using the global 'globalThis' property 
	*/
	```
	- *Function context (inside a function):* the value depends on how the function is called.
	```javascript
	/*
	in the example is not in strict mode, so, 'this' will be default to the global object (a.k.a the window ina browser)
	*/
	function myFunction(){
	   return this;
	}

	myFunction() === window; // true

	/*
	In strict mode, however, if the value of this is not set when entering an execution context, it remains as undefined, as shown in the following example:
	*/
	
	function f2() {
  	   'use strict'; // see strict mode
  	   return this;
	}
	
	f2() === undefined; // true
	```
	- *Class context:* it is similar as the function, just there are some differences and caveats. Within a class constructor, `this` is a regular object. All non-static methods within the class are added to th prototype of `this`

### Thur 24th, September 2020 *JavaScript.- Spread syntax*
The spread syntax (`...`) allows an iterable such as an array expression or string to be expanded in places where zero or more arguments or elements are expected, or object expression to be expanded in places where zero or more key-value pairs are expected.
The spread syntax:
- function calls: `myFunction(...iterableObj);`
- array literals or strings: `[...iterableObj, '4', 'five', 6];`
- object literals (new in ECMAScript 2018): `let objClone: {...obj};`
```javascript
function sum(a, b, c){
   return a + b + c; 
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expect output: 6


// any argument in the argument list can use spread syntax, and the spread syntax can be used multiple times

function myFunc(){ }

const args = [0, 1];

myFunc(-1, ...arg, 2, ...[3]);
```

### Fri 25th, September 2020 JavaScript.- RegExp
The RegExp is an object, is used for matching text with a pattern
There are two ways to create a RegExp object:
- **literal notation:** function's parameters are enclosed between slashes and do not use quotation marks `let re = /ab+c/i;`
- **constructor:** function's parameters are not enclosed between slashes but do use quotation marks 
```javascript
   let re = new RegExp('ab+c', 'i'); // Constructor with string pattern as first argument

   let re = new RegExp(/ab+c/, 'i'); // Constructor with regular expresion literal as first argument (starting with ECMAScript 6);

   // with new RegExp(/ab+c/, 'i') the first argument is a RegExp and the second is the flag
```

## Week 11

### Mon 28th, September 2020 RN.- Guides (android): Native Modules
If React Native doesn't have a corresponding module that we need to access to a platform API. Maybe we want to reuse some existing Java code without having to reimplement it in JavaScript, or write some high performance. 
With React Native is possible to write real native code and have access to the fullpower of the platform. If React Native doesn't support a native feature that we need, we should be able to build it ourself.
The native modules are usually distributed as npm package, apart from the typical javascript files and resources they will contain an Android library project. 

### Tues 29th, September 2020 JS.- Array.prototype.some()
the `some()` method check if at least one element of the array have the condition that you give it. Let's see an example: 
```javascript
const myArray = [1, 2, 3, 4, 5];

const isEven = myArray.some((element) => element % 2 === 0);
console.log(isEven);

// We expected output: true. Because 2 and 4 are even

```
`some()` runs a `callback` function once for every element on the array until finding an element that returns `true`. If the function find an element, it will return `true` immediately, but if not it will return `false` 

### Wed 30th, September 2020 JS.- Array.prototype.map()
The `map()` method *creates a new array* with the result of calling a provided function on every element
```javascript
const array = [1, 4, 9, 16];

const map = array.map((element) => element * 2)

console.log(map) // expected output: [2, 8, 18, 32]
```
`map` calls a `callback` function once for each element in an array, in order, and constructs a new array from the results.
We shouldn't use `map()` if:
- We're not using the array it returns; and/or
- We're not returning a value from the callback

### Thur 1st, October 2020 RN.- Headless JS
Headless JS is a way to run tasks in JavaScript while your app is in the background. It can be used, for example, to sync fresh data, handle push notifications, or play music.
This task is a async function that we register on `AppRegistry`, similar to registering React applications: 
```javascript
import {AppRegistry} from 'react-native';
AppRegistry.registerHeadlessTask('SomeTaskName', () =>
   require('SomeTaskName');
);
```
Then, int `SomeTaskName.js`: 
```javascript 
module.exports = async (taskData) => {
   // do stuff 
}; 
```
After all of this, we can do anything in your task such as network requests, timers and so on, as long as it doesn't touch UI.

### Fri 2nd, October 2020 *RN.- Publishing to Google Play Store*
Android requires that all apps be digitally signed with a certificate before they can be installed. To distribute our Android application via Google Play it needs to be signed with a release key that then needs to be used for all future updates. Before that our application binary is uploaded to Gooogle Play it needs to be signed with an upload key. If we want to know more about this go to [Sign your app](https://developer.android.com/studio/publish/app-signing) on the Android Developers documentation.
We can generate a private signing key using `keytool`. On Windows must be run from `C:\Program Files\Java\jdkx.x.x_x\bin`.
This command:
- `$ keytool -genkeypair -v -keystore my-upload-key.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000`
prompts you for passwords for the keystore and key and for the Distinguished Name fields for your key. It then generates the keystore as a file called `my-upload-key.keystore`.
On Mac, if you don't know where your JDK bin folderis, run this command to find it:
- `$ /usr/libexec/java_home`
After that the output of that command will be the directory of the JDK, which will look like this:
- `/Library/Java/JavaVirtualMachines/jdkX.X.X_XXX.jdk/Contents/Home`
after that move into that directory and use the keytool command with sudo permission like this:
- `$ sudo keytool -genkey -v -keystore my-upload-key.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000`
**Remember to keep the keystore file private.**
When you have your the key, now we need to setting up gradle.
1. Place the `my-upload-key.keystore` file under the `android/app` directory in your proyect.
2. Edit `~/gradle/gradle.properties` or `android/gradle.properties` and all the following:
```
MYAPP_UPLOAD_STORE_FILE=my-upload-key.keystore
MYAPP_UPLOAD_KEY_ALIAS=my-key-alias
MYAPP_UPLOAD_STORE_PASSWORD=*****
MYAPP_UPLOAD_KEY_PASSWORD=*****
```
These are going to be global Gradle variables, which we can later use in our Gradle config to sign our app.
The last configuration step that need to be done is to setup release builds to be signed using upload key. Edit the file `android/app/build.gradle` and add the signing config:
```
...
android {
    ...
    defaultConfig { ... }
    signingConfigs {
        release {
            if (project.hasProperty('MYAPP_UPLOAD_STORE_FILE')) {
                storeFile file(MYAPP_UPLOAD_STORE_FILE)
                storePassword MYAPP_UPLOAD_STORE_PASSWORD
                keyAlias MYAPP_UPLOAD_KEY_ALIAS
                keyPassword MYAPP_UPLOAD_KEY_PASSWORD
            }
        }
    }
    buildTypes {
        release {
            ...
            signingConfig signingConfigs.release
        }
    }
}
...
```
Now run in your terminal:
```
$ cd android
$ ./gradlew bundleRelease
```
Gradle's `bundleRelease` will bundle all the JavaScript needed to run your app into the AAB (Android App Bundle).
Before uploading the release build to the Play Store, make sure you test it thoroughly. First uninstall any previous version of the app you already have installed. Install it on the device using the following command in the project root:
- `$ npx react-native run-android --variant=release`
Note that --variant=release is only available if you've set up signing as described above.

## Week 12

### Mon 5th, October 2020 RN.- Default Permissions
By default, some permissions are added to your Android APK, and they are:
- android.permission.INTERNET -Required fot debug mode.
- android.permission.SYSTEM_ALERT_WINDOW - Required for debug mode.
- android.permission.READ_PHONE_STATE - Not required for debug or production.
- android.permission.WRITE_EXTERNAL_STORAGE - Not require for debug or production.
- android.permission.READ_EXTERNAL_STORAGE - Not required for debug or production.
In this case, we are going to start by removing *READ_PHONE_STATE*, *WRITE_EXTERNAL_STORAGE0*, and *READ_EXTERNAL_STORAGE* from both production and debug APKs as it is not required in either.
1. open the `android/app/src/main/AndroidManifest.xml` file
2. Even though these three permissions are not listed in the manifest they get added in. We add the three permissions with tools:node="remove" attribute.
```
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.myappid"
+   xmlns:tools="http://schemas.android.com/tools"
    >

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW" />
+   <uses-permission tools:node="remove" android:name="android.permission.READ_PHONE_STATE" />
+   <uses-permission tools:node="remove" android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
+   <uses-permission tools:node="remove" android:name="android.permission.READ_EXTERNAL_STORAGE" />

    <application
      android:name=".MainApplication"
      android:label="@string/app_name"
      android:icon="@mipmap/ic_launcher"
      android:allowBackup="false"
      android:theme="@style/AppTheme">
      <activity
        android:name=".MainActivity"
        android:label="@string/app_name"
        android:configChanges="keyboard|keyboardHidden|orientation|screenSize"
        android:windowSoftInputMode="adjustResize">
        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
      </activity>
      <activity android:name="com.facebook.react.devsupport.DevSettingsActivity" />
    </application>

</manifest>
```

### Tues 6th, October 2020 RN.- Native Modules (iOS)
If React Native doesn't have a module to access a platform API yet. You could reuse some existing Objective-C, Swift or C++ code without using JavaScript. React Native is design also to write real native code to have full power of the platform. 
The native modules are usually distributed as npm packages, except for the native modules that contain Xcode.
In React Native documentation we can find an example using the iOS Calendar Module

### Wed 7th, October 2020 RN.- Native UI Components (iOS)
There are tons of native UI widgets out there ready to be used in the latest apps, some of them are part of the platform and others are available as third-party libraries. React Native has the most critical platform component like "ScrollView" and "TextInput", but RN doesn't have all of them. Fortunately, we can wrap up these existing components for seamless integration with your RN application. 
This part is more advanced, because we assume that you're somewhat familiar with iOS programming . 
[Go here to watch an example with iOS MapView](https://reactnative.dev/docs/native-components-ios#ios-mapview-example)

### Thur 8th, October 2020 RN.- Linking Libraries
Not every app uses all the native capabilities, and including the code to support all those feature would impact the binary size. With that in mind, RN exposed many of these features as idependent static libraries.
Most of the libs it'll be as quick as dragging two files, sometimes a third step will be necessary.
All those Libraries you can find on the [Libraries](https://github.com/facebook/react-native/tree/master/Libraries) on the React Native repository.
You decide how do you want to link the library that you need:
- [Automatic Linking](https://reactnative.dev/docs/linking-libraries-ios#automatic-linking)
- [Manual Linking](https://reactnative.dev/docs/linking-libraries-ios#manual-linking)

### Fri 9th, October 2020 RN.- Running on Simulator(iOS)
When you create a React Native project and run it with `$ npx react-native run-ios` you will see the *iPhone 11* by default. But if you want it  you can change the simulator, to do it, just use the `--simulator` flag and then the device like:
`$ npx react-native run-ios --simulator="iPhne SE"`
The device names correspond to the list of devices available in Xcode. You can check it running this command on the console `$ xcrun simctl list devices`

## Week 13

### Mon 12th, October 2020 RN.- App Extensions (iOS)
App extensions let you provide custom functionality and content outside of your main app. There are different types of this extentios and you can check it [here](https://developer.apple.com/library/archive/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
- **Memory use in extensions:**  these extensions have small memory usage limits. It's always highly recommended to test your application on an actual device, and more so when developing app extensions: too frequently, developers find that their extension works fine in the iOS Simulator, only to get user reports that their extension is not loading on actual devices.
- **Today widget:** Today widget implementations using React Native may work unreliably because the memory usage tends to be too high. You can tell if your Today widget is exceeding the memory limit if it yields the message 'Unable to Load'

### Tues 13th, October 2020 JS.- async function
An async function is a function declared with the `async` keyword. This functions are instances of the `AsyncFunction` constructor, and the `await` keyword is permitted within them. The `async` and `await` keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.
Example:
```javascript
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

async function asyncCall() {
  console.log('calling');
  const result = await resolveAfter2Seconds(); 
  // the constant result will wait what the resolveAfter2Seconds function will return us and then will continue with the next line of code
  console.log(result);
  // expected output: "resolved"
}

asyncCall();
```
The async functions can contain zero or more `await` expressions. Await expressions **suspend progress through an async function, yielding control and subsequently resuming progress**  

**NOTE:** The `await` keyword is only valid **inside async functions**. If you use it outside of an async function's body, you will get a `SyntaxError`

### Wed 14th, October 2020 JS.- ArrayBuffer
The ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. It is an array of bytes, often referred to in other languages as a "byte array".
You cannot directly manipulate the contents of an ArrayBuffer; instead, you create one of the typed array objects or a DataView object which represents the buffer in a specific format, and use that to read and write the contents of the buffer.

### Thur 15th, October 2020 JS.- SharedArrayBuffer
The SharedArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer, similar to the ArrayBuffer object, but in a way that they can be used to create views on shared memory. 
To share memory using SharedArrayBuffer objects from one agent in the cluster to another, , postMessage and structured cloning is used.  The SharedArrayBuffer object is transmitted to the receiver resulting in a new, private SharedArrayBuffer object in the receiving agent.

### Fri 16th, October 2020 JS.- JSON
The **JSON** object contains methods for parsing JavaScript Object Notation (JSON) and converting values to JSON.
JSON is a syntax for serializing objects, arrays, numbers, strings, booleans, and null. It is based upon JavaScript syntax but is distinct from it: some JavaScript is not JSON.
##### Static methods
- **JSON.parse(text[, reviver])** -> parse the string *text* as JSON, optionally transform the produed value and its properties, and return the value. 
- **JSON.stringify(value[, replacer[, space]])** -> return a *JSON string* corresponding to the speified value, optionally including only certain properties or replacing property values in  a user-defined manner.

## Week 14

### Mon 19th, October 2020 React.- Handling Events
Handling events with React elements is very similar to handling events on DOM elements. The differences are: 
- React events are named using camelCase
- With JSX you pass a function as the event handler, rather than a string
example: 
- With HTML: 
```javascript
<button onclick="activateLasers()">
   Activate Lasers
</button>
```
- With React:
```javascript
<button onClick={activateLasers}>
   Activate Lasers
</button>
```
When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.
When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class.
```javascript
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState(state => ({
      isToggleOn: !state.isToggleOn
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}

ReactDOM.render(
  <Toggle />,
  document.getElementById('root')
);
```
Be careful about the meaning of `this` in JSX callbacks. In JS, class methods are not bound by default. If you forget to bind `this.handleClick` and pass it to `onClick`, `this` will be `undefined` then the function is actually called.
Generally, if you refer to a method without () after it, such as `onClick={this.handleClick}`, you should bind that method.

### Tues 20th, October 2020 React.- Conditional Rendering
Working with React, you can create distinct components that encapsulate behavior you need. So, you canrender only some of them depending of your application's state.
It works at the same way conditions in JavaScript like `if` or `conditional operator`. With that in mind let's see this example:
```javascript
function UserGreeting(props) {
   return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
   return <h1>Please sign up.</h1>;
}

/*
We’ll create a Greeting component that displays either of these components depending on whether a user is logged in
*/

function Greeting(props) {
   const isLoggedIn = props.isLoggedIn;
   if(isLoggedIn) {
      return <UserGreeting />
   }
   return <GuestGreeting />
}
```
We can change a little the component Greeting using conditional operator that it will be the same:
```javascript
function Greeting(props) {
   const isLoggedIn = props.isLoggedIn;
   return isLoggedIn ? <UserGreeting /> : <GuestGreeting />;
}
```

And if you want you can use variables to store elements. This can help you conditionally render a part of the component while the rest of the output doesn’t change.

### Wed 21st, October 2020 React.- List and Keys
Let's review how yo transform list in JS. We use the `map()` function to double thier values:
```javascript
const numbers = [1,2,3,4,5];
const double = numbers.map((number) => number * 2);
console.log(double); // the output will be = [2, 4, 5, 6, 8, 10];
```
In React, transforming arrays into list of elements is nearly identical. We can build collections of elements and include them in JSX using `{}`.
So, now we loop through the `numbers` array using `map()` and return a `<li>` element:
```javascript
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) => <li>{number}</li>);

// We will see the list of numbers on the browser
ReactDOM.render(
   <ul>{listItems}</ul>,
   document.getElementById('root')
);
```

We usually would render lists inside a component:
```javascript
function NumberList(props) {
   const  {numbers} = props;
   const listItems = numbers.map((number) => {
	<li>{number}</li>;
   });
   return <ul>{listItems}</ul>;
}

const numbers = [1, 2, 3, 4, 5];

ReactDOM.render(
   <NumberList numbers={numbers} />,
   document.getElementById('root');
);

```
After run this code, you'll be given a **WARNING** that a key should be provided for list items. To prevent this **warning**, we need a *key*.
This `key` help React identify which items hace changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity: 
```javascript
const numbers = [1, 2, 3, 4, 5];

const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
); 
/*The best way to pick a key is to use a string that uniquely identifies a list item among its sibling*/
```

### Thur 22nd, October 2020 React.- Forms
HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.
```
<form>
   <label>
      Name: 
      <input type="text" name="name" />
   </label>
   <input type="submit" value="Submit" />
</form>
```
The next form has the default HTML form behavior of browsing to a new page when the user submits the form. It's convenient to have a JS function that handles the submission of the form and access to the data that the user entered into the form.
The standard way to achieve this is with a technique called "controlled components".
In  HTML, form elements such as `<input>`, `<textarea>`, and `<select>` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components and only updated with `setState()`.
We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.
For example, if we want to make the previous example log the name when it is submitted, we can write the form as a controlled component: 
```javascript
class NameForm extends React.Component {
   constructor(props){
      super(props);
      this.state = {
         value: '',
      };
      this.handleChange = this.handleChange.bind(this);
      this.handleSubmit.bind(this);
   }

   handleChange(event) {
      this.setState({value: event.target.value});
   }
   
   handleSubmit(event) {
      alert(`A name was submitted: ${this.state.value}`);
      event.preventDefault();
   }

   render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

### Fri 23rd, October 2020 React.- Lifting State Up
Often, several components need to reflect the same changing data. We recommend lfting the shared state up to their closest common ancestor. Let's see how this works in action.
we will create a temperature calculator that calculates whether the water would boil at a given temperature.
We will start with a component called BoilingVerdict. It accepts the celsius temperature as a prop, and prints whether it is enough to boil the water:
```javascript
function BoilingVerdict(props) {
  if (props.celsius >= 100) {
    return <p>The water would boil.</p>;
  }
  return <p>The water would not boil.</p>;
}
```
we will create a component called `Calculator`. It renders an `<input>` that lets you enter the temperature, and keeps its value in this.state.temperature. It renders the BoilingVerdict for the current input value.
```javascript
class Calculator extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
    this.state = {temperature: ''};
  }

  handleChange(e) {
    this.setState({temperature: e.target.value});
  }

  render() {
    const temperature = this.state.temperature;
    return (
      <fieldset>
        <legend>Enter temperature in Celsius:</legend>
        <input
          value={temperature}
          onChange={this.handleChange} />
        <BoilingVerdict
          celsius={parseFloat(temperature)} />
      </fieldset>
    );
  }
}
```
Our new requirement is that, in addition to a Celsius input, we provide a Fahrenheit input, and they are kept in sync.
We can start by extracting a TemperatureInput component from Calculator. We will add a new scale prop to it that can either be "c" or "f":
```javascript
const scaleNames = {
  c: 'Celsius',
  f: 'Fahrenheit'
};

class TemperatureInput extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
    this.state = {temperature: ''};
  }

  handleChange(e) {
    this.setState({temperature: e.target.value});
  }

  render() {
    const temperature = this.state.temperature;
    const scale = this.props.scale;
    return (
      <fieldset>
        <legend>Enter temperature in {scaleNames[scale]}:</legend>
        <input value={temperature}
               onChange={this.handleChange} />
      </fieldset>
    );
  }
}

/*
Now change the Calculator component to render two temperture inputs
*/

class Calculator extends React.Component {
   render() {
      return (
         <div>
	    <TempertureInput scale="c" />
	    <TempertureInput scale="f" />
	 </div>
      );
   } 
}
```
We have two inputs now, but when you enter the temperature in one of them, the other doesn’t update. And we want to keep them in sync.
Also we can't display the `BoilingVerdict` from `Calculator`. The `Calculator` doesn't know the current temperture because it is hidden inside the `TempertureInput`.

We nedd to write two functions to convert Celsius to Fahrenheit and back:
```javascript
const toCelsius = (fahrenheit) => return (fahrenheit - 32) * 5 / 9;

const toFahrenheit = (celsius) => return (celsius * 9 / 5) + 32;

/*
Next we need another function that takes a string temperature and a converter
function as arguments and returns a string.
*/

const tryConvert = (temperture, convert) => {
   const input = parseFloat(temperture);
   if (Number.isNaN(input)){
      return '';
   }
   const output = convert(input);
   const rounded = Math.round(output * 1000) / 1000;
   return rounded.toString();
};

tryConvert('abc', toCelsius); // return an empty string
tryConvert('10.22', toFahrenheit); // return '50.396'
```
The `TemperatureInput` components independently keep their values in the local state, and we want these inputs in sync with each other.
In React, sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called ****Lifting state up***. We will remove the local state from the TemperatureInput and move it into the `Calculator` instead.

If the Calculator owns the shared state, it becomes the “source of truth” for the current temperature in both inputs. It can instruct them both to have values that are consistent with each other. Since the props of both `TemperatureInput` components are coming from the same parent `Calculator` component, the two inputs **will always be in sync**.

We need to replace `this.state.temperture` with `this.props.temperture` in the `TempertureInput` component.
```javascript
// on TempertureInput
render() {
   const temperture = this.props.temperture;
}
```
Keep in mind that props **are read-only**, so we can't call `this.setState()` because the temperture that we receive is in props. But in React this is solved by making a component "controlled". Just like the DOM `<input>` accepts both a `value` and an `onChange` props, so can the custom TemperatureInput accept both temperature and onTemperatureChange props from its parent `Calculator`.
Now when the `TempertureInput` wants to update its temperture, it calls `this.props.onTempertureChange`:
```javascript
handleChange(e) {
   // BEFORE: this.setState({temperature: e.target.value});
   this.props.onTempertureChange(e.target.value);
   /*
   It will handle the change by modifying its own local state,
   thus re-rendering both inputs with the new values.
   */
}

/* 
   -------------------- 
   Now the TemperatureInput component looks like this:
*/

class TemperatureInput extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e) {
    this.props.onTemperatureChange(e.target.value);
  }

  render() {
    const temperature = this.props.temperature;
    const scale = this.props.scale;
    return (
      <fieldset>
        <legend>Enter temperature in {scaleNames[scale]}:</legend>
        <input value={temperature}
               onChange={this.handleChange} />
      </fieldset>
    );
  }
}
```
Next let's turn to `Calculator` component.
We will store the current input’s temperature and scale in its local state. This is the state we “lifted up” from the inputs, and it will serve as the “source of truth” for both of them. It is the minimal representation of all the data we need to know in order to render both inputs.

```javascript
class Calculator extends React.Component {
  constructor(props) {
    super(props);
    this.handleCelsiusChange = this.handleCelsiusChange.bind(this);
    this.handleFahrenheitChange = this.handleFahrenheitChange.bind(this);
    this.state = {temperature: '', scale: 'c'};
  }

  handleCelsiusChange(temperature) {
    this.setState({scale: 'c', temperature}); // Modify the state when the user type on the celsius' input
  }

  handleFahrenheitChange(temperature) {
    this.setState({scale: 'f', temperature}); // Modify the state when the user type on the fahrenheit's input
  }

  render() {
    const scale = this.state.scale;
    const temperature = this.state.temperature;
    /*
    With the celsius and fahrenheit constants, we check if we need to convert the values   
    */
    const celsius = scale === 'f' ? tryConvert(temperature, toCelsius) : temperature;
    const fahrenheit = scale === 'c' ? tryConvert(temperature, toFahrenheit) : temperature;

    return (
      <div>
        <TemperatureInput
          scale="c"
          temperature={celsius}
          onTemperatureChange={this.handleCelsiusChange} />
        <TemperatureInput
          scale="f"
          temperature={fahrenheit}
          onTemperatureChange={this.handleFahrenheitChange} />
        <BoilingVerdict
          celsius={parseFloat(celsius)} />
      </div>
    );
  }
}
```

## Week 15

### Mon 26th, October 2020 React.- Composition vs Inheritance
React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.
We will consider a few problems where developers new to React often reach for inheritance, and show how we can solve them with composition.
##### Containment
Some components don’t know their children ahead of time. Especially for components like `Sidebar` or `Dialog` that represent generic "boxes".
React recommend that such components use the special `children` prop to pass children elements:
```javascript
function FancyBorder(props) {
   return (
      <div className={'FancyBorder FancyBorder-' + props.color}>
         {props.children}
      </div>
   );
}

/*
This lets other components pass arbitrary children to them by nesting the JSX
*/

function WelcomeDialog() {
   return (
      <FancyBorder color="blue">
         <h1 className="dialog-title">welcome</h1>
         <p className="Dialog-message">
            Thank you for visiting our spacecraft!
         </p>
      </FancyBorder>
   );
}
```
##### Specialization
Sometimes we think about components as being “special cases” of other components. For example, we might say that a WelcomeDialog is a special case of Dialog.
In React, this is also achieved by composition, where a more “specific” component renders a more “generic” one and configures it with props:
```javascript
function Dialog(props) {
  return (
    <FancyBorder color="blue">
      <h1 className="Dialog-title">
        {props.title}
      </h1>
      <p className="Dialog-message">
        {props.message}
      </p>
    </FancyBorder>
  );
}

function WelcomeDialog() {
  return (
    <Dialog
      title="Welcome"
      message="Thank you for visiting our spacecraft!" />
  );
}
```
**Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. Remember that components may accept arbitrary props, including primitive values, React elements, or functions.**

### Tues 27th, October 2020 React.- Thinking in React
React is the premier way to build big, fast Web apps with JavaScript and scale very well.
One of the many great parts of React is how it makes you think about apps as you build them.
Let's see how we walk through the thought process of building with React
1. Break the UI into a component hierarchy
2. Build a static version in React
3. Identify the minimal (but complete) representation of UI state
4. Identify where your state should live
5. Add inverse data flow

### Wed 28th, October 2020 React.- Accessibility
Web accessibility is the design and creation of websites that can be used by everyone. Accessibility support is necessary to allow assistive technology to interpret web pages.
React fully supports building accessible websites, often by using standard HTML techniques.
##### Standards and Guidelines
- WCAG ([Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/)): Provides guidelines for creating accessible web sites
- WAI-ARIA ([Web Accessibility Initiative - Accessible Rich Internet Applications](https://www.w3.org/WAI/standards-guidelines/aria)): it is a document that contains techniques for building fully accessible JavaScript widgets.

### Thur 29th, October 2020 React.- Code-splitting
##### Bundling
Bundling is the process of following imported files and merging them into a single file: a "bundle". This bundle can them be included on a webpage to load an entire app at once
Example:
```javascript
// App.js
import { add } from './math.js';

console.log(add(16,26)); // 42

// math.js
export function add(a, b) {
   return a + b;
} 
```
Bundle: 
```javascript
function add(a, b) {
   return a + b;
}

console.log(add(16, 26));
```
##### Code splitting
Bundling is great, but as your app grows, your bundle will grow too. To avoid large bundle, it's good to get ahead fo the problem and start "splitting" your bundle. Code-Splitting is a feature supported by bundlers like Webpack, Rollup and Browserify which cn create multiple bundles that can be dynamically loaded at runtime.
Code-Splitting your app can help your "lazy-load" just the things that are currently neededby the user. 
The best way to introduce code-splitting into your app is through the dynamic `import()` synta.
- Before:
```javascript
import {add} from './math';

console.log(add(16,26));
```
- After:
```javascript
import("./math").then(math => {
   console.log(math.add(16, 26));
});
```
###### React.lazy
`React.lazy` function lets you render dynamic import as a regular component.
- Before: 
```javascript
import OtherComponent from './OtherComponent';
```
- After: 
```javascript
const OtherComponent = React.lazy(() => import('./OtherComponent'));

/*
React.lazy takes a function that must call a dinamic import(). This most return a Promise
which resolves to a module with a default export containing a React component
*/
```
This will automatically load the bundle containing the `OtherComponent` when this component is first rendered.

The lazy component should be rendered inside a `Suspense` component. This component allows us to show some fallback content while we are waiting gor the lazy component to load.

```javascript
import React, { Suspense } from 'react';

const OtherComponent = React.lazy(() => import('./OtherComponent'));

function MyComponent() {
  return (
    <div>
      <Suspense fallback={<div>Loading...</div>}>
        <OtherComponent />
      </Suspense>
    </div>
  );
}
/*
The fallback prop accepts any React elements that you want to render while waiting for hte component to load. 
*/
```

### Fri 30th, October 2020 React.- TypeChecking with PropTypes
As your app grows, you can catch a lot of bugs with typechecking. You can use extensions like Flow or TypeScript to typecheck your app. React has some built-in typechecking abilities, to run typechecking on the props for a component, you can assign the special `propTypes` property:
```javascript
import React, {Component} from 'react';
import PropTypes from 'prop-types';

class Greeting extends Component {
   constructor(props) {
      super(props);
   }
   render() {
      return (
         <h1>Hello, {this.props.name}</h1>
      );
   }
}

Greeting.propTypes = {
   name: PropTypes.string
};

// You can use function components instead class components
```
`PropTypes` exports a range of validators that can be used to maje sure the data you receive is valid. For example: 
If we use `PropTypes.string`. When an invalid value is provided for a prop, a warning will be shown in the JS console.
[See here all the examples](https://reactjs.org/docs/typechecking-with-proptypes.html#proptypes)

## Week 16

### Mon 2nd, November 2020 React.- ReactDOM
If you load React from a `<script>` tag, these top-level APIs are available on the ReactDOM global. If you use ES6 with npm, you can write `import ReactDOM from 'react-dom'`. If you use ES5 with npm, you can write `var ReactDOM = require('react-dom')`.
React-dom package provides DOM-specific methods that can be used at the top level of your app and as an escape hatch to get outside of the React modelif you need to. Most of your components should not need to use this module.
- render(): Render a React element into the DOM in the supplied container and return a reference to the component:
 ```javascript
 ReactDOM.render(element, container[, callback])
 ```
- hydrate(): same as render(), but is used to hydrate a container whose HTML contents were rendered by ReactDOMServer.
 ```javascript
 ReactDOM.hydrate(element, container[, callback])
 ```
- unmountComponentAtNode(): Remove a mounted React component from the DOM and clean up its event handlers and state.
 ```javascript
 ReactDOM.unmountComponentAtNode(container)
 ```
- findDOMNode(): If this component has been mounted into the DOM, this returns the corresponding native browser DOM element.
  ```javascript
  ReactDOM.findDOMNode(component)
  ```
- createPortal(): Creates a portal. Portals provide a way to render children into a DOM node that exists outside the hierarchy of the DOM component.
  ```javascript
  ReactDOM.createPortal(child,container)
  ```

### Tues 3rd, November 2020 React.- Context
Context provides a way to pass data through the component tree without having to pass props down manually at every level
When you use React, the data is passed top-down (parent to child) via props, but this can be cumbersome for certain types od props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.

Context is designed to share data that can be considered "global" for a tree of React component, such as the current authenticated user, theme, or preferred language.
The code below we manually thread through a "theme" prop in order to style the Button component:
```javascript
class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

class ThemedButton extends React.Component {
  render() {
    return <Button theme={this.props.theme} />;
  }
}
```

With context, we can avoid passing props through intermediate elements:

```javascript
/*
Context lets us pass a value deep into the component tree
without explicitly threading it through every component.

Create a context dor the current theme (with "light" as the default).
*/

import React, {Component} from 'react';

const ThemeContext = React.createContext('light');

/*
   React.createContext creates a Context object. When React renders a component
   that subscribe to this Context object it will read the current context value from
   the closest matching Provider above it in the tree
*/


class App extends Component {
  render() {
    /*
    	Use a Provider to pass the current theme to the tree below.

	Any component can read it, no matter how deep it is. 

	In this example, we're passing "dark as the current value"
    */
    return (
      /*
         ThemeContext.Provider allows consuming components to subscribe
	 to context changes.

	 One Provider can be connected to many consumers
      */
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

/*
   A component in the middle doesn´t have to pass the 
   theme down explicitly anymore.
*/

const Toolbar = () => {
  return (
    <div>
      <ThemeButton />
    </div>
  );
}

class ThemeButton extends Component {
  /*
     Assign a contextType to read the current theme context.
     React will find the closest theme Provider above and use its value.
     Remember that the current theme is "dark"
  */
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```
Context is primarily used when some data needs to be accesible by many components at different nesting levels.

### Wed 4th, November 2020 JavaScript.- EventListener
`EventListener` represents an object that can handle an event dispatched by an EventTarget object.
**Example: **

##### HTML
`<buttonid="btn">Click here!</button>`

##### JavaScript

```javascript
const buttonElement = document.getElementById('btn');
 
// Add a handler for the 'click' evenet by providing a callback function.
// Whenever the element is clicked, a pop-up with "Element clicked!!" will appear.

buttonElement,addEventListener('click', e => alert('Element clicked through function!'));
```

### Thur 5th, November 2020 React.- Error Boundaries
A javaScript error in a part of the UI shouldn't  break the whole app. To solve this problem for React users, React introduces a concept of an "error boundary".
Error boundaries are React components that **cath JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI** instead of the component tree that crashed.
Error boundaries **DO NOT** catch errors for: 
- Event handlers
- Asynchronous code (e.g. `setTimeOut` or `requestAnimationFrame` callbacks)
- Server side rendering
- Error throw in the error boundary itself (rather than its children)

A class component becomes an error boundary if it defines either (or both) of the lifecycle methods static getDerivedStateFromError() or componentDidCatch(). Use static detDerivedStateFromError() to render a fallback UI after an error has been thrown. Use componentDidCatch() to log error information.
```javascript
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError(error) {
    // Update state so the next render will show the fallback UI.
    return { hasError: true };
  }

  componentDidCatch(error, errorInfo) {
    // You can also log the error to an error reporting service
    logErrorToMyService(error, errorInfo);
  }

  render() {
    if (this.state.hasError) {
      // You can render any custom fallback UI
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children; 
  }
}
```
The you can use it as a regular component:
```javascript
<ErrorBoundary>
  <MyWidget />
</ErrorBoundary>
```
Error boundaries work like a JavaScript `catch {}` block, but for components.
Only class components can be error boundaries.
Note that **error boundaries only catch errors in the components below them in the tree**

### Fri 6th, November 2020 React.- Forwarding Refs
Is a technique for automatically passing a ref through a component to one of its children. This is typically not necessary for most components in the application. It can be useful for some components, especially in reusable component libraries.

Consider a `FancyButton` component that renders the native `Button` DOM element:
```javascript
function FancyButton(props) {
  return (
    <button className="FancyButton">{props.children}</button>
  );
}
```
React components hide their implementation details, including their rendered output. Other components **using FancyButton usually will not need to** obtain a ref to the inner button DOM element.
Although such encapsulation is desirable for application-level components like FeedStory or Comment, it can be inconvenient for highly reusable “leaf” components like FancyButton or MyTextInput. These components tend to be used throughout the application in a similar manner as a regular DOM button and input, and accessing their DOM nodes may be unavoidable for managing focus, selection, or animations.

**Ref forwarding is an opt-in feature that lets some components take a ref they receive, and pass it further down (in other words, “forward” it) to a child.**

In this example below, `FancyButton` uses `React.forwardRef` to obtain the `ref` passed to it, and then forward it to the DOM `button` that it renders:
```javascript
const FancyButton = React.forwardRef((props, ref) => (
  <button className="FancyButton">{props.children}</button>
));

// you can now get a ref directly to the DOM button:
const ref = React.createRef();
<FancyButton ref={ref}>Click me!</FancyButton>
```
This way, components using FancyButton can get a ref to the underlying button DOM node and access it if necessary—just like if they used a DOM button directly.

## Week 17

### Mon 9th, November 2020 React.- Fragment
A common pattern in React is for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DOM.
```javascript
render() {
  return (
    <React.Fragment>
      <ChildA />
      <ChildB />
      <ChildC />
    </React.Fragment>
  );
}
```
A common pattern is for a component to return a list of children.
```javascript
import React, {Component} from 'react';

class Table extends Component {
  render() {
    return (
      <table>
        <tr>
	  <Column />
	</tr>
      </table>
    );
  }
}

// Column component would need to return multiple <td> elements
// in order for the rendered HTML to be valid. If a parent div was used
// inside the render() of <Column />, then the resulting HTML will be invalid

class Column extends Component {
  render() {
    return (
      <div>
        <td>Hello</td>
	<td>World</td>
      </div>
    );
  }
}

// The result in Table component:
<table>
  <tr>
    <div>
      <td>Hello</td
      <td>World</td>
    </div>
  </tr>
</table>

```

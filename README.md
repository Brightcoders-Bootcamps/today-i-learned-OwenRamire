# Today I Learned by *Owen Ramirez*

React Native and JavaScript official documentation reading personal journal

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
	- `<Text style={{color: 'red'}}>I'm red</Text>`   
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
    {/* This view will use all the available screen*/}
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
      <View style={{flex: 1>
	{/* This view will use 1/3 of the screen*/}
        <View style={{flex: 1, backgroundColor: 'red'}}/>
	{/*This view will use 2/3 of the screen*/}
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

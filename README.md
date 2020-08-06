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


### Fri 24th, July 2020 * JavaScript.- **Grammar and types***
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
  function (`const *yourComponent* = () => { return(); };` or `function *yourComponent()*{ return(); };`) or it could be as a 
  class (`class *YourClass* extends React.Component { render( { return(); } ) }`)
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
  in this example if the OS is iOS the height will be 200 and if is Android will be 100
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
- **Static Analysis: **checks our code for errors as we write it 
- **Unit Test: ** cover the smallest part of code, like individual functions or classes
- **Integration Test: **real individual units are combined and tested together to ensure that their cooperation works as expected. 
- **End-to-End Test (E2E): **verify our app is working as expected on a device

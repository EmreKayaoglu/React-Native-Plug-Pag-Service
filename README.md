# react-native-plug-pag-service

## Getting started

`$ npm install react-native-plug-pag-service --save`

### Mostly automatic installation

`$ react-native link react-native-plug-pag-service`

### Manual installation


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-plug-pag-service` and add `PlugPagService.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libPlugPagService.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainApplication.java`
  - Add `import com.reactlibrary.PlugPagServicePackage;` to the imports at the top of the file
  - Add `new PlugPagServicePackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-plug-pag-service'
  	project(':react-native-plug-pag-service').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-plug-pag-service/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-plug-pag-service')
  	```
4. AndroidManifest.xml
  - Permissions
	To integrate the library with the PlugPagService library in Android applications you must add the following permission to AndroidManifest.xml.
	```
	<uses-permission android:name="br.com.uol.pagseguro.permission.MANAGE_PAYMENTS"/>
	```

	This permission allows the library to bind to PlugPagService , Moderninha Smart's embedded service , which manages all payment transactions.

  - Intent-filter
	In order for your app to be chosen as the default payment app and receive Card Insertion Intents, you need to add the following code to your AndroidManifest.xml within your main Activity.
	```
	<intent-filter>
	      <action android:name="br.com.uol.pagseguro.PAYMENT"/>
	      <category android:name="android.intent.category.DEFAULT"/>
	</intent-filter>
	```

## Usage
```javascript
import PlugPagService, { PlugPag, PlugPagPaymentData, PlugPagActivationData } from 'react-native-plug-pag-service'

// TODO: What to do with the module?
PlugPagService;
```

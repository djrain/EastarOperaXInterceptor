[![](https://jitpack.io/v/djrain/EastarPermission.svg)](https://jitpack.io/#djrain/EastarPermission)


# What is permission?

After Marshmallow in Android<br/>
�ȵ���̵忡���� ������ ��û�մϴ�.

This library is a simple library designed to help you with authorization requests.<br/>
�� ���̺귯���� ���� ��û �۾� ������ �ְ��� ������� ������ ���̺귯�� �Դϴ�.

For more information about Android privilege requests, please see:<br/>
�ȵ���̵� ���� ��û�� ���� ���� ������ �Ʒ� �ּҸ� ���� �Ͻø� �˴ϴ�.<br/>
([See permissions overview](https://developer.android.com/guide/topics/permissions/overview))<br/>

You can make check function yourself.<br/>
([How to Requesting Permissions at RunTime](http://developer.android.com/intl/ko/training/permissions/requesting.html))<br/>

�ȵ���̵� ���� ��û�۾��� ���ؼ��� ������ ���� �Լ����� ����ؾ� �ϸ�<br/>
(`checkSelfPermission()`, `requestPermissions()`, `onRequestPermissionsResult()`, `onActivityResult()` ...)
���� ģ���� ����� ���ؼ��� �ݺ����� �߰� �۾��� �ʿ�� �մϴ�.

permission is most of simple and smallest permission check helper.


<br/><br/>



## Demo


![Screenshot](https://github.com/djrain/EastarPermission/blob/readme/demo.gif?raw=true)    
           

sample RESULTDLG
1. Request permission
2. Show message dialog for setting when denied permission



<br/><br/>




## How...

### Gradle with jitpack

#### Add it in your root build.gradle at the end of repositories:
```javascript

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

```
#### Add the dependency
```javascript

	dependencies {
	        implementation 'com.github.djrain:EastarPermission:2.2.2'
	}


```



If you think this library is useful, please press star button at upside.
<br/>


<br/><br/>

## How to use


### 1. Make PermissionListener
We will use PermissionListener for Permission Result.
You will get result to `onPermissionGranted()`, `onPermissionDenied()`

```javascript
  var request =  PermissionRequest.builder(this, Manifest.permission.WRITE_EXTERNAL_STORAGE
                                                , Manifest.permission.READ_CALENDAR)
          .setRequestMessage("for contact photo save image")
          .setRequestPositiveButtonText("OK")
          .setRequestNegativeButtonText("cancel")
          .run()
```

<br/>

##Customize
You can customize something ...<br />

* `setRequestMessage(R.string.xxx or CharSequence)`
* `setRequestPositiveButtonText(R.string.xxx or CharSequence) (default: confirm / Ȯ��)`
* `setRequestNegativeButtonText(R.string.xxx or CharSequence) (default: close / �ݱ�)`
* `setDenyMessage(R.string.xxx or CharSequence)`
* `setDenyPositiveButtonText(R.string.xxx or CharSequence) (default: close / �ݱ�)`
* `setDenyNegativeButtonText(R.string.xxx or CharSequence) (default: setting / ����)`

<br/><br/>





## Thanks 





<br/><br/>


## License 
 ```code
Copyright 2016 eastar Jeong

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

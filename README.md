# flutter_slide_done with null safety

[![License](https://img.shields.io/badge/license-MIT-green.svg)](/LICENSE)
[![Awesome Flutter](https://img.shields.io/badge/Awesome-Flutter-blue.svg?longCache=true&style=flat-square)](https://stackoverflow.com/questions/tagged/flutter?sort=votes)

Credits to [xuelongqy](https://github.com/xuelongqy/flutter_slide_done)

SlideDone is inspired by sliding unlocking, which can be defined as a slide switch that can be unidirectional 
or bidirectional. You can customize the parameters of SlideDone to make it look what you want.

## Features:

 - Support for sliding trigger events
 - Support for active trigger events
 - Support for custom styles
 - Support one-way and two-way, initialize the default location

## Demo
[Download APK-Demo](https://github.com/xuelongqy/flutter_slide_done/raw/master/art/pkg/SlideDone.apk)

![](https://github.com/xuelongqy/flutter_slide_done/raw/master/art/image/apk_QRCode.png)

## Project demonstration
|Example|
|:---:|
|![](https://raw.githubusercontent.com/xuelongqy/flutter_slide_done/master/art/image/snipaste_index.png)
|[main.dart](https://github.com/xuelongqy/flutter_slide_done/blob/master/example/lib/main.dart)|

## Simple use case
#### 1.Add a dependency in pubspec.yaml
```
//github way
dependencies:
  slide_done_nully:
    git:
      url: https://github.com/ulisseshen/flutter_slide_done_nullsafety.git
      ref: master
```
#### 2.Add SlideDone to the layout file
```dart
import 'package:slide_done_nully/slide_done.dart';
....
  GlobalKey<SlideDoneNSState> slideDoneKey = GlobalKey<SlideDoneNSState>();
....
  SlideDoneNS(
    key: slideDoneKey,
    onStart: () async {
      await Future.delayed(Duration(seconds: 2), (){});
    },
    onEnd: () async {
      await Future.delayed(Duration(seconds: 2), (){});
    },
  ),
```
#### 3.Trigger action
```dart
  // If you don't need it, you don't need to set the key for SlideDone.
  slideDoneKey.currentState.callOnStart();
  slideDoneKey.currentState.callOnEnd();
```

# Donation
If you like this project, please in the upper right corner of the project "Star". Your support is my biggest encouragement! ^_^
You can also donate:

[![Donate to this project using Pagseguro](https://stc.pagseguro.uol.com.br/public/img/botoes/doacoes/84x35-doar-azul.gif)](https://pag.ae/7XX9rYL66)
[![Donate to this project using Paypal](https://img.shields.io/badge/paypal-donate-yellow.svg)](https://www.paypal.com/donate/?hosted_button_id=XZ7WCJCCXV6HL)


## Open source licenses
 
```
 
MIT License

Copyright (c) 2018 xuelongqy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

 
 ```

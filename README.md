<p align="center">
  <img src="https://raw.githubusercontent.com/nateshmbhat/card-scanner-flutter/master/.github/logo.png?sanitize=true" width="250px">
</p>
<h2 align="center">Fast , Accurate and Secure Credit & Debit card scanner </h2>

[![](https://img.shields.io/pub/v/card_scanner)](https://pub.dev/packages/card_scanner)
[![](https://img.shields.io/badge/package-flutter-blue)](https://github.com/nateshmbhat/card-scanner-flutter)
[![](https://img.shields.io/github/license/nateshmbhat/card-scanner-flutter)](https://github.com/nateshmbhat/card-scanner)
[![](https://img.shields.io/github/languages/code-size/nateshmbhat/card-scanner-flutter)](https://github.com/nateshmbhat/card-scanner-flutter)
[![](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2Fnateshmbhat%2Fcard-scanner-flutter)](https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2Fnateshmbhat%2Fcard-scanner-flutter)


**card_scanner** is a flutter plugin for accurately and quickly scanning debit and credit cards.


### [Documentation & Samples](https://pub.dev/documentation/card_scanner/latest/) 📖

## Features

- 🔒Fully **OFFLINE** scan makes it a completely **secure scanner** !
- 🎈 Can scan **Expiry date** , **Card Holder name** and **Card Issuer** (lacked by other scanners) along with the **Card number**✨
- 🔋Powered by Google's Machine Learning models
- ⚡ Great performance and accuracy
- 🎚Supports controlling parameters that determine the balance between speed and accuracy
- ❤️ Simple, powerful, & intuitive API 


## Install

Add this to your package's pubspec.yaml file:

```yaml
dependencies:
  card_scanner: <latest-version>
```
> get the [latest version number here](https://pub.dev/packages/card_scanner#-installing-tab-)

## Usage
Just import the package and call `scanCard`

```dart
import 'package:card_scanner/card_scanner.dart';
var cardDetails = await CardScanner.scanCard()

print(cardDetails)
```
Example Output : 
```dart
Card Number = 5173949117389006 
Expiry Date = 11/26
```

The above code opens the device camera , looks for a valid card and gets the required details and returns the `CardDetails` object

---

### Scan Options : 
If you wish to obtain the card holder name and card issuer , you can specify the options.
```dart
import 'package:card_scanner/card_scanner.dart';
var cardDetails = await CardScanner.scanCard(
    scanOptions: CardScanOption (
        scanCardHolderName: true, 
        scanCardIssuer: true
    )
);


print(cardDetails)
```
Example Output : 
```dart
Card Number = 5173949117389006 
Expiry Date = 11/26
Card Issuer = mastercard
Card Holder Name = PAUL SAMUELSON
```

---

### What next ? 
+ IOS support coming very soon 🚀
+ More control options for scanning behavior
+ Better optimizations for name scanning is in the todo list :)

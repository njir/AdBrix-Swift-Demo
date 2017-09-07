# AdBrix-Swift-Demo
Demo project for integrating Igaworks [Adbrix](https://partners.igaworks.com/) to Swift

## 🔧 Installation

### CocoaPods
AdBrix is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'IgaworksCore'
```

### How to integrate Adbrix to Swift project
- Add bridging header to project as below
![image](https://user-images.githubusercontent.com/7614353/29651852-abf3ad72-88dd-11e7-9f56-6223f0157851.png)
- Add header path to Objective-C Bridiging Header
  - Go [Build Settings] -> Objective-C Bridging Header
![image](https://user-images.githubusercontent.com/7614353/29651856-b152fd68-88dd-11e7-8333-bd4bc697b906.png)
- Add below code to AppDelegate.swift
```swift
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
    // Override point for customization after application launch.
    
    // init
    IgaworksCore.igaworksCore(withAppKey: "57308193", andHashKey: "522040fdbe0d4291")
    // set log level
    IgaworksCore.setLogLevel(IgaworksCoreLogTrace)
     
    return true
}
```

- Please refer Demo project for more information

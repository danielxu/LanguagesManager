LanguagesManager
================

An easy way to control manually the language in your application

### Usage ... very simple, just configure your supported languages
```objective-c
[[LanguagesManager sharedInstance] setSupportedLanguages:@[@"en", @"fr"]];
```

###  Change the language

```objective-c
[[LanguagesManager sharedInstance] setLanguage:@"en"]
```

###  Refresh UI ?
#### hard .... but why not
Reset your window.rootViewController 

#### clean
Listen to the NSNotification
```objective-c
[[LanguagesManager sharedInstance] setNotificationEnable:YES];

[[NSNotificationCenter defaultCenter] addObserver:self                                                                                                          selector:@selector(reloadMyUI:)
                                      name:LanguagesManagerLanguageDidChangeNotification
                                      object:nil];
```






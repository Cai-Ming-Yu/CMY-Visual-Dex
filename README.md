# 彩銘羽 Visual Dex
Dexファイルをより微妙な方法で難読化する！

Obfuscate Dex files even more by setting the contents of the file "proguard-rules.pro"!

## How to use
- Change your class package name to empty: ```-repackageclasses ''```.
- Use a custom obfuscation dictionary to obfuscate your class name and content: 
``` proguard
-obfuscationdictionary FILE
-classobfuscationdictionary FILE
-packageobfuscationdictionary FILE
-renamesourcefileattribute FILE
```
- For more confusion optimization, please download the "proguard-rules.pro" file and the "彩銘羽" file of this project. They contain more obfuscation optimizations

You can use the file by, for example, adding the following code to "build.gradle" in your project's app.
``` groovy
android {
    buildTypes {
        release {
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
        debug {
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
}
```

## Finally, if you find it practical, please order a Star for this project!
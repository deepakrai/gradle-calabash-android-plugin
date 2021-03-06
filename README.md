gradle-calabash-android-plugin
==============================

Gradle Plugin for Calabash

Version Information
-----
Version 0.1.1 : Support for Android Gradle Plugins before build was moved to build/outputs
Version 1.0+ : Support for newer Android Gradle Plugins that use the build/outputs directory.

Usage
-----

Add the plugin to your `buildscript`'s `dependencies` section:
```groovy
classpath 'org.notlocalhost.gradle:gradle-calabash-android-plugin:1.+'
```

Apply the `calabash-test` plugin:
```groovy
apply plugin: 'calabash-test'
```

To configure the features path and profiles from within the build.gradle file add a calabashTest section.
To set the path of the features add a featuresPath item to the newly created calabashTest section, these are not essential.
```groovy
calabashTest {
    featuresPath = "functional-tests/features/"
    profile = "android"
}
```

If you do not wish to override the above items, the calabash 'features' folder should be at the top level of your project. 

And then just run `./gradlew clean calabash<Variation>` you can look at the 
Gradle tasks to know all possible Variations that can be run. ( `./gradlew tasks` )

Output
------

The HTML report output is put in `build/reports/calabash/${variationName}/report.html`

License
-------

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

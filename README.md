[![CircleCI](https://circleci.com/gh/twofortyfouram/android-spackle.svg?style=svg)](https://circleci.com/gh/twofortyfouram/android-spackle)

# Overview
Spackle smooths things over and fills in the cracks.  This is a hodgepodge of utility classes that we reused several times and just bundled them together.

We don't anticipate others to rely on this much directly, as our purpose in publishing it was more as an internal dependency for our other open source projects.  Put another way, we anticipate more churn in this library.


# API Reference
JavaDocs for the library are published [here](https://twofortyfouram.github.io/android-spackle).


# Compatibility
The library is compatible and optimized for Android API Level 9 and above.


# Download
## Gradle
The library is published as an artifact to jCenter.  To use the library, the jCenter repository and the artifact need to be added to your build script.

The build.gradle repositories section would look something like the following:

    repositories {
        jcenter()
    }

And the dependencies section would look something like this:
    
    dependencies {
        compile group:'com.twofortyfouram', name:'android-spackle', version:'[3.0.0,4.0['
    }

# History
* 2.0.0: Initial release
* 2.0.1: PermissionCompat handles WRITE_SETTINGS and REQUEST_IGNORE_BATTERY_OPTIMIZATIONS on Android Marshmallow
* 2.0.2: ContextUtil avoids breaking out of test context
* 2.0.3: PermissionCompat implementation handles null arrays from PackageManager.  This is unlikely to impact usage, except during automated tests.
* 3.0.0: Added IClock interface, ProcessUtil, and SignatureUtil.  Deleted TraceCompat.
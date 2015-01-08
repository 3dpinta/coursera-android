SimpleCalcTest
====================

Original SimpleCalcTest does not import correctly into Android Studio.
It fails with a gradle sync error due to a dependency on an APK.

This version includes the main and androidTest directories together.

Gradle seems to be able to build the test apk: `gradle assembleDebugTest`
or the non-test apk: `gradle assemble`.

~~~

The original import includes two gradle subprojects of SimpleCalcTest:
simpleCalc and simpleCalcTest. simpleCalc (and APK) is a dependency
of simpleCalcTest. This is illegal.

simpleCalcTest includes the test sources. simpleCalc includes the
application _and_ test sources.

# DesugarFirestoreTestIssue

When running `:app:connectedDebugAndroidTest`, this sample should trigger the following issue : 

```
Execution failed for task ':app:connectedDebugAndroidTest'.
> There were failing tests. See the report at: file:///C:/Users/nitro/Documents/Workspace/Test/app/build/reports/androidTests/connected/index.html
2020-04-07 02:00:39.099 4884-4915/com.nitro.test E/TestRunner: failed: useAppContext(com.nitro.test.ExampleInstrumentedTest)
2020-04-07 02:00:39.099 4884-4915/com.nitro.test E/TestRunner: ----- begin exception -----
2020-04-07 02:00:39.100 4884-4915/com.nitro.test E/TestRunner: java.lang.NoClassDefFoundError: Failed resolution of: Lkotlin/jvm/internal/Intrinsics;
        at com.nitro.test.ExampleInstrumentedTest.useAppContext(ExampleInstrumentedTest.kt:21)
        at java.lang.reflect.Method.invoke(Native Method)
        at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:50)
        at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
        at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:47)
        at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
        at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:325)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:78)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:57)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at androidx.test.ext.junit.runners.AndroidJUnit4.run(AndroidJUnit4.java:104)
        at org.junit.runners.Suite.runChild(Suite.java:128)
        at org.junit.runners.Suite.runChild(Suite.java:27)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:137)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:115)
        at androidx.test.internal.runner.TestExecutor.execute(TestExecutor.java:56)
        at androidx.test.runner.AndroidJUnitRunner.onStart(AndroidJUnitRunner.java:392)
        at android.app.Instrumentation$InstrumentationThread.run(Instrumentation.java:2189)
     Caused by: java.lang.ClassNotFoundException: Didn't find class "kotlin.jvm.internal.Intrinsics" on path: DexPathList[[zip file "/system/framework/android.test.runner.jar", zip file "/system/framework/android.test.mock.jar", zip file "/data/app/com.nitro.test.test-NbhAGipcHLIWZzMm8Kue8w==/base.apk", zip file "/data/app/com.nitro.test-rONpDfn5hvJISTDvOQ-UEw==/base.apk"],nativeLibraryDirectories=[/data/app/com.nitro.test.test-NbhAGipcHLIWZzMm8Kue8w==/lib/x86_64, /data/app/com.nitro.test-rONpDfn5hvJISTDvOQ-UEw==/lib/x86_64, /system/lib64, /system/product/lib64]]
        at dalvik.system.BaseDexClassLoader.findClass(BaseDexClassLoader.java:196)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:379)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:312)
        at com.nitro.test.ExampleInstrumentedTest.useAppContext(ExampleInstrumentedTest.kt:21) 
        at java.lang.reflect.Method.invoke(Native Method) 
        at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:50) 
        at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12) 
        at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:47) 
        at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17) 
        at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:325) 
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:78) 
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:57) 
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290) 
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71) 
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288) 
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58) 
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268) 
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363) 
        at androidx.test.ext.junit.runners.AndroidJUnit4.run(AndroidJUnit4.java:104) 
        at org.junit.runners.Suite.runChild(Suite.java:128) 
        at org.junit.runners.Suite.runChild(Suite.java:27) 
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290) 
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71) 
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288) 
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58) 
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268) 
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363) 
        at org.junit.runner.JUnitCore.run(JUnitCore.java:137) 
        at org.junit.runner.JUnitCore.run(JUnitCore.java:115) 
        at androidx.test.internal.runner.TestExecutor.execute(TestExecutor.java:56) 
        at androidx.test.runner.AndroidJUnitRunner.onStart(AndroidJUnitRunner.java:392) 
        at android.app.Instrumentation$InstrumentationThread.run(Instrumentation.java:2189) 
2020-04-07 02:00:39.100 4884-4915/com.nitro.test E/TestRunner: ----- end exception -----
```

On another project, the missing is completely different :
```
2020-04-07 01:41:59.980 32096-32096/fr.arae.data.test E/AndroidRuntime: FATAL EXCEPTION: main
    Process: fr.nitro.data.test, PID: 32096
    java.lang.NoClassDefFoundError: Failed resolution of: Landroidx/test/internal/runner/listener/InstrumentationRunListener;
        at java.lang.Class.newInstance(Native Method)
        at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6391)
        at android.app.ActivityThread.access$1300(ActivityThread.java:219)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1859)
        at android.os.Handler.dispatchMessage(Handler.java:107)
        at android.os.Looper.loop(Looper.java:214)
        at android.app.ActivityThread.main(ActivityThread.java:7356)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
     Caused by: java.lang.ClassNotFoundException: androidx.test.internal.runner.listener.InstrumentationRunListener
        at java.lang.VMClassLoader.findLoadedClass(Native Method)
        at java.lang.ClassLoader.findLoadedClass(ClassLoader.java:738)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:363)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:312)
        at java.lang.Class.newInstance(Native Method) 
        at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6391) 
        at android.app.ActivityThread.access$1300(ActivityThread.java:219) 
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1859) 
        at android.os.Handler.dispatchMessage(Handler.java:107) 
        at android.os.Looper.loop(Looper.java:214) 
        at android.app.ActivityThread.main(ActivityThread.java:7356) 
        at java.lang.reflect.Method.invoke(Native Method) 
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492) 
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930) 
     Caused by: java.lang.NoClassDefFoundError: Failed resolution of: Lorg/junit/runner/notification/RunListener;
        at java.lang.Class.newInstance(Native Method) 
        at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6391) 
        at android.app.ActivityThread.access$1300(ActivityThread.java:219) 
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1859) 
        at android.os.Handler.dispatchMessage(Handler.java:107) 
        at android.os.Looper.loop(Looper.java:214) 
        at android.app.ActivityThread.main(ActivityThread.java:7356) 
        at java.lang.reflect.Method.invoke(Native Method) 
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492) 
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930) 
     Caused by: java.lang.ClassNotFoundException: Didn't find class "org.junit.runner.notification.RunListener" on path: DexPathList[[zip file "/data/app/fr.nitro.data.test-_D3iuZkhX-rv4mnWXFSfMw==/base.apk"],nativeLibraryDirectories=[/data/app/fr.nitro.data.test-_D3iuZkhX-rv4mnWXFSfMw==/lib/x86_64, /system/lib64, /system/product/lib64]]
        at dalvik.system.BaseDexClassLoader.findClass(BaseDexClassLoader.java:196)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:379)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:312)
        at java.lang.Class.newInstance(Native Method) 
        at android.app.ActivityThread.handleBindApplication(ActivityThread.java:6391) 
        at android.app.ActivityThread.access$1300(ActivityThread.java:219) 
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1859) 
        at android.os.Handler.dispatchMessage(Handler.java:107) 
        at android.os.Looper.loop(Looper.java:214) 
        at android.app.ActivityThread.main(ActivityThread.java:7356) 
        at java.lang.reflect.Method.invoke(Native Method) 
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492) 
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930) 
```

The culprits I found is a combination of having the last desugar api activated, with the last firestore library included.
Disabling either one of the two makes the test runnable again.


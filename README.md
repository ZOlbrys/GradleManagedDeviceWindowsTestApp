# GradleManagedDeviceWindowsTestApp

Run `pixel2api30DebugAndroidTest` task to run tests with the managed device setup in the `build.gradle` file in the app module.

Current issues:
1. On windows computers, this task fails with the errors (See https://issuetracker.google.com/issues/249111286):

```
Execution failed for task ':app:pixel2api30Setup'.
> A failure occurred while executing com.android.build.gradle.internal.tasks.ManagedDeviceSetupTask$ManagedDeviceSetupRunnable
   > java.lang.IllegalStateException: Gradle was not able to complete device setup for: dev30_default_x86_64_Pixel_2
     This could be due to having insufficient resources to provision the number of
     devices requested. Try running the test again and request fewer devices or
     fewer shards.
```

However on Mac computer it works well without any trouble.

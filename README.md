# react-native-orientation
Listen to device orientation changes in React-Native and set preferred orientation on screen to screen basis.

###Usage (iOS)
* in AppDelegate.m
```
#import "Orientation.h"

- (UIInterfaceOrientationMask)application:(UIApplication *)application supportedInterfaceOrientationsForWindow:(UIWindow *)window {
  return [Orientation getOrientation];
}
```

###Usage (Android)
* in MainActivity.java)
```
import android.content.Intent;
import android.content.res.Configuration;

@Override
public void onConfigurationChanged(Configuration newConfig) {
  super.onConfigurationChanged(newConfig);
  Intent intent = new Intent("onConfigurationChanged");
  intent.putExtra("newConfig", newConfig);
  this.sendBroadcast(intent);
}
```

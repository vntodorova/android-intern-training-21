# Getting started

Hello, interns! 
I assume you already know how the computer works, which is your favourite browser, how to work with git and how to lock your screen when you go pee. That's why we can jump right at the dry theory.

# Kotlin is love

The programming language that you will use throughout the end of the internship is Kotlin. This is basically the modern java and is very similar to Swift, which you might have used. You will love it.

# My first Android Project

Start by reading about __activities__ [here](https://developer.android.com/guide/components/activities/index.html). Roughly speaking activities represent a screen in the app. You will read a bit about the activity lifecycle, but we will dig deeper into that after building our first app.

Luckily for me, Google have that very convenient [first app tutorial](https://developer.android.com/training/basics/firstapp/index.html). Read it carefully and follow the steps. In the process you will install Android Studio, setup a development environment and learn how to run it on real device (if you are poor enough not to have an iPhone) or emulator. Then you will build a simple interface and add a little action to the whole thing.

When you are done and have your first app running, I want you to understand the __Activity Lifecycle__ by overriding the following methods in an activity in the app you've already built: 
`onCreate(Bundle)`, `onStart`, `onResume`, `onPause`, `onStop`, `onRestart`, `onDestory`. 
Add the following code `Log.i("Lifecycle", METHOD_NAME);` in the methods implementation, METHOD_NAME being a string of each method name.

Now open __Logcat__ in Android Studio (lower left corner). It shows you real-time logging.

![alt text](/resources/T0/0.png "Logcat")

Select your device from the upper left corner and experiment with your app - rotate the device/emulator, minimize the app to recents and maximize it again, lock the device and then unlock it. Notice when each method is called.

Now read about the [**activity lifecycle**](https://developer.android.com/guide/components/activities/activity-lifecycle.html) where the workflow of these methods is explained in depth.  

Finally read about activity [**state changes**](https://developer.android.com/guide/components/activities/state-changes.html).

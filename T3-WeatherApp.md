# Weather Report app

You will build a simple app that reports the current weather conditions in a city of choice. The app, depending on the device that is used to run it, has one or two screens. If you use a phone you will have two consecutive screens, if you use a tablet you will have two __"subscreens"__ that now share the large visible area of the screen.

![alt text](https://developer.android.com/images/fundamentals/fragments.png "Fragments")

To implement this you will use [fragments](https://developer.android.com/guide/components/fragments). You will consume [REST APIs](https://en.wikipedia.org/wiki/Representational_state_transfer) and will work with [JSON](https://en.wikipedia.org/wiki/JSON).

## Cities list

The first screen on a phone (or the left subscreen on a tablet) shows a cities list. 
When the app loads if there are existing cities (persisted in a database) some basic weather data (City name, temperature, current weather icon) is loaded for each city and shown in the list. 
Here the user should also be able to add new cities to the list. 
If the user clicks on a city in the list in case of phone the Weather details screen is opened, and in case of tablet - the Weather details screen is renewed with the information of the city.

## Weather details

In this screen you should show some detailed information upon the basic information (temperature, icon) for the weather in each city - like humidity, pressure, wind speed and so on. 
You can also show the forecast for the next 5 days. Visual implementation is up to you, but you may try to impress me. (I will remind you once again about [**Material Design**](https://material.io/).)

## Fragments
Fragments have their own lifecycle that is tied to the lifecycle of the parent activity but there are several differences. Make sure you read carefully the following [section](https://developer.android.com/guide/components/fragments#Lifecycle). Nesting of fragments inside other fragments is also possible but can lead to other problems. If you don't really need to do it - don't. Also fine-grained backstack manipulation leads to a ton of problems, so the easiest way is to not use the backstack at all. We will use a lot of fragments in the future for implementing  View parts of various MV-Whatever architectural patterns. 


## Consuming REST APIs and asynchronous execution


You will need to register to [OpenWeatherMap](https://openweathermap.org/api) to use their REST API. See the documentation for _Current weather data_ and _5 day / 3 hour forecast_. For implementing the network requests for the API use the plain old [HttpURLConnection](https://developer.android.com/reference/java/net/HttpURLConnection). You cannot execute network calls on the Main Thread so you'll need a way to execute them in a background thread. You will do this is by using an [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask). If you struggle to put everything together read the following [article](https://medium.com/@JasonCromer/android-asynctask-http-request-tutorial-6b429d833e28). You will need to parse the JSON results of the requests. Don't do it manually! Use a JSON parser library like [Kotlin serialization](https://kotlinlang.org/docs/serialization.html) or [gson](https://github.com/google/gson). AsyncTasks and manual HTTP requests are not used anymore by anyone that knows their craft in 2018, but if you need to look at older code/examples you will see them everywhere. You will learn all about the the new and shiny alternatives in future projects.

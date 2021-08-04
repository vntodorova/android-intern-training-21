# Hacker news

Your next task will be to make a mobile version of [Hacker news](https://news.ycombinator.com/). This is a social news website focusing on computer science, which contains lots of articles from various websites, that are separated in 3 categories - "New", "Top" and "Best". It provides the ability for users to login, add comments below each article and 'like' them.

Hacker news also provides free [API](https://github.com/HackerNews/API), which is pretty straightforward to use, but make sure you read the documentation.

## Main screen

The main screen should be something like this:

<img src="/resources/T6/0.png" width="300">

For the 'New', 'Top' and 'Best' tabs use [ViewPager](https://developer.android.com/guide/navigation/navigation-swipe-view). You should also read about [Fragments](https://developer.android.com/guide/fragments), which are the elements that the view pager uses to display different screens in each tab.

In each tab you should display the articles with their name, author, time, number of 'likes', number of comments, share button and 'Add to favourites' button (I will explain each of these later).

On the bottom you must have a [Bottom Navigation View](https://developer.android.com/reference/com/google/android/material/bottomnavigation/BottomNavigationView) with 3 navigation items - News, Search and Favourites.

## News screen

When the user clicks on:

- An article - a 'popup' fragment must be displayed with the article's webpage loaded. For implementing this you must read about [WebViews](https://developer.android.com/guide/webapps/webview).

<img src="/resources/T6/1.png" width="300">

- The comments button - a new *Comments screen* must be opened. It should display the name of the article and the top-level comments of the article. When the user clicks on a comment with replies, the next-level replies must be loaded and so on, with each comment containing the author and time.

<img src="/resources/T6/2.png" width="300">

- The share button - a [Share sheet](https://developer.android.com/training/sharing/send) should be displayed, with different sharing options.

<img src="/resources/T6/3.png" width="300">

- The 'Add to favourites' button - this should save the article and display it in the 'Favourites' screen.

## Search screen

The search screen must consist of a field for typing text and a button 'Search' which performs a search for the articles containing the searched text. The results should be displayed in a list.

## Favourites screen

The favourites screen must contain a list of the articles that are added to 'Favourites' with the same actions available as in the *News screen* (Sharing, Removing from Favourites, Comments).

## Some more requirements

For consuming the API I want you to use [Retrofit](https://square.github.io/retrofit/) and [RxJava](https://github.com/ReactiveX/RxAndroid). You can watch this [tutorial](https://www.youtube.com/watch?v=0IKHxjkgop4&t=1888s) by Jake Wharton, who explains why reactive is better. 
Also you will need *Room* again for saving the 'Favourite' articles and you may also [use RxJava for the requests to the database](https://medium.com/androiddevelopers/room-rxjava-acb0cd4f3757). 

You can add this at a later point, but I want you to [implement pagination](https://medium.com/mindorks/implement-pagination-in-recyclerview-using-rxjava-operators-686fb202b9dc) in the news recycler view. This means that more stories must be loaded while scrolling down.

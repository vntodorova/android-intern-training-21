# Notes Application Part 2

When you are finished with the basic version of the Notes Application, I want you to upgrade it a bit, so that it will offer a bit more functionality and customization to the user and also learn something about Andorid's database.

## Database

I guess you've already worked with databases, at least during your iOS training, so I will not go into details. 
2 or 3 years ago, working with database in Android was a pain in the a$$, but Google worked towards making it easier for developers and came up with **Room**. There is a nice guide that you can read [here](https://developer.android.com/training/data-storage/room).
Basically for every table in the database, you must create *Entity* and to make requests you will need *data access object* (DAO). SQLite (Android's database management system) does not offer everything there is, but it is enough, if you know how to use it. 

So what I want you to do is to start storing data in local database using Room, instead of saving it physically on the device storage.

## Layout Manager

Maybe you've already came across RecyclerView's layout managers, but now I want you to go deeper. 

Add a button somewhere (make it pretty), which will change the view mode of the notes list from *List* to *Grid*.

## Some more functionality for the user

Give the users the ability to *delete* and *edit* the notes they already have. You can add that functionality wherever you see fit.

## Add support for dark mode

Maybe you've noticed the files res/values/themes.xml and res/values-night/themes.xml that Android Studio automatically generated for you. These contain mainly colors that your app uses, if you do not override them, which are different depending on whether the user has turned on the 'Dark mode' in the device's settings. Since I like the dark mode, please make it pretty 😍. 


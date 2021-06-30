# Notes Application

You will create an application, where you can keep notes. Pretty much something like a basic verison of [Google Keep](https://play.google.com/store/apps/details?id=com.google.android.keep). 

## Requirements

You will have one main activity (screen) where you will display the notes in a list, with each note having a title, a part of the content and the date & time it was created/last modified. You will have a 'plus' button, which will open another activity for creating new note.

The second activity will have a field for the note's title and a field for the note's text. Also at the bottom there will be a button 'Save/Create/Add/Whatever' for saving the note and 'Cancel' if you want to go back without saving it. When pressed both buttons will lead back to the list of notes.

We will need a third activity, which will be for viewing the existing notes. It will display the note's title, content and date & time, also have a back button for going back to the main list.

I want you to save the notes physically in your [app specific external storage](https://developer.android.com/training/data-storage/app-specific) for now.

## What to use

* For the list with notes go for [Recycler View](https://developer.android.com/guide/topics/ui/layout/recyclerview). It is easy to implement, just follow the tutorial, but also try to understand what you are doing.
* For the 'plus' button you can check the [Floating Action Button](https://developer.android.com/guide/topics/ui/floating-action-button) by Material Design, which is very recongnizable for every Android user.

## Source control

You might want to create a github repository before you start this and every other project. 

## Future improvements

When you are finished with the above task, I want you to do the following improvements:

* Take a look at [this](https://developer.android.com/training/data-storage/room) article about saving data in local database using Room and implement that instead of storing the files physically in the device storage.
* Add a button somewhere (make it pretty), which will change the view mode of the notes list from *List* to *Grid*.
* Add [search](https://developer.android.com/guide/topics/search), so that the user finds his notes more quickly.
* Add delete and edit functionality.

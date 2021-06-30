# User Interface

When developing Android applications, the user interface is very important to the customer, because it can vary from extremely ugly to winning Play Store's design awards.
Android provides a variety of pre-built UI components such as structured layout objects and UI controls that allow you to build the graphical user interface for your app. You can also create your own (and you will, at some point).

# Views

By 'views' we mean Buttons, EditTexts, TextViews, etc. The most important attribute that all views have are **layout_width** and **layout_height**, which must always be set.
For width and height you can set a constant in density-independent pixels (dp), match_parent or wrap_content, which are pretty self explanatory.
Also you can set **id** to each view, which makes it easy to get a handle of and add constraints for it.

# Layouts

As you have probably seen in the starting project, to define your interface you will need an .xml file, where you declare the elements you want to display.
The 'root' element of the .xml file is usually a layout. Inside the layout you start adding other layouts or views. You can read a bit more details about the view hierarchy [here](https://developer.android.com/guide/topics/ui/declaring-layout).

We are now going to go through some of the most used layouts out there by placing buttons in different configurations, using different layouts.

Create a new project (or use the one you already have), open the .xml and start 'designing'. 

# LinearLayout

[LinearLayout](https://developer.android.com/guide/topics/ui/layout/linear) is the most simple layout, used just for the simplest UIs, because it's not very configurable. It's main purpose is to align all its children in a single direction, vertically or horizontally.

The important attributes that you will have to use are:
* **orientation**
* **layout_gravity**

Construct the following layouts, by using only LinearLayout and Buttons, and you can only use a constant number when setting the layout_width and layout_height of the buttons. 

*Hint: You can use more than one LinearLayout for some of the tasks.*

# LinearLayout sub-task 1

![alt text](/resources/T1/0.png "LinearLayout0")

# LinearLayout sub-task 2

![alt text](/resources/T1/1.png "LinearLayout1")

# LinearLayout sub-task 3

![alt text](/resources/T1/2.png "LinearLayout2")

# RelativeLayout

[RelativeLayout](https://developer.android.com/guide/topics/ui/layout/relative) is one of the most popular layouts in Android, since it has a lot of attributes that can create much more configurations of the views. It's really intuitive and easy to use.

The most common attributes that you will use are:
* **layout_toEndOf / layout_toStartOf / layout_below / layout_above**
* **layout_alignBottom / layout_alignTop / layout_alignStart / layout_alignEnd**
* **layout_alignParentBottom / layout_alignParentTop / layout_alignParentStart / layout_alignParentEnd**
* **layout_centerVertical / layout_centerHorizontal**

Construct the following layout, by using only RelativeLayout and Buttons, and you can only use a constant number when setting the layout_width and layout_height of the buttons.

![alt text](/resources/T1/3.png "RelativeLayout")

# ConstraintLayout

[ConstraintLayout](https://developer.android.com/training/constraint-layout) is the newest and by far my favourite layout, because you can achieve almost everything with it. It is very customizable and can automatically create animations in your UI.

One very useful view that you can use in ConstraintLayout is **Guideline**. It is very convenient when you want to use a percentage of the screen for something, and the rest for something else. You will need to set it's **orientation** which can be horizontal and vertical and **layout_constraintGuide_percent**.

The important attributes that you will have to use are:
* **layout_constraintStart(End/Bottom/Top)_toStart(End/Bottom/Top)Of** which accepts *parent* or *id* of a view.

Construct the following layout, by using only ConstraintLayout and Buttons, and you can only use a constant number when setting the layout_width and layout_height of the buttons.
The layout is very similar to the previous one, but it should occupy only 80% of the screen. The bottom 20% should be empty.

![alt text](/resources/T1/4.png "ConstraintLayout")



* *When you finish those tasks you will go through most of the attributes you will need to build any future layout. Of course the possibilities are endless if working on the user interface is interesting to you, as it is to me. :)*


